This set-up assumes precipitation data from IMERG in this folder. The control file block is:

[PrecipForcing IMERGE]
TYPE=TIF
UNIT=mm/30u
FREQ=30u
LOC=Precip/
NAME=IMERG.YYYYMMDD_HHUU00.3B-HHR-E.MS.MRG.3IMERG.V06B.30minAccum.tif

If a different rainfall product/dataset is used, then make the appropriate changes in the block in the control file, or create a new "PrecipForcing" block for your product/dataset.
