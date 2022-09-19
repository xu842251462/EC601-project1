# EC601-project1
  Bin Xu
  
  Topic: 15-Delivery Bot
  
  Project 1 due: Sep 18
  
  link: https://docs.google.com/document/d/17_W3ligz6PbwJd79i5bmxHV36b5YZ2MMXnjsYRbyeic/edit
  
  pdf version uploaded in this repo: EC601 Project 1 final paper
  
  
Introduction

In most supply chains, the final phase of product delivery, from the warehouse or distribution center to the end-user, accounts for about 28% of total transportation costs. Congestion in cities, remote locations, incorrect or erroneous address information, difficult-to-find destinations, and a severe labor shortage for providing on-demand delivery services are all factors that affect last-mile delivery. Thereby, certain factors are contributing to the market growth. Moreover, continued e-commerce expansion, as well as rising consumer expectations for faster and frictionless deliveries, have produced attractive industry growth potential(Source: Facts & Factors).
Delivery Robot is a complex engineering product in the industry. We need an algorithm about road planning, an algorithm for avoiding obstacles and an algorithm for detecting human and other features. If we can use delivery robots to do delivery, it is possible to reduce the expense of labor for the company. Technology from delivery robots will help us develop self-driving technology.


Current Application

Security.
Space Exploration. 
Entertainment. Robots are also a big draw in the entertainment industry. ...
Agriculture
Health Care
Underwater Exploration
Food Preparation
Manufacturing.


Current Research

In the past, robots used digital maps to detect the surrounding area and find the optimal route. The hard part is to classify the image in real realtime. It is possible to find the driveway for the delivery robot, but the route from the curb to the door is hard to be recognized.
After doing the research on this topic, I found that the MIT research team uses one technology called image to image translation. They layered the polygon on the object from the image and assigned the color to the object. When the drone works on the driveway, it detects the object with the colored map. The main idea of the research is to use static objects to train the machine. After training, the robot can identify the object faster and classify the feature on the road without seeing it before. 

Path Planning Constraints

In order to apply path planning, there are four constraints needed to be considered. 
Minimum Route Leg Length
Maximum Turning Angle
Route Distance Constraint
Fixed Approach Vector to Goal Position
For the minimum route leg length, it controls the route for a predetermined minimum distance before initiating a turn. For the drone, there is no such constraint. But for the delivery robot running on the driveway, this is an important constraint to be considered.
For the maximum turning angle,  it allows turns less than or equal to a predetermined maximum turning angle. When the delivery robot turns over the max angle, it will cause the collision to the pedentraint. The sensor on the delivery robot needs to calculate the turning angle in real-time to make sure the delivery robot can smoothly turn in a different direction.
For the route distance constraint, the path planning algorithm needs to calculate the optimized distance for the delivery robot. The optimal route will meet the requirement of cost control and time control. For the company which wants to apply the delivery robot to deliver the package, cost and time constraints are closely related to the cost of delivery.
For the fixed approach vector to goal position, path planning algorithms need to set the goal position for the delivery robot. When there are destination and source, it is possible to set path planning.


Different base path planning algorithm

Most geometrical route planning algorithms can be considered either grid-based or graphic-based in nature. Each type of algorithm has its own associated advantages and disadvantages.
For grid-based route planning, it is good to finish analyzing in real-time. But this approach has difficulty in finding the maximum route distance and maximum turning angle. The grid-base map is shown in figure 1. A digitized grid consisting of square cells of equal size represents the environment in which the route planning is performed. The size of the environment (or path planning workspace) is m £ n grid cells(3). A route is planned from the starting point in the grid,  each grid cell corresponds to a particular location in the environment. A cost estimation step establishes a “cost” value for a particular cell, corresponding to the cost incurred by traveling through that particular region(3). 
![alt text](https://github.com/xu842251462/EC601_2022fall/blob/main/Capture.PNG)
For graphic-based route planning, it is more accurate but is hard to be applied in the real-time situation. When a robot accepts the image on the driveway, it is good to classify the feature by the deep learning algorithm. The problem is that analyzing images takes a long time to classify the object. This is hard for delivery robots to finish in real-time. 

Combination of grid-base and graph-based approach

From the above research on the path planning algorithm, in order to combine the advantage of two based approaches in the further research I plan to use both approaches in my research paper. The goal of the optimized path planning algorithm is to improve the time-consumption on the path planning and is possible to be applied in real-time. Using the grid-base approach to calculate the rough route planning at first, then using real images to adjust the turning angle and avoid the obstacles in real-time.
References

L. Fridman et al., "MIT Advanced Vehicle Technology Study: Large-Scale Naturalistic Driving Study of Driver Behavior and Interaction With Automation," in IEEE Access, vol. 7, pp. 102021-102038, 2019, doi: 10.1109/ACCESS.2019.2926040.
R. J. Szczerba, P. Galkowski, I. S. Glicktein and N. Ternullo, "Robust algorithm for real-time route planning," in IEEE Transactions on Aerospace and Electronic Systems, vol. 36, no. 3, pp. 869-878, July 2000, doi: 10.1109/7.869506.
E. Nishani and B. Çiço, "Computer vision approaches based on deep learning and neural networks: Deep neural networks for video analysis of human pose estimation," 2017 6th Mediterranean Conference on Embedded Computing (MECO), 2017, pp. 1-4, doi: 10.1109/MECO.2017.7977207.

Open source project
Autonomous Delivery Robot: https://github.com/IvLabs/autonomous-delivery-robot. 
Auto pilot: https://github.com/ApolloAuto

Other References: 
How MIT Uses Artificial Intelligence to Train Delivery Robots to Find Front Doors, 
Brian Nordli, https://builtin.com/artificial-intelligence/mit-research-team-built-pizza-delivery-robot



