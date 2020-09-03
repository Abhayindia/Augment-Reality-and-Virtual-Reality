# Augment-Reality-and-Virtual-Reality
It is a platform for developers to rapidly build augmented reality (AR) and virtual reality (VR) experiences. Developers write in React Native, and runs their code natively across all mobile VR (including Google Daydream, Samsung Gear VR, and Google Cardboard for iOS and Android) and AR (iOS ARKit and Android ARCore) platforms. 

This project contains the full source code, and various sample projects.

The platform is free to use with no limits on distribution.

## Instructions for running sample projects using Testbed app:

1. Follow directions 
2. Clone the repo into your workspace with git.
3. Go into the code-samples directory.
4. Run `npm install` from the root of this project.
5. Run `npm start` from the root of this project.
6. Open the Media App, slide out the left panel and select "Enter Testbed".
7. Type the entire ngrok URL output (xxxxxx.ngrok.io) at the top of the terminal into the text field and hit 'GO'
8. You should now be in the application! Enjoy!.

## Instructions for running sample code as a stand alone project (with no Testbed app):
Tried the samples through our Testbed app and now want to try deploying sample code to your device as standalone apps? These quick steps below should get you started:
1. Follow steps 1 - 4 from above (instructions for using with Testbed app)
2. For Android, make sure you have downloaded and installed Android Studio from [here](https://developer.android.com/studio/install) to get required SDK and platform-tools for building android apps
    Make sure you have the required environment variables set - `$ANDROID_HOME`, and added `platform-tools` to `$PATH` variable. If not,
    ```
    export ANDROID_HOME=/YOUR_PATH_TO/Android/sdk
    export PATH=$ANDROID_HOME/platform-tools:$PATH
    export PATH=$ANDROID_HOME/tools:$PATH
    ```
    Build and launch android app by executing the following from the root of the project
    ```
    react-native run-android --variant=gvrDebug
    ```
3. For iOS, in Xcode open `Sample.xcworkspace` in `ios/` directory.
    Select the right "Team" for `Sample` and `SampleTest` target under `General -> Signing`
    Hit play to build and launch the app on your iOS device

### Changing Between Samples

1. Open App.js in a text editor.
2. For AR, set showARScene=true at line 44.
3. For VR, Modify line 61: `scene: scenes['360 Photo Tour'],` to a scene defined in the `scenes` dictionary on line 30.
3. Reload/restart the application.

## Instructions for using a CI-built React platform from Mainline:
You can also try the latest mainline build containing bleeding edge features and fixes. Please keep in mind that mainline builds may not be as stable as release builds. To do so, simply:

1. Go to the project.
2. You should see a list of "Pipeline" workflows.
3. Click on the latest successfully built workflow pipeline (should be a checkmark next to it).
4. Download the latest built React.tgz artiface.
4. Clone this repo into your workspace with git`.
5. Go into the code-samples directory.
6. Run `npm install` from the root of this project. 
7. Remove the React framework that was pulled down from the npm install (you are going to use the pre-built one).
8. npm install ../path/to/your/downloadedArtifact.tgz
