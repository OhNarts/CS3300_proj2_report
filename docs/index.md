# Project 2 Report

## Introduction/Background 

Dyad is a Unity game designed to challenge and provide entertainment for players, along with providing user-user competition through a global leaderboard. The game is cross-platform and can run on Windows, Mac, and Linux. Project management was done through git with a communication channel on Discord. We focused heavily on testing, both with the Unity Test Framework and play testing all the major functionality of the game.  


## Literature Review 

Dyad is based on a mobile video game called Duet. It has a similar game mechanic of two player-controlled spinning circles, but in Dyad the player controls the location of the circles rather than their rotation. The scoring is also different, scoring based on closely avoiding obstacles compared to surviving for a certain amount of time.

There is a lot of related work on standard ways to develop games using Unity. We adopted best practices such as event handling with the observer pattern to create cleaner, more efficient code.



## Software Technologies

- Unity - Good for Cross-Platform-Compatibility and creating different game stages 
- Google Cloud DataStore - helpful in creating a global leaderboard for players to compete with
- Unity Test Framework - An extention to the Unity editow, allowing unit testing of all components of the game
- Git - standard version control software for developing code as a team



## Project Lifecycle 

We used the waterfall method of developement due to the time constrained nature of the project and we did not anticipate major changes after coming up with the game idea.

### Stages
**Requirements**: we generated a list of requirements based around Minimum Marketable Features such as having a leaderboard

**Design**: We identified the core components of the game (player controller, level generation, shop, UI, leaderboard), and created a rough outline of how those features would be implemented in Unity

**Developement**: We collaborated on features to satisfy the MMF's, following the design plan we created

**Testing**: We used the Unity Test Framework as well as debug play mode to unit test and play test all core game functionality

We tracked features and bugs on a Discord channel created for the project.


## Requirements 
#### Functional requirements:
1. The system has a main screen to navigate to shop, levels, or leaderboard
2. The system has 10 levels the user can play with
3. The system has mouse tracking to drag the circles around each level
4. The system has a global leaderboard where scores are updated as different players achieve them
5. The system has a shop where Users can purchase items
6. The system will automatically apply purchased items to levels 
7. The system will increase money when a level is beaten, and decrease money when an item is purchased

#### Non-Functional Requirements:
1. The game should run at 60 fps on desktop platforms
2. There should not be noticable input lag. The player-controlled object should follow the player's mouse with no delay
   
#### MMFs
1. Leaderboard: The Leaderboard serves as a means to foster competitve spirit and encourage Players to not only beat the levels but to try and challenge themselves further by getting a high score that makes it onto the global leaderboard

2. Levels: there are 10 levels that get increasingly more difficult, in order to challenge the player. Each level has obstacle in them that the player must avoid touching in order to reach the end of the level, or they die.

3. Shop: Users can buy items to help them beat levels, earn more money, and increase their score.  There are three items available in the shop:
    1. reduces the distance between the two circles so it becomes one circle
    2. slows down the rotation of the circles, making it easier to increase your score
    3. doubles the amount of money you receive from a level, so you can buy more items
   
We identified and prioritized requirements based on the user experience and enjoyability of the game.


## Design 
- Present architectural and low-level design diagrams.
- Explain your design decisions and their impact.


## Testing 

- Elaborate on the Test Strategy, including whitebox and blackbox testing methods.
- List various tools used for testing and explain their purpose.
- Provide detailed test cases and their outcomes.
- Discuss how testing influenced the development process and the final product.

#### Whitebox testing
The Unity Test Framework was used to perform whitebox unit testing directly within the Unity editor. We identified potential errors based on the code and attempted to cover as much functionality as possible with the unit tests.

#### Blackbox testing
Blackbox play testing was conducted running the application in Unity in debug mode. This allowed us to test all game functionality as a user would see it. The play testing focused on user experience and ensuring the game mechanics worked smoothly.

#### Test cases

Leaderboard score updates - the leaderboard should add and save the right score associated with the correct level **passed**

Start Screen - the user should see the start screen upon running the game, and be able to select the shop, levels, leaderboard, or quit **passed**

Level Selection - the level selection screen should take the player to the correct level **passed**

Mouse movement - the in-game player should follow the user's mouse **passed**

Obstacle collision detection - the game should end when a player collides with an object **passed**

Shop items - shop items should activate properly after being bought **passed**

Framerate - the game should update at 60FPS, measurable in debug mode **passed**

Scoring - the player's score should increment when successfully dodging an obstacle **passed**

Exit - the quit buttons should safely quit the game **failed - the quit button in certain levels does not work**

Testing allowed us to catch bugs and ensure the MMF's worked correctly. Play testing also lead to design improvements, such as increasing the width between the two player controlled circles to improve the game's playability. 





