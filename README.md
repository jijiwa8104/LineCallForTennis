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

### If you face the problem of not recognizing the command "conda"

Windows -> Edit the system environment variables -> Environment Variables -> System variables -> Path -> Edit -> New

-> C:\Users\Your_User_Name\anaconda3, C:\Users\Your_User_Name\anaconda3\Scripts, C:\Users\Your_User_Name\anaconda3\Library\bin -> OK



### How To Use A Virtual Environment In VS Code
[ref](https://code.visualstudio.com/docs/python/environments)

1. Select The Explorer Tab
2. Open A Project Folder
3. Open The Command Palette (Ctrl + Shift + P)
4. Create A Conda Environment (Python: Create Environment -> Conda -> Python 3.11(star marked)
5. Open The Command Palette (Ctrl + Shift + P)
6. Select Interpreter (Python: Select Interpreter -> Python 3.11.9('.conda': conda)(Recommended)
7. > conda env list
If you can see *, that is the one currently activated.
