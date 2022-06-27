# FeetChecker

#### MonoBehaviour

<p>&nbsp;</p>

[back to table of contents](/CodeDescription/TableOfContents.md)

<p>&nbsp;</p>

## Description:  
This is the script that attaches to the 'feet' gameobject. Through hitboxes, it determines whether the character's feet have touched the ground or not. When a character lands on the ground (when the collision detects a ground object), it takes time to be grounded. For a certain duration, a landing variable is set to be true before the grounded variable is set to true.


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

`float landTime`  
the time it takes for the character to land before it is grounded

### **Private:**

`bool landing`  
a variable that tells us if the character is landing before it is grounded

`bool isGrounded`  
tells whether or not the character is grounded.

<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

`OnTriggerEnter2D(Collider2D collision)`
starts the `Land()` coroutine, setting a timer to be grounded when the feet check the ground (character got right ontop of ground)

`OnTriggerExit2D(Collider2D collision)`  
deactivates the landing and isGrounded variables (character has left the ground)

`Land()`  
a coroutine that runs a timer to transition from landing to grounded, changing the variables respectively

`Grounded()`
returns whether the character is grounded
