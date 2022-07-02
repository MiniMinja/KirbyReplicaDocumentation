# KirbyMovementController

#### MonoBehaviour

<p>&nbsp;</p>

[back to table of contents](/CodeDescription/TableOfContents.md)

<p>&nbsp;</p>

## Description:
This script controls and defines Kirby's movement including jumping and fluttering. It reads user input and behaves accordingly ('a' is left, etc). This script also shares data about Kirby's movement such as whether or not Kirby is in the air or crouching. This script uses public functions to *activate* a movement behavior (for example, jumping is *activated* by the Jump function).

Alot of the code uses variables as a means to communicated information between the `Update()` and the `FixedUpdate()` function. In order to communicate ideas about button presses, variables are set through public functions

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

`void Jump()`  
sets the jump variable to true.

`void Flutter()`  
sets the flutter variables to true. It also changes the drag appropriately. 
It also calls the sprite script to do fluttering animations. 

`void LoseFlutter()`  
sets all flutter variables to false. It also changes the drag appropriately.
It calls the sprite script to do idle animations.

`bool IsFluttering()`  
returns the `fluttering` variable.

`void ExitFlutter()`  
starts the transition to exiting flutter by setting the `exitFlutter` to true.

`void FullyExitFlutter()`
finalizes the transition of exiting flutter by setting `exitFlutter` to false.

`bool ExitingFlutter()`  
returns the `exitFlutter` variable.

`int CurrentDirection()`  
returns the `dir` variable.

`bool Grounded()`  
acts as a passing function for the `FeetChecker.Grounded()` function.

### **Private:**

`Start()`  
initializes all the private variables.

`Update()`  
commands the logic of Kirby's movement from user input. This calls the public functions instead of changing the variables directly.

`FixedUpdate()`  
depending on the state of the variables, it applies certain forces to Kirby's rigidbody component.