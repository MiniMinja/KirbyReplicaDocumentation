# CharacterDamageBehavior

#### MonoBehaviour

<p>&nbsp;</p>

[back to table of contents](/CodeDescription/TableOfContents.md)

<p>&nbsp;</p>

## Description:
Does damage effects to the character this component is attached to. Effects include:
- taking damage
- being knocked back
- being invulnerable after damage

Also deals damage to itself whenever it enters a specified "enemy collider". 

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

`float invulnerableTime`  
invulnerability duration

`float knockBackPower`  
how strong the knockback is  

`string opposingTag`  
the tag that causes the gameobject to take damage. Basically, kirby takes damage from enemy and the enemy takes damage from kirby.

<br>

### **Private:**
`bool invulnerable`  
tells whether or not the character is invulnerable

`BoxCollider2D this_collider`  
character's collider

`Rigidbody2D rb`  
character's rigidbody (physics component)

<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

### **Public:**

`TakeDamage(Vector3 knockBackDir)`  
calls for invulnerability and deals knockback when character is not invulnerable. Calls `BeInvulnerable()` and `Knockback()` functions.

`BeInvulnerable()`  
a coroutine that makes the character invulnerable. Invulnerability duration is specifed in the `invulnerableTime` variable

`Invulnerable()`  
returns whether or not the character is invulnerable

`Knockback(Vector3 knockbackDir)`  
adds a(n impulse) force to the character, simulating a knockback

`GetSucked(Vector3 pullDir)`

### **Private:**

`Start()`  
initializes the instance variables

`Update()`

`OnTriggerEnter2D(Collider2D collider)`  
checks for collision with enemy colliders
