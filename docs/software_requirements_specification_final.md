# Overview
The purposes of this document is to communicate a plan for the development for a turn based dungeon crawler game. In this document you will see all the functional and nonfunctional requirmeents collated and described for the necessary qualities and features of the game. In addition to the requirements, all the artifacts that model how the user interacts with the system and use case descriptions have been included in this document.
# Software Requirements
This section lays out all the functional and non-functional requirements of the game in a table. Each requirement also has a unique ID and test case that is linked to it.
## Functional Requirements
### Interactive Map
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| FR1 | The player shall be able to progress to different areas of the map. | IT1, IT5, ST1 |
| FR2 | Each area shall have a tavern. | TC2 |
| FR3 | The map shall get updated after certain events are completed. | TC1,TC2, IT5, ST5 |
| FR4 | Enemy encounters shall be turned off when defeating the final floor boss, and turned on when entering a new floor. | TC1,TC2 |
| FR5 | Certain areas shall be blocked off until certain items are obtained. | TC1,TC2, IT4, ST4 |

### Combat
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| FR6 | There shall be multiple enemies to fight. | TC1, ST1 |
| FR7 | Each encounter with an enemy shall be random. | ... |
| FR8 | There shall be multiple methods of attacking enemies. | UT7, UT8, ST3 |
| FR9 | Each area shall have a final boss fight. | TC1,TC2, ST1 |
| FR10 | Special enemies shall not include the option to escape. | TC1,TC2, ST3 |

### NPCs
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| FR11 | The player shall have the ability to recruit certain NPC’s into their party. | UT5, UT6, IT3, ST2, ST5 |
| FR12 | Recruitable NPCs shall have a requirement that must be met before they join the user’s party. | IT3, IT4, ST2, ST5 |
| FR13 | Recruitable NPC’s shall have the ability to assist in combat. | TC1,TC2, ST2, ST3 |
| FR14 | Events shall be triggered when their requirements have been met. | TC1,TC2, ST1, ST4, ST5 |
| FR15 | Non-recruitable NPC's shall offer items and quests to the user. | UT6, ST5 |

## Non-Functional Requirements
### Map aesthetics
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| NFR1 | Each map shall have different areas. | TC4 |
| NFR2 | Each area shall have a tavern. | ... |
| NFR3 | Each area shall have a unique theme. | IT5 |
| NFR4 | Every character shall have a unique look. | TC6 |
| NFR5 | Enemies shall have a theme matching the theme of the floor they are on. | TC6 |
### UI
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| NFR6 | The UI shall be simple to navigate. | TC4, UT4 |
| NFR7 | The UI shall be consistent throughout the game. | IT5 |
| NFR8 | The UI shall display the name of the character who is speaking. | TC6, ST5 |
| NFR9 | The UI shall include a picture of the character who is speaking. | TC6, ST5 |
| NFR10 | The UI shall display the items in the user's inventory and the quantity of said items. | IT2, ST3 |
### Performance
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| NFR11 | The game shall not experience large interruptions to gameplay. | UT1, IT5 |
| NFR12 | The player shall have the option to save their progress. | UT9, UT10 |
| NFR13 | The game shall maintain a stable framerate. | TC6 |
| NFR14 | The game responds to input without noticeable lag. | UT2, UT3, UT4 |
| NFR15 | There shall be 20 save files available to save and load games. | UT9, UT10 |

# Test Specification
Tests done to ensure functions in the game are working properly, and seek out possible bugs to be fixed.
## Unit tests
| ID | Description | Steps | Input Values | Expected Output | Actual Output | Pass/Fail | Requirement Link |
| :-------------: | :----------: | :----------: | :----------: | :----------: | :----------: | :----------: | :----------: |
| UT1 | Game Creates Self on Startup | 1.Run Game 2.Navigate menu to New Game 3.Select New Game| Mouse click/Keyboard input to select menu options | Successful game start with player starting in first floor | As expected | Pass | NFR11 |
| UT2 | Testing basic movement with keyboard input | 1.Run Game 2.Start New Game file 3.Key Input | Four arrow keys on keyboard  | User should move north, south, east, and west when holding/pressing "Up","Down","Right","Left" respectively | As expected | Pass | NFR14 |
| UT3 | Testing basic movement with mouse input | 1.Run Game 2.Start New Game file 3.Mouse Input | Mouse left click on map tile  | User should move to location that was selected by mouse input if location is available | As expected | Pass | NFR14 |
| UT4 | In-Game Menu Navigation | 1.Run Game 2.Start New Game file 3.Press ESC 4.Key Input | Mouse left click on options/Keyboard arrow keys and spacebar for select | User should be able to interact with menu options through use of the keyboard/mouse | As expected | Pass | NFR6,NFR14 |
| UT5 | Chest Interaction | 1.Run Game 2.Start New Game file 3.Travel to chest at bottom left of first floor area 4.Key Input| Mouse left click or spacebar when facing chest | User should be able to interact with chests | As expected | Pass | FR11 |
| UT6 | NPC Interaction | 1.Run Game 2.Start New Game file 3.Travel upwards to first NPC 4.Key Input | Mouse left click or spacebar when facing chest | User should be able to interact with NPC | As expected | Pass | FR11,FR15 |
| UT7 | Combat Win | 1.Run Game 2.Start New Game file 3.Travel until a random fight encounter occurs 4.Continue using base attack until enemy is defeated | Spacebar input or mouse left click on Attack menu item | User should be able to continue progressing through their current floor | As expected | Pass | FR8 |
| UT8 | Combat Loss | 1.Run Game 2.Start New Game file 3.Travel until a random fight encounter occurs 4.Continue using guard until user is defeated | Spacebar input or mouse left click on Guard menu item | User should be returned to the main menu | As expected | Pass | FR8 |
| UT9 | Save file | 1.Run Game 2.Start New Game file 3.Press ESC 4.Navigate to Save and select a file | Spacebar input or mouse left click in in-game menus | User should be returned to in-game menu and when Save is selected, a game file should appear  | As expected | Pass | NFR12,NFR15 |
| UT10 | Load file | 1.Run Game 2.Navigate and select Continue in Main Menu 3.Select saved game file | Spacebar input or mouse left click in in-game menus | User should appear in previously explored floor when save file occurred | As expected | Pass | NFR12,NFR15 |
## Integration tests
| ID | Description | Steps | Input Values | Expected Output | Actual Output | Pass/Fail | Requirement Link |
| :-------------: | :----------: | :----------: | :----------: | :----------: | :----------: | :----------: | :----------: |
| IT1 | Game spawns user at beginnig of floor after finishing previous one. | 1. Defeat Final Boss. 2. Walk through "passage" to the next floor. | Mouse input to attack final boss and keyboard input to walk through the "passage" | The user spawns at the beginning of the next level | As Expected | Pass | FR1 |
| IT2 | Shop Transactions | 1.Talk to merchant NPC 2. Select and item to purchase  | Mouse left click on NPC and item | User should have item in inventory and lose the correct ammount of gold | As expected | Pass | NFR10 |
| IT3 | NPC joins user's party after completing their required task. | 1. The user must ask the NPC to join their party. 2. The user must accomplish whatever task is asked of them to recruit them. 3. The user must talk to the NPC after finishing the task to finally recruit them.| Mouse and keyboard inputs to talk to NPCs and accomplish their tasks. | The NPC accepts their request and starts following the user | As Expected | Pass | FR11, FR12 |
| IT4 | Key/Quest Items | 1.Aquire Key item 2. Use key item in applicable area | Mouse click on event that uses key item | Event should respond to if player has Key/Quest item in inventory | As expected | Pass | FR5,FR12 |
| IT5 | Seamless music continuation between areas that use same track | 1. Enter area, track starts 2. Enter connected area that uses same track 3. Repeat step 2 | Mouse or keyboard input on area transition tiles | Track should continue seamlessly or stop in an area of different track | As expected | Pass | FR1,FR3,NFR11,NFR7,NFR3 |
## System tests
| ID | Description | Steps | Input Values | Expected Output | Actual Output | Pass/Fail | Requirement Link |
| :-------------: | :----------: | :----------: | :----------: | :----------: | :----------: | :----------: | :----------: |
| ST1 | Game Completion | 1. Defeat F1 boss 2. Defeat F2 boss 3. Defeat F3 boss 4. Defeat F4 boss | Mouse or keyboard to navigate floors, mouse or keyboard to send commands in battle | Win Screen | | | FR1, FR6, FR9, FR14 |
| ST2 | Party System | 1.Switch order of party members. 2. Equip an item. 3. Unequip an item. 4. Use skills to affect party outside of battle. 5. Add a new party member. | Mouse click on party interface | The in game party system should all be functioning correctly and be able to do all the steps mentioned | As expected | Pass | FR11,FR12,FR13 |
| ST3 | Combat System | 1.Enter combat 2. Attack and use skills 3. Damage enemies 4. Use items. 5. Take damage from enemy attacks and skills 6. Get affected by something that alters state 7. Leave combat. | Arrow keys or mouse clicks on combat UI  | The in game combat system should all be functioning correctly and be able to do all the steps mentioned | As expected | Pass | FR8,FR10,FR13,NFR10 |
| ST4 | Special Items | 1. Complete the challenge to acquire a special item 2. Go to location item is to be used 3. Use item | Keyboard or mouse commands | Successfull unlocking of game feature | As expected | Pass | FR5, FR 14 |
| ST5 | NPC Dialogue System | 1.Talk to a NPC 2. Choose from an option 3. Buy an item 4. Update the dialogue tree 5. Update the NPC event so the NPC is no longer a visible on-map event | Mouse click on dialogue interface| The in game NPC dailogue system should all be functioning correctly and be able to do all the steps mentioned | As expected | Pass | FR3,FR11,FR12,FR14,FR15,NFR8,NFR9 |
# Software Artifacts
* [Combat System Diagram](https://github.com/ConnorWeb/GVSU-CIS350-FantasyGame/blob/master/artifacts/use_case_diagrams/Combat%20System.pdf)
* [Map Diagram](https://github.com/ConnorWeb/GVSU-CIS350-FantasyGame/blob/master/artifacts/use_case_diagrams/MapUML.pdf)
* [Use Case Diagram](https://github.com/ConnorWeb/GVSU-CIS350-FantasyGame/blob/master/artifacts/use_case_diagrams/NPC%20System.pdf)
* [ NPC Use Case Description](https://github.com/ConnorWeb/GVSU-CIS350-FantasyGame/blob/master/artifacts/use_case_diagrams/NPC%20System%20Use%20Case%20Description.pdf)
* [Burndown Chart](https://github.com/ConnorWeb/GVSU-CIS350-FantasyGame/blob/master/docs/Burn_Down_Chart.pdf)
* [Midterm Presentation](https://github.com/ConnorWeb/GVSU-CIS350-FantasyGame/blob/master/docs/Midterm%20Presentation.pdf)
* [Final Presentation](https://github.com/ConnorWeb/GVSU-CIS350-FantasyGame/blob/master/docs/Final%20Presentation.pdf)