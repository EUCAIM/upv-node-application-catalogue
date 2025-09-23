# extract-info-dataset

## Description
Extract information from a dataset.

## Usage

`jobman submit -i extract-info-dataset -- <DATASET_DIR>  [other optional parameters]`

The first parameter `<DATASET_DIR>` is required and is the path to the directory that contains the dataset.

Other optional parameters:
```
    -v, --verbose         Show all info on screen about the creation process of the dictionaries. 
    -f, --manufacturers   Show all manufacturers in the dataset.
    -b, --bodyparts       Show all body parts included in the dataset.
    -s, --numberseries    Show number of series.
```

Example:
```
jobman submit -i extract-info-dataset -- ~/datasets/87f3be56-4725-45c3-9baa-d338de530f73 -s -f -b -v
```

## Authors
I3M-UPV

## Contact info
https://github.com/EUCAIM/extract-info-dataset/issues

## URL
Public dockerfile repository:
https://github.com/EUCAIM/extract-info-dataset/

## License
https://github.com/EUCAIM/extract-info-dataset/blob/8a63e83d8e50337ce3c41417154872af5e84c433/LICENSE
