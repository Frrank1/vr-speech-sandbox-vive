# WORK IN PROGRESS

We're still baking this journey, come back in a few weeks to get something fully baked.


## IBM Speech Sandbox

[![IBM Speech Sandbox](http://img.youtube.com/vi/FlMvLDw6cYc/0.jpg)](http://www.youtube.com/watch?v=FlMvLDw6cYc)

In this repo is an example of how to put the [Watson Speech to Text](https://www.ibm.com/watson/developercloud/speech-to-text.html) and [Watson Conversation](https://www.ibm.com/watson/developercloud/conversation.html) services into a Unity Virtual Reality game. For more information about the project you can check out our [Case Study](https://www.ibm.com/innovation/milab/work/speech-sandbox/). Or if you just want to play a built version with a lot of pre-loaded objects you can download the game on [Viveport](https://www.viveport.com/apps/bbde0cff-98c1-4117-acd8-e808ded515ca).

## Before You Begin

### Things You'll Need

* [IBM Bluemix Account](https://console.ng.bluemix.net/registration/)
* ["VR Ready" PC](https://www.vive.com/us/ready/)
* [HTC Vive](https://www.vive.com/us/product/)
* [SteamVR](http://store.steampowered.com/steamvr)
* [Unity](https://unity3d.com/get-unity/download)

### Service Setup

On your local machine:
1. `git clone https://github.com/IBM/speech-sandbox.git`
2. `cd speech-sandbox`

On [IBM Bluemix](https://console.ng.bluemix.net/):
1. Create a [Speech To Text](https://console.ng.bluemix.net/catalog/speech-to-text/) service instance.
2. Create a [Conversation](https://console.ng.bluemix.net/catalog/services/conversation/) service instance.
3. Once you see the services in the Dashboard, select the Conversation service you created and click the !["Launch Tool"](/doc/source/images/workspace_launch.png?raw=true) button.
4. After logging into the Conversation Tool, click the !["Import"](/doc/source/images/import_icon.png?raw=true) button.
5. Import the [`Conversation.json`](Conversation.json) file located in your clone of this repository.

## Building and Running

If you followed the previous steps you should already be inside your local clone and ready to get started running the app from Unity.

1. `git clone https://github.com/watson-developer-cloud/unity-sdk.git`
2. Open Unity and inside the project launcher select the ![Open](doc/source/images/unity_open.png?raw=true) button.
3. Navigate to where you cloned this repository and open the "Creation Sandbox" directory.
4. If prompted to upgrade the project to a newer Unity version, do so.
5. Follow [these instructions](https://github.com/watson-developer-cloud/unity-sdk#getting-the-watson-sdk-and-adding-it-to-unity) to add the Watson Unity SDK downloaded in step 1 to the project.
6. Follow [these instructions](https://github.com/watson-developer-cloud/unity-sdk#configuring-your-service-credentials) to add your Speech To Text and Conversation service credentials (located on [IBM Bluemix](https://console.ng.bluemix.net/)).
7. Select `Advanced Mode` in the configuration window.
8. Click `Add Variable` and name your new variable `ConversationV1_ID` then set its value to the Workspace ID of your Conversation workspace.
    ![Variable Configuration Example](doc/source/images/add_variable.png?raw=true)
 You can find your workspace ID by selecting the expansion menu on your conversation workspace and selecting `View details`.
    ![View Details Location](doc/source/images/workspace_details.png?raw=true)
9. Press Play

# Project Structure

Here is a general overview of some of the more important directories in the project.

```
.
├── data
│   └── workspace.json      // an export of a basic Speech Sandbox conversation setup
├── Creation Sandbox        // the Unity project
│   ├── Assets                  // contains all project assets
│   │   ├── _Scenes                 // all game scenes
│   │   │   ├── MainGame
│   │   │   │   ├── MainMenu            // the main menu scene
│   │   │   │   ├── Tutorial            // the tutorial scene
│   │   │   │   └── Sandbox             // the main sandbox scene
│   │   ├── Prefabs                 // the games prefabs
│   │   │   ├── CreatableObjects        // all objects that can be created
│   │   │   ├── Tutorial                // objects pertaining to the tutorial
│   │   │   └── Widgets                 // contains custom widgets (like VoiceSpawner)
│   │   ├── Scripts                 // all custom game scripts
│   │   │   ├── Controls                // scripts related to the game controls
│   │   │   ├── Objects                 // scripts related to the objects that can be created
│   │   │   ├── SceneManagement         // scripts related to manageing scene state
│   │   │   ├── Tutorial                // scripts related to running the tutorial
│   │   │   └── UI                      // scripts related to any menuing 
│   │   ├── SteamVR                 // the SteamVR plugin
│   │   └── VRTK                    // the VRTK plugin
│   └── ProjectSettings         // contains configuration files for the project
```

For additional help understanding the code you can check out [this blog](https://www.ibm.com/innovation/milab/watson-speech-virtual-reality-unity/) written by [Kyle Craig](https://twitter.com/thekylecraig) about how to implement this type of speech control in your own projects.

# Links

* [Viveport](https://www.viveport.com/apps/bbde0cff-98c1-4117-acd8-e808ded515ca)
* [Dev Blog](https://www.ibm.com/innovation/milab/watson-speech-virtual-reality-unity/)
* [Case Study](https://www.ibm.com/innovation/milab/work/speech-sandbox/)
* [Watson Unity SDK](https://github.com/watson-developer-cloud/unity-sdk)
* [IBM Bluemix](https://www.ibm.com/cloud-computing/bluemix/)

# Acknowledgements

* [Kyle Craig](https://github.com/craigkj312): The original Author of the code
* [VRTK](https://github.com/thestonefox/VRTK)
* [Borodar](http://www.borodar.com/)
* [Kabbalistic Villiage](https://soundcloud.com/kabbalisticvillage)

# License

[Apache 2.0](LICENSE)

