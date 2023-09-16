# Unity-tripups-in-Godot


DATE of document: 09/14/2023 (pardon my formatting)

Just some common road blocks I find in Godot that you can address to make your experience better as a fellow person who migrated to Unity
Most of my struggles come from utilizing c# so it may not apply to your experience.

*

Issue 1: why can't I see variables in Godot Inspector like in Unity Inspector displays public Variables (may need to check what version of Godot you have if it support its)
   
	Purpose: To add the drag and drop references directly from scene to the specific script instead of searching for it through scripting.

	Solution:
 
 ![image](https://github.com/rerako/Unity-tripups-in-Godot/assets/10995602/d2999b7e-3d44-425d-ac8c-809af083c6a1)


 add [Export] to variable;
 
	To do same for Godot example:

<format 1>

	[Export]
 
	public float variable;
<format 2>

	[Export]	public float variableB;
 
	Tip to quickly edit script to export multiple ones hold down "alt" and "mouse select" and drag the lines and position to the left of the multiple variables you want to add the [Export] clause to. 

*

*


Issue 2: I've installed  Editor IDE compatible with Godot and requirements, why is it going to default godot script editor?
   
	Purpose: everyone likes their own editor type and Godot is compatible with a few others.

	Solution:

 ![image](https://github.com/rerako/Unity-tripups-in-Godot/assets/10995602/a003edf2-5a7e-483e-b117-a1d947b46a9a)


	To set it to external editor too go to the Editor Tab -> Editor Settings (opens mini wondow)-> General -> Dotnet -> Editor

	 1st option toggles which external editor to choose 

*

*


Issue 3: I've setup external IDE but it keeps requesting I refresh or resave the script
![image](https://github.com/rerako/Unity-tripups-in-Godot/assets/10995602/a5ce0ec7-3097-467c-96f3-75b49dbfd35b)

   
	Purpose: save time and maintain only one version of script

	Solution:

	Close all scripts in Godot interal editor.

*

*


Issue 4: How to check variables and scene when running a build in editor?
	Purpose: to check variables mid run
	Solution:
 	When running Godot, the scene window adds two tabs to select(Remote for live data and Local for scene nonlive data):
  
  ![image](https://github.com/rerako/Unity-tripups-in-Godot/assets/10995602/9a482b4c-fd2a-4581-bc23-4c386fa1c580)


*

*


For C# what I noticed:


*

Issue 4: Why is positions undefined in scripting when I try to use Transform component for Nodes
   
	Purpose: Manipulating the position/rotation/scale(Vector3) of a game object/node for mechanics on a certain gameobject

	Unity:

		Gameobject->transform (component)-> position/rotation/scale-> x/y/z
  
	Godot:

		Node-> Node3D(Node2D) (component)-> Position/Rotation/Scale -> X/Y/Z
  
	Note: Transform is like a Superclass in Godot that has other methods




TIPS:

*

*

Tip 1: 

		C# in Godot follows PascalCase format 

		GDScript in Godot follows snake_case  format

*

*

Tip 2:
		To translate certain method names from Godot documentation from GDScript(default language) to C#

		You would translate it like so:

		has_focus() -> HasFocus()

*

*

Tip3: 
		Input and InputEvent are seperate classes for different input methods, easy to get mixed up. 

		For the defaults control inputs you would use Input class.

*

*

Tip4: 

	How to check input mappings and built in actions: Project Tab -> Project Settings (opens mini wondow)-> Input Map -> built in actions (top right toggle in mini window )
 ![image](https://github.com/rerako/Unity-tripups-in-Godot/assets/10995602/1dae3bfe-6ff5-4951-ab23-e080d4bba1cb)

