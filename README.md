# Identification of Dynamic Model of A 5-DOF Robot Arm
The goal of this thesis is to identify the dynamic model of youBot arm. Since the dynamic force is relatively small compared to friction and gravity, the friction and gravity must be enough accurately identified. 

The identification is separeted into two steps:
1. Friction and gravity identification
2. Rigid body identification

# identification of friction and gravity
After investigation, the friction is not only realted to velocity but also to the load, which is driven by the transmission system. 
Since the dynamic force is relatively small, its influence on the friction can be igored. 

After identification of friction and gravity, they are compensated in identifcation of rigid body. The identicication of rigid body is based on optimaly excitation trajectory. There are two common optimization criterion: minimizing condition number and d-optimality. The former is to minimize the sensitivity to the disturbance, while the latter aims to minimize the variance of the estimted parameters. 

The trajectory with minimization of condition number as criterium tends to move slowly compared to d-optimality. In terms of excitation of the parameters, d-optimality is more suitable to dientify the robot, whose dynamic parameters are very small. 

The estimation technology is least square. Since the standard deviation of the measurements are not the same, the weighted least square estimator is applied. 

Result: Joint 1: not good, the reason maybe the time-variance of the friction or the ignored influence of dynamic on friction
        Joint 2,3 OK
        Joint 4,5 acceptable
