# mammography-density-segmenter

## Description
Dense tissue segmentation.

## Usage
Two arguments are required:
 - `-p <input_dicom file>`
 - `-o <output_dir>`

Example of usage:
`jobman submit -i mammography-density-segmenter -r small-gpu -- -p ~/datasets/630ee013.../12826.../12826.../1.3.46....2.dcm -o ~/persistent-home/mammography-density-segmenter`

Note the output directory path should be any within the persistent-home, which is shared between all desktops and jobs created by the user, 
otherwise the results will be lost after the end of the job. 

## Authors
ITI

## Contact info
??

## URL
Private\* dockerfile repository:
https://github.com/dsilveira29/image_batch_Dense_Tissue_Segmentation  
\* You will see error 404 if you don't have permissions to access.

## License
None
