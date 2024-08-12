# Memory-Based-Cuckoo-Search-Algorithm
Minimizing the energy consumption in Robotic mixed-model assembly line

### Based on this article :
[Solving the energy-efficient Robotic Mixed-Model Assembly Line balancing problem using a Memory-Based Cuckoo Search Algorithm](https://www.sciencedirect.com/science/article/abs/pii/S0952197622002494?via%3Dihub)

# How to define the parameter of your "Robotic Mixed-Model Assembly Line" :
Write down on the excel sheets all the parameters that define your case. (Some examples [here](www.google.com))
Your .xlsx file should be name DonnéesX.xlsx. X is a number (eg : Données3.xlsx, Données15.xlsx)
### 1. Define the equipment("sheet1")
![image](https://github.com/user-attachments/assets/f9ea4783-717e-40f8-a2f3-38fafa614375)

### 2. Define the energy consomation for each tasks and standby for each robots("sheet1")
![image](https://github.com/user-attachments/assets/79d689b9-c979-41f0-b637-2b0880058f44)

### 3. Setup the precedence of your Mixed-Model ("sheet2")
![image](https://github.com/user-attachments/assets/a3fbdc93-3db7-4048-9ec1-1184b788b54b)
In the figure, the 1 in the cell : <u>column "1" row "3"</u> means that the task "3" need to wait the task "1" to be completed to start.
eg : The task 4 (row 4 in the figure) need tasks 1 and 2 completed to start.

# How to solve your problem :
### 1. Execute the python code here, be sure to put in the same repertory your .xlsx file and your .py file 
After executing the code, a new window should open :
![image](https://github.com/user-attachments/assets/333dc351-f80c-4df6-ae9a-a9db7bbf73b8)

### 2. Input the hyperpameters of Memory-Based-Cuckoo-Search-Algorithm.
To assure you better result, I recommend you to read the article which my code is based on.
In other way, the default are good to treat small problem as Données1.xlsx at Données4.xlsx.

<u>/!\The only cell you should pay attention/!\</u> is "Numero du Probleme" the number indicate have to be the same as your X in DonnéesX.xlsx.

Click on "Lancer l'algorithme" to launch the script.

### 3. Result.
To have access to your solutions you have to open the file "Résultat.xlsx"
![image](https://github.com/user-attachments/assets/590ab731-2986-4705-9e24-60d0127ef98c)
In the figure, you can see 10 different solutions.

The column "Robots" shows the robot attributed to the workshop
Solution "0" shows that workshop 1 & 2 should have the robot 1 and workshop 3 should have robot 2

The column "NbTaches" shows how many tasks should be attributed to each workshop.
Solution "0" shows that each workshop have 4 tasks to treat

The column "Ordonnancement" shows the task scheduling. The column "Fitness" is the energy cosumption of your solution. The column "CycleTime" is the cycle time of your solution. Then you have access to the calculation time.
