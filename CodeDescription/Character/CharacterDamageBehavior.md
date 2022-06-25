# CharacterDamageBehavior

#### MonoBehaviour

<p>&nbsp;</p>
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
    - [Instance](#instance)
- [Functions](#functions)

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

### **Instance:**
`bool invulnerable`  
tells whether or not the character is invulnerable

`BoxCollider2D this_collider`  
character's collider

`Rigidbody2D rb`  
character's rigidbody (physics component)

<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

`Start()`  
initializes the instance variables

`Update()`

`OnTriggerEnter2D(Collider2D collider)`  
checks for collision with enemy colliders

`TakeDamage(Vector3 knockBackDir)`  
calls for invulnerability and deals knockback

`BeInvulnerable()`

`Invulnerable()`

`Knockback(Vector3 knockbackDir)`