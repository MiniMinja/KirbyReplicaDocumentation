# DebugDeterminer

#### MonoBehaviour

<p>&nbsp;</p>
<p>&nbsp;</p>

## Description:
Given to the camera object, displays certain debug data.  
Currently, debug data displays
- kirby's velocity
- enemy's velocity

<p>&nbsp;</p>
<p>&nbsp;</p>

# Table of Contents
- [Data](#data)
    - [kirby](#public-gameobject-kirby)
    - [showVelocity](#public-gameobject-showVelocity)
    - [enemy](#public-gameobject-enemy)
    - [showVelocityOfEnemy](#public-bool-showVelocityOfEnemy)
    - [kirby_rb](#rigidbody2d-kirbyrb)
    - [enemy_rb](#rigidbody2d-enemyrb)
- [Functions](#functions)
    - [Start()](#start)
    - [Update()](#update)

<p>&nbsp;</p>
<p>&nbsp;</p>

## Data:
### *public* GameObject **kirby**
reference to kirby gameobject
### *public* bool **showVelocity**
toggles whether or not velocity shows for kirby
### *public* GameObject **enemy**
reference to enemy gameobject
### *public* bool **showVelocityOfEnemy**
toggles whether or not velocity shows for enemy

<p>&nbsp;</p>

### Rigidbody2D **kirby_rb**
reference to kirby rigidbody
### Rigidbody2D **enemy_rb**
reference to enemy rigidbody

<p>&nbsp;</p>
<p>&nbsp;</p>

## Functions:

### Start()
initializes **kirby_rb** and **enemy_rb**.

### Update()
draws a line that represents the velocity vector of both kirby and enemy. The velocity is only displayed if the respective boolean 'switches' are true.