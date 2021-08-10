# SealNet GUI

This is the GUI for SealNet.

# Prerequisite

1. You need Python version 3.8 and above. Check if you have Python/your current version of python by running `python3 -V`. If you don't have Python 3.8 or above, you can download Python 3.9 from here: https://www.python.org/downloads/. Then install python3.9-tk with `brew install python-tk@3.9`

2. Clone the repository into your desktop by running:
```
cd ~/Desktop
git clone https://github.com/hieudo-hn/recognitionGUI.git
```

3. You must have used the face recognition model in https://github.com/zbirenbaum/SealFaceRecognition and download the result.json file and move it to the folder here.

# Display the GUI

1. Assess this repository from the terminal by running `cd ~/Desktop/recognitionGUI`, then run `git pull` to pull any software updates.
2. [Ignore this step if you have created the virtual environment] Create a virtual environment by running:
`python3 -m venv py39`
3. Activate the environment with `source ./py39/bin/activate`
4. [Ignore this step if you have installed the dependencies] Install the dependency with `pip install -r requirements.txt`.
5. [Ignore this step if you have your have created the /data folder with /processed and /probe] We want our pathing to be similar to data pathing in https://github.com/zbirenbaum/SealFaceRecognition, so let's make a data folder by running:
```
mkdir data && cd data && mkdir processed && mkdir probe && cd ..
```
6. [Ignore this step if your photos are already in their respective data folder]
Your probe photos should be in ./data/probe and your gallery (database) should be in ./data/processed. Please move the same folders that you used on the AWS machine to their respective destinations.
7. Run `python gui.py` to open the GUI to view predictions. Choose your matched seal by clicking "Check" on the corresponding seal or "No Match"
if you think there is no match. Save your result by clicking "Save", you can view a summary of your choice by clicking "Save & View Summary".
When you are absolutely certain with your choices, you can click "Save & Merge" to merge your probe to your database. This is not a reversible action, 
you might have to manually move the photos if you change your mind.
Your updated databased is the one in ./data/processed.
8. When done, close the virtual environment with `deactivate`

# Additional Info:
1. SealNet: https://github.com/zbirenbaum/SealFaceRecognition


