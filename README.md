# :pencil: (Use Case) Tutorial System
---------

:pushpin: Overview
---------
An Independent tutorial system that has its own layer above the game with a focus on modularity and easy modify by nontechnical people. Here is a tutorial use case that we solve and I would like to share it with you.

![TutorialArchitecture](https://user-images.githubusercontent.com/14979589/83567193-e4daad00-a529-11ea-805c-38362a59382d.png)

:bulb: Idea
---------
We need to develop a machine state tutorial-based system which will be independent of the game and will be easily modified by nontechnical people. The system contains an editor tool & tutorial system.

:white_check_mark: Goals
---------
* Editor for designers
* Easy export-import JSON data
* MachineState based core system
* Component actions subsystem 
* Checkpoint subsystem
* Debugging subsystem
* Independent layer
* Generic solution

:rocket: Result
---------
Editor <br>
![ToolResult](https://user-images.githubusercontent.com/14979589/83565759-99bf9a80-a527-11ea-8f5f-645b74f92514.png)

Demo Gameplay <br>
![TutorialDemo](https://user-images.githubusercontent.com/14979589/83566166-3da94600-a528-11ea-9c97-f1c664bef19f.gif)

:pushpin: How these thigs works?
---------
**Tutorial Editor** <br> 
Using reflection by TActionReflect from the tutorial system and provide an interface for setup data with ability of easy JSON export.

**Tutorial Trigger / Tutorial Handler** <br>
Taking care about prefabs management and setup whole actions for a tutorial which will be in usage during the gameplay.

**Entity Database** <br>
On the beggining of the game are game entitties assigned into a central object database and ready for later usage.

**ExecutionManager** <br>
Manage whole tutorial execution logic, creating action by a component system which provide game mechanics.

**Components** <br>
The tutorial contains several components, each component has own specialization with focus on modularity (Camera, GameData, UI).

**TActionBase / TActionReflect** <br>
Component reflect subsystem which provides reflection data about components for editor tool, later read data from JSON and generate game actions.

:package: Package to download
---------
* Tutorial structure template
  * Events
  * Execution Manager
  * Components & reflection template
  * Simplified state machine core
