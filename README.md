# dexter

"Dexter" is a script that can help in applying workaround for dex count issues during android build for a Unity Android project.

The script parses the Unity project for Android libraries that can be refactored to reduce the overall method count via the process mentioned in our documentation linked below: 
https://developers.helpshift.com/unity/troubleshooting-android/#dex-64k-issue

## NOTE:
* This script refactors the folder structure and the AndroidManifest.xml files of the Android libraries in your project. The app needs to be thoroughly tested after executing the script. 
* Updating the refactored plugins can have issues. A Unity plugin/android library upgrade generally looks for updating a predefined folder/file path. Since this script can potentially change the folder/file structure, upgrading plugins can have issues. Update of any plugin/library needs to be thoroughly tested for integration and functionality.
* Although the script itself checks for updates, you should always check that you're using the latest version of the script.

## Setup/Installation

* Make sure you are running Python version `2.7.x`.

* Make sure pip is installed. If not, follow instructions here -
  https://packaging.python.org/installing/

* `dexter` depends on a few external Python libs, which can be
  installed by running the following command,

  ```bash
      pip install requests==2.7.0 PyYAML==3.10
  ```

* Make the script executable

  ```bash
      chmod u+x dexter
  ```

## Script arguments
| Argument  | Description |
| ------------- | ------------- |
| '-v', '--verbose'          | Enables logging.   |
| '-p', '--project-dir'      | Path to the project directory. Default is the present working directory.  |
| '-b', '--backup-suffix'    | Suffix to add to dir where backup is taken. Default is '.bkp'. |
| '-a', '--android-target'   | Android target version to be added in the project.properties file of refactored android libraries. |
                
          
        
