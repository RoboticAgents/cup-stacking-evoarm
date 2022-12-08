# Report by Evelyn Griffith and Trang Hoang

## Project Summary

TODO: Describe the completed project. Provide motivation for your project, application that your robot is utilized for, specific goals/tasks it completes, and include any background references you used to develop the idea for your project (links are okay).

## Project Implementation Details

TODO: First, outline all steps one must take to run your project, including any needed installations. Then describe **all** steps you took to implement the task, including all non-technical and technical details. Please include references (links are okay) to all resources you have used.

In order to run this project one must:

1.) Obtain the required Evoarmminni from the Allegheny ALIC Lab (or obtain and build a new Evoarm Mini Model)
2.) Plug in the robot to a reliable outlet
    - making sure that all of the wiring is set up correctly as the 334 model has the tendency to have wires that disconnect
    - If the robot is working appropriately it will give you an indication that it is on and all the wires are working correctly (usually this is some form of motion that gets it to its home position).
3.) Now you should connect your laptop to the robot wifi connection
    - Turn the wifi on your computer off and back on (just to give it the chance to detect new networks)
    - look for a wifi connection called `Evoarmmini334` or `Evoarmmini###` with the hashtags representing the number of your evoarm
    - click on that wifi connection and give it a few second to fully connect
    - Once connected it should say something like: `No internet, secured`
4.) Now you can connect to the robot's online interface by typing this in your browser `http://10.10.0.1:9072/`
5.) From there an interfact should pop up that allows you to manually drive the robot along with several other tabs along the top of the screen
6.) Type on the `Apps` tab and you will notice that a list of different applications for running the evoarm come up.
7.) For one of these apps (preferably one written in python) scroll to the far right hand side of the screen and click on the little box that says `edit`. 
8.) Once you're there you will see a box that says `name` Rename the task to `CupStacking.py` and click either `save` or `save a copy`. This will create a new document back on the apps screen that you can edit.
9.) Click on the same `edit` button for `CupStacking` and clear whatever is in the contents section of the app.
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
     { "command": "e:+55","delay": 2.0  }, # first cup placed down in stack position 1

     { "command": "y:+75","delay": 1.0  },
     { "command": "a:+52","delay": 1.0  }, # ready to pick up next cup
     { "command": "y:-55","delay": 1.0  },
     { "command": "e:-72","delay": 2.0  }, 
     { "command": "y:+75","delay": 2.0  },
     { "command": "a:-66","delay": 1.0  },
     { "command": "f:+15","delay": 2.0  },
     { "command": "x:-10","delay": 2.0  },
     { "command": "y:-90","delay": 3.0  },
     { "command": "e:+7","delay": 2.0   }, # second cup placed next to first

     { "command": "y:+75","delay": 1.0  },
     { "command": "e:+50","delay": 1.0  },
     { "command": "a:+64","delay": 1.0  }, # ready to pick up next cup
     { "command": "x:+10","delay": 1.0  },
     { "command": "y:-80","delay": 3.0  },
     { "command": "e:-80","delay": 3.0  }, 
     { "command": "y:+75","delay": 2.0  },
     { "command": "a:-35","delay": 1.0  },
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-95","delay": 3.0  },
     { "command": "x:+10","delay": 2.0  },
     { "command": "e:+7","delay": 3.0   },
     { "command": "e:+55","delay": 1.0  }, # third cup placed

     { "command": "y:+90","delay": 1.0  },
     { "command": "a:+34","delay": 1.0  }, # ready to pick up next cup
     { "command": "y:-95","delay": 1.0  },
     { "command": "e:-75","delay": 2.0  }, 
     { "command": "y:+75","delay": 2.0  },
     { "command": "a:-43","delay": 1.0  },
     { "command": "x:-10","delay": 1.0  }, # moving back to better place the fourth cup
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-75","delay": 1.0  },
     { "command": "e:+60","delay": 1.0  }, # fourth cup placed

     { "command": "y:+80","delay": 1.0  },
     { "command": "a:+45","delay": 1.0  }, # ready to pick up next cup
     { "command": "x:+15","delay": 2.0  }, # shifting forward to grab the next cup
     { "command": "y:-85","delay": 1.0  },
     { "command": "e:-70","delay": 2.0  }, #grabbing the fifth cup 
     { "command": "y:+100","delay": 2.0 },
     { "command": "a:-61","delay": 1.0  },
     { "command": "x:-10","delay": 1.0  }, # moving back to better place the cup
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-77","delay": 1.0  }, # fifth cup placed
     { "command": "e:+7","delay": 1.0   }, 
     { "command": "y:+85","delay": 2.0  },
     { "command": "e:+45","delay": 1.0  }, # arm out of danger

     { "command": "a:+61","delay": 1.0  },
     { "command": "y:-113","delay": 1.0 },
     { "command": "x:+5","delay": 1.0  },
     { "command": "e:-90","delay": 3.0  }, # grabbing 6th cup
     { "command": "y:+113","delay": 2.0 },
     { "command": "a:-55","delay": 1.0  },
     { "command": "y:-50","delay": 2.0  },
     { "command": "e:+60","delay": 2.0  }, # final cup placed
     { "command": "y:+60","delay": 1.0  }
]
```

## Experimental Results

TODO: Conduct at least three experiments with your completed implementation, where something is varied in each experiment (for example changes in the environment). Produce visual representation of these experiments (pictures or videos). Describe your observations of the outcome of these experiments (how did the robot behave in these experiments? were there variations?).

## Ethical Implications

Based on your experiences with the project and from our discussions in class, please provide answers for the following questions as related to the project you chose to implement:

1. Who would typically make the technology of the similar type as your project? Why?

TODO: Add an answer to the question above.

1. Who are the intended users of this robotic application? How does this technology benefit them?

TODO: Add an answer to the question above.

1. Who is not supposed to use this technology? Why?

TODO: Add an answer to the question above.

1. How can the type of robotic application implemented in your project cause harm?

TODO: Add an answer to the question above.

1. What solutions can be developed to avoid the harm caused by this type of technology or to fix the harm?

TODO: Add an answer to the question above.

## Team Working Strategy

TODO: Describe the details of your team working strategy, specifically explain how did you complete this work as a team and describe the specific contributions of each team member.

## Challenges and Learning Experiences

TODO: Discuss any challenges you have encountered during the work on this assignment and describe the biggest learning takeaways.
