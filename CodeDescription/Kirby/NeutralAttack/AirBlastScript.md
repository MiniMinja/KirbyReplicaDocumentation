# AirBlastScript

#### MonoBehaviour

<p>&nbsp;</p>

[back to table of contents](/CodeDescription/TableOfContents.md)

<p>&nbsp;</p>

## Description:
This script attaches to an AirBlast gameobject and defines its behavior. It mostly moves in one direction, and decelerates, eventually being destroyed once it stops moving.

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

`string enemy_tag`  
the tag this airblast should check collisions with.

`float initial_air_blast_speed`  
the speed of the airblast at the its start

### **Private:**

`float blastSpeed`  
the speed of the airblast through its path (decreases as it exists).

`int dir`  
the direction the airblast moves (`-1` for left, `1` for right).

<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

### **Public:**

`void Blast(int dir)`  
this function is like an "*activation code*" that 1. sets this object to be active and 2. initializes all the proper variables. It's like an accessible `Start()` function.

### **Private:**

`void Start()`  

`void Update()`  
moves the object in a set direction and destroys it once it fully slows down.

`void OnTriggerEnter2D(Collider2D collision)`  
if the airblast hits an enemy, it deals damage to the enemy calling the `TakeDamage` function in [CharacterDamageBehavior](/CodeDescription/Character/CharacterDamageBehavior.md).
