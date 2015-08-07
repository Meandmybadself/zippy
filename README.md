# zippy
Filesystem-based zipcode-to-location web service.

## Why?
You need to quickly get a latitude/longitude from a zipcode and don't want to set up a database / Cray supercomputer.

## Example usage 
[Location data for Niles, Ohio, 44446](https://zippy.permanentrecord.io/44446)

## Instructions for usage via hosted-service
Access data via this hosted service (but heavily consider against using it for production sites where it's good practice to not trust a foreign web service).

https://zippy.permanentrecord.io/ZIPCODE

## Instructions for usage via self-hosting
### Apache
* Clone project from github
* Configure .htaccess to add CORS headers or remove .json extension