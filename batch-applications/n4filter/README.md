# n4filter

## Description
The tool is designed to perform image pre-processing to reduce the bias field effect, improving the quality of the image. Two main functionalities are offered: (1) Apply N4 filter to image/images (either with the default parameters values or with parameters values defined by the user) (2) Find the optimal configuration of the N4 filter for specific image/images by measuring the Full Width at Half Maximum (FWHM) of the periprostatic fat distribution.

## Usage

`jobman submit -i n4filter -- <INPUT_DIR> <OUTPUT_DIR> [-h] [-N] [-t T] [-s S] [-f F] [-I I] [-m] [-c] [-P]`

The two mandatory arguments:  
 - INPUT_DIR: the path that contains the folders with the original DICOM image of each patient
 - OUTPUT_DIR: the path where the N4 filtered image of each patient will be saved

Other available arguments: 
 - -h, --help: show this help message and exit 
 - -N, --n4filter: Performs N4 bias field correction method 
 - -t T, --threshold T: Convergence threshold 
 - -s S, --shrinkFactor S: Shrink factor 
 - -f F, --fittingLevel F: Fitting level 
 - -I I, --Iterations I: Number of iterations 
 - -m, --masks: If specified, the N4 algorithm uses masks 
 - -c, --custom-masks: Path with whole gland masks. If specified, custom masks are used. If not specified, the masks will be extracted automatically by the algorithm 
 - -P, --pipeline: Apply the whole pipeline to identify the optimal N4 configuration

The two main options are:
 - Apply N4 filter to image/images, by specifying -N
 - Find the optimal N4 configuration, by specifying -P
 
Example:  
  ```
    jobman submit -i n4filter -- ~/datasets/87f3be56-4725-45c3-9baa-d338de530f73/ ~/persistent-home/n4filter-results/ -N
  ```
Note the output directory path should be any within the persistent-home, which is shared between all desktops and jobs created by the user, 
otherwise the results will be lost after the end of the job.

## Authors
Foundation for Research and Technology-Hellas (FORTH)

## Contact info
dovrou@ics.forth.gr

## URL
Quick start guide:
https://cbml-gitlab.ics.forth.gr/adovrou/n4biasfilter/-/tree/eucaim?ref_type=heads

Documentation:
https://docs.google.com/document/d/1Hl6WfsCJ3JLdZvDNixVvF9QWTUOxoH90/edit

Public dockerfile repository:
https://cbml-gitlab.ics.forth.gr/adovrou/n4biasfilter/-/tree/eucaim

## License
https://cbml-gitlab.ics.forth.gr/adovrou/n4biasfilter/-/blob/eucaim/LICENSE

