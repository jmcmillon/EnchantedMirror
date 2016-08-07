# Module: Clock

The `clock` module is one of the default modules of the EnchantedMirror. This module displays the current date and time. The information will be updated realtime.

## Using the module

To use this module, add it to the modules array in the `config/config.js` file:

```javascript
modules: [
    {
        module: 'clock',
        position: 'top_left',    // This can be any of the regions.
        config: {
            // The config property is optional.
            // See 'Configuration options' for more information.
        }
    }
]
```

## Configuration options

The following properties can be configured:

Option            | Description
----------------- | -----------------------------------------------------------------------------------------------------------------------------------------------
`timeFormat`      | Use 12 or 24 hour format.<br><br>
**Possible values:** `12` or `24`<br>
**Default value:** uses value of _config.timeFormat_
`displaySeconds`  | Display seconds.<br><br>
**Possible values:** `true` or `false`<br>
**Default value:** `true`
`showPeriod`      | Show the period (am/pm) with 12 hour format.<br><br>
**Possible values:** `true` or `false`<br>
**Default value:** `true`
`showPeriodUpper` | Show the period (AM/PM) with 12 hour format as uppercase.<br><br>
**Possible values:** `true` or `false`<br>
**Default value:** `false`
`clockBold`       | Remove the colon and bold the minutes to make a more modern look.<br><br>
**Possible values:** `true` or `false`<br>
**Default value:** `false`
