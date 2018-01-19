---
layout: project
type: project
image: images/firstlogo.jpg
title: First Robotics
permalink: projects/vacay
# All dates must be YYYY-MM-DD format!
date: 2013-09-01
labels:
  - C++
summary: My first experience with Computer Science in a FIRST robotics competition.
---

FIRST robotics is a high school robotics competition where students come together as a team to build a robot to compete against other teams. The rules of the competition is different every year and each team is given a standard set of parts along with a budget for other parts. For this particular project that I am detailing, the competiton required a robot to shoot as many balls into any of the 3 baskets, each worth different points, to score. The objective was to obtain a higher score than the other team. To do this, the robots also had to be able to navigate through the field to collect as many balls as possible. Also, the robots are given a 15-second period to score additional points autonomously. 

For this project, I was one of the 3 programmers responsible for the autonomous mode as well as the basic controls. Using C++, we began with the basic functions of making the chassy move. Next, we programmed the controls for the shooting mechanism and the pick-up mechanism. These included motors to both pick up balls on the ground and fire them with the appropirate strength. The autonomous portion was more difficult as we had to design a code such that the robot could "sense" the target, align itself accordingly, adjust its distance, and shoot the ball. We used a sensor that could detect the box put around each basket and used that to have the robot position itself for the best possible shot. Our robot placed within the finals for our regional competition and we advanced to the national competition.

More information about this competition can be found their website:
https://www.firstinspires.org/robotics/frc
