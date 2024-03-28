# DLC-MotorBox

DLC User Guide for Tracking and Analysis: MotorBox

Video Preparation
1.	Before analyzing videos through DeepLabCut, the videos must be prepped, or cropped. To do this, you must open the anaconda prompt.
2.	Once in the prompt, you must activate the deeplabcut environment. Type: activate DEEPLABCUT 
3.	You will know that the environment is activated when you see (base) change to (DEEPLABCUT) at the front of the path. After, type this onto the prompt: python -m deeplabcut (Assuming you have created your DLC environment).
4.	This will launch a gui. Select load project and upload the MotorBox-Maureen-2023-05-23 config.yaml project file.
5.	Next, on the top bar, go to the last tab “Video editor(*)”. Change the settings to: Video height of 1000 and a Trim of 1 to 120 sec. Next, click “select videos” [make sure you have selected MP4] and upload the recorded GoPro footage. Once the video is selected, click “Crop” and a popup window will appear. 
6.	Click and drag your mouse over the base of the MotorBox. Once you do, a red box will appear specifying the area you want to keep, while all that is not inside of the red box will be cropped. Be sure to make the crop box fall inside of the thick borders on the base of the MotorBox as shown below.   
7.	The anaconda prompt window will specify the progress of cropping for the video. Once you see the teal colors on the prompt, the video is done, and you can move on to the next video. Cropped videos will appear in the same folder as the original video. 
8.	Once all videos have been cropped, you can now analyze them through deeplabcut.

Video Tracking through deeplabcut
1.	To analyze videos, you can apply 2 methods. You can analyze videos through the gui or scripts. If you would like to analyze videos through the gui, go back to step 5 and instead of the “video editor(*)” tab, go to the “Analyze videos” tab and select all settings seen below. Once you have changed all settings to match, click select videos and select either 1 or multiple videos to analyze, then click “Analyze Videos” on the bottom right.
2.	If you prefer to use my script, then open the file: DLC Workflow.ipynb. Change the config_path to the path where you have saved: MotorBox-Maureen-2023-05-23 config.yaml
3.	Scroll to the section that is titled ”Analyze videos, create .csv, create skeleton” and change the file path to where your videos are stored (change ”your file path”). 
4.	Run all.
   a.	Select a python environment that has all required packages or create your own
 
Analysis
1.	DLC above has provided the X, Y coordinates of each limb, now you will have this analyzed using Python and Pandas packages. If you check back to the folder of your data, you should have 8 created files for each analyzed video. DO NOT DISCARD THESE CREATED FILES. 
   a.	You will be using the el_filtered.csv files. NOT THE _el.csv FILES.
2.	Open the MotorBox.ipynb file using VS Code. Next, IN THE SAME FOLDER AS THE MotorBox.ipynb file, add all el_filtered.csv files of all of your videos. 
3.	Go to the "Collect Data Files" section and run this to collect the file names of the .el_filtered.csv files in the folder. 
4. Scroll to the bottom of the script and find the to_excel function. This function will create an excel sheet with all of the calculations from your data. In between the quotations, this will be the name of your file and you can change it to whatever you prefer BUT DO NOT REMOVE THE .xlsx at the end of the name.
5.	The final step is to go to the top left and select the Run All option
6.	 Once you do, you will be prompted to select the environment, remember to create an environment with all the necessary packages.
8.	Your excel sheet will be found in the same folder as your MotorBox.ipynb file
