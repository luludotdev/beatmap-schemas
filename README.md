# Beatmap Schemas
_A collection of JSON Schemas for Beat Saber's Level Format_

# VSCode setup

It's possible to set [VSCode](https://code.visualstudio.com/) to format, validate, and display tooltip hints for beatmap files using this schema.

## Access the VSCode settings.json file:
In VSCode, click on `File -> Preferences -> Settings` then click on the `Open Settings (JSON)` button in the top right corner of the page.

## Add the following code to your VSCode settings.json file.
```json
"files.associations": {
    "*.dat": "json"
},
"json.schemas": [
    {
        "fileMatch": [
            "Easy*.dat",
            "Normal*.dat",
            "Hard*.dat",
            "Expert*.dat",
            "ExpertPlus*.dat"
        ],
        "url": "https://raw.githubusercontent.com/lolPants/beatmap-schemas/master/schemas/difficulty.schema.json"
    },
    {
        "fileMatch": [
            "info.dat"
        ],
        "url": "https://raw.githubusercontent.com/lolPants/beatmap-schemas/master/schemas/info.schema.json"
    }
]
```

## Open a beatmap in VSCode
Now when you open a beatmap file in VSCode, you can format the document using the default JSON formatting by pressing:
`Shift + Alt + F` on Windows
`Shift + Option + F` on Mac

If any invalid data is found, it should be noted with a squigly underline.

You can also see the descriptions for each property by hovering over the name of the property.
