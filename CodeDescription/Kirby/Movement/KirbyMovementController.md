# KirbyMovementController

#### MonoBehaviour

<p>&nbsp;</p>

[back to table of contents](/CodeDescription/TableOfContents.md)

<p>&nbsp;</p>

## Description:
This script controls and defines Kirby's movement including jumping and fluttering. It reads user input and behaves accordingly ('a' is left, etc). This script also shares data about Kirby's movement such as whether or not Kirby is in the air or crouching.

<p>&nbsp;</p>
<p>&nbsp;</p>

# Table of Contents
- [Data](#data)
    - [Public](#public)
    - [Private](#private)
- [Functions](#functions)
    - [Public](#public-1)
    - [Private](#private-1)

<p>&nbsp;</p>
<p>&nbsp;</p>

## Data:

### **Public:**

`float regularDrag`  
the movement drag when Kirby is deflated.

`float flutterDrag`  
the drag when Kirby is fluttering. Drag is higher, making Kirby feel slower.

`float floatForce`  
the power of Kirby's fluttering.

`float jumpForce`  
the power of Kirby's jump.

`float moveForce`  
the power of Kirby's walk (only affects horizontal movement).

### **Private:**

`Rigidbody2D rb`   
reference to the Rigidbody component.

`FeetChecker feet_script`  
reference to the FeetChecker component (see [FeetChecker](/CodeDescription/Character/FeetChecker.md)).

`CrouchBehavior crouch_script`  
reference to the CrouchBehavior component (see [CrouchBehavior](/CodeDescription/Kirby/Movement/CrouchBehavior.md)).

`KirbySpriteBehavior kirby_sprite_script`  
reference to the KirbySpriteBehavior
(see [KirbySpriteBehavior](/CodeDescription/Kirby/SpriteWork/KirbySpriteBehavior.md)).

`bool jump`  
tells whether or not Kirby has jumped. This variable is used to indicate an event between two functions that get executed on different threads (i.e. `Update()` and `FixedUpdate()`).

`bool flutter`  
tells whether or not Kirby flutters (pushed up in flutter form), differing from `fluttering`. This is used to indicate an event between two functions that get executed on different threads (i.e. `Update()` and `FixedUpdate()`).

`bool fluttering`
tells whether or not Kirby is in the fluttering form (inflated or not).

`bool exitFlutter`
tells whether or not Kirby is exiting flutter, acting as an indicator for the *transition* between fluttering and non-fluttering states.

`int dir`
tells which direction Kirby is facing (`-1` is left, `1` is right).

<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

### **Public:**

### **Private:**

`Start()`

`Update()`