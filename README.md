# OctoPrint-FilamentRedux

Based on the Octoprint-Filament plugin by MoonshineSG (https://github.com/MoonshineSG/Octoprint-Filament), and the Octoprint-FilamentReloaded plugin by kontakt, this modification restores the ability to query for the filament status.

Future developments are planned to include multiple filament sensors, pop-ups, pre-print validation and custom filament run-out scripting.

## Setup

Install via the bundled [Plugin Manager](https://github.com/foosel/OctoPrint/wiki/Plugin:-Plugin-Manager)
or manually using this URL:

    https://github.com/borrillis/Octoprint-Filament-Redux/archive/master.zip

Using this plugin requires a filament sensor. The code is set to use the Raspberry Pi's internal Pull-Up resistors, so the switch should be between your detection pin and a ground pin.

## API
An API is available to check the filament sensor status via a GET method to `/plugin/filamentredux/status` which returns a JSON

- `{status: "-1"}` if the sensor is not setup
- `{status: "0"}` if the sensor is OFF (filament not present)
- `{status: "1"}` if the sensor is ON (filament present)
