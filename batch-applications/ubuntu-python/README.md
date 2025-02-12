# ubuntu-python

## Description
A basic image with ubuntu 22.04, python 3.10.6 and a few other useful tools/libraries like pandas, pydicom.  
The tag `latest-cuda` and those ending with `cuda11` include also the CUDA toolkit/libraries.

The tags `latest-cuda` and `latest` always point to the last version with and without CUDA libraries.
If you leave the tag empty then the `latest` will be used.

## Usage
Put the command you want to execute after the `--` in the `jobman submit` command.  
Examples:  
  `jobman submit -i ubuntu-python -- ls -l persistent-home/`  
  `jobman submit -i ubuntu-python:latest-cuda -r small-gpu -- nvidia-smi`  
  `jobman submit -i ubuntu-python -- python3 application-examples/list-all-dcm-files.py datasets/dc0dbf84-ebcf-470a-8b45-ef682ddafc6c`  
  `jobman submit -i ubuntu-python -- python3 application-examples/filter-series-by-orientation.py datasets/dc0dbf84-ebcf-470a-8b45-ef682ddafc6c Z_SAGITTAL persistent-home/index-prostate-sagittal.json`

## Authors
I3M-UPV

## Contact info
https://github.com/EUCAIM/upv-node-workstation-images/issues

## URL
Public dockerfile repository:
https://github.com/EUCAIM/upv-node-workstation-images/tree/main/ubuntu-python

## License
https://github.com/EUCAIM/upv-node-workstation-images/blob/87a57cff6b79d8c85dc65a3f01a27e3f967d22a4/LICENSE
