# ![mdf-logo](docs/img/atwork.gif) Python Web Development

---

## Goal
This is a collection of python web projects. 

## Setup
`conda` is the preferred virtual environment management tool for this project.

### Download the Project Code
Use `clone -- recursive` to get the submodule code.
```shell
$ git clone --recurse git@github.com:c-w-m/vs2022_dev.git       ## SSH
$ git clone --recurse https://github.com/c-w-m/vs2022_dev.git   ## https or
```

----
## Directory Layout
| Directory  | Description            |
|------------|------------------------|
| docs/*     | links and notes        |
| ipynb/*    | sandbox/demo notebooks |
| src/*      | projects               |
| src/demo   | sandbox code           |
|------------|------------------------|

----

## Submodules
The following projects were added under the `src/` directory.

### demo/
```shell
cd demo
/demo$ git submodule add   #
````

### src/
```shell
$ cd src
/src$ git submodule add 
```

### Recursive Update Submodules
```shell
$ cd src # or cd demo
/src$ git submodule update --init --recursive
/src$ git submodule foreach --recursive git fetch
/src$ git submodule foreach git merge origin master
```

### Removing Submodules
```shell
$ git submodule deinit -f src/yloader
$ rm -rf .git/modules/src/yloader
$ git rm -f src/yloader
```
```shell
git submodule deinit -f demo/yloader
rm -rf .git/modules/demo/yloader
git rm -f demo/yloader
```

Here is a more verbose example.
```shell
# Remove the submodule entry from .git/config
git submodule deinit -f src/<submodule_name>

# Remove the submodule directory from the super-project's .git/modules 
directory
rm -rf .git/modules/src/<submodule_name>     #nix
rd /s /q '.git\modules\src\<submodule_name>' #win

# Remove the entry in .gitmodules and remove the submodule directory located at path/to/submodule
git rm -f src/<submodule_name>

# optional last two steps
git rm -r --cached src/<submodule_name>
git commit -m "removing <submodule_name>"
```

----

## Feature Branches

### `lint`
Get the code to pass  `pylint` from PyCharm IDE and `tox -e check`.

```shell
(vs2022_dev36) $ git fetch && git checkout dev/lint

Branch 'dev/lint' set up to track remote branch 'dev/lint' from 'origin'.
Switched to a new branch 'dev/lint'
(vs2022_dev36) $ 
```

----

## Anaconda Environment
#### Using Conda
Each project will have it's own `requirements.txt` list of packages:
```shell
# activate conda base
$ conda activate base
(base)$ conda create -y --name vs2022_dev{38,39} python=3.{8,9}
(base)$ conda install --force-reinstall -y -q --name vs2022_dev{38,39} -c anaconda -c conda-forge -c defaults --file requirements.txt
(base)$ conda activate vs2022_dev{38,39}
(vs2022_dev{38,39})$ conda install <any missing packages>
...
(vs2022_dev{38,39})$ deactivate
(base)$
```
Additional commands can be found in the [cheet-sheets.pdf](https://docs.conda.io/projects/conda/en/latest/_downloads/843d9e0198f2a193a3484886fa28163c/conda-cheatsheet.pdf).

### Create and Load Conda Environment From `yml` File
>Note: The `<os>` designation is either `ubnt1604` (for Ubuntu 16.04) or `win10` (for Windows 10).
```shell
(base)$ conda env create -f vs2022_dev{38,39}.<os>.yml
(base)$ conda activate eda_dev39 
(vs2022_dev{38,39})$ cd ipynb
(vs2022_dev{38,39})$ jupyter lab
```

### Install New Conda Environment Packages
```shell
(vs2022_dev{38,39}) $ conda install <package name>
```

### Update Conda Environment Packages
```shell
(vs2022_dev{38,39}) $ conda update <package name>
```

### Export Conda Environment
```shell
(vs2022_dev{38,39}) $ conda env export > vs2022_dev{38,39}.<os>.yml
```

### Get Conda Environment
```shell
(vs2022_dev{38,39}) $ conda info -e
```

### Remove Conda Environment
```shell
(vs2022_dev{38,39}) $ conda remove -n <env_name> -all
```

----

## PIP Installations
### Install
```shell
(vs2022_dev{38,39})$ pip install <package-name>
```
### Uninstall
```shell
(vs2022_dev{38,39})$ pip uninstall <package-name>
```

----

## Jupyter Notebooks
Remember to use `ipykernel` to expose your python environment in Jupyterlab.
```shell
$ conda activate eda_dev39
(vs2022_dev{38,39})$ python -m ipykernel install --user --name=vs2022_dev{38,39}
(vs2022_dev{38,39})$ jupyter lab
```

#### List All Kernels
```shell
$ jupyter kernelspec list
```
#### Remove a Kernel
```shell
$ jupyter kernelspec uninstall <kernel_name>
```

----

## Develop Installations
### Install
```shell
<package-dir>(vs2022_dev{38,39})$ python setup.py develop
```
### Uninstall
```shell
<package-dir>(vs2022_dev{38,39})$ python setup.py develop --uninstall
```
or, in case the installation was not using develop
```shell
python setup.py install --record files.txt
# followed by
xargs rm -rf < files.txt
```
you'll need to delete the directories in the project as well

develop creates an .egg-link file in the site-packages directory, which points back to the
location of the project files. The same path is also added to the easy-install.pth file in
the same location. Uninstalling with setup.py develop -u removes that link file again.

Do note that any install_requires dependencies not yet present are also installed, as
regular eggs (they are easy_install-ed). Those dependencies are not uninstalled when
uninstalling the development egg.

----

## References
* [Quickstart: Create your first Python web app using Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/quickstart-python?view=vs-2022)

