# SealNet GUI

This is the GUI for SealNet.

# Prerequisite (Only do this once)

1. Open Terminal and check your Python version by typing `python -V`. If the terminal shows you have python version >= 3.8, you can skip this part.
Else, if it is "command not found" or lower version of python, then do the following:
Install python 3.9: https://www.python.org/downloads/
Then install python3.9-tk with `brew install python-tk@3.9`

2. Clone the repository into your desktop by running:
```
cd ~/Desktop
git clone https://github.com/hieudo-hn/recognitionGUI.git
```

3. You must have used the face recognition model in https://github.com/zbirenbaum/SealFaceRecognition and download the result.json to the Downloads folder.
4. Move the result.json file to this directory named recognitionGUI in your Desktop. 
5. On the terminal, run `cd ~/Desktop/recognitionGUI`
6. Create a virtual environment by running:
`python3 -m venv py39`
7. Run `source ./py39/bin/activate` to activate the virtual environment
8. Install the dependency with `pip install -r requirements.txt`.
9. We want our pathing to be similar to data pathing in https://github.com/zbirenbaum/SealFaceRecognition, so let's make a data folder by running:
```
mkdir data && mkdir data/processed && mkdir data/processed/train && mkdir data/processed/probe
```

# Display the GUI
1. Remember to move the result.json file from the Downloads folder to the recognitionGUI folder in your Desktop before executing the next steps:
2. Assess this repository from the terminal by running `cd ~/Desktop/recognitionGUI`, then run `git pull` to pull any software updates.
3. Run `source ./py39/bin/activate` to activate the virtual environment
4. [Ignore this step if your photos are already in their respective data folder]
Your probe photos should be in ./data/processed/probe and your gallery (database) should be in ./data/processed/train. Please move the same folders that you used on the AWS machine to their respective destinations.
5. Before opening the GUI, you should know about the match.json file:
    + match.json saves your previous predictions if you have used the GUI before. 
    + If you are loading a new probe data, make sure to delete the match.json file if it is present.
    + If you are using the previous probe data, do not delete the match.json file.
6. Opening the GUI: Run `python gui.py` to open the GUI to view predictions. 
Choose your matched seal by clicking "Check" on the corresponding seal or "No Match"
if you think there is no match. Save your result by clicking "Save", you can view a summary of your choice by clicking "Save & View Summary".
When you are absolutely certain with your choices, you can click "Save & Merge" to merge your probe to your database. This is not a reversible action, 
you might have to manually move the photos if you change your mind.
Your updated databased is the one in ./data/processed.
7. When done, close the terminal

# Additional Info:
1. SealNet: https://github.com/zbirenbaum/SealFaceRecognition


