********************************************************************************************
All software should be run by double clicking it or through the terminal (use python to run)
********************************************************************************************
*****NOTE***********************************************************************************************************************
All processed files are present in their associated directories. If you wish to run my software make sure to delete all files in the following directories:
	3D Maps
	3D Maps(resized)
	Do Nothing
********************************************************************************************************************************

Explination of directories:
	Do Nothing - Contains the latitudes, longitudes, and matrices when my software does not solve for any missing data
	3D Maps - Contains the latitudes, longitudes, and matrices when my software solves for any missing data
	Drone Data - Contains the point clouds generated by pix4D and any test point clouds
	Analysis - contains the baseline mesurements used in my analysis
	3D Maps(resized) - Contains the latitudes, longitudes, and matrices after they have been resized

Files intended to be run:
	ProcPointCloud.py
	analysis.py
	resize.py	(Only used when graphing multiple terrain maps in MATLAB)

Files that were used for debugging (can be run):
	doNothing.py
	noneTest.py
	maxMinTest.py

Data Guide:
	point cloud storage: 	./Drone Data/sample(x).xyz
	processed data storage: ./3D Maps/3D Latitudes(y).txt
				./3D Maps/3D Longitudes(y).txt
				./3D Maps/3D Matrix(y).txt

My software will prompt for each of these at some point. The iteration is the y in the example above.
	 Point Cloud        Iteration     Inches/Pixel
	sample(5).xyz   ---->   0    ---->   .24
	sample(0).xyz   ---->   1    ---->   .32
	sample(1).xyz   ---->   2    ---->   .4
	sample(2).xyz   ---->   3    ---->   .48
	sample(3).xyz   ---->   4    ---->   .56

Answers to possible prompts (refer above):
	Enter the inches per pixel: Inches/Pixel
	Enter file name: Point Cloud
	Enter file iteration: Iteration

Order in which files are intended to run:
	Before analysis.py is run all five of the above stated test files should be processed by ProcPointCloud.py, unless you only want to see the analysis of one file.
	(O) - represents an optional file to run
	ProcPointCloud.py ---> resize.py ---> maxMinTest.py(O) ---> noneTest.py(O) ---> analysis.py
	doNothing.py(O) ---> maxMinTest.py(O) ---> noneTest.py(O)


