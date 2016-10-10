# razberry-gettingstarted
Example code for using [Razberry](http://razberry.z-wave.me/) to control Z-Wave devices for building IoT solutions.

## API
### Authentication
It is possible to use simple authentication to perform the requests with no extra authentication request, e.g.:

```
http://username:password@ip:8083/anyurl
```

### List devices
To see all the connected devices use the following URL:
```
http://ip:8083/ZAutomation/api/v1/devices
```

### Commands
To send a command to a particular device use the following URL:
```
http://ip:8083/ZAutomation/api/v1/devices/ZWayVDev_zway_{ID}/command/on
```

ID is the full identifier, e.g. ZwayVDev_zway_2-0-48-1 – dash [-] separated _node_, _instance_, _command class_, and _scale_.

Example:
```
http://ip:8083/ZAutomation/api/v1/devices/ZWayVDev_zway_2-0-37
http://ip:8083/ZAutomation/api/v1/devices/ZWayVDev_zway_2-0-37/command/on
```

### Get information from a device
#### High level API
```
http://ip:8083/ZAutomation/api/v1/devices/ZWayVDev_zway_2-0-49-4
```

#### Low level API
Get values:
```
http://ip:8083/ZWaveAPI/Run/devices[2].instances[0].commandClasses[49].data[4].val.value
```
Set values:
```
http://ip:8083/ZWaveAPI/Run/devices[2].instances[0].commandClasses[37].Set(255)
```

## Resources
* General info about Razberry: http://razberry.z-wave.me/
* Installation: http://razberry.z-wave.me/index.php?id=24
* Quick doc: http://razberry.z-wave.me/docs/RaZberryEndUserManual20.pdf
* Full doc: http://razberry.z-wave.me/docs/zwayDev.pdf
