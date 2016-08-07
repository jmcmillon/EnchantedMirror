# Module: Compliments

The `compliments` module is one of the default modules of the EnchantedMirror. This module displays a random compliment.

## Using the module

To use this module, add it to the modules array in the `config/config.js` file:

```javascript
modules: [
    {
        module: 'compliments',
        position: 'lower_third',    // This can be any of the regions.
                                    // Best results in one of the middle regions like: lower_third
        config: {
            // The config property is optional.
            // If no config is set, an example calendar is shown.
            // See 'Configuration options' for more information.
        }
    }
]
```

## Configuration options

The following properties can be configured:

Option           | Description
---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
`updateInterval` | How often does the compliment have to change? (Milliseconds)<br><br>
**Possible values:** `1000` - `86400000`<br>
**Default value:** `30000` (30 seconds)
`fadeSpeed`      | Speed of the update animation. (Milliseconds)<br><br>
**Possible values:**`0` - `5000`<br>
**Default value:** `4000` (4 seconds)
`compliments`    | The list of compliments.<br><br>
**Possible values:** An object with three arrays: `morning`, `afternoon` and`evening`. See _compliment configuration_ below.<br>
**Default value:** See _compliment configuration_ below.

### Compliment configuration

The `compliments` property contains an object with three arrays: `morning`, `afternoon` and`evening`. Based on the time of the day, the compliments will be picked out of one of these arrays. The arrays contain one or multiple compliments.

#### Default value:

```javascript
config: {
    compliments: {
        morning: [
            'Good morning, handsome!',
            'Enjoy your day!',
            'How was your sleep?'
        ],
        afternoon: [
            'Hello, beauty!',
            'You look sexy!',
            'Looking good today!'
        ],
        evening: [
            'Wow, you look hot!',
            'You look nice!',
            'Hi, sexy!'
        ]
    }
}
```
