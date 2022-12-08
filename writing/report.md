# Report by Evelyn Griffith and Trang Hoang

## Project Summary

Describe the completed project. Provide motivation for your
project, application that your robot is utilized for, specific
goals/tasks it completes, and include any background references
you used to develop the idea for your project (links are okay).

## Project Implementation Details

First, outline all steps one must take to
run your project, including any needed installations.
Then describe **all** steps you took to implement the task,
including all non-technical and technical details. Please include
references (links are okay) to all resources you have used.

In order to run this project one must:

1.) Obtain the required Evoarmminni from the Allegheny
ALIC Lab (or obtain and build a new Evoarm Mini Model)

2.) Plug in the robot to a reliable outlet
    - making sure that all of the wiring is set up
    correctly as the 334 model has the tendency to have wires
    that disconnect.
    - If the robot is working appropriately it will give you an
    indication that it is on and all the wires are working correctly.
    (usually this is some form of motion that gets it to its home position).

3.) Now you should connect your laptop to the robot wifi connection
    - Turn the wifi on your computer off and back on
    (just to give it the chance to detect new networks).
    - look for a wifi connection called `Evoarmmini334` or
    `Evoarmmini###` with the hashtags representing the number
    of your evoarm.
    - click on that wifi connection and give it a few second to fully connect
    - Once connected it should say something like: `No internet, secured`

4.) Now you can connect to the robot's online interface
by typing this in your browser `http://10.10.0.1:9072/`

5.) From there an interfact should pop up that allows
you to manually drive the robot along with several other
tabs along the top of the screen.

6.) Type on the `Apps` tab and you will notice that a list
of different applications for running the evoarm come up.

7.) For one of these apps (preferably one written in python) scroll
to the far right hand side of the screen and click on the
little box that says `edit`.

8.) Once you're there you will see a box that says `name`
Rename the task to `CupStacking.py` and click either `save`
or `save a copy`. This will create a new document back on the apps
screen that you can edit.

9.) Click on the same `edit` button for `CupStacking` and clear
whatever is in the contents section of the app.
    - make sure that this is a python file

10.) Paste this code block into the section that you just cleared:

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

11.) From here you should be able to press the home button
to make sure that the robot is in its home position and
then run the code using the play button in the top left corner.

12.) Things to note:
    - Due to the hardware being inconsistent, you
    may have to make adjustments to the code.
    - When we did this project, we decided to cut out
    little circles of cardboard so that the cups wouldn't shift
    around as they landed. We also decided to prop the cup stack
    on a box because the robot arm wasn't able to move all the way
    to the ground to place the cups.

13.) Happy Cup Stacking!

## Experimental Results

Conduct at least three experiments with your
completed implementation, where something is varied
in each experiment (for example changes in the environment).
Produce visual representation of these experiments (pictures or videos).
Describe your observations of the outcome of these experiments (how did the
robot behave in these experiments? were there variations?).

## Ethical Implications

Based on your experiences with the project and from
our discussions in class, please provide answers for
the following questions as related to the project you chose
to implement:

1. Who would typically make the technology of the similar
type as your project? Why?

- I think a factory might use code similar to this with
a robotic arm if they were trying to stack certain materials
or blocks in a pyramid for shipment or storage. They might not
have the robot stack things in this way, but the similarities
are still present.

2. Who are the intended users of this robotic
application? How does this technology benefit them?

- I think the intended users of this application could
honestly be children. The code is complex, but it would
be a really great way to get them to experience robotics
in a way that shows something familiar to them (I know that
I did a lot of cup stacking when I was little). However, like
I said in the previous question, I do think that this application
has a lot of potential for factory implementation because it would
allow them to stack things in an organized way.

3. Who is not supposed to use this technology? Why?

- I don't think there is anyone that shouldn't
use this technology. It is meant to be more of a
fun game than anythything else and I think that that
is something that everyone should be allowed to experience,
but I also think that if factories were to start using this code,
they should consider how their materials would be effected by
it and how it would effect those materials to be stacked in a
tower-like structure instead of however they were to usually package it.

4. How can the type of robotic application implemented in your 
project cause harm?

- I think that it could cause harm in factories if it took
away jobs. I also think it could potentially harm materials
or people if it was used in a factory setting and not adjusted
for that factory's specific needs.

5. What solutions can be developed to avoid the harm
caused by this type of technology or to fix the harm?

- I think that in order to fix the problem of this technology,
new jobs need to be created that are things that only humans can do.
That or I think this robot implementation should only be used if there
are no people willing to do that labor-intensive job anymore.
I also think that making sure that this technology is altered
for each specific factory environment is very important because
it would help to keep safety and efficiency levels in a good place.

## Team Working Strategy

Describe the details of your team working strategy,
specifically explain how did you complete this work as a
team and describe the specific contributions of each team member.

- For this project, our team decided to just do
everything together. We always met up to work on tasks
together and we were able to create the code as well as
fix hardware issues together. Trang was very good at fixing
the hardware issues and Evelyn was very good at doing the coding,
but both of us were present in order to help with those issues
as well as add our opinions when making decisions regarding the
project. Overall, I think we worked very well together and were able to accomplish a lot!

## Challenges and Learning Experiences

Discuss any challenges you have encountered during the work on this
assignment and describe the biggest learning takeaways.
