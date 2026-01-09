# ct_slice_thickness_harmonization

## Description
AI based tool that performs slice thickness harmonization in CT images.

## Usage

`jobman submit -i ct_slice_thickness_harmonization -- <INPUT_DIR> <OUTPUT_DIR> <MODEL> <INPUT_TYPE>`

The application accepts 4 parameters:
 - The path to the input directory with DICOM files.
 - The path to the output directory where harmonized DICOM files will be saved.
 - The model to use. Options: `lung`.
 - The type of input directory. Options: `series` (folder with .dcm files), `study` (folder containing series).
 
Example:  
  ```
    jobman submit -i ct_slice_thickness_harmonization -- ~/datasets/87f3be56-.../patient01/12826.../12826.../   \
                                                         ~/persistent-home/results_hamonization/ \
                                                         lung series
  ```
If you want to accelerate the process with a GPU, you must use the proper tag in the image (`:latest-cuda`) and add a resource flavor with GPU (for example `-r small-gpu`):  
  ```
    jobman submit -i ct_slice_thickness_harmonization:latest-cuda -r small-gpu -- ~/datasets/87f3be56-.../patient01/12826.../12826.../ \
                                                                                  ~/persistent-home/results_harmonization/ \
                                                                                  lung series
  ``` 
Note the output directory path should be any within the persistent-home, which is shared between all desktops and jobs created by the user, 
otherwise the results will be lost after the end of the job. 

## Authors
QUIBIM

## Contact info
xavierrafael@quibim.com
anajimenez@quibim.com

## URL
Private\* dockerfile repository:
https://github.com/EUCAIM/ct_slice_thickness_harmonization/tree/development
\* You will see error 404 if you don't have permissions to access.

## License
None
