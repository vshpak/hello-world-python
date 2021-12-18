# Hello World Python

This repo contains is a sandbox to play on education tasks for python.

Scripts tested and works correctly on python >= 3.8.


## Repository structure

Here is a hierarchy of directories and files.

```ruby
hello-world-python
├── .gitignore
├── CHANGELOG.md
├── README.md
└── hello-py/
    ├── hello-py/
    │   ├── __init.py__
    │   ├── app.py
    │   ├── lib.py
    │   └── version.py
    └── setup.py
```

### "Hello-Py" application and library

According initial idea need to create a mini project on Python contains the following two parts:
* Library which contains hello() function which is returns "hello" string,
* Application just prints "hello" string by calling hello() function.

Program modes (options):
* help: `hello-py -h` or`hello-py --help`
* version: `hello-py -v` or `hello-py --version`
* ordinary greetings: `hello-py`
    * i.e. without arguments

### Git's auxiliary files

**.gitignore** - patterns / paths of files to exclude from Git management 
(build files (.o, .pyc etc.), binaries, IDEs' configs). There are many templates 
for different programmer languages, also good collection could be found at 
[github](https://github.com/github/gitignore/blob/master/Global/JetBrains.gitignore) 
for PyCharm IDE and Python.
Also ignore the whole **.idea** directory


## Installation

### Installation (from GitLab)
Use the below command to install latest version of the application:
```sh
$ pip install -vv git+ssh://git@gitlab.com/vshpak/hello-world-python.git#subdirectory=production/hello-py
```
This assumes SSH access to GitLab is already configured and SSH key is available to SSH client.


### Installation (setuptools)
Clone the repository and navigate into the local directory with the project.
You can install everything from build directory using setuptools utility by the following command:
```sh
$ cd hello-py
$ sudo python3 setup.py install
```

### Installation (pip)
To create so called wheel file please execute the following:
```sh
$ cd hello-py
$ sudo python3 setup.py bdist_wheel
```
The required wheel file will be created into the "dist" subdirectory.
You can install using pip utility please navigate to the "dist" directory and execute the following command:
```sh
$ cd hello-py/dist
$ sudo python3 -m pip install hello-py*.whl
