# GriefDungeon
## This is a small game I made for a project for the Tech Academy. Each Level is meant to represent one of the stages of grief.

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
For the Bargaining level 


https://user-images.githubusercontent.com/78393505/155412219-29a48d79-e805-45b3-9f67-eb315e8e829f.mp4

![Bargaining](https://user-images.githubusercontent.com/78393505/155424723-9c0e3c81-1d3a-4fdf-83fe-dae7bc441eed.png)
![Bargaining2](https://user-images.githubusercontent.com/78393505/155424741-f4592c1f-3fa3-46ec-81ea-6df289057924.png)


https://user-images.githubusercontent.com/78393505/155412924-09e17555-b0f9-48d7-84a7-a702d0526a4e.mp4



https://user-images.githubusercontent.com/78393505/155414812-37982697-ecaf-499e-9f60-0db29d3d863c.mp4

