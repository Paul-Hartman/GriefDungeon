# GriefDungeon
### This is a small game I made for a project for the Tech Academy. Each Level is meant to represent one of the stages of grief.

<ins>Denial</ins><br>
For this level I wanted to represent Denial by making the player take damage if they look at the statue. To do this I set up a line trace from the first person camera that operated on the event tick. This line trace was activated and deactivated by colliders at the entrance and exit of the room. If the line trace hit the statue it would call the Lose Health function and decrement the health variable that I mapped to a health bar on the screen. If the player health got to zero it would destroy the actor and call the function controlling the death functionality that I will show later.






https://user-images.githubusercontent.com/78393505/155409473-4d38891a-71e1-495c-bb41-23190adff28d.mp4



![DenialBP](https://user-images.githubusercontent.com/78393505/155419426-3bae5e34-88f3-43fa-ad85-dc2e578f763b.png)

<ins>Anger</ins><br>
For the Anger level you have to break all of the pots to open the door to the next level. I did this by converting all of the static meshes for the pots into destructable meshes and adding different Random seeds and cell counts for all of them. I then converted those to blueprints with on component hit events that incremented a counter in the first person charachter blueprint. Once all 30 of the pots had been smashed entering the collider in front of the door would open it as well as turn off the raycast from the last level.


https://user-images.githubusercontent.com/78393505/155409005-2b6f4b23-25b5-468d-97ff-01f39c8019c4.mp4

![AngerBP1](https://user-images.githubusercontent.com/78393505/155421803-3bbb3f70-4e4b-45d8-9abe-8fc54b1aabd0.png)




![AngerBP2](https://user-images.githubusercontent.com/78393505/155421814-d0906783-50c0-4e2c-be57-babbbf778150.png)


<ins>Bargaining</ins><br>
For the Bargaining level you need to trade some coins for a peice of treasure to unlock the doors. The doors are supposed to be a Mortons Fork meaning something that looks like a choice but isnt because both doors go to the same room full of lasers. For the skeletons I made a collider under the chained skeleton that casts to the coin blueprint and increments a counter that once it reaches 4 makes the treasure detach from actor and simulate physics so you can bring it over to the other skeleton which it attaches to and switches a boolean letting the doors open. In the laser room I made a blueprint for a particle effect that turns on and off and sets a collider that does damage to the player on and off based on the particle effect. I set the different laser blueprints delay intervals to multiples of 2 so they would alternate and sometimes all turn on at once. If the player loses to much health the first person charachter is destroyed and it sets off the OnPlayerDeath function in the first person game mode. This function puts up a death widget then respawns the charachter at the last checkpoint they crossed and then possesses the pawn.


https://user-images.githubusercontent.com/78393505/155412219-29a48d79-e805-45b3-9f67-eb315e8e829f.mp4
![LaserBP](https://user-images.githubusercontent.com/78393505/155426221-907ab49c-cfaa-4a3d-a2c6-2ed0fe9c4e05.png)



![DeathBP](https://user-images.githubusercontent.com/78393505/155426230-242cc8bb-5e1b-4e65-bbed-b7d71789703d.png)

<ins>Depression</ins><br>
For the Depression level the charachter is slowed over time to a crawl and they need to make a leap of faith to break out of it. I did this by making a collider in the doorway that activates the slow funciton. This decreases the players energy on the event tick with .3 second delays, the level of energy is then used to set the players movement speed decreaseing until it reaches 10. Jumping down the tube resets these variables.
https://user-images.githubusercontent.com/78393505/155412924-09e17555-b0f9-48d7-84a7-a702d0526a4e.mp4

![DepressionBP](https://user-images.githubusercontent.com/78393505/155427667-395eee21-5d3b-458b-872a-20df3dcc257b.png)


https://user-images.githubusercontent.com/78393505/155414812-37982697-ecaf-499e-9f60-0db29d3d863c.mp4

![FanBP](https://user-images.githubusercontent.com/78393505/155430385-00eae8fb-ea35-4bab-9007-7bbb46ed7571.png)


![AcceptanceBP](https://user-images.githubusercontent.com/78393505/155430371-aaf33aff-0f98-466e-b3a6-6af0df0be366.png)
