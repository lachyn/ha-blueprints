# DHW Control with Legionella Protection

This blueprint allows you to control Domestic Hot Water (DHW) temperature based on Day/Night schedules for Weekdays and Weekends. It also includes a weekly Legionella protection cycle.

## Features

- 🚿 **DHW Control**: Supports `climate` or `water_heater` entities.
- 📅 **Day/Night Schedule**: Separate start/end times for Weekdays and Weekends.
- 🦠 **Legionella Protection**: Weekly cycle to raise temperature for protection.
- 🔔 **Notifications**: Sends notifications on mode changes and Legionella cycle (optional).

## Installation

Click the button below to import this blueprint into your Home Assistant instance:

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint URL pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Flachyn%2Fha-blueprints%2Fblob%2Fmain%2Fdhw_control.yaml)

## Configuration

### Inputs

| Input | Description | Default |
|-------|-------------|---------|
| **DHW Entity** | The entity to control (`climate` or `water_heater`). | Required |
| **Day (Comfort) Temperature** | Target temperature during active hours. | `50°C` |
| **Night (Eco) Temperature** | Target temperature during inactive hours. | `40°C` |
| **Weekday Day Start** | Time when Day mode starts on weekdays. | `06:00` |
| **Weekday Day End** | Time when Day mode ends on weekdays. | `22:00` |
| **Weekend Day Start** | Time when Day mode starts on weekends. | `07:00` |
| **Weekend Day End** | Time when Day mode ends on weekends. | `23:00` |
| **Enable Legionella Protection** | Enable the weekly anti-legionella cycle. | `true` |
| **Legionella Temperature** | Target temperature for the Legionella cycle. | `60°C` |
| **Legionella Day** | Day of the week to run the Legionella cycle. | `Sunday` |
| **Legionella Start Time** | Time to start the Legionella cycle. | `04:00` |
| **Legionella Duration** | How long to maintain the Legionella temperature. | `1 hour` |
| **Enable Notifications** | Send notifications when mode changes. | `true` |

## Requirements

- A working Home Assistant installation.
- A configured `climate` or `water_heater` entity.

## Author

[lachyn](https://github.com/lachyn)
