# How do I change the screens?

Currently, the screens depend on a mechanical turk in order to actually change the content. However, the single source of truth is this repository.

1. Find what screen you'd like to change. Eg. `FRONT-01`
2. Locate the configuration file for that screen. Configuration files are located in [screens/](screens/).
3. Edit the content of this configuration file by either opening up your favourite editor or through Github UI.
4. Change the value of `content`.

#### Example

This is how the file looks like before you edit:

```JSON
{
  "schedule": {
    "Value": [
      {
        "items": [
          {
            "autoReload": 0,
            "cachePolicy": "forever",
            "content": "http://rtd.opm.jbv.no:8080/web_client/std?station=OSL",
            "repetition": "-",
            "zone": "fs",
            "zoneHeight": "30%",
            "zoneWidth": "30%",
            "zoneXOffset": "0",
            "zoneYOffset": "0"
          }
        ],
        "name": "FRONT-01"
      }
    ]
  }
}
```

This is after:


```JSON
{
  "schedule": {
    "Value": [
      {
        "items": [
          {
            "autoReload": 0,
            "cachePolicy": "forever",
            "content": "http://vg.no",
            "repetition": "-",
            "zone": "fs",
            "zoneHeight": "30%",
            "zoneWidth": "30%",
            "zoneXOffset": "0",
            "zoneYOffset": "0"
          }
        ],
        "name": "FRONT-01"
      }
    ]
  }
}
```

Notice the `http://vg.no`. Make sure that it is still a valid JSON file by checking that the URL is still surounded `"`.

5. Open a Pull Request with your changes.

@cobraz will review the changes (and make sure that the configuration file is still valid) and upload it to the screen
you'd like to change once it's accepted.
