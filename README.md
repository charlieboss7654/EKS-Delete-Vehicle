
### EKS Vehicle Deletion Script

This FiveM script provides two essential vehicle cleanup commands:

* `/dv` — Deletes your current vehicle or a nearby unoccupied vehicle.
* `/dvall` — Deletes all unoccupied vehicles server-wide with a 20-second warning. Restricted to users with proper ACE permissions.

## Features

* Delete the vehicle you're in or a nearby empty one
* Admins can trigger a 20-second global deletion warning
* Prevents deletion of vehicles with players or AI inside
* Uses `ox_lib` for modern progress bars and notifications

## Files

* `fxmanifest.lua` – Resource manifest file
* `client.lua` – Handles `/dv`, progress bar, and clientside deletion
* `server.lua` – Handles permission checks and global broadcast of deletion

## Installation

1. Install and start `ox_lib` first:
  https://overextended.dev/ox_lib
(only if you do not already have it)

2. Add this resource to your `resources` folder and `server.cfg`:
   ensure ox_lib
   ensure EKS_DV

3. Set up ACE permissions for `/dvall`:
   add_ace group.admin command.dvall allow
   Or for a specific user:
   add_principal identifier.steam:yoursteamhex group.admin
   
## Usage

* `/dv`
  Deletes your current vehicle, or a nearby empty one if you're on foot.

* `/dvall`
  Displays a 20-second countdown using a progress bar. After that, all **unoccupied** vehicles are deleted. Only accessible by users with `command.dvall` permission.

## Notes

* Occupied vehicles (with players or NPCs) are never deleted.
* Works reliably across all players by using clientside deletion logic after the server broadcasts the trigger.
* Designed for performance and safety on live servers.

support can be found in the discord

https://discord.gg/busQ9w6dqa


**DO NOT CHANGE THE NAME OF THE MAIN FILE - DO NOT CHANGE ANYTHING IN THE FXMANIFEST, OR THE SCRIPT WILL NOT WORK**
