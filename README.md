# Cup Stacking Arm

## Project Summary

Our final project is the cup stacking program.
We tried to stack six mini cups to make a cup tower.
We used the EvoArmMini334 to grab the cups
and place them correctly to build the tower.
Our inspiration for this project is the cup tower challenge for the kids
which teach them the design skills and promote creativity.
With this project we want to prove that robots can do the tasks like human does.
This project is great for community demonstration,
as other people can see how the EvoArm creates the cup tower.
The robot is controlled by a Python program which has the command tell it
what to do while building the tower,
so it can create the cup tower without any human interference.
Based on this project, we can program the robot's arm to grab any object
to achieve the task that we want.
The EvoArm has a gripper which can grab the mini cups,
we programed it to make it only grabs one cup
at a time and placed it in the right position.
After coding and testing process,
we have the robot to build the cup perfectly and have a video of it.

![Cup Stacking Process](cups.png)

## Project Implementation Details

First, outline all steps one must take to
run your project, including any needed installations.
Then describe **all** steps you took to implement the task,
including all non-technical and technical details. Please include
references (links are okay) to all resources you have used.

In order to run this project one must:

1) Obtain the required Evoarmminni from the Allegheny
ALIC Lab (or obtain and build a new Evoarm Mini Model)

2) Plug in the robot to a reliable outlet
    - making sure that all of the wiring is set up
    correctly as the 334 model has the tendency to have wires
    that disconnect.
    - If the robot is working appropriately it will give you an
    indication that it is on and all the wires are working correctly.
    (usually this is some form of motion that gets it to its home position).

3) Now you should connect your laptop to the robot wifi connection
    - Turn the wifi on your computer off and back on
    (just to give it the chance to detect new networks).
    - look for a wifi connection called `Evoarmmini334` or
    `Evoarmmini###` with the hashtags representing the number
    of your evoarm.
    - click on that wifi connection and give it a few second to fully connect
    - Once connected it should say something like: `No internet, secured`

4) Now you can connect to the robot's online interface
by typing this in your browser `http://10.10.0.1:9072/`

5) From there an interface should pop up that allows
you to manually drive the robot along with several other
tabs along the top of the screen.

6) Type on the `Apps` tab and you will notice that a list
of different applications for running the evoarm come up.

7) For one of these apps (preferably one written in python) scroll
to the far right hand side of the screen and click on the
little box that says `edit`.

8) Once you're there you will see a box that says `name`
Rename the task to `CupStacking.py` and click either `save`
or `save a copy`. This will create a new document back on the apps
screen that you can edit.

9) Click on the same `edit` button for `CupStacking` and clear
whatever is in the contents section of the app.
    - make sure that this is a python file

10) Paste this code block into the section that you just cleared:

```python
#example
#populate the sequence array with the commands you want in your sequence
#each entry must have a "command" value
#copy this script from the Apps screen to make your own python apps

sequence = [
     { "command": "d:-15","delay": 1.0  },
     { "command": "a:+32","delay": 1.0  },
     { "command": "x:+30","delay": 1.0  },
     { "command": "y:-25","delay": 1.0  },
     { "command": "e:-74","delay": 2.0  },
     { "command": "y:+55","delay": 2.0  },
     { "command": "a:-50","delay": 1.0  },
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-90","delay": 2.0  },
     { "command": "e:+55","delay": 2.0  },

     { "command": "y:+75","delay": 1.0  },
     { "command": "a:+52","delay": 1.0  },
     { "command": "y:-55","delay": 1.0  },
     { "command": "e:-72","delay": 2.0  }, 
     { "command": "y:+75","delay": 2.0  },
     { "command": "a:-66","delay": 1.0  },
     { "command": "f:+15","delay": 2.0  },
     { "command": "x:-10","delay": 2.0  },
     { "command": "y:-90","delay": 3.0  },
     { "command": "e:+7","delay": 2.0   },

     { "command": "y:+75","delay": 1.0  },
     { "command": "e:+50","delay": 1.0  },
     { "command": "a:+64","delay": 1.0  },
     { "command": "x:+10","delay": 1.0  },
     { "command": "y:-80","delay": 3.0  },
     { "command": "e:-80","delay": 3.0  }, 
     { "command": "y:+75","delay": 2.0  },
     { "command": "a:-35","delay": 1.0  },
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-95","delay": 3.0  },
     { "command": "x:+10","delay": 2.0  },
     { "command": "e:+7","delay": 3.0   },
     { "command": "e:+55","delay": 1.0  },

     { "command": "y:+90","delay": 1.0  },
     { "command": "a:+34","delay": 1.0  },
     { "command": "y:-95","delay": 1.0  },
     { "command": "e:-75","delay": 2.0  }, 
     { "command": "y:+75","delay": 2.0  },
     { "command": "a:-43","delay": 1.0  },
     { "command": "x:-10","delay": 1.0  },
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-75","delay": 1.0  },
     { "command": "e:+60","delay": 1.0  },

     { "command": "y:+80","delay": 1.0  },
     { "command": "a:+45","delay": 1.0  },
     { "command": "x:+15","delay": 2.0  },
     { "command": "y:-85","delay": 1.0  },
     { "command": "e:-70","delay": 2.0  },
     { "command": "y:+100","delay": 2.0 },
     { "command": "a:-61","delay": 1.0  },
     { "command": "x:-10","delay": 1.0  },
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-77","delay": 1.0  },
     { "command": "e:+7","delay": 1.0   }, 
     { "command": "y:+85","delay": 2.0  },
     { "command": "e:+45","delay": 1.0  },

     { "command": "a:+61","delay": 1.0  },
     { "command": "y:-113","delay": 1.0 },
     { "command": "x:+5","delay": 1.0  },
     { "command": "e:-90","delay": 3.0  },
     { "command": "y:+113","delay": 2.0 },
     { "command": "a:-55","delay": 1.0  },
     { "command": "y:-50","delay": 2.0  },
     { "command": "e:+60","delay": 2.0  },
     { "command": "y:+60","delay": 1.0  }
]
```

1) From here you should be able to press the home button
to make sure that the robot is in its home position and
then run the code using the play button in the top left corner.

2) Things to note:
    - Due to the hardware being inconsistent, you
    may have to make adjustments to the code.
    - When we did this project, we decided to cut out
    little circles of cardboard so that the cups wouldn't shift
    around as they landed. We also decided to prop the cup stack
    on a box because the robot arm wasn't able to move all the way
    to the ground to place the cups.

3) Happy Cup Stacking!

## Experimental Results

Our cup tower is made of total six cups.
The cups tower has 3 layers which are the bottom layer: 3 cups,
the middle layer: 2 cups and the top layer: 1 cup.
First, we code some commands for the robot to make the first layer.
The robot picks up the first cup on the cup stack
and moves to the tower position.
Then, the first cup of the bottom layer is placed in the middle of the tower position.
After that, the robot move back to the cup stack and pick up the second cup.
This time the arm moves further to place the second cup
at the right of the first cup.
And the third cup is placed at the left of the first cup.
Now, we have the first layer.
For the second layer, we need to placed two cups.
The EvoArm grabs the cup from the cup stack
and places the left and right cup respectively.
After placed the cups the Arm goes up
to make sure it does not touch any cups next to it.
Finally, the EvoArm places the last cup on top of the two cups in the middle layers,
and we have the cup tower that we want to.

## Ethical Implications

1) Who would typically make the technology of the similar
type as your project? Why?

- I think a factory might use code similar to this with
a robotic arm if they were trying to stack certain materials
or blocks in a pyramid for shipment or storage. They might not
have the robot stack things in this way, but the similarities
are still present.

2) Who are the intended users of this robotic
application? How does this technology benefit them?

- I think the intended users of this application could
honestly be children. The code is complex, but it would
be a really great way to get them to experience robotics
in a way that shows something familiar to them (I know that
I did a lot of cup stacking when I was little). However, like
I said in the previous question, I do think that this application
has a lot of potential for factory implementation because it would
allow them to stack things in an organized way.

3) Who is not supposed to use this technology? Why?

- I don't think there is anyone that shouldn't
use this technology. It is meant to be more of a
fun game than anything else and I think that that
is something that everyone should be allowed to experience,
but I also think that if factories were to start using this code,
they should consider how their materials would be effected by
it and how it would effect those materials to be stacked in a
tower-like structure instead of however they were to usually package it.

4) How can the type of robotic application implemented in your
project cause harm?

- I think that it could cause harm in factories if it took
away jobs. I also think it could potentially harm materials
or people if it was used in a factory setting and not adjusted
for that factory's specific needs.

5) What solutions can be developed to avoid the harm
caused by this type of technology or to fix the harm?

- I think that in order to fix the problem of this technology,
new jobs need to be created that are things that only humans can do.
That or I think this robot implementation should only be used if there
are no people willing to do that labor-intensive job anymore.
I also think that making sure that this technology is altered
for each specific factory environment is very important because
it would help to keep safety and efficiency levels in a good place.