# CrouchBehavior

#### MonoBehaviour

<p>&nbsp;</p>

[back to table of contents](/CodeDescription/TableOfContents.md)

<p>&nbsp;</p>

## Description:
This script defines the logic for Kirby's crouch. The logic behind Kirby's crouching turns out to be way less intuitive than it might seem at first. Not only does the crouch button need to be pressed, Kirby needs to be deflated and grounded.

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

### **Private:**

`bool crouching`  
tells whether or not Kirby is crouching.

`bool groundedOnceAfterCrouch`  

`float collider_width, collider_height`  
defines the collider's width and height at the beginning (non-crouched). This way, when Kirby is crouched, the collider height can be set to half of a constant value.

`float sprite_width, sprite_height`

`BoxCollider2D kirby_collider`  
reference to Kirby's collider component.

`KirbySpriteBehavior kirby_sprite`  
reference to the [sprite script](/CodeDescription/Kirby/SpriteWork/KirbySpriteBehavior.md).

`KirbyMovementController kirby_move_script`  
reference to the [movement script](/CodeDescription/Kirby/Movement/KirbyMovementController.md).

`FeetChecker feet`  
reference to the [feet script](/CodeDescription/Character/FeetChecker.md).

<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

### **Public:**

### **Private:**

`Start()`  
initializes all the variables defined in the [data](#data) above.

`Update()`  
defines the logic for when Kirby has crouched. Not only does kirby need to be grounded, kirby has to be deflated (not-fluttering). Then the key for crouching is checked before Kirby's sprite and collider is halved.

`Crouching()`  
returns whether or not Kirby is crouching.
