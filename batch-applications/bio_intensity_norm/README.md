# bio_intensity_norm

## Description
The Biologically motivated normalization techniques tool is designed to perform normalization at the image-level. This normalization method aims to reduce the variability in the intensity values of the Magnetic Resonance (MR) prostate images due to different scanners, acquisition protocols and conditions, based on the intensity values of specific tissues. This tool implements three biologically-motivated intensity normalization techniques: 
(1) The fat-based normalization method.
(2) The muscle-based normalization method.
(3) The single tissue (fat or muscle) piece-wise normalization method.

## Usage

`jobman submit -i bio_intensity_norm -- <INPUT_DIR> <OUTPUT_DIR> [-h] [-f] [-m] [-p]`

The two mandatory arguments:
 - INPUT_DIR: the path that contains the folders with the original DICOM image of each patient. Only for the __piece-wise__ normalization techniques, the input path should contain 2 folders, i.e. "__train__" and "__test__" folder. The train folder contains the folders of the patients that are used for the training of the algorithm, while the test folder contains the folders of the patients whose images will be normalized.
 - OUTPUT_DIR: the path where the normalized image of each patient will be saved

Other available arguments:
 - -h, --help: show this help message and exit  
 - -f, --fat-based: If specified, the fat-based normalization algorithm is applied 
 - -m, --muscle-based: If specified, the muscle-based normalization algorithm is applied
 - -p, --piece-wise: If specified, the single tissue piece-wise normalization algorithm is applied, Default = fat tissue piece-wise

For instance, if the user wants to apply the single muscle tissue piece-wise normalization method, the arguments -p -m should be specified.
If the user specifies only the argument -p, then the fat tissue piece-wise normalization method will be applied by default.
 
Example:  
  ```
    jobman submit -i bio_intensity_norm -- ~/datasets/87f3be56-4725-45c3-9baa-d338de530f73/ ~/persistent-home/bio_intensity_norm-results/ -p
  ```
Note the output directory path should be any within the persistent-home, which is shared between all desktops and jobs created by the user, 
otherwise the results will be lost after the end of the job.

## Authors
Foundation for Research and Technology-Hellas (FORTH)

## Contact info
dovrou@ics.forth.gr

## URL
Public dockerfile repository:
https://cbml-gitlab.ics.forth.gr/adovrou/biointensitynorm/-/tree/eucaim

## License
https://cbml-gitlab.ics.forth.gr/adovrou/biointensitynorm/-/blob/eucaim/LICENSE

