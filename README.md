# GriefDungeon
This is a small game I made for a project for the Tech Academy. Each Level is meant to represent one of the stages of grief.

<ins>Denial</ins><br>
For this level I wanted to represent Denial by making the player take damage if they look at the statue. To do this I set up a line trace from the first person camera that operated on the event tick. This line trace was activated and deactivated by colliders at the entrance and exit of the room. If the line trace hit the statue it would call the Lose Health function and decrement the health variable that I mapped to a health bar on the screen. If the player health got to zero it would destroy the actor and call the function controlling the death functionality that I will show later.






https://user-images.githubusercontent.com/78393505/155409473-4d38891a-71e1-495c-bb41-23190adff28d.mp4



![DenialBP](https://user-images.githubusercontent.com/78393505/155419426-3bae5e34-88f3-43fa-ad85-dc2e578f763b.png)



https://user-images.githubusercontent.com/78393505/155409005-2b6f4b23-25b5-468d-97ff-01f39c8019c4.mp4








https://user-images.githubusercontent.com/78393505/155412219-29a48d79-e805-45b3-9f67-eb315e8e829f.mp4



https://user-images.githubusercontent.com/78393505/155412924-09e17555-b0f9-48d7-84a7-a702d0526a4e.mp4



https://user-images.githubusercontent.com/78393505/155414812-37982697-ecaf-499e-9f60-0db29d3d863c.mp4

