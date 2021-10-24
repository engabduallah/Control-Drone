# Designing Control System for Drone Wing Motor

![image](https://user-images.githubusercontent.com/87785000/126638350-ce308e14-2b6b-4641-a5bc-3112809b1c87.png)

This Project is done by Eng. Abduallah Damash, and assigned to me by Asst. Prof. Dr. ‪Canras Batunlu‬ as part of EE302 (Feedback System) course.

If you have any issues or comments on the project, contact me on Linkedin (https://www.linkedin.com/in/engabduallah).
I also provided all the files that I used in this project so that you can try it by yourself. 

Insight about the project: 

The aim of the project is to run an analytical simulation to decide what is the better approach for controlling the motor of drone wing. That is by designing three types of controllers for different speeds to decide which one will make the system more stable in term of the maximum overshot and settling time for all the speed. Also, the system will continue three main components which are the controller, the motor, and the negative unite feedback. 

Motor Circuit Design: 

in order to design a control system that contain a DC motor, controller for adjusting the speed of the motor, and a unity negative feedback, we can model the DC motor by using DC-DC boost converter that will switch when the controller need to adjust the speed. 

![image](https://user-images.githubusercontent.com/87785000/138581823-627dbc4c-3f98-419b-abf5-5dacc63ac7c8.png)

Controller Parameters:

Let consider the transfer function of the PID, PD, and PI controllers in order to find the 𝐾𝑃,𝐾𝐼, 𝑎𝑛𝑑 𝐾𝐷 parameters in the closed loop system. In fact, these parameters can be found using Ziegler-Nichols Tuning Method.

![image](https://user-images.githubusercontent.com/87785000/138581863-c6429e75-f1b6-4a75-a79f-6f7b363952f5.png)

Notice that each type of controller has different gain parameters because they need to meet the requirement of maximum overshot to be less than 15% and settling time around 3 seconds.

MATLAB Circuit:

![image](https://user-images.githubusercontent.com/87785000/138581892-e4c3a551-83b4-4dd1-853b-cd69e029f9d2.png)

Simulation Results:

Now, in order to generate 3 different speeds, there are two step inputs that start at 4000 rpm, and then increased to 7500 rpm ending at 10000 rpm at each 10 second, so total simulation time is 30 seconds. Running the simulation with the values found in Table.1, it will be as following:

  -PID Controller Simulation Output:
  
  ![image](https://user-images.githubusercontent.com/87785000/138581934-2086a9a9-25b7-4374-bcbf-18dae0b96634.png)  
  
  -PI Controller Simulation Output:
  
  ![image](https://user-images.githubusercontent.com/87785000/138581953-06bd37d6-9bc2-425d-bf93-f8ce4821e54c.png) 
  
  -PD Controller Simulation Output:
  
  ![image](https://user-images.githubusercontent.com/87785000/138581963-14bf149f-eedf-492d-9235-5d61d321daf9.png)
  
Conclusion:

![image](https://user-images.githubusercontent.com/87785000/138581980-b1d4a428-88b3-483a-90a6-f8f0772f7035.png)

In the end, we can conclude that the best approach for designing an effective control system for the drone motor that is using PID controller because it meets the parameter of the overshot and settling time. 
However, using PD will be better in systems where we need to minimize the overshot of the system as shown in the graph. 
Also, PI optimizes the raising time compering to other ones so it can be used in systems where raising time is a critical parameter. 

Each type of controller has its advantage and disadvantage and choosing which one is better depends on the different parameter in the system such as settling time, overshot, raising time.etc. That come from experience and observing different control systems in different application. 

Enjoy it. 

All rights saved, if you want to use any piece of the code, mentioning my name will be enough.
