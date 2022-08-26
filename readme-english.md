# Set Up Guide

<!-- TOC -->

* [Beginner's Guide](#beginners-guide)
    * [Download the course materials](#download-the-course-materials)
    * [Install Python](#install-python)
    * [Install an Interactive Development Environment (Optional)](#install-an-interactive-development-environment-optional)
    * [Open A Terminal and Navigate To the Course Files](#open-a-terminal-and-navigate-to-the-course-files)
    * [Create a Virtual Environment](#create-a-virtual-environment)
    * [Activate the Virtual Environment and Launch Jupyter Notebooks](#activate-the-virtual-environment-and-launch-jupyter-notebooks)
* [Advanced Guide](#advanced-guide-assumes-you-have-python-and-git-already-installed)
    * [Download or Clone the course materials](#download-or-clone-the-course-materials)
    * [Create your Virtual Environment and Install Dependencies, And Launch Jupyter Notebooks](#create-your-virtual-environment-and-install-dependencies-and-launch-jupyter-notebooks)

<!-- TOC -->

# Beginner's Guide

### Download the course materials

- Head to [GitHub] (https://github.com/LinkedInLearning/machine-learning-marketer-2460053), click the green 'Code'
  button and Select 'Download ZIP'.
- The course materials will be downloaded as a zipped folder called 'machine-learning-marketer-2460053-main' in the
  location you instructed the computer to download them. Go to that location and unzip the folder. Also, unzip the
  folder OnlineRetail.csv to the same location.
- Rename the folder. This is optional but will make the instructions simpler. I will rename the downloaded project to '
  ml_in_marketing'; the rest of the instructions assume this is your project name.

### Install Python

Python Version 3.7 was used to develop this course, but 3.8 and 3.9 should work. There may be incompatibilities in both
the course code and these instructions if you use other python versions. (Note that Python versions usually have three
numbers, e.g. 3.7.1, but you can ignore the third number; 3.7.1 suffices for 3.7, for example).

- Linux/MacOS usually come with a version of Python 3.8.X installed, which will work fine.
    - If for any reason you have Linux/Mac OS and don't have Python installed, instructions for installing it can be
      found at [wiki.python.org] (https://wiki.python.org/moin/BeginnersGuide/Download). This includes a link to the
      Python downloads page at python.org, where you can select your operating system and be taken to a list of Python
      downloads.
- Windows requires installing [git](https://git-scm.com/) and [Python](https://www.python.org/downloads/windows/)
    - A helpful package manager for installing Python on Windows is chocolatey. You can install it using the
      instructions [here](https://chocolatey.org/install) (be sure to run the terminal as an administrator, as they
      say).
    - Then you can use chocolatey to set up Python. Either use ```choco install python --version=3.8.0``` (recommended) 
  or ```choco install python```, which will install whatever the current latest version of Python is.

How to figure out which (if any) Python version you have:

- Mac users: Type ```which python```
- Windows users: Type ```python```. A Python console will open up within your terminal with a heading describing the
  version, e.g. 3.7. Type quit() to get out of the Python console.

If you have anything other than 3.7, 3.8 or 3.9, you may wish to install one of these versions using the instructions
listed above.

### Install an Interactive Development Environment (Optional)

Various IDEs are available and all provide their own installation instructions. An easy starting point is Visual Studio
Code: It is free, fast and has a huge community with extensions and features behind it. PyCharm is another popular
choice, although it has a lot of features and might be overwhelming at first.

If you would like to work with an IDE (optional for the next small step but otherwise not required at all) and don't
have one yet, then please look up the online instructions for your desired IDE and your operating system.

### Open A Terminal and Navigate To the Course Files

There are two ways to do this, depending on whether you've decided to use an IDE or not.

#### Option A: Via a Computer Terminal or Visual Studio Code

Open a Terminal on your computer (you can usually open a Terminal like you would any other program, or check online for
the shortcut for your operating system). Alternatively, open Visual Studio Code and click the 'Terminal' button (in
the top menu bar) and choose 'New Terminal'.

Navigate to the location where the course files are stored. To do this, type ```cd``` followed by space followed the
path to the folder location. The path will consist of all the directories between where you are and where you have to
go, separated by a / slash (Mac/Linux) or a \ slash (Windows). The example in the next step assumes that I am on Mac OS,
and that my terminal opens to my user directory, 'munro', and that inside this directory is a folder 'Documents', and
inside this is the folder with the course materials. You'll need to adapt the path accordingly, and you want to navigate
all the way until you select the folder name which contains the file 'requirements.txt'. Again, you'll find resources
online to help you if you get really stuck.

#### Option B: Via an IDE

Start your IDE of choice. I'll use PyCharm for these instructions, but the process for e.g. IntelliJ should be similar.
Select File > Open > navigate to the folder containing the course materials, e.g. requirements.txt, and click 'Open'. 
If PyCharm asks you whether to trust the project, choose to do so! Also, if PyCharm asks you whether you want to open 
the project in the existing window or a new one, select 'New Window'.

Open a Terminal within the IDE. The button should either be along the bottom left menu or along the top left side menu,
but if you can't find it, type Cmd+Shift+A (Mac) or Ctrl+Shift+A (Windows) to bring up the Actions search panel, and
then type 'Terminal'.

### Create a Virtual Environment

Most Python projects you get from other people will require you to download so-called 'dependencies', which are the
Python libraries used in the project. These dependencies are listed in a file called 'requirements.txt'. An easy (but
warning - wrong!) way to install these dependencies is to open a Terminal, navigate to the location of the requirements
file and typing `pip install -r requirements.txt` (assuming you have installed the package manager 'pip'). This will
install the dependencies directly on your computer, which is a big risk: later if you work on other Python projects, the
dependencies of that project might be incompatible with what you've already installed.

This is why you should create a so-called 'virtual environment' for each of your Python projects. The easiest way to do
this is using pipenv. Here are all the commands you'll need to use (you can skip the first line if you already completed
it in the last step).

```bash
cd Documents/ml_in_marketing # Navigate to the folder you want to work in (skip this if you already did it)
pip3 install pipenv # You need only do this once; in future if you're starting new projects with new virtual environments, you can skip this line
pipenv install --python=3.8 -r requirements.txt
```

Now you'll have to wait a couple of moments for the virtual environment to be created and for the dependencies to be
installed.

### Activate the Virtual Environment and Launch Jupyter Notebooks

Once the last step finishes, you should see the message 'Successfully created virtual environment!'.

If you see 'Warning: Python 3.8 was not found on your system', it means pipenv could not find a version of Python 3.8 on
your computer to use. First, remove the environment via `pipenv --rm`. Then, follow the instructions in 
['Install Python'](#install-python) to figure out which version you have. If you don't have 3.8, you can install it, and
then start again from ```pipenv install --python=3.8 -r requirements.txt```. Alternatively, you can use your existing 
version in the install command, as long as it is 3.7, 3.8 or 3.9 (ignore the third number in your system Python version,
 e.g. if you have Python 3.9.1 just say 3.9).

If you suspect anything else has failed, you can remove the environment via `pipenv --rm` and start again.

Once the virtual environment is successfully created, you can activate it and launch Jupyter Notebooks in your browser:

```bash
pipenv shell # Activate the virtual environment
jupyter notebook # Launch jupyter notebooks
```

Congratulations, now you're ready to get started!

Finally, here are some tips for how to close the notebook, deactivate the virtual environment, and activate it again at
a later time:

Ctrl+c in the Terminal will close a Jupyter Notebook (make sure you've saved your notebook in the browser first!). After
typing this, you'll be prompted to type ```y``` to confirm you want to close the notebook.

```deactivate``` will leave the virtual environment and put you back into the system. You can then close the terminal.

If you want to start again later, open the terminal (on your computer or in the IDE), navigate to the project location,
type ```pipenv shell``` and again ```jupyter notebook```.

# Advanced Guide (assumes you have Python and Git already installed)

### Download or Clone the course materials

- Head to [GitHub] (https://github.com/LinkedInLearning/machine-learning-marketer-2460053) and clone the repository, or
  download and unzip the course files using the green 'Code' button.
- Rename the folder. This is optional but will make for a nicer virtual environment name (if you use the pipenv install
  option I'll describe here). I'm using 'ml_in_marketing'.

### Create your Virtual Environment and Install Dependencies, And Launch Jupyter Notebooks

If you have your own preferred means of creating a virtual environment and installing dependencies,
e.g. ```via pip install -r requirements.txt```, then feel free to do so. Alternatively, below are the instructions for 
using pipenv.

Open your IDE of choice or your computer's Terminal app and execute the following commands:

```bash
cd Documents/ml_in_marketing # Navigate to the folder of course materials
pip3 install pipenv # If you don't have pipenv already
pipenv install --python=3.8 -r requirements.txt # You can choose a different Python version; 3.7-3.9 should work
# Wait for it to finish; it will say 'Successfully created virtual environment!'
pipenv shell # Activate the environment
jupyter notebook # Launch jupyter notebooks
# When you're finished working, use Ctrl+c to stop the notebook (save it in the browser first!)
deactivate # Leave the virtual environment
```

- Pipenv will automatically scan your system and find the first usable Python version, e.g. 3.8.
- There are many alternative ways to manage Python environments
    - conda (Anaconda, miniforge) or mamba (faster conda), which install stricter binaries and tend to work more
      reliably but are bigger and slower
    - virtualenv via various helper scripts, which does the same as pipenv but is less intuitive. Below is an example:

  ```bash
  virtualenv ml_in_marketing
  source ml_in_marketing/bin/activate
  pip install -r requirements.txt
  jupyter notebook
  # Ctrl+C to exit
  deactivate # or just close the Terminal window
  ```