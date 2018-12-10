# wideq-homeassistant
An integration for European LG Washers with Home Assistant

This is based on the awesome work by [Adrian Sampson](https://github.com/sampsyo), [wkd8176](https://github.com/wkd8176) and everyone else who has contributed to the original project.

I just took the original, removed anything that wasn't about the LG Washer, and made it work with the EU models (Called TITAN2 in the API)


Currently everything is working except statuses for Turbo Wash and Crease Care (maybe the API doesn't push proper states for those?)

Also for some reason if an error occurs in the washer the script will crash (Instead of the API sending a proper error code it sends the actual context of the error code which i don't know how to detect)

Link to a dump of all options available on my Washer: https://hastebin.com/anovubolad.json


# Installation

To install this all you have to do is install the "Custom deps deployment" addon on hassio and use the following as the config

```
{
  "pypi": [
    "https://github.com/wkd8176/wideq/archive/master.zip#wideq"
  ],
  "apk": []
}
```

After you're done and started the addon (so it installs the dependencies) download my repo and replace anything if asked.

Documentation on how to use the actual API and how to create custom sensors is available here: https://github.com/wkd8176/hass-smartthinq/blob/master/README.md

# Contributing
If you'd like to contribute i'd suggest contributing directly to either [Adrian Sampson](https://github.com/sampsyo) repo or [wkd8176](https://github.com/wkd8176)

However if you'd like to fix something small (like the error codes) then feel free to open a pull request :)
