# ThirdPersonControllerAI
The modified version of ThirdPersonController to control AI Characters using third person controller provided by Unity.
Video : https://www.youtube.com/watch?v=x4TwKOVMfnk
- Start A New Project from Unity Hub and Select Core / Third Person
- Open PlayGround from Scenes (if it is not already open)
- Delete big Ground from the Scene (Environment > Greybox > Primitives > Ground)
- Add Box Collider to Ground_Mesh (Environment > Greybox > Primitives > Ground_Mesh)
- Open Navigation tab (Windows > AI > Navigation)
- Select Bake Tab and Hit Bake. (Make sure all the Environment GameObjects are set to Navigation Static
- Select PlayerFollowCamera, UI_EventSystem, UI_Canvas_Starter, MainCamera, and Delete.
- Add a new Camera to the Scene
- Select PlayerArmature
- Remove ThirdPersonController, BasicRigidBodyPush, StarterAssetsInputs, PlayerInput.
- Add NavMeshAgent
- Change NavMeshAgent's Base Offset to -0.05 or -0.08
- Add ThirdPersonControllerAI Script
- Set Ground Layers to Everything
- Add an (empty) GameObject and Set ThirdPersonControllerAI's target to it.
- Hit Play.

You can access ThirdPersonControllerAI using
myAI = GetComponent\<ThirdPersonControllerAI\>();
myAI.Target myAI.Sprinting myAI.Jump

Removed null checks, not tested thoroughly, use it at your own risk.
Waypoints, Chase Enemy, Meele, and Ranged Attack are being implemented.
ergin3d.com
