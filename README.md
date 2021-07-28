Instruction Manual
1.	Matlab Code(convert image to sketch)
•	Copy the location of the folder the contain the images needed to e convert in the variable called "location" in file (convert2Sketch.m).
•	Copy the location of the destination folder in the variable called "folder" file (convert2Sketch.m).
•	Run (convert2Sketch.m).

2.	Sketch Simplification Code(need at least 12 GB ram to run this)
•	Put the sketches needed to simplify into the "figs" folder.
•	If you need to resize the sketches run the "resize.py" file (the sketch size must be between 512*512 : 1024*1024).
•	Run "simplify.py" file and the result will show in the project directory.  

	needed libraries  
(CV2,os,PIL,tqdm,torch,torchvision,gc,argparse).

3.	Main Code(Colab Version)
    1)To Train
•	First you must upload your project in Google Drive and mount your drive in Colab.
•	Put all your sketches in (GP_project\Realistic_Face\datasets\w\train_A) folder and it's original images in (GP_project\Realistic_Face\datasets\w\train_B) folder.
•	Open the Colab note book,mount your drive,Install all dependency and libraries , change your directory to your project location in Google Drive , let the project sees your training directory.
•	Run the train.py script and change the parameters to match your needs.
2)To Test
•	put your test sketches in (GP_project\Realistic_Face\datasets\w\test_A) folder.
•	Run test.py script, select the number of sketches need to be test and the Results will be in (GP_project\Realistic_Face\results\w\test_40\images) folder. 


4.	Main Code(Local Version)(Need decent NVIDIA card to run and at least 12 GB ram)

1)To Train
•	Same steps as the Colab version but you don't need to upload anything.

2)To Test
•	Same steps as the Colab version.

3)To Edit
•	Upload the sketch 
•	Convert it 
•	start Editing the hair, mouth, skin, eyebrows and eyes by changing the values of the (Red, Green, Blue) Bars.

	needed libraries 
(CV2,numpy,argparse,os,torch,sys,functools, random,ntpath,time,fractions).



•	Train Line
(!python train.py --label_nc 0 --no_instance --name w --dataroot /content/drive/My\ Drive/pix2pixHD-colab/pix2pixHD/datasets/w --continue_train --display_freq 100 --checkpoints_dir /content/drive/My\ Drive/pix2pixHD-colab/pix2pixHD/checkpoints --which_epoch latest --save_epoch_freq 10 ) .


•	Test Line 
(!python test.py --dataroot /content/drive/My\ Drive/pix2pixHD-colab/pix2pixHD/datasets/w --name w --netG global --resize_or_crop none --label_nc 0 --no_instance --how_many 13 --checkpoints_dir ./trained --which_epoch 30 ) .

	Model is placed in (GP_project\Realistic_Face\trained\gp_male_femal) folder.



