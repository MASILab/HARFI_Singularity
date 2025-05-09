# HARFI_Singularity

The pre-built Singularity container can be downloaded at https://zenodo.org/records/15376547

Usuage:

`singularity run 
  --bind [INPUT_DIR]:/input,[OUTPUT_DIR]:/output 
  [PATH_TO_HARFI_SIF_FILE] 
  [R] [DISCRETE] [TR] [N] 
  [FMRI_IMAGE_NAME] [BRAIN_MASK_NAME] [REFERENCE_IMAGE_NAME] [OUTPUT_NAME]`

The parameters are: 

R: radius of integration (voxels)

DISCRETE: discrete steps in integration 

TR: repetition Time (in seconds)

N: number of volumes to remove from beginning

Users need to provide FMRI_IMAGE_NAME, BRAIN_MASK_NAME, and REFERENCE_IMAGE_NAME in the INPUT_DIR. The output files, OUTPUT_NAME.mat (MATLAB data storing all parameters and results), OUTPUT_NAME.nii.gz (correlation maps), and OUTPUT_NAME_SH_even4.nii.gz (FODs), will be saved to the OUTPUT_DIR.
