---
title: "RTS orientated Group Behaviors"
layout: default
---    

## Boids System

**1. INTRODUCTION TO BOID SYSTEM:**
A model that mimics the collective behavior observed in flocks of birds, schools of fish, or herds of animals. In this virtual environment, each entity is referred to as a "Boid," representing an agent within the simulated group. Reffering more to its usage in the current features, it can simulate big armies behaviors that makes the game look more realistic, such as following their designated leader and running away from dangerous environments.

To begin with, the Boid System operates on three foundational principles: Alignment, Cohesion, and Separation on top of which is added the Collision Avoidance. Alignment involves Boids adjusting their movements to match the average direction of their neighboring entities. Cohesion wants Boids to move towards the average position of their peers and Separation ensures that Boids avoid crowding by steering away from nearby entities, maintaining a reasonable distance. As it is designed to be RTS orientated,  Boid leaders can be designated, in the area of which those previously described featured are activated. 

**2. CORE CONCEPTS OF BOID BEHAVIOR:**
I built an independent system that recognize its environment and combines the three previously described behaviors as weighted by the user while apllying collision avoidance . To dive into it , I used ray casting as main method of recognizing future possible collision, and steering as a way of adapting the direction according to the environment build up of cirular and rectangular shapes. Each boid has a predifined angle of view for casting rays. Depending on each cast result, it is decided the steering away from obstacle direction. Also, on an RTS level, Path finding can be applied to boids and combined with the three fundamental laws. The boids tend to steer back to their initial state after avoiding obstacles in the way. This prevents sudden and unnatural changes in velocity .

*Collision Avoidance technic, advantages and eventual limitations*

*Final Boid System Demo*

//pune gif demo

**3. REAL-WORLD APPLICATIONS OF BOID SYSTEMS:**
Battlefield Crowd Dynamics: The chaos of a battlefield, where individual units dynamically navigate through the terrain, avoiding collisions and coordinating movements.  The boid System in an RTS game can simulate these crowd dynamics. 

Traffic Flow in City building Games: City building RTS games often feature dynamic traffic systems where citizens or vehicles traverse the city . The boid system can mimic traffic flow and big crowds.

I reckon that the advantage of adding the current system into an RTS context is a dynamic response to situations. For instance, in the case of an enemy attack, Boids AI can make up unit formations for defensive strategies or coordinate retreats, making the process look more realistic.

**4. OPTIMIZATION AND PERFORMANCE CONSIDERATIONS:**
Distance-based Calculations:

Calculations are optimized by focusing on interactions within a specified radius dictated by a boid leader.  Entities beyond this range have negligible impact on each other and they are excluded from computations, reducing the overall workload.


## Group Formation and Management

**1. INTRODUCTION TO GROUP FORMATION AND MANAGEMENT:**
The implementation of an Organized Group Movement System represents an important feature in real-time strategy gaming dynamics. This system grants players the capability to command groups of entities, not just by grouping them together but by shaping them into specific formations capable of navigating as a whole. A range of RTS gaming experiences have this as their basis.

**2. CORE CONCEPTS OF GROUP FORMATION:**
The system dispose of two group formation shapes: circular and quadratic . The player can switch between them during the player experience. The system can handle obstacle avoidance on the way and speeding up to get back to the formation.

3. USER INTERACTION SYSTEM:
The Group Formation system is supported by UI used for group shape choices , selection and target setting

**4. REAL-WORLD APPLICATIONS OF GROUP FORMATION:**

Military Strategy Simulations:
In military strategy games, the Group Formation system shows real-world tactics. Entities can form different tactical shapes responding intelligently to player commands. Navigating these groups collectivelywhile sticking to their formation to execute strategic maneuvers enhances the realism of military simulations.

Resource Gathering Efficiency:
In RTS games that involve resource gathering, the Group Formation system can also enhance the experience. Entities responsible for resource collection can organize into groups.

Multiplayer Team-based Games:
Multiplayer games with team dynamics benefit from the Group Formation system. Players can command entities to organize into formations during team based matches.