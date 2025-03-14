# Eyeblink_events_analysis
These scripts are used to analyze the mouse eyeblink events within the trace interval through MATLAB. The source codes of Main1-Main4 are built by Dr Liu Kaiyuan and the source codes of Main5-Main7 and VideoAnalyzer are built by Dr Liu Zhen.
1. The input file should be a video of the mouse's closed-eye behavior captured from a fixed camera position. The video should have a stable frame rate to allow for frame-by-frame image comparison.
2. 
Usage Instructions:![image](https://github.com/user-attachments/assets/bc09b795-456a-48c2-898e-36d327df7f63)

	a. Place this folder in the MATLAB run path.
	b. Put the video file to be processed in the "dataset1" folder.
	c. Run main1_video_cut, and select the eye region in the image (it is recommended to choose a slightly larger range).
	d. Run main2_video_resize.
	e. Run main3_video_base_get, and select the image that is closest to the actual mouse eye image from the 9 clustered images provided.
	f. Run main4_1_video_run. After the run is completed, you will find a .mat file named final_convex_results in the newly created folder named cluster_results. The array in this file contains the frame-by-frame data of the mouse eye opening area for the video.
	g. Run VideoAnalyzer, click the select file button to choose the same video file, and click the set ROI button to select the ROI (it is recommended to choose the position of the LED light source as the ROI). Click the export data button to output the data, where the blueData variable represents the frame-by-frame data of the light source intensity changes.
	h. Open the results output by VideoAnalyzer and the corresponding final_convex_results file simultaneously, then run main5_1_restrict1_video_ana. Adjust the parameters of the findpeak function to filter the peaks of the light. You can adjust the range of the slot0.eye_area variable to control the time interval of the trace.
	i. Run main6_save_output and main7_1_output_read to obtain the duration of each mouse eye-closing event within the corresponding trace interval time period.
