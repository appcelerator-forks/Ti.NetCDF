#Ti.NetCDF 

<img src="https://clas-pages.uncc.edu/techne/wp-content/uploads/sites/93/2013/12/netcdf.png" width=140 />

This the Titanium version of NetCDF. 

NetCDF is a set of software libraries and self-describing, machine-independent data formats that support the creation, access, and sharing of array-oriented scientific data.

##Usage

```javascript
var NetCDFModule = require("de.appwerft.netcdf");
var BUFRfn = "PAAH21EDZW101030.buf";
var foo = Ti.Filesystem.getFile( Ti.Filesystem.resourcesDirectory,"BUFS",BUFRfn);
var bar  = Ti.Filesystem.getFile( Ti.Filesystem.applicationDataDirectory,BUFRfn);
bar.write(foo.read());
var CDF = NetCDFModule.createNetCDF(bar);
console.log(CDF.getFileType());
```
List of available file types [are listed here](http://www.unidata.ucar.edu/software/thredds/current/netcdf-java/reference/formats/FileTypes.html)

##Data types
These are possible types of datas:
```javascript
CDFModule.DATATYPE_INT
CDFModule.DATATYPE_DOUBLE
CDFModule.DATATYPE_FLOAT
CDFModule.DATATYPE_CHAR
CDFModule.DATATYPE_STRING
CDFModule.DATATYPE_UINT8
CDFModule.DATATYPE_SHORT
```

```javascript
CDF.getCDL();
CDF.getDetailInfo();
CDF.getVariables()
 // ...
 
CDF.close();
```
