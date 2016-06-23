# razberry-gettingstarted
Example code for using Razberry to control Z-Wave devices for builing IoT solutions

## API
### Authentication
It is possible to use simple authentication to perform the requests with no extra authentication request, e.g. ```http://admin:Senseloop1@ip:8083/anyurl```.

### List devices
To see all the devices connected use the following URL: ```http://ip:8083/ZAutomation/api/v1/devices```.

### Commands
To send a command to a particular device use the following URL: ```http://ip:8083/ZAutomation/api/v1/devices/ZWayVDev_zway_{ID}/command/on```.

## Resources
* General info about Razberry: http://razberry.z-wave.me/
* Installation: http://razberry.z-wave.me/index.php?id=24
* Quick doc: http://razberry.z-wave.me/docs/RaZberryEndUserManual20.pdf 
* Full doc: http://razberry.z-wave.me/docs/zwayDev.pdf

