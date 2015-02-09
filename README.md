HipFM-Server
============

Post "now playing" track from last.fm to HipChat room in a HipChat Server instance.


## Command line usage

node server.js [last.fm API Key] [last.fm User] [HipChat Key] [HipChat Room] [HipChat Name] [HipChat Server] 

```shell
node server.js THISISMYLASTFMAPIKEY blueflagmusic HIPCHATKEY "My Room" "HipFM" hipchat.example.com
```

## Config file (hipfm.json) usage

```shell
node server.json -f
```

** Example **

```json
{
    "hipchat": {
        "server": "https://hipchat.example.com",
        "key": "11111111111111111111111111111111",
        "room": "Music"
    },
    "lastfm": {
        "users": [
            {
                "displayName": "User1Music",
                "username": "lastfm_username1",
                "key": ""
            },
            {
                "displayName": "User2Music",
                "username": "lastfm_user2",
                "key": "11111111111111111111111111111111"
            }
        ]
    }
}
```


* **last.fm API Key**: Get one here [Last.fm Web Services](http://www.last.fm/api/account/create)
* **last.fm User**: The user's playlist you want to follow (eg. [blueflagmusic](http://ws.audioscrobbler.com/1.0/user/blueflagmusic/recenttracks.rss))
* **HipChat Server**: The URL for your HipChat server API.
* **HipChat Key**: Either an Admin or Notification key. Get one here [https://hipchat.com/admin/api](https://hipchat.com/admin/api)
* **HipChat Room**: The room you want to post to. Must be created in HipChat first.
* **HipChat Name**: _(Optional)_ Name to display in HipChat (usually where the username goes).


Special Thanks
==============

Special thanks to [BlueFlag][https://github.com/blueflag], who wrote the initial [HipFM][https://github.com/blueflag/HipFM].  This project is a _very_ slight modification of BlueFlag's original work.
