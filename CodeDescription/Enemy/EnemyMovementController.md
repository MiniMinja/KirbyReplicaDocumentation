# EnemyMovementController

#### MonoBehaviour

<p>&nbsp;</p>

[back to table of contents](/CodeDescription/TableOfContents.md)

<p>&nbsp;</p>

## Description:  
This script defines the automation of enemy movement. 
Currently, the enemy just moves in a straight line, and, once colliding with a wall, will switch direction.


<p>&nbsp;</p>
<p>&nbsp;</p>

# Table of Contents
- [Data](#data)
    - [Public](#public)
    - [Private](#private)
- [Functions](#functions)
    - [Public](#public-1)
    - [Private](#instance-1)

<p>&nbsp;</p>
<p>&nbsp;</p>

## Data:

### **Public:**

`float moveForce`  
power of enemy's walk 

### **Private:**

`Rigidbody2D rb`  
reference the rigidbody component of enemy

`Walldetector leftSide`  
the left "hand" of the enemy that detects collision with wall. See [WallDetector](/CodeDescription/Character/WallDetector.md)

`Walldetector rightSide`  
the right "hand" of the enemy, the other side of the `leftSide` variable.

`FeetChecker feet`  
the "feet" of the enemy. Checks to see if the enemy is grouded or not. See [FeetChecker](/CodeDescription/Character/FeetChecker.md)

`int dir`  
the direction the enemy is moving horizontally. `-1` if moving left, `1` if moving right.

<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

### **Public:**

### **Private:**

`Start()`  
initializes all the instance variables. Starts the enemy moving in the left direction (`-1`).

`FixedUpdate()`  
defines the behaviour of the enemy's scripted movement. Currently, the enemy will walk in a straight direction until it collides with a wall, on which it will switch direction and walk the other way.