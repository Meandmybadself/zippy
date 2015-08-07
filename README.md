# zippy
Filesystem-based zipcode-to-location web service for cities in the United States.

## Why?
You need to quickly get a latitude/longitude from a zipcode and don't want to set up a database / Cray supercomputer.

## Example usage 
[Location data for Niles, Ohio, 44446](https://zippy.permanentrecord.io/44446)

## Return data
A valid zipcode should return the following data:

* _latitude_ - Precise to four places.
* _longitude_ - Precised to four places.
* _zipcode_ - The zipcode (am debating if this silly or not)
* _msa_ - Marketing Statistic Area
* _dma_ - Direct Marketing Area
* _state_ - The state, as two-letters.

## Instructions for usage via hosted-service
Access data via this hosted service (but heavily consider against using it for production sites where it's good practice to not trust a foreign web service).

https://zippy.permanentrecord.io/ZIPCODE

## Instructions for usage via self-hosting
### Apache
* Clone project from github (https://github.com/Meandmybadself/zippy)
* Configure .htaccess to add CORS headers or remove .json extensions from request _like a gentleman_.

## Questions I would ask
* Can I save this many files (41,789) to the file system?
	* You shouldn't have a problem ext2 & ext3 file systems might be a bit slow. [Stackoverflow post on the subject](http://stackoverflow.com/a/466596/412643) 
* How accurate is this data?
	* As roughly accurate as free data usually is.