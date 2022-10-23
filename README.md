# VTT_File_Cleaner

This is based on the fantastic work done by the webvtt-py , a Python module for reading/writing WebVTT caption files.

It also features caption segmentation useful when captioning HLS videos and is available at https://pypi.org/project/webvtt-py/ 

Unfortunately I found that the webvtt-py library does not cope well when timestamps are in format of 0:0:0.0 vs 00:00:00.000 and gives an error 

Therefore I made this simple ipynb file that reformats the timestamps of VTT (transcript file) that is usually produced together with video recordings from tools 
such as Microsoft Teams and uses the WEBVTT library to extract relevant information (start/finish times, speaker name, transcribed text) into a dataframe 

The sample input file "SampleWorkshopTranscript.VTT" in this git repo came from a MS Teams meeting recording 

The simple panda dataframe that is then exported into an output file : "cleaned_table.xlsx which is then used as input for a PBIX file to show case 
how these transcripts can be used to run a simple sentiment and key phrase word analysis thru Microsoft PowerBI's Text Analysis features

This github repo is accompanied by 
A Youtube video https://youtu.be/iZ0pOSL8JZw
A Medium article https://zhijingeu.medium.com/building-a-meeting-transcript-exploratory-text-analysis-tool-with-python-power-bi-860f4238dce6
