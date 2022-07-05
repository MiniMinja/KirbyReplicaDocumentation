# AttackHitboxScript

#### MonoBehaviour

<p>&nbsp;</p>

[back to table of contents](/CodeDescription/TableOfContents.md)

<p>&nbsp;</p>

## Description:
This script defines the hitbox for attacks, particularly close-range combat (non-projectiles). For this project, this attaches to the SlideAttack gameobject. 

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

`string enemyTag`  
the tag of the objects that Kirby attacks. Thre collision detections will check for these objects.

### **Private:**

`KirbyMovementController movement_script`  
reference to `KirbyMovementController` script.

<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

### **Public:**

### **Private:**

`void Start()`  
initializes the private variables.

`void Update()`  

`void OnTriggerEnter2D(Collider2D collision)`  
looks for the enemy objects and deals damage, calling their `TakeDamage()` function from their [CharacterDamageBehavior](/CodeDescription/Character/CharacterDamageBehavior.md) script.