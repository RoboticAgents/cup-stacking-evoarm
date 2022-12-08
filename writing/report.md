# Report by Evelyn Griffith and Trang Hoang

## Project Summary

Describe the completed project. Provide motivation for your project, application that your robot is utilized for, specific goals/tasks it completes, and include any background references you used to develop the idea for your project (links are okay).

Our final project is the cup stacking program, we tried to stack six mini cups to make a cup tower. We used the EvoArmMini334 to grab the cups and place them correctly to build the tower. Our inspiration for this project is the cup tower challenge for the kids which teach them the design skills and promote creativity. With this project we want to prove that robots can do the tasks like human does. This project is great for community demonstration as other people can see how the EvoArm creates the cup tower. The robot is controlled by a Python program which has the command tell it what to do while building the tower; therefore, it can create the cup tower without any human interference. Based on this project, we can program the robot's arm to grab any object to achieve the task that we want. The EvoArm has a gripper which can grab the mini cups, we programed it to make it only grab one cup at a time and placed it in the right position. After coding and testing process, we have the robot to build the cup perfectly and have a video of it.

## Project Implementation Details

TODO: First, outline all steps one must take to run your project, including any needed installations. Then describe **all** steps you took to implement the task, including all non-technical and technical details. Please include references (links are okay) to all resources you have used.

## Experimental Results

Conduct at least three experiments with your completed implementation, where something is varied in each experiment (for example changes in the environment). Produce visual representation of these experiments (pictures or videos). Describe your observations of the outcome of these experiments (how did the robot behave in these experiments? were there variations?).

Our cup tower is made of total six cups. The cups tower has 3 layers which are the bottom layer: 3 cups, the middle layer: 2 cups and the top layer: 1 cup. First, we code some commands for the robot to make the first layer. The robot picks up the first cup on the cup stack and moves to the tower position. Then, the first cup of the bottom layer is placed in the middle of the tower position. After that, the robot move back to the cup stack and pick up the second cup. This time the arm moves further to place the second cup at the right of the first cup. And the third cup is placed at the left of the first cup. Now, we have the first layer. For the second layer, we need to placed two cups. The EvoArm grabs the cup from the cup stack and places the left and right cup respectively, after placed the cups the Arm goes up to make sure it does not touch any cups next to it. Finally, the EvoArm places the last cup on top of the two cups in the middle layers, and we have the cup tower that we want to.

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

Trang: Discuss any challenges you have encountered during the work on this assignment and describe the biggest learning takeaways.

We faced a lot of challenges while doing this project. The biggest challenge is the hardware inconsistency, each time we work with the Arm we need to modify our code to make it works like we expect. So our strategy is to finish the project as soon as possible and take a video each when the program runs perfectly. Each time the robot pick up a cup the cup stack will be shorter, so we need to use 2 boxes to make the cup stack higher. Sometimes, the Arm does not drop the cup in the right position, so one of your classmate has helped us to print laser three circle on a carton paper to make the cups more stabilize in it positions. After all, we can get the project done and create a nice cup tower.