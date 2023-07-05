Let's say we want to throw projectiles by aiming wherever we want:

## Pawn Rotation
To aim the projectile we have to update the projectiles rotation with the player's rotation.
Setting the Player Pawn rotation to be the projectile's spawn rotation doesn't work because the value doesn't get updated. To get the updated version we have to use the ==Get Control Rotation==. This function gets the Controller rotation of the actor. That way, the projectile will be rotated wherever we rotate the player camera.

## Forward Vector
Secondly, to launch the projectile forward, we have to update the rotation of the Impulse by a forward vector amount that will determine how much the projectile will go forward. We can give the impulse a value using the ==Get Actor Forward Vector== function that will return the correct forward vector rotation.

![[Screenshot 2023-06-18 191738.png]]