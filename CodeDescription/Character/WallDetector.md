# WallDetector

#### MonoBehaviour

<p>&nbsp;</p>

[back to table of contents](/CodeDescription/TableOfContents.md)

<p>&nbsp;</p>

## Description:
This script attaches to the 'hand' objects (left and right). This script checks for collisions to check for collisions against walls. This wall-checking script can be used for automated characters to interact with the wall and react (such as changing direction when running into a wall).


<p>&nbsp;</p>
<p>&nbsp;</p>

# Table of Contents
- [Data](#data)
- [Functions](#functions)

<p>&nbsp;</p>
<p>&nbsp;</p>

## Data:

### **Public:**

### **Instance:**

`bool foundWall`  
tells whether the 'hand' gameobjects collided with the wall

<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

### **Public:**

`bool WallFound()`  
returns the `foundWall` variable

### **Instance:**

`Start()`  
initializes the foundWall variable

`Update()`

`OnTriggerEnter2D(Collider2D collision)`  
checks for a wall and sets the `foundWall` variable respsectively

`OnTriggerExit2D(Collider2D collision)`  
checks for a wall and sets the `foundWall` variable respsectively
