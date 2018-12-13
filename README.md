## Installation

```
sudo npm uninstall -g homebridge-plex-sensors
npm install -g ayalon/homebridge-plex-sensors
```


## Settings
/var/homebridge/config.json auf Rasperry Pi

```
{
    "bridge": {
        "name": "Homebridge_ayalon",
        "username": "CC:22:3D:E3:CE:30",
        "port": 51826,
        "pin": "123-45-999"
    },
    "description": "Homebridge",
    "platforms": [
        {
            "platform": "homebridge-plex-sensors.Plex",
            "logSeenPlayersAndUsers": true,
            "debug": true,
            "sensors": [
                {
                    "name": "Movie Playing",
                    "customFilters": {
                        "event": "media.play"
                    },
                    "players": [
                        "ce23bce397ba97e1-com-plexapp-android"
                    ],
                    "users": [
                        "brainski"
                    ]
                },
                {
                    "name": "Movie pause",
                    "customFilters": {
                        "event": "media.pause"
                    },
                    "players": [
                        "ce23bce397ba97e1-com-plexapp-android"
                    ],
                    "users": [
                        "brainski"
                    ]
                },
                {
                    "name": "Movie resume",
                    "customFilters": {
                        "event": "media.resume"
                    },
                    "players": [
                        "ce23bce397ba97e1-com-plexapp-android"
                    ],
                    "users": [
                        "brainski"
                    ]
                },
                {
                    "name": "Movie stops",
                    "customFilters": {
                        "event": "media.stop"
                    },
                    "players": [
                        "ce23bce397ba97e1-com-plexapp-android"
                    ],
                    "users": [
                        "brainski"
                    ]
                }
            ]
        }
    ],
    "accessories": []
}
```