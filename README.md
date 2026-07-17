# us-map-weather
This program experiements with the weather APIs provided by Open-Meteo in order to display current weather conditions for US major cities on a US map, which is provided by Simplemaps.com and uses the Lambert Azimuthal Equal-Area (LAEA) projection:

### Mathematical Formulation

The forward transformation equations for the Lambert Azimuthal Equal-Area projection are:

$$

x = k \cdot \cos(\phi) \sin(\lambda - \lambda_0)

$$

$$

y = k \cdot \left[ \cos(\phi_0) \sin(\phi) - \sin(\phi_0) \cos(\phi) \cos(\lambda - \lambda_0) \right]

$$

Where the scale factor $k$ is:

$$

k = \sqrt{\frac{2}{1 + \sin(\phi_0) \sin(\phi) + \cos(\phi_0) \cos(\phi) \cos(\lambda - \lambda_0)}}

$$

**Parameters:**
* $x, y$: Projected planar coordinates.
* $k$: Scale factor variable.
* $\phi, \lambda$: Point coordinates.
* $\phi_0, \lambda_0$: Center coordinates.