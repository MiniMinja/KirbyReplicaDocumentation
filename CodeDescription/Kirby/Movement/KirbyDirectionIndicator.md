# KirbyDirectionIndicator

#### MonoBehaviour

<p>&nbsp;</p>

[back to table of contents](/CodeDescription/TableOfContents.md)

<p>&nbsp;</p>

## Description:
This script exists to flip Kirby's sprite to show the player which direction kirby is facing. This is done by changing its scale to be -1.

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

`KirbyMovementController kirby_move_script`  
reference to the [move script](/CodeDescription/Kirby/Movement/KirbyMovementController.md)

<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

### **Public:**

### **Private:**

`Start()`  
initializes `kirby_move_script`

`Update()`  
transforms the `transform.localScale` to flip kirby around depending on the [movement script](/CodeDescription/Kirby/Movement/KirbyMovementController.md). A value of `-1` indicates left and `1` indicates right.