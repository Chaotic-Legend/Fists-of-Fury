[![Static Badge](https://img.shields.io/badge/Godot%20Engine-4.3-blue?style=plastic&logo=godotengine)](https://godotengine.org/) ![GitHub top language](https://img.shields.io/github/languages/top/Chaotic-Legend/2D-Movement-Tutorial?logo=godotengine)

# Fists of Fury | Project Touchstone #
[Tutorial: Create a Beat'em Up game in Godot!](https://youtube.com/playlist?list=PLNNbuBNHHbNGtZjygmnJ2fBvp6JmDNkAm&si=qjgzBgI2tMU1-evd) by [The GameDev Tavern](https://gadgaming.itch.io/) ([YouTube](https://www.youtube.com/@GameDevTavern))

This multipart tutorial is a structured, follow-along project that guides viewers through building a 2D player controller and core combat system, demonstrating how movement, input handling, attack mechanics, enemy interactions, and animations are organized and implemented in the Godot Engine to create a functional "beat 'em up" game experience. It also served as the foundation for completing a structured implementation task on Feather, with the project integrated into the broader development workflow supporting the Handshake AI Project Touchstone initiative.

# Assets #
[BeatEmUp Assets](https://drive.google.com/file/d/1_9-KLpjMYAJK3ND6mXnnAFaaJ586n939/view?usp=sharing) by [The GameDev Tavern](https://nicolasbize.com/blog/) ([GitHub](https://github.com/nicolasbize))

![Sprite Asset](assets/art/characters/player.png)

# Create a Godot task #
<ins> What application is this task for? </ins>
<br>
Godot

### **Task prompt** ###
First, enter the **task prompt** and any relevant reference files (e.g., docs, diagrams, sketches, photos, schematics).

Tasks should sound like what a manager might give a skilled but junior employee: high-level guidance with some leeway on executional details, but with very clear success metrics. What a good outcome looks like must be very clear and easy to understand.

Include any relevant **reference files** (docs, diagrams, sketches, photos, schematics, etc) needed for someone to complete this task.

Reminder on the difference between reference and starting state files:
- **Reference files**: anything the Employee should look at or read while completing the project that does not need to be directly loaded into the application (*'please make something that looks like XYZ image'*)
- **Starting state files (upload below)**: anything that the Employee would need to load into their workspace to complete the task (*'here is the existing file you should adapt'*)

<ins> Task prompt (ask the Employee) </ins>
<br>
We are beginning development for the player controller of a new 2D pixel-art "beat 'em up" game prototype. Your task is to design and implement a functional player movement and combat system using a pixelated character sprite, establishing the core mechanics and a responsive gameplay foundation. The system should prioritize smooth, precise, and consistent control by incorporating well-structured keyboard input handling, responsive combat interactions, and a side-scrolling camera system. All visual assets, including the player sprite, enemies, destructible objects, and environment props, should render sharply and clearly without distortion, preserving the visual clarity expected in a pixel-art environment. You will set up the necessary nodes, apply the character sprite, and configure collision and physics properties to ensure proper interaction with the environment and enemies. The player character must respond to keyboard inputs for directional movement, jumping, and attacking, and demonstrate responsive behavior throughout gameplay. The player character should remain visible and correctly oriented in the camera view at all times to maintain a consistent on-screen experience. The player character should be able to interact with destructible objects, such as barrels, and engage enemies in combat through attacks that deal damage and trigger visible reactions. The completed movement system should support the following abilities:

- The arrow keys allow the player character to move in all directions.
- The X key allows the player character to jump upward.
- The C key allows the player character to attack enemies.
- A jump kick allows the player character to attack while airborne.
- Destructible objects can be damaged and broken through attacks.
- Enemies approach the player character to attack and deal damage.
- Enemies react to damage with hurt and knockdown responses.

Vertical motion should behave consistently, with gravity producing a natural downward pull. Interactions with the environment must be stable and precise, allowing the character to move seamlessly across surfaces, respond accurately to barriers, and maintain proper positioning without unintended overlap or clipping. The street environment should include walkable ground areas and obstacles, along with destructible objects such as barrels placed within the level. There is no strict layout requirement, but the level should provide enough space and structure to support combat encounters and movement testing. The camera should follow the player character while preventing backtracking into areas that are no longer visible, maintaining forward progression through the level. The player character must always face the correct direction when moving or attacking, with smooth and uninterrupted animations that clearly convey impact through visual feedback and enemy reactions. The enemies actively target the player character and approach the player until they are within proximity, aligning themselves into a clear interaction position. Overall behavior should demonstrate tight responsiveness, smooth transitions between movement and combat, and a level of polish that supports further development of the "beat 'em up" gameplay system.

<ins> Which of the following best fits this task? </ins>
<br>
Task from scratch

<ins> How long would you anticipate an 'Employee' to complete this task? (in hours) </ins>
<br>
4

### **Starting state** ###
Please describe and include below any information about the starting state of this project:
- Existing work to be modified
- Other assets or other inputs the Employee needs to bring to be able to complete this task

Reminder on the difference between the starting state and the reference files:
- **Starting state files**: anything that the Employee would need to load into their workspace to complete the task ('*here is the existing file you should adapt*')
- **Reference files (upload above)**: anything the Employee should look at or read while completing the project that does not need to be directly loaded into the application ('*please make something that looks like XYZ image*')

<ins> Starting state description </ins>
<br>
The starting state for this task consists of a newly created 2D Godot project that provides the essential assets and minimal setup required to begin development of this pixel-art "beat 'em up" game. The project includes imported sprite sheets for the player character, enemies, and destructible objects such as barrels to support animations for movement, combat, damage, and destruction. It also contains environment sprites and decorative props to build a side-scrolling level suitable for combat encounters and gameplay testing. The Employee is responsible for creating the level layout using the provided assets, setting up the player and enemy scenes with appropriate nodes and collision shapes, and organizing the project structure with folders for assets, scenes, scripts, and resources. The Employee must implement the player controller, animations, camera behavior, attack systems, enemy behavior, and object interactions. This task includes defining input actions, attaching scripts, configuring movement and combat logic, and ensuring proper interaction between the player, enemies, and environment. The reference materials show how to use the provided assets to build a cohesive level that supports forward progression, more combat encounters, and overall gameplay.

### **Overall context** ###
Finally, include context on this task and why it is realistic and representative of real-life work:
- Why is this a reasonable task for a manager to ask a junior-level employee to do?
- Is there a larger project it might be a part of?

<ins> Task context </ins>
<br>
This task is a realistic and representative assignment for a junior-level developer, as it focuses on implementing core movement and combat mechanics within a structured, well-defined environment using provided assets. It requires applying foundational programming, problem-solving, and design skills to translate clear gameplay requirements into functional systems, such as player control, enemy behavior, destructible objects, collision handling, and camera tracking. These are common duties in game development, with clear success criteria tied to responsiveness, visual feedback, and system interaction. The task also reflects real-world workflows, where developers build upon an existing project setup, organize assets and scenes, and implement features in a modular and extensible way. It emphasizes integrating multiple systems into a cohesive gameplay experience typical of early-stage feature development and can be further expanded and refined in its current state. The implemented mechanics can later support expanded features such as additional enemy types, combo systems, level progression, UI elements, sound design, and more advanced gameplay interactions. Completing this task ensures the core gameplay loop is functional and reliable, marking a significant milestone for further iteration and development.

<ins> Rubric Items </ins>
<br>
1. The characters, level background, and level props all appear sharp.
- Run the main scene and observe that all character sprites, level background, and environment props appear sharp and clear.
- The task prompt requires that all character sprites, level background, and level props remain visually sharp and clear.

2. The animations play smoothly and always face the correct direction.
- Run the main scene and move the player character to observe smooth animation transitions and the correct facing direction.
- The prompt requires that all character sprite animations play smoothly while facing the correct direction of movement.

3. The gravity physics produces a natural and consistent downward pull.
- Run the main scene and observe the player character falling to confirm that gravity causes a natural downward acceleration.
- The prompt requires that the environment's gravity produce realistic falling behavior and a consistent downward pull for entities.

4. The sprites properly collide with the environment, objects, and walls.
- Run the main scene and move the player character across the level to confirm it collides with all level and environmental objects.
- The task prompt requires functional collision bodies for the player character to interact correctly with all level environment elements.

5. The camera follows the player character and prevents backtracking.
- Run the scene and move through the level to confirm the camera follows the player and prevents backtracking into unseen areas.
- The task prompt requires the camera to maintain player tracking while blocking access to previously passed sections.

6. The sprite moves with the arrow keys and stops when input is released.
- Run the scene, use the arrow keys to move the player character in all directions, and then release to confirm it stops immediately.
- The prompt requires the arrow keys for full directional movement, and the player character must stop when releasing input.

7. The player character can jump upward when pressing the X key.
- Run the main scene, and then press the X key to observe the player character jump upward in the level.
- The task prompt requires that pressing the X key triggers the player character to perform an upward jump.

8. The player character can punch to attack when pressing the C key.
- Run the main scene, and then press the C key to observe the player character perform a punch attack.
- The task prompt requires the player character to execute a quick punch attack when pressing the C key.

9. A barrel takes damage and breaks when the player character attacks it.
- Run the main scene, position the player character next to the barrel, and attack it with either a punch or a jump kick to destroy it.
- The task prompt requires the barrel to take damage and break when the player character punches or jump kicks it.

10. The sprite performs a jump kick when attacking midair during a jump.
- Run the main scene, press the X key to jump upward, then press the C key while airborne to execute a jump-kick attack.
- The task prompt requires a distinct midair attack animation when the attack input is triggered while the player character is jumping.

11. Enemies approach the player character to position themselves nearby.
- Run the main scene and observe the enemies to confirm they actively approach and align themselves next to the player character.
- The task prompt requires enemy behavior that targets the player character and moves into proximity to position itself for interaction.

12. The player character can attack enemies to hurt and knock them back.
- Run the main scene, attack an enemy, and observe that the enemy takes damage, shows a hurt response, and gets knocked down.
- The prompt requires enemy reactions to player attacks, including damage handling, visual feedback, and knockdown behavior.
<br>
Godot - https://feather.openai.com/tasks/8e817669-0fe2-483f-90da-e5461d5b9717/stage/prompt_creation - Finished prompt creation.

# Create a Godot task #
<ins> What application is this task for? </ins>
<br>
Godot

### **Task prompt** ###
First, enter the **task prompt** and any relevant reference files (e.g., docs, diagrams, sketches, photos, schematics).

Tasks should sound like what a manager might give a skilled but junior employee: high-level guidance with some leeway on executional details, but with very clear success metrics. What a good outcome looks like must be very clear and easy to understand.

Include any relevant **reference files** (docs, diagrams, sketches, photos, schematics, etc) needed for someone to complete this task.

Reminder on the difference between reference and starting state files:
- **Reference files**: anything the Employee should look at or read while completing the project that does not need to be directly loaded into the application (*'please make something that looks like XYZ image'*)
- **Starting state files (upload below)**: anything that the Employee would need to load into their workspace to complete the task (*'here is the existing file you should adapt'*)

<ins> Task prompt (ask the Employee) </ins>
<br>
We are developing a combat update for our 2D pixel-art "beat 'em up" game prototype, focusing on extending the core gameplay systems with advanced enemy behavior, weapon interactions, and combo-driven combat mechanics. Your task is to implement and refine gameplay features that build upon the existing movement and combat framework, ensuring that all systems remain responsive, visually clear, and consistent within a side-scrolling environment. The implementation should prioritize precise input handling, reliable combat interactions, more detectable collision bodies, and stable physics-based responses. The player and enemy systems should interact seamlessly with weapons, environmental boundaries, and collision systems while maintaining consistent performance and readability during combat. Enemy behavior must demonstrate both offensive and defensive behaviors, while the player character must be able to engage in varied attack patterns, weapon usage, and movement-based combat actions. All interactions must produce clear visual feedback, including knockback, collision responses, and state changes such as defeat or item loss. The updated system should support the following capabilities:

- Enemy characters can execute punch attacks that deal damage.
- The player character can damage enemies until they are defeated.
- The player can execute various attacks when repeatedly attacking.
- The player can launch enemies after completing an attack combo.
- Enemies collide with walls by bouncing back after being launched.
- Throwable knife items are placed throughout the level to utilize.
- The characters can pick up a knife and perform a knife attack.
- The player character can hold onto the knife during a jump kick.
- The characters can lose or drop the knife after taking damage.
- A new goon enemy sprite can move away from the player character.

Movement and physics behavior must remain consistent, with gravity producing natural downward motion and collisions behaving predictably against level geometry. The side-scrolling environment should include navigable ground areas, obstacles, and space for combat encounters that support both close-range and ranged interactions. The camera system must maintain player focus while ensuring stable framing of combat scenarios and preventing disorientation during knockback sequences. The player character must remain correctly oriented during movement and attacks, with readable animations that clearly show each behavior. Enemy behaviors should be distinguishable and responsive, supporting both aggressive pursuit and evasive movement patterns depending on state. Overall, the updated system should demonstrate tight responsiveness, cohesive combat logic, and extensibility for future enhancements to this ongoing "beat 'em up" game.

<ins> Which of the following best fits this task? </ins>
<br>
Part of a chained series of tasks that build up to one very large project

<ins> If part of a series of tasks, what other task IDs are in this series? </ins>
<br>
8e817669-0fe2-483f-90da-e5461d5b9717

<ins> How long would you anticipate an 'Employee' to complete this task? (in hours) </ins>
<br>
3

### **Starting state** ###
Please describe and include below any information about the starting state of this project:
- Existing work to be modified
- Other assets or other inputs the Employee needs to bring to be able to complete this task

Reminder on the difference between the starting state and the reference files:
- **Starting state files**: anything that the Employee would need to load into their workspace to complete the task ('*here is the existing file you should adapt*')
- **Reference files (upload above)**: anything the Employee should look at or read while completing the project that does not need to be directly loaded into the application ('*please make something that looks like XYZ image*')

<ins> Starting state description </ins>
<br>
The starting state file for this task consists of a partially developed 2D Godot project that provides a foundational framework for a "beat 'em up" gameplay system for the Employee to import. The project includes preconfigured player and enemy scenes with assigned sprite assets, collision bodies, basic animation setups, and a main scene with an initial background layout. It also contains destructible object assets, such as barrels, along with organized folders for scripts, scenes, and visual resources, and predefined input mappings for player controls. The Employee is responsible for extending the existing scenes by refining player movement, implementing new combat mechanics, and improving interactions between the player, enemies, and destructible objects. This project includes working from the starting state files derived from the prior task for initial development, updating scripts, adding new collision bodies, and enhancing animation transitions to ensure smooth gameplay. The Employee must also integrate the weapon assets to support expanded combat mechanics in the "beat 'em up" game, expand the level layout using the provided environment assets, and ensure all gameplay systems function cohesively within the current project structure.

### **Overall context** ###
Finally, include context on this task and why it is realistic and representative of real-life work:
- Why is this a reasonable task for a manager to ask a junior-level employee to do?
- Is there a larger project it might be a part of?

<ins> Task context </ins>
<br>
This task directly continues from the previous assignment, extending the existing foundation of the "beat 'em up" project to develop and enhance the core gameplay systems. It reflects a realistic junior-level development responsibility, focusing on implementing movement and combat mechanics within a structured environment using provided assets and an established project framework. It requires applying foundational programming, problem-solving, and design skills to extend previously implemented systems into more complete gameplay features, such as enemy behavior, destructible objects, new weapons, and new attacks. This task also reflects real-world workflows, where developers iteratively build on earlier work, organize and expand existing assets and scenes, and implement features in a modular and extensible way. It emphasizes integrating multiple systems into a cohesive gameplay experience typical of early-stage feature development while ensuring compatibility with prior implementations. The implemented mechanics can later support expanded features such as additional enemy types, combo systems, level progression, UI elements, sound design, and more advanced gameplay interactions. Completing this continuation ensures the core gameplay loop becomes more robust and reliable, marking a significant milestone for further iteration and development.

<ins> Rubric Items </ins>
<br>
1. Enemy characters can execute punch attacks that damage the player.
- Run the main scene and observe enemy characters initiating attack animations when close to the player character to deal damage.
- The task prompt requires enemy characters to perform punch-based attacks that successfully register damage against the player.

2. The player character can damage enemies until they are defeated.
- Run the main scene and repeatedly attack enemies to confirm that they take damage, get knocked down, and slowly disappear.
- The task prompt requires the player character to execute attacks that reduce enemy health, resulting in knockback and elimination.

3. The player can execute various attacks when repeatedly attacking.
- Run the main scene, then press the C key repeatedly in sequence to trigger and observe a chained attack for expanded combat.
- The task prompt requires a combo-based input system for chaining multiple attacks when repeatedly pressing the attack input.

4. The player can launch enemies after completing an attack combo.
- Run the main scene, perform a full attack combo on an enemy, and observe the enemy getting launched in a directional force.
- The task prompt requires combo completion to trigger a knockback effect that propels enemies into environmental boundaries.

5. Enemies react to wall collisions by bouncing back after being launched.
- Run the main scene, launch enemies into walls, and observe collision response with a bounce or rebound effect upon impact.
- The task prompt requires physical interaction between launched enemies and wall collision surfaces with visible reaction behavior.

6. Throwable knife items are placed throughout the level to interact with.
- Run the main scene and locate knife objects within the environment to confirm they are present, clearly visible, and interactable.
- The task prompt requires throwable knife assets that are fully integrated into the combat system for the characters to use.

7. The player and enemies can pick up a knife and perform a knife attack.
- Run the main scene, pick up a knife with the C key, then press the C key again to confirm the player character performs a knife attack.
- The task prompt requires implementing knife pickup functionality, allowing characters to equip a knife and perform weapon attacks.

8. The player character holds the knife while executing a jump kick attack.
- Run the main scene, pick up a knife, then perform a jump kick to verify that the player character holds the weapon during the action.
- The task prompt requires weapon persistence during airborne attack states without losing the equipped weapon during gameplay.

9. The player character and enemies lose the knife when taking damage.
- Run the main scene, equip a knife to a character, then allow the character to take damage and observe the knife getting removed.
- The task prompt requires implementing weapon loss behavior, causing characters to lose a knife when taking damage.

10. A new goon enemy sprite can move away from the player character.
- Run the main scene and observe that the new enemy type is actively moving a distance away from the player character.
- The task prompt requires a distinct enemy behavior pattern that includes moving away to challenge the player character.
<br>
Godot - https://feather.openai.com/tasks/e9050755-8a6d-4100-9905-6620b5323ef4/stage/prompt_creation - Awaitng response.
