# LineCallForTennis

## Use a smartphone camera as an IP camera
1. install an app called DroidCam on the phone.

## virtual environment
[ref](https://docs.kanaries.net/topics/Python/conda-remove-environment)
[ref](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-pkgs.html)
```
// Check If Conda Is Up To Date
conda update conda
// How Do I List All The Conda Environments?
conda env list
// How Do I List All The Packages In The Current Environment?
conda list
// How Do I List All The Packages In A Specific Environment?
conda list -n <env_name>

// How To Create A Conda Environment
// 끝에 anaconda 붙이면 anaconda 배포판에 포함된 패키지들 같이 설치
conda create -n <env_name> python=x.x anaconda
// Install Additional Python Packages To A Virtual Environment
conda install -n <env_name> <package>

// How To Remove A Conda Environment
conda env remove --name <env_name>
// How To Delete A Conda Package
conda env remove --name <env_name> <pkg_name>

// Save Packages For Future Use
conda list –-export > <package_list.txt>

// Reinstall Packages From An Export File
conda create -n <env_name> –-file <package_list.txt>
```

## Package List(requirements.txt)
### Create a file of the package list you need for your project
```
# Option 1
pip freeze > requiremetns.txt
# Option 2
pip install pipreqs
pipreqs /path/to project
```
### Install all the packages you need for the project
```
pip install -r requirements.txt
```

### Create a file of the list of all you installed with the pip install command
[ref](https://stackoverflow.com/questions/31684375/automatically-create-file-requirements-txt)



### If you face the problem of not recognizing the command "conda"

Windows -> Edit the system environment variables -> Environment Variables -> System variables -> Path -> Edit -> New

-> C:\Users\Your_User_Name\anaconda3, C:\Users\Your_User_Name\anaconda3\Scripts, C:\Users\Your_User_Name\anaconda3\Library\bin -> OK



### How To Use A Virtual Environment In VS Code
[ref](https://code.visualstudio.com/docs/python/environments)</br>
You can create a conda environment with a name of it, but only in the default location(~\anaconda3\envs\)</br>
If you create a conda environment in your working directory, you can't have the name for it.
If you want to use a conda environment for your project directory, make one with a name and activate it when you work on it.
1. Select The Explorer Tab
2. Open A Project Folder
3. Create A Conda Environment for Your Project
```
(base) PS path\to\your\project\folder> conda create --name {your_env} python=3.11.9
```
4. Activate Your Environment
```
(base) PS path\to\your\project\folder> conda activate your_env
(your_env) PS path\to\your\project\folder> 
```
6. Open The Command Palette (Ctrl + Shift + P)
7. Select Interpreter (Python: Select Interpreter -> Python 3.11.9('your_env') ~\anaconda3\envs\your_env\python.exe)
```
(lineCall) PS C:\Users\kitki\Project_TennisLineCall> conda env list
# conda environments:
#
base                     C:\Users\kitki\anaconda3
jiji                     C:\Users\kitki\anaconda3\envs\jiji
lineCall              *  C:\Users\kitki\anaconda3\envs\lineCall
```
*(asterisk) means that it is the active environment.



# Red Flags(Red Color Text in the terminal)
## Problem_01
```
. : File C:\Users\kitki\Documents\WindowsPowerShell\profile.ps1
cannot be loaded because running scripts is disabled on this
system. For more information, see about_Execution_Policies at
https:/go.microsoft.com/fwlink/?LinkID=135170.
At line:1 char:3
+ . 'C:\Users\kitki\Documents\WindowsPowerShell\profile.ps1'
+   ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : SecurityError: (:) [], PSSecurityEx
   ception
    + FullyQualifiedErrorId : UnauthorizedAccess
PS C:\Users\kitki\Project_TennisLineCall>
```
## Solved
1. Open the terminal
2. Change the execution policy (default: Restricted -> RemoteSigned or Unrestricted)
3. Reopen the terminal
```
# Change the policy
PS C:\Users\kitki\Project_TennisLineCall> Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
# Now you can see the PowerShell prompt below
(base) PS C:\Users\kitki\Project_TennisLineCall>
```
