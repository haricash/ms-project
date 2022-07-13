### Some tips

* Initialize maps(for maps of the data) or cube(spectrum, flux) or whatever you want to deal with
* Remember that you can initiate a cube and still access other data like *Maps* or *RSS* or *Image* using the getXXX method
* Check the maskbits of the `quality_flag` and `target_flag`. The first tells us about errors in collecting the data itself, whereas the second
indicates which sample the galaxy belongs to
* There is additional data available for each MaNGA galaxy object we load :
** NASA Sloan Atlas catalog (access via `cube.nsa`) tells us photometric and shape profile information
** DAPall catalog (access via `cube.dapall`) contains aggregate data for the observation (for the entire galaxy?)
** Value Added Catalogs (access via `cube.vacs`) are catalogs that SDSS members provide based on derived data. `cube.vacs` provides all the available VAC and we can just call the VAC using its name 
* We can also download and work with the data locally using the `download()` method after initiating an instance. We can also download lists of data by passing a list of plateids etc. into a `dowloadList` function
* We can work with spaxels, more on this in the documentation. Why do spaxel maps and cube maps give the same result?

### Bitmasks
These are representations of truth values in base 2 expressed in base 10. These correspond to some truth values for some conditions about the data. Refer to [this link](https://www.sdss.org/dr17/algorithms/bitmasks/)
