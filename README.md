# Night Mode Heating Control (OTGateway)

This blueprint allows you to automatically set a lower heating temperature at a specified time (night mode) and restore the original temperature at another time (day mode). It is designed for use with OpenTherm Gateway (OTGateway) but works with any `climate` entity.

## Features

- 🌙 **Night Mode**: Automatically lowers the temperature at night to save energy.
- ☀️ **Day Mode**: Automatically restores the comfort temperature in the morning.
- 📅 **Flexible Scheduling**: Supports different schedules for weekdays (Mon-Fri) and weekends (Sat-Sun).
- 🔔 **Notifications**: Sends notifications when the mode changes.

## Installation

Click the button below to import this blueprint into your Home Assistant instance:

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint URL pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Flachyn%2Fha-blueprints%2Fblob%2Fmain%2Fnight_mode_heating.yaml)

## Configuration

### Inputs

| Input | Description | Default |
|-------|-------------|---------|
| **Climate Entity** | The climate entity to control (e.g., `climate.opentherm_heating`). | Required |
| **Use Different Schedule for Different Days** | Enable to set different times for weekdays and weekends. | `false` |
| **Night Mode Start Time (Default)** | Time when night mode activates (if weekday schedule is disabled). | `23:00` |
| **Night Mode End Time (Default)** | Time when night mode deactivates (if weekday schedule is disabled). | `06:00` |
| **Weekday Night Start Time** | Time when night mode activates on weekdays (Mon-Fri). | `23:30` |
| **Weekday Night End Time** | Time when night mode deactivates on weekdays (Mon-Fri). | `05:30` |
| **Weekend Night Start Time** | Time when night mode activates on weekends (Sat-Sun). | `00:00` |
| **Weekend Night End Time** | Time when night mode deactivates on weekends (Sat-Sun). | `08:00` |
| **Night Temperature** | Target temperature for night mode. | `16°C` |
| **Day Temperature** | Target temperature for day mode. | `21°C` |

## Requirements

- A working Home Assistant installation.
- A configured `climate` entity (e.g., via MQTT, OpenTherm Gateway, or other integration).

## Author

[lachyn](https://github.com/lachyn)
