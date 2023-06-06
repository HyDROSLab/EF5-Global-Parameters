[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4694759.svg)](https://doi.org/10.5281/zenodo.4694759)

# EF5-Global-Parameters
Parameters for CREST and kinematic wave models in EF5 for the globe.

Set of parameters based on methodology and globally available geospatial datasets described in:

Clark, R.A., Flamig, Z.L., Vergara, H., Hong, Y., Gourley, J.J., Mandl, D.J., Frye, S., Handy, M. and Patterson, M., 2017. Hydrological modeling and capacity building in the Republic of Namibia. Bulletin of the American Meteorological Society, 98(8), pp.1697-1715.

Update 04/15/2021:

Parameters at 5-km pixel resolution as presented in Clark et al. (2017).

Update 06/06/2023:

EF5 control file, FAO PET grids, and basic DEM and derivatives included to enable out-of-box simulation capabilities. No rainfall data are included.

## Data format and other details

Files are GeoTIFFs using EPSG:4326. Values are Float32, which is required by EF5. No Data vaues has been set to -9999.
