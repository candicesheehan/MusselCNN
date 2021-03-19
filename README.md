# Mussel_CNN

This repo uses RetinaNet for object detection in microscope imagery (specifically, parasitic cysts in a mosaics of bivalves). Note that the scripts have been generalized to accommodate other uses beyond parasites. All operations are currently written to be executed in Google Colab, though they can also be run on a local machine if you skip the first section and point to necessary input files. To run in Colab, if you are viewing in GitHub or locally in Jupyter Notebook, click the "launch in Google Colab" button at the top to launch the script in Google Colab instead. If you clone or fork this project be sure to update those pointer buttons in the markdown to link to your new version.

You will need: \
(1) a web browser \
(2) a [google drive](https://www.google.com/intl/en/drive/) account (you can create and use a "dummy" account if you want) \
(3) a file unzipper (such as [7-Zip](https://www.7-zip.org/), [WinRAR](https://www.win-rar.com/) or [WinZip](https://www.winzip.com/)) \
\
Each script pulls in files from a Google Drive folder <b> that you must specify, if using your own data, </b> and spits out files that will download in your browser, usually as a zip archive that you must extract. When you move on to the next script <b> you must put these files into a publicly shared Google Drive folder and point that script to that folder</b>. It doesn't have to be the same drive folder every time, but makes sense to do it that way, because many files get used multiple times in the workflow.

Pay attention to the markdown at the start of each script, which specifies what's needed to run the script. The markdown at the end of each script explains what's ahead, and how the outputs fit together in the next steps.

<b>Note that each of these scripts will prompt you to allow Google permissions to use Google Cloud SDK.</b>  You will need to grant permissions and paste a code into an input box at the start of each script when pulling files from Google Drive. After that, the code should run smoothly without requiring any further input (though some variables require customization if using your own dataset).

<b>Estimated time for each step:</b>

<b>[Step 1](https://colab.research.google.com/github/gl7176/GreySealCNN/blob/master/1_orthomosaic_to_tiles.ipynb):</b> < 5 minutes + time to download mosaic tiles (varies by mosaic size) \
<b>[Step 2](https://colab.research.google.com/github/gl7176/GreySealCNN/blob/master/2_VIA_annotations.ipynb):</b> Multiple hours (varies depending on size of mosiac, number of annotations, ease of detecting annotations, familiarity with VIA) \
<b>[Step 3](https://colab.research.google.com/github/gl7176/GreySealCNN/blob/master/3_VIA_to_RetinaNet_subsetted.ipynb):</b> < 1 minute \
<b>[Step 4](https://colab.research.google.com/github/gl7176/GreySealCNN/blob/master/4_CNN_setup_training_testing.ipynb):</b> < 10 minutes in demo-mode (ranges much longer, depending on how long you train the model) \
<b>[Step 5](https://colab.research.google.com/github/gl7176/GreySealCNN/blob/master/5_export_outputs.ipynb):</b> < 1 minute 

You'll also spend a little time handling files between steps.

To start this workflow, create a google drive folder (it does not need to be your personal google account, you may want to create a new account to store these data). Create a folder on that drive and upload the orthomosaic you're working with (the default folder/mosaic is https://drive.google.com/drive/folders/1wuAONrdYYNylyb_ZV2hpd-SrYjk-UXty). Make sure the drive is shared publicly (so "anyone with the link can view") and be sure to point to your working folder's link in each script.

Note: workflow is designed for working on one mosaic at a time, but inputs and outputs can be merged/separated between steps to process multi-mosaic datasets.

If you encounter any errors or have any questions, please reach out to Candice Sheehan at candice.k.sheehan@gmail.com
