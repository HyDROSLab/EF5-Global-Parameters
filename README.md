[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4694759.svg)](https://doi.org/10.5281/zenodo.4694759)

# EF5-Global-Parameters
Parameters for CREST and kinematic wave models in EF5 for the globe.

Set of parameters based on methodology and globally available geospatial datasets described in:

Clark, R.A., Flamig, Z.L., Vergara, H., Hong, Y., Gourley, J.J., Mandl, D.J., Frye, S., Handy, M. and Patterson, M., 2017. Hydrological modeling and capacity building in the Republic of Namibia. Bulletin of the American Meteorological Society, 98(8), pp.1697-1715.

|Parameter|Units|Description|
|-|-|-|
|DEM|meters|**basic/dem.tif** - Digital Elevation Model used for slope calculation and inundation mapping.|
|FAM|pixels|**basic/flowacc.tif** - Flow accumulation map. Indicates size of upstream drainage in number of pixels.|
|DDM|unitless|**basic/flowdir.tif** - Flow direction map. Coding scheme that dictates downstream connectivity between pixels. Uses ESRI's 8-direction coding scheme (1-128).|
|PWM|millimeters|**parameters/soil_param_wm_5km_global.tif** - Maximum Soil Water Capacity, calculated based on estimated effective porosity (see Rawls et al., 1983 at https://doi.org/10.1061/(ASCE)0733-9429(1983)109:1(62)) and soil depth-to-bedrock.|
|PB|unitless|**parameters/soil_param_b_5km_global.tif** - Exponent of power function fitted to matric potential to measures of moisture retention as described in Cosby et al. 1984 ([doi:10.1029/WR020i006p00682](https://doi.org/10.1029/WR020i006p00682)).|
|PFC|millimeters per hour|**parameters/soil_param_fc_5km_global.tif** - Soil's saturated hydraulic conductivity based on soil texture (see Rawls et al., 1983 at https://doi.org/10.1061/(ASCE)0733-9429(1983)109:1(62)).|
|PIM|percentage|**parameters/imperv_5km_global.tif** - Percent of impervious area within each pixel based on satellite estimates of built-up areas. Used to compute direct runoff (no infiltration).|
|alpha0|$\frac{seconds^{3/5}}{meters^{1/5}}$|**parameters/Alpha0_World_5km_geo_v0.tif** - Coefficient in Manning's equation applied to wide-rectangular channel, where beta0 = 0.6. Computed based on terrain's slope and Manning's roughness coefficient - $\alpha_0=\left(\frac{n}{\sqrt{S_0}}\right)^{\beta_0}$.|
|alpha|-|**parameters/Alpha_World_5km_geo_v0.tif** - Coefficient of Kinematic Wave's momentum equation applied to a prismatic channel - $A=\alpha Q^{\beta}$. Computed based on fit to power function relating cross-sectional area and flow rates data in metric units following Vergara et al. (2016) (https://doi.org/10.1016/j.jhydrol.2016.06.011).|
|beta|-|**parameters/Beta_World_5km_geo_v0.tif** - Exponent of Kinematic Wave's momentum equation applied to a prismatic channel - $A=\alpha Q^{\beta}$. Computed based on fit to power function relating cross-sectional area and flow rates data in metric units following Vergara et al. (2016) (https://doi.org/10.1016/j.jhydrol.2016.06.011).|

Update 02/07/2026:

Added Units METADATA to GeoTIFF files. Included table above for quick reference as well.

Update 06/06/2023:

EF5 control file, FAO PET grids, and basic DEM and derivatives included to enable out-of-box simulation capabilities. No rainfall data are included.

Update 04/15/2021:

Parameters at 5-km pixel resolution as presented in Clark et al. (2017).

## Data format and other details

Files are GeoTIFFs using EPSG:4326. Values are Float32, which is required by EF5. No Data vaues has been set to -9999.
