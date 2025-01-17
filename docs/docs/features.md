## OSD Setup
### WTRTI (Built-in)

This type of OSD is enabled by default, if it is not, you can enable it at:  
 **Settings -> OSD -> OSD Type -> WTRTI**  

Start the game. In the graphics settings, switch to **Fullscreen window** mode.  

![#](images/wt_fullscreen_mode.png)

That's it. Go to the "Test Flight" for testing.  


!!! tip
    To change the font, see [Changing the fonts](features.md/#wtrti).  
!!! warning
    Make sure that **"Hardware Accelerated GPU Scheduling" (HAGS)** is **disabled**.  
    See [Troubleshooting section](troubleshooting.md#the-overlay-is-stutteringfreezing-or-data-is-not-updating-when-alt-tab-to-the-game)

## Tooltips
Most controls have tooltips. Simply hover over them and a tooltip will appear.
![#](images/wtrti_tooltip.png)


## Groups
Groups controls how the indicators are displayed, their position and layout.  

![#](images/wtrti_groups.png)

You can also move a group using keyboard.   
Select a group in the main window, **ALT-TAB** to the game and press:  
**SHIFT + ALT + ARROWS**

### Multi-value layout
This option allows you to change the layout of neighboring multi-value indicators.

- **List**:  ENGN1, ENGN2, ENGN3, RPM1, RPM2, RMP3, etc
- **Shuffle**:  ENGN1, RPM1, ENGN2, RPM2, ENGN3, RPM3, etc


## Colors and Color Schemes
WTRTI works with color slots.  
You can **Add**, **Delete** and **Set** a color slots (maximum 32).  
![#](images/wtrti_color_editor.png)

By default, all indicators have the same color scheme (All).  
![#](images/wtrti_color_scheme_all.png)

You can change the color for every part of an indicator: Name, Value, Units.  
If you want to set up colors for a specific indicator, enable the **Separate** Color scheme, then you can change the colors in the indicators settings.  
![#](images/wtrti_color_scheme_separate.png)
![#](images/wtrti_indic_colors.png)


## Profiles
### Vehicle Profiles
Profiles saved with vehicle name, e.g. bf-109f-4, mig_29_9_13, spitfire_mk1.  
To save the profile, go to Test Flight and ALT-TAB in the main window, and press the Save button.  

### Auto-loading profiles
Priorities:  
1. Vehicle Profiles.  
2. By a Type: Flighter, Strike, etc.  
3. By a Propulsion: Prop, Jet.  

### Hotkeys
Loading profiles by Hotkeys (Profiles slots). Only works while in the battle. Max. 5 slots.
![#](images/wtrti_hotkey_profiles.png)

## Indicators
**Double-click** on the indicator in the main window to open the indicator settings window.

### General
#### Alert
Alerts, allows you to specify a range of values within which you will be alerted visually (color change) or sound playback when the value exceeds the threshold.  

![#](images/wtrti_alert_1.png)
![#](images/wtrti_alert_2.png)
![#](images/wtrti_alert_3.png)
!!! tip
    For sound alerts, it's recommended that you use a 'relative paths' for audio files by selecting them from the WTRTI root directory, e.g. **Sounds** folder.  
    This makes the profile more portable, so you can share it with others.
![#](images/wtrti_alert_4.png)


### Advanced
#### In "State" list
This option allows you to place the final value of the indicator, after all postprocessing, into the "State" list (press **F2** in the main window).  
Enable the option and specify the **key** that will be in this list.

![#](images/wtrti_indic_advanced_in_state.png)

All In-State indicators are calculated in a separate order, from top to bottom, before Non-In-State indicators.  
The indicator with an in-state key that depends on another in-state indicator (chained), must be placed below that indicator in the main list, otherwise it will be **N/A**.  


## Logging the data to a CSV file
1. Go to Test Flight.
2. Activate **Benchmark mode** with **CTRL + ALT + B** (by default).
3. To start logging press **X** key.
4. Press again **X** to stop.

All these hotkeys you can rebind in the **Settings -> Hotkeys tab**.  
You can change the logging interval in milliseconds, at  
**Settings -> General tab -> Benchmark mode -> Logging Interval**  
Generated .CSV files are located in the **Logs** folder.   

In the OSD, the benchmark information is positioned in the last group, so if you want to place it in a specific location, create an empty group and move it as you wish.  

![#](images/wtrti_bench_mode.png)
![#](images/wtrti_logs_folder.png)

You can toggle `Logging` for a specific indicator in the **Indicator's Settings**, by default it's enabled.
![#](images/wtrti_indic_logging.png)

## Game Chat
Game chat - allows you to see, copy or translate messages of the in-game chat.  
You can enable the auto-logging feature, **Game Chat** -> **Settings** -> **Logging**, this will automatically write into a log file for every game session.  
Log files are located in the **Logs** folder.  
![#](images/wtrti_game_chat.png)


## Battle Log
Shows recorded battle events, with ability Logging to file.  
You can enable the auto-logging feature, **Battle Log** -> **Settings** -> **Logging**, this will automatically write into a log file for every game session.  
Log files are located in the **Logs** folder.  
![#](images/wtrti_battle_log.png)


#### Highlights
Located at Battle Log -> Settings. Allows you to set a "keywords" to highlight certain words in battle log messages.  
![#](images/wtrti_battle_log_settings_window.png)


## VR
VR support is implemented with **SteamVR**.  

1. Install **SteamVR**.
2. Start WTRTI and enable **VR mode** (**Settings -> Advanced**). 
3. Click the **VR** button in the main window to display the **VR Settings**.

!!! warning
    If you have an **iGPU**, make sure you are using WTRTI on the discrete GPU (High performance):  
    <https://pureinfotech.com/set-gpu-app-windows-10/>

### SteamVR Controller Bindings support
Allows you to assign VR controller buttons to specific WTRTI actions.  
To make settings to be available in SteamVR, you need first go in a "Test Flight", then select WTRTI from the list of programs in the SteamVR's Controller Bindings window.  

### Hotkeys
- **CTRL + ALT + V** - toggles "HMD tracking" mode.
- **CTRL + ALT + Z** - toggles "Left controller tracking" mode.
- **CTRL + ALT + X** - toggles "Right controller tracking" mode.
- **CTRL + ALT + S** - saves the overlay's position and rotation from "tracking" modes to the no "tracking" mode.
- **SHIFT + ALT + R** - resets the overlay's position and rotation(x:0.0, y:0.0, z:-0.5).
- **SHIFT + ALT + LEFT/RIGHT** - moves the overlay along the X axis.
- **SHIFT + ALT + UP/DOWN** - moves the overlay along the Y axis.
- **SHIFT + ALT + PAGE UP/PAGE DOWN** - moves the overlay along the Z axis.
- **SHIFT + ALT + Q** - decrease the overlay's size.
- **SHIFT + ALT + E** - increase the overlay's size.


### Oculus users
To make the game run through SteamVR, you have to set the compatibility mode to Windows 7, for **aces.exe** in win32 and win64 folders.  
How-To:  
In the game root folder, open **win32** folder and find **aces.exe**, open its **Properties** and set **Compatibility mode** to Windows 7:  
![#](images/aces_properties.png)

Do the same for aces.exe in the win64 folder.  
It is also recommended to run the game through Steam.  


## Advanced
### RTSS OSD Setup
1. [Download](https://www.guru3d.com/files-details/rtss-rivatuner-statistics-server-download.html) and Install RTSS.
2. Start WTRTI.
3. **Settings -> OSD -> OSD Type -> RTSS**
![#](images/wtrti_rtss_mode.png)

!!! warning 
    RTSS **only** works with text-based indicators.  
    Also, RTSS only supports **ASCII** characters.

To change the font, see [Changing the fonts](features.md/#rtss).

### Gamescope Setup (Linux)
There are two ways to use gamescope:

##### Create a script:
```
#!/bin/bash
export PATH=$PATH:/path/to/WTRTI
./launcher &
WTRTI
```
Place it in the game root directory, where the launcher is, and run it with Gamescope:  
`gamescope ./run.sh`

##### From command line:
1. Start the game with Gamescope:  
   `gamescope ./launcher`
2. Launch WTRTI from another command line:  
   `GAMESCOPE_DISPLAY=:2 ./WTRTI`

!!! note
    **GAMESCOPE_DISPLAY** should be the name of the gamescope Xwayland server.  
    When you start the game with gamescope, you can see what name gamescope uses.  
    `wlserver: [xwayland/server.c:108] Starting Xwayland on :2`

!!! warning
    After playing, **first close WTRTI** and then the game!  
    Otherwise it will crash and you may lose your configuration.

### FM Mode
This mode contains additional indicators, that **only** works in "Test Flight":  

- Excess power, W
- Drag, kgf (lbf)
- Total mass, kg (lb)
- No fuel mass, kg (lb)
- Thrust to Weight ratio
- Critical G, % (in-battle approximate version)

To make these indicators to work, follow these steps:  

1. Open the game root folder.
2. Open **config.blk** file with text editor.
3. Find `debug` section
4. Emplace this line:
```
enableFMCommands:b=yes
```
![#](images/wt_config_debug_fm_mode.png)  
5. Save the file and Start/Restart the game.
6. Enable "FM mode" in **Settings -> Advanced**.


### Custom indicators
Open **Add** window (**+** button) -> **New** (or **RMB** on the indicators list).  
![!](images/wtrti_custom_indic_1.png)
![!](images/wtrti_custom_indic_2.png)

Use **State** window(press **F2** in the main window) to see which parameters are available.  
!!! warning
    Empty **State Key** - switches the indicator into "label" mode, which will only show OSD name and trigger an alerts.  

![!](images/wtrti_state.png)

#### Multiple values
Replacing numbers in the **State Key** with `%d`, allows reading multiple parameters (e.g. multiple engines) with the same key.  
Examples:  
**`RPM 1`** -> **`RPM %d`**  
**`manifold_pressure1`** -> **`manifold_pressure%d`**  

#### "Lua-script" option
Allows you write a custom value processing in Lua.  
Right after enabling this option and pressing OK, a template script will be created, you can find it at:  
**`Indicators/NAME/update.lua`**  

Also have a look at the [Lua API](lua-api.md) to see all the functions that are available.  

## OSD on a second screen
Simply switch "Window mode" (Settings->OSD) to "Windowed" and move the "WTRTI OSD" window to a second screen.
![#](images/wtrti_windowed_mode.png)

## Receive data from another PC or Console on the local network
Set another PC's **local** IP address in **Settings** -> **Network** -> **Address**:
!!! warning
    Leave **`8111`** port unchanged

![#](images/wtrti_network_ip.png)

## DCS World Setup
1. Copy-Paste the **DCS/Scripts/Export.lua** into  
   **`%USERPROFILE%/Saved Games/DCS/Scripts/`**  
   For **DCS Open Beta** use this directory:  
   **`%USERPROFILE%/Saved Games/DCS.openbeta/Scripts/`**
2. Start WTRTI, open **Settings -> Advanced tab -> Enable "TCP Listener"**.
3. Start the game.

### Multiplayer
##### Hosted server
Check if the server has these options in the DCS World multiplayer lobby window:

![#](images/dcs_mp_server_permissions.png)

##### Creating a Server
Click on **Advanced** and enable these options:

![#](images/dcs_mp_server_settings.png)


## Changing the fonts
### WTRTI
![#](images/wtrti_font_1.png)
![#](images/wtrti_font_2.png)

!!! tip
    You can use a custom font file.  
    Simply place a TTF file into **Fonts** folder and select it in Settings.

### RTSS
![#](images/rtss_font_1.png)
![#](images/rtss_font_2.png)

!!! tip
    In order to use custom font files, you will need to install them on your system.

