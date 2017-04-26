# dexter

"Dexter" is a script that can help in applying workaround for dex count issues during android build for a Unity Android project.

The script parses the Unity project for Android libraries that can be refactored to reduce the overall method count via the process mentioned in our documentation linked below: 
https://developers.helpshift.com/unity/troubleshooting-android/#dex-64k-issue

## NOTE:
* This script refactors the folder structure and the AndroidManifest.xml files of the Android libraries in your project. The app needs to be thoroughly tested after executing the script. 
* Updating the refactored plugins can have issues. A Unity plugin/android library upgrade generally looks for updating a predefined folder/file path. Since this script can potentially change the folder/file structure, upgrading plugins can have issues. Update of any plugin/library needs to be thoroughly tested for integration and functionality.
* Although the script itself checks for updates, you should always check that you're using the latest version of the script. 

## Prerequisites
Set executable permission for the script. You can set it with the following command: 'chmod +x dexter' 
      2. Python 2.7.10 or higher version. Install python from here: https://www.python.org/downloads/
      3. The following packages need to be installed:
1. yaml
2. json
3. requests
4. shutil
5. xml.dom.minidom
6. logging
7. argparse
8. zipfile
9. contextlib

If any of the above are not installed on your system, you can install them with the following command:

pip install `<package-name>`

If you don't have the "pip" tool installed, you can follow the steps mentioned here: 

https://packaging.python.org/installing/

## Script arguments
| Argument  | Description |
| ------------- | ------------- |
| '-v', '--verbose'          | Enables logging.   |
| '-p', '--project-dir'      | Path to the project directory. Default is the present working directory.  |
| '-b', '--backup-suffix'    | Suffix to add to dir where backup is taken. Default is '.bkp'. |
| '-a', '--android-target'   | Android target version to be added in the project.properties file of refactored android libraries. |
                
          
        
