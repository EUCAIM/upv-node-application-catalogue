# trace4harmonization

## Description
Harmonize numerical values extracted from medical images (e.g. acquired with different models of image-acquisition system)

## Usage
Example of run for the **calibration stage** (training):
`jobman submit -i trace4harmonization -- -- OPERATION=calibrate WORKDIR=~/persistent-home/trace4harmonization TRAINING_CALIBRATION_FILENAME=harmonization_training.csv`

And an example of run for the **application stage**:
`jobman submit -i trace4harmonization -- -- OPERATION=apply WORKDIR=~/persistent-home/trace4harmonization CLASSIFICATION_APPLY_FILENAME=file_to_be_harmonized.csv`

Note the "WORKDIR" (working directory) path have to be within the persistent-home, which is shared between all desktops and jobs created by the user, 
in that working directory should be any input file (the calibration file and the file to be harmonized in the "application stage"). 

## Authors
DeepTrace Technologies s.r.l.

## Contact info
https://github.com/deeptracetech/Trace4Harmonization-Docker/issues

## URL
Public dockerfile repository:
https://github.com/deeptracetech/Trace4Harmonization-Docker

## License
The code in the dockerfile repository is distributed under the AGPL-v3.0 license attached. 
PLEASE NOTICE that the license refers ONLY TO THE CODE publicly visible there in the repository AND NOT IN ANY WAY to the attached asset files in the release section, 
that are not generated from code packaging and are included in the image. 
In particular, the software Trace4Harmonization.exe, for which you can find more details here: https://openebench.bsc.es/tool/trace4harmonization, 
is distributed only with a commercial license and YOU SHOULD CONTACT DeepTrace Technologies s.r.l. for its usage and redistribution.
