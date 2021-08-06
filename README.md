# SealNet GUI

This is the GUI for SealNet.

# Prerequisite

1. You need Python version 3.8 and above. Check if you have Python/your current version of python by running `python3 -V`. If you don't have Python 3.8 or above, you can download Python 3.9 from here: https://www.python.org/downloads/. Then install python3.9-tk with `brew install python-tk@3.9`

2. You must have used the face recognition model in https://github.com/zbirenbaum/SealFaceRecognition and download the result.json file and move it to the folder here.

# Display the GUI

1. Run `git pull` to pull any software updates.
2. [Ignore this step if you have created the virtual environment] Create a virtual environment by running:
`python3 -m venv py39`
3. Activate the environment with `source ./py39/bin/activate`
4. [Ignore this step if you have installed the dependencies] Install the dependency with `pip install -r requirements.txt`.
5. Run `python gui.py` to open the GUI
6. When done, close the virtual environment with `deactivate`


