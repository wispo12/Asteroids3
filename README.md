Asteroids (Part 3) 
==================
Adding bullets and finishing the game
-------------------------------------
To finish our Asteroids game, we need to write a new class that represents Bullets. We will store the Bullets in an `ArrayList` much like we did with the Asteroids. Once we can shoot the bullets and destroy Asteroids, we will have a working game. Your Asteroids game doesn't have to look like any other. Feel free to modify it in any way you wish.

Suggested steps to completing this assignment
---------------------------------------------

1. Create a new Bullet.pde file in your AsteroidsGame folder. One way to do this is in Sublime is to choose *New | New File* and
then choose *File | Save as* and name your file `Bullet.pde`.
2. On line 14 of `index.html` add `Bullet.pde` to the list of files in the `data-processing-sources` and choose *File | Save*.
2. Write a `Bullet` class that `extends Floater` in `Bullet.pde`. 
2. Write a constructor that takes one ship argument: `Bullet(Spaceship theShip)` This constructor will use the `public` "getter" (accessor) functions of the `Spaceship` class to:
  - Intialize `myCenterX` and `myCenterY` of the bullet to be the same as the ship.
  - Initialize `myPointDirection` of the bullet to be the same as the direction the ship is pointing.
  - convert `myPointDirectio`n to radians with the following code: `double dRadians =myPointDirection*(Math.PI/180);`
  - Initialize `myDirectionX` as `5 * Math.cos(dRadians) +` the directionX of the ship
  - Initialize `myDirectionY` as `5 * Math.sin(dRadians) +` the directionY of the ship
3. Override the `show()` method of the `Floater` class so that you can use circular bullets
4. Now, add just one bullet to your program. First, just draw it to the screen. Make sure you can see it before continuing to the next step.
5. Now, move the bullet.
6. Now create an `ArrayList` of Bullets. The list should be empty to start with. Everytime you press the key to "shoot", add a `new Bullet` to the `ArrayList`. Modify the program with loops that draw and move all the bullets in the ArrayList
7. One way to check for collisions between the bullets and the Asteroids is to write a loop within a loop. 
  - a loop that goes through all the bullets to see if there is a collision between that bullet and the asteroid
  - if there is a collision remove both the asteroid and the bullet from their `ArrayLists` then use `break;` to stop the loop to prevent any index out of bounds execptions.


10. Submit the same URL for your AsteroidsGame that you submitted for the three previous assignments to the school loop drop box.

Extensions
----------
If you have extra time, you might add some extra features to your Asteroids game. Have fun and be creative!
* Randomly shaped Asteroids
* Different types of weapons besides bullets
* Have two Asteroids classes, one large and one small. When a large Asteroid is removed from the ArrayList add two small ones with the same x and y
* Add a second ship (UFO) that appears after a while and shoots at the space ship
* Keep track of the score and/or the health of the ship
* Save the score or health to [save the player's progress](https://github.com/apcslowell/SaveProgress/)
* Andrew Ong put a [video](https://www.youtube.com/watch?v=qiRtD9vJ2K8) up of his Asteroids Game from several years ago which has a number of amazing features.
 
