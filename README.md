# UnityNavHelper
A simple navigation helper for Unity games.

UnityNavHelper contains two helpful actions:

1) Navigate to a new scene and send an object as a parameter (and the functionality to automatically 'receieve' the parameter in the next scene.
2) Navigate backwards to the previous scene without needing to name it.



UnityNavHelper consists of two scripts:
1) NavigationHelper - this provides static navigation methods to change the current scene and pass a parameter to the next scene.
2) OnSceneLoad - an abstract class that inherits MonoBehaviour and requires a handler method (called from MonoBehaviour's Awake method), that receives and interprets any parameter sent during navigation.

The parameter sent to a scene is stored in a static field of the NavigationHelper class. The script receiving the parameter object must inherit OnSceneLoad, and must implement the InterpretArgs method to cast/handle the object for the new scene.
