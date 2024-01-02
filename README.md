# File Copy Utility
A python script for ArcGIS folder copying 

## Requirements:
- a number of folders in a directory are given with some naming like this `S2A_MSIL2A_20190601T074611_N0212_R135_T36LTK_20190601T111243.SAFE`
- For each folder in the top directory:
  - extract the name before the second date, eg) `LTK`, extract the month from the folder name
  - make two directories in each folder with name: `Month_Name_bands` (eg `June_LTK_bands`) and `Month_Name_resampled` (eg `June_LTK_resampled`)
  - To `Month_Name_bands` copy from `GRANULE` -> sub folder -> `IMG_DATA` -> `R20m` -> `B05 to B12`
  - To `Month_Name_bands` copy from `GRANULE` -> sub folder -> `IMG_DATA` -> `R60m` -> `B01 + B09`
  - Has a default mode `--default` but also offers the ability to customise what is copied

## Usage

You will need python 3.6 and above (lower than 3.6 will give an error about `f''` f-strings) installed on your system and added to your environment variables. To run the script, open `cmd` in the folder where the script is and type

`python file-copy --mode=default --root="your path here"`

Replacing `your path here` with the path to where your folders beginning `S2A_` are located. eg) `C:/Users/MyUser/FolderWithS2AFolders` 

You can type `python file-copy --help` for details on script arguments
