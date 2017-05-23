# PluginToAAR

"PluginToAAR" is a script that converts the "Assets/Plugins/Android/helpshift" folder to an "aar" file.

Helpshift SDK depends on Android support libraries and needs a Gradle dependency for a successful build.
Unity's in-built Gradle build support does not support plugin specific Gradle build script. Hence, Helpshift SDK cannot add its own gradle script to declare these dependencies by default.


For configuring "Helpshift" plugin to build via the in-built Unity Gradle system you will need to convert the "Assets/Plugins/Android/helpshift" directory to an "aar" file. This enables the Gradle build system to figure out the dependencies by itself.

Please follow these steps:

* Integrate the Helpshift plugin as per your requirements. If using the Helpshift Configurator, make sure the config is saved. [Refer here](https://developers.helpshift.com/unity/getting-started-android/#gui-inspector)
* Delete the following Android support libraries that are packaged with Helpshift plugin as directories: 
    * appcompat-23.4.0
    * design-23.4.0
    * cardview-23.4.0
    * recyclerview-23.4.0
    * support-v4-23.4.0
    * support-vector-drawable-23.4.0
* Copy the "aar" files of the above mentioned Android support libraries from your Android SDK installation directory.
* Run the `PluginToAAR` script. This will create "Assets/Plugins/Android/Helpshift.aar" file.
* Run the project build using the Gradle build system in Unity.
* Test Helpshift features.


## NOTE:
* This script creates a back up of "Assets/Plugins/Android/helpshift" folder in "Assets/" and creates a "Assets/Plugins/Android/Helpshift.aar" file.
* Although the script itself checks for updates, you should always check that you're using the latest version of the script.



## Setup/Installation

* Make sure you are running Python version `2.7.x`.

* Make sure pip is installed. If not, follow instructions here -
  https://packaging.python.org/installing/

* `PluginToAAR` depends on a few external Python libs, which can be
  installed by running the following command,

  ```bash
      pip install requests==2.7.0
  ```

* Make the script executable

  ```bash
      chmod u+x PluginToAAR
  ```

## Script arguments
| Argument  | Description |
| ------------- | ------------- |
| '-p', '--project-dir'      | Path to the project directory. Default is the present working directory.  |               
          
        
