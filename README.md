# Logger

A filebased logging plugin, for [Godot](https://godotengine.org/) game engine.

## Setup

Assuming you have this plugin installed into Godot.

> Need help installing a plugin? Try [HERE](https://docs.godotengine.org/en/stable/tutorials/plugins/editor/installing_plugins.html)

From there simply active the plugin, then add a Logger node to your scene or create a new Logger instance via code.

```gdscript
var Log

func _ready():
    Log = Logger.new()
    # Don't forget to configure the Logger node too!
```

## Configuration

If you've used the Godot editor to create the Logger node then you can simply use the inspector.

| Value | Type | Description |
|------------|------------|-----------|
| Persist Debug | Bool | Does the log file get cleared on start of the scene/instance/use of logging? |
| File Dir | String | The path to store the log file. |
| File Name | String | The name of the log file. (See Format Template section for help on what {dt} means) |
| File Name Time Format | String | Defines {dt} in File Name. (See Format Template section for help on what {dt} means) |
| Formatting | String | The format of all logging lines (I.E. `09-01-2020 01:00:00 PM DEBUG A Debug Statement.`) |
| Time Format | String | The format of {dt} for in Formatting. |
| Debug | Bool | Do we log debug statements/calls. |
| Info | Bool | Do we log info statements/calls. |
| Warn | Bool | Do we log warn/warning statements/calls. |
| error | Bool | Do we log error statements/calls. |
| Crit | Bool | Do we log crit/critical statements/calls. |

## Format Template

This allows fully customised log files.

| Value | Description |
|-------|-------------|
| dt    | Typically used to indicate date time stamp. (Once defined)
| level | The logging level (DEBUG, INFO, WARN, ERROR, CRITICAL)
| msg   | The message passed to one of the logging statements/calls. 
| month | The current month as 2 digits. (I.E. January is `01`)
| day   | The current day as 2 digits. (I.E. First day of the month is `01`)
| year | The current year as 4 digits. (I.E. 2000 is `2000`)
| 24hour | The current hour as 24 hour (Millitary time), as 2 digits. (I.E. 1 PM is `13`)
| 12hour | The current hour as 12 hour (Use `ampm` to add the AM/PM), as 2 digits. (I.E. 1 PM is `01`)
| min | The current minute as 2 digits. (I.E. 5 minutes is `05`)
| sec | The current second as 2 digits. (I.E. 2 seconds is `02`)
| ampm | A string describing if it's AM or PM. (Only use with `12hour`)

> dt is used to abreviate date time in File Name, and Formatting.

## Contact me

Please leave an issue/bug report if anything goes wrong or you come up with some other suggestions/feature requests.

## Credits

* `Logging.png` was based off of [Node](https://github.com/godotengine/godot/blob/master/editor/icons/Node.svg) from the Godot game engine.
