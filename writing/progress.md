# Team member: Trang Hoang, Evelyn

## Completed Prototype

Describe your working prototype: what can your robot currently do?

What's interesting about this progress report is that Trang and I were able to effectively get our robot to pick up and stack four cups. However, we were having some errors with the hardware and needed to start from the beginning because the hardware was malfunctioning and making the code no longer consistent. It was because of this that we decided to start over and write new code that took into account the inconsistencies that we've been struggling with for this lab period. We still have our successful code saved. And below is an example of what it looks like, however, we were not able to successfully make progress with the 2 other cups we need the robot to stack. The other main issue that we've been facing is that we tell the code to do something and the robot will not move according to the degrees that we specified. So we told the robot arm to go down with the y command but it will move very little if at all, which is a problem because the cup stack gets shorter and shorter the more cups you take away from it. Other than that, I think we have been doing well, and we have plans to meet up on saturday to trouble shoot these issues.

```python
sequence = [
     { "command": "a:+34","delay": 1.0  },
     { "command": "e:+100","delay": 1.0 },
     { "command": "x:+30","delay": 1.0  },
     { "command": "y:-60","delay": 1.0  },
     { "command": "e:-55","delay": 2.0  },
     { "command": "y:+55","delay": 2.0  },
     { "command": "a:-50","delay": 1.0  },
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-75","delay": 2.0  },
     { "command": "e:+55","delay": 2.0  }, # first cup placed down in stack position 1

     { "command": "y:+75","delay": 1.0  },
     { "command": "a:+52","delay": 1.0  }, # ready to pick up next cup
     { "command": "y:-68","delay": 1.0  },
     { "command": "e:-60","delay": 2.0  }, 
     { "command": "y:+75","delay": 2.0  },
     { "command": "a:-65","delay": 1.0  },
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-85","delay": 1.0  },
     { "command": "e:+55","delay": 1.0  }, # second cup placed next to first

     { "command": "y:+75","delay": 1.0  },
     { "command": "a:+65","delay": 1.0  }, # ready to pick up next cup
     { "command": "y:-90","delay": 1.0  },
     { "command": "e:-60","delay": 2.0  }, 
     { "command": "y:+75","delay": 2.0  },
     { "command": "a:-34","delay": 1.0  },
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-100","delay": 2.0  },
     { "command": "e:+55","delay": 1.0  }, # third cup placed

     { "command": "y:+90","delay": 1.0  },
     { "command": "a:+34","delay": 1.0  }, # ready to pick up next cup
     { "command": "y:-95","delay": 1.0  },
     { "command": "e:-60","delay": 2.0  }, 
     { "command": "y:+75","delay": 2.0  },
     { "command": "a:-43","delay": 1.0  },
     { "command": "x:-10","delay": 1.0  }, # moving back to better place the fourth cup
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-80","delay": 1.0  },
     { "command": "e:+55","delay": 1.0  }, # fourth cup placed

     { "command": "y:+80","delay": 1.0  },
     { "command": "a:+45","delay": 1.0  }, # ready to pick up next cup
     { "command": "e:-55","delay": 1.0  },
     { "command": "y:-120","delay": 1.0 },
     { "command": "e:-60","delay": 2.0  }, 
     { "command": "y:+100","delay": 2.0 },
     { "command": "a:-58","delay": 1.0  },
     { "command": "x:-10","delay": 1.0  }, # moving back to better place the fourth cup
     { "command": "f:+15","delay": 1.0  },
     { "command": "y:-80","delay": 1.0  },
     { "command": "e:+55","delay": 1.0  }, # fifth cup placed
]
```

## Remaining Work

Describe what needs to be completed in order for your project to satisfy its acceptance criteria

Next time we meet, the first step we take is to let the robot do the previous task, because sometimes the robot's hardware is inconsistent. If the robot works well with previous code, we will continue to do the command so the robot can stack more cups. Last time, we have the code stacking 4 cups, in total we need to stack 6 six cups. Next step we do is coding the command for the robot to stack the last 2 cups on top of the previous cups. Finally, we will have 6 cups stack perfectly. to make a cup tower. However, if the project will not go well as we expect, we will test the previous code and get the cups in the right position we want. In the case that any hardware problem occurs, we will look at the problem and fix it as soon as possible.  
