# LineCallForTennis

## Use a smartphone camera as an IP camera
1. install an app called DroidCam on the phone.

## virtual environment
[ref](https://docs.kanaries.net/topics/Python/conda-remove-environment)
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
conda create -n <env_name> python=x.x anaconda
// Install Additional Python Packages To A Virtual Environment
conda install -n [env_name] [package]

// How To Remove A Conda Environment
conda env remove --name [env_name]
// How To Delete A Conda Package
conda env remove --name [env_name] [pkg_name]

// Save Packages For Future Use
conda list –-export > [package_list.txt]

// Reinstall Packages From An Export File
conda create -n [env_name] –file [package_list.txt]
```

```
// How To Use A Virtual Environment In VS Code
