# AnberPorts-Joystick
Emulated keyboard / mouse / joystick for Anbernic rg351p / rg351m / rg351v

# Howto
Launch with `sudo ./oga_controls` or add current user to uinput via udev rule to avoid using sudo.

If you append application as argument to launch command, you can quit by using Start + Select like so:

`sudo ./oga_controls Application &`

This will `pgrep -f Application  | xargs kill -9` when pressing Start + Select.

# /etc/udev/rules.d
```
SUBSYSTEM=="misc", KERNEL=="uinput", MODE="0660", GROUP="uinput"
```

## Controls
gamecontrollerdb.txt, this file can be edited to suit any game port if not able to edit in game settings.

`Blood example:`
```
# quit
back = esc
start = enter
a = enter
b = a
x = z
y = space
l1 = [
l2 = x
l3 = tab
r1 = ;
r2 = leftctrl
r3 = leftshift
up = up
down = down
left = a
right = d
left_analog_up = up
left_analog_down = down
left_analog_left = ,
left_analog_right = .
right_analog_up = pageup
right_analog_down = pagedown
right_analog_left = left
right_analog_right = right
deadzone_y = 2100
deadzone_x = 1900
```

Furthermore mouse control can be enabled with the following:
```
left_analog_up = mouse_movement_up
left_analog_down = mouse_movement_down
left_analog_left = mouse_movement_left
left_analog_right = mouse_movement_right

right_analog_up = mouse_movement_up
right_analog_down = mouse_movement_down
right_analog_left = mouse_movement_left
right_analog_right = mouse_movement_right
```

Support the project
---

[![Donate](https://github.com/krishenriksen/AnberPorts/raw/master/donate.png)](https://www.paypal.me/krishenriksendk)
[![Patreon](https://github.com/krishenriksen/AnberPorts/raw/master/patreon.png)](https://www.patreon.com/bePatron?u=54003740)
[![Sponsor](https://github.com/krishenriksen/AnberPorts/raw/master/sponsor.png)](https://github.com/sponsors/krishenriksen)
