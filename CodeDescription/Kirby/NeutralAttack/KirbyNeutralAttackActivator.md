# KirbyNeutralAttackActivator

#### MonoBehaviour

<p>&nbsp;</p>

[back to table of contents](/CodeDescription/TableOfContents.md)

<p>&nbsp;</p>

## Description:
This script acts as a "communicator" between the attack objects and user inputs. It essentially activates hitboxes and gameobjects when certain events happen in [KirbyAttackBehavior](/CodeDescription/Kirby/NeutralAttack/KirbyNeutralAttackBehavior.md).

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

`GameObject airblast_obj`  
a prefab for the airblast projectile in its deactivated state.

### **Private:**

`KirbyAttackBehavior attack_script`  
reference to the [KirbyAttackBehavior](/CodeDescription/Kirby/NeutralAttack/KirbyNeutralAttackBehavior.md). The activator reads from the behavior to see if it any variable state changes.

`GameObject slideAttack`  
reference to the slide attack gameobject.

`GameObject suckClose, suckFar`  


<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

### **Public:**

`void AirBlast()`  
creates a copy of the airblast object then sends it off in the direction Kirby is facing.

### **Private:**

`Start()`  
initializes all private variables.

`Update()`  
checks the `attack_script` variable to see either do slide attacks or airblasts.