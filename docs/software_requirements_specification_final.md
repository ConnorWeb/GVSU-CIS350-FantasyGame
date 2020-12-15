# Overview
The purposes of this document is to communicate a plan for the development for a turn based dungeon crawler game. In this document you will see all the functional and nonfunctional requirmeents collated and described for the necessary qualities and features of the game. In addition to the requirements, all the artifacts that model how the user interacts with the system and use case descriptions have been included in this document.
# Software Requirements
This section lays out all the functional and non-functional requirements of the game in a table. Each requirement also has a unique ID and test case that is linked to it.
## Functional Requirements
### Interactive Map
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| FR1 | The player shall be able to progress to different areas of the map. | TC1 |
| FR2 | Each area shall have a tavern. | TC2 |
| FR3 | The map shall get updated after certain events are completed. | TC1,TC2 |
| FR4 | Enemy encounters shall be turned off when defeating the final floor boss, and turned on when entering a new floor. | TC1,TC2 |
| FR5 | Certain areas shall be blocked off until certain items are obtained. | TC1,TC2 |

### Combat
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| FR6 | There shall be multiple enemies to fight. | TC1 |
| FR7 | Each encounter with an enemy shall be random. | TBD |
| FR8 | There shall be multiple methods of attacking enemies. | TC1,TC2 |
| FR9 | Each area shall have a final boss fight. | TC1,TC2 |
| FR10 | Special enemies shall not include the option to escape. | TC1,TC2 |

### NPCs
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| FR11 | The player shall have the ability to recruit certain NPC’s into their party. | TC1 |
| FR12 | Recruitable NPCs shall have a requirement that must be met before they join the user’s party. | TBD |
| FR13 | Recruitable NPC’s shall have the ability to assist in combat. | TC1,TC2 |
| FR14 | Events shall be triggered when an NPC's requirements have been met. | TC1,TC2 |
| FR15 | Non-recruitable NPC's shall offer items and quests to the user. | TC1,TC2 |

## Non-Functional Requirements
### Map aesthetics
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| NFR1 | Each map shall have different areas. | TC4 |
| NFR2 | Each area shall have a tavern. | TBD |
| NFR3 | Each area shall have a unique theme. | TC6 |
| NFR4 | Every character shall have a unique look. | TC6 |
| NFR5 | Enemies shall have a theme matching the theme of the floor they are on. | TC6 |
### UI
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| NFR6 | The UI shall be simple to navigate. | TC4 |
| NFR7 | The UI shall be consistent throughout the game. | TBD |
| NFR8 | The UI shall display the name of the character who is speaking. | TC6 |
| NFR9 | The UI shall include a picture of the character who is speaking. | TC6 |
| NFR10 | The UI shall display the items in the user's inventory and the quantity of said items. | TC6 |
### Performance
| ID | Requirement | Test Cases |
| :-------------: | :----------: | :----------: |
| NFR11 | The game shall not experience large interruptions to gameplay. | TC4 |
| NFR12 | The player shall have the option to save their progress. | TBD |
| NFR13 | The game shall maintain a stable framerate. | TC6 |
| NFR14 | The game responds to input without noticeable lag. | TC6 |
| NFR15 | There shall be 20 save files available to save and load games. | TC6 |

# Test Specification
Description of what this section is
## Unit tests
| ID | Description | Steps | Input Values | Expected Output | Actual Output | Pass/Fail | Requirement Link |
| :-------------: | :----------: | :----------: | :----------: | :----------: | :----------: | :----------: | :----------: |
| UT1 | Game Creates Self on Startup | 1.Run Game 2.Navigate menu to New Game 3.Select New Game| Mouse click/Keyboard input to select menu options | Successful game start with player starting in first floor | As expected | Pass | Placeholder |
| UT2 | Testing basic movement with keyboard input | 1. Start | Four arrow keys on keyboard  | User should move north, south, east, and west when holding/pressing "Up","Down","Right","Left" respectively | As expected | Pass | Placeholder |
| UT3 | Testing basic movement with mouse input |  | Mouse left click on map tile  | User should move to location that was selected by mouse input if location is available | As expected | Pass | Placeholder |
| UT4 | Menu Navigation |  |  | User should be able to interact with menu options through use of the keyboard/mouse | As expected | Pass | Placeholder |
| UT5 | Chest Interaction |  |  | User should be able to interact with  | As expected | Pass | Placeholder |
| UT6 | NPC Interaction |  |  | User should be able to interact with NPC | As expected | Pass | Placeholder |
| UT7 | Combat Win |  |  | User should be able to continue progressing through their current floor | As expected | Pass | Placeholder |
| UT8 | Combat Loss |   | 1.  | User should be returned to the main menu | As expected | Pass | Placeholder |
## Integration tests
(copy/paste the above table a minimum of 5 times)
## System tests
(copy/paste the above table a minimum of 5 times)
# Software Artifacts
<Describe the purpose of this section>
* [I am a link](to_some_file.pdf)