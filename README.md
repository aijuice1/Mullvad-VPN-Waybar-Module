# Mullvad-VPN-Waybar-Module
<img width="30" height="33" alt="image" src="https://github.com/user-attachments/assets/60a334e6-9401-4138-be53-0cc9b9675e3d" />
<img width="26" height="29" alt="image" src="https://github.com/user-attachments/assets/22adf7fb-37d3-49c5-8fa0-8094ef757d33" />

## Dependencies
```
Mullvad-vpn
#or
Mullvad-vpn-cli
```
Use your package manager for your Linux Distro

## Getting Started
What you will need. Files available above.
1) Mullvad.sh script
2) Mullvad Module.json
3) Mullvad Config Module.css
4) Mullvad Config Module Location.conf

## Installation

1) Place Mullvad.sh in folder where you want it to pull from. 
I personally use ~/.config/scripts to house my various scripts.
Make the script executable. Typically by using the command
```
cd /path/to/your/file
chmod +x filename.sh
```
For my recommended location this would be
```
cd ~/.config/scripts
chmod +x Mullvad.sh
```
2) Add the script to your waybar.json file. Make sure to place your path to wherever you put your Mullvad.sh file
Feel free to add your own custom icons. I used [nerdfonts](nerdfonts.com) for this portion
```
 // Mullvad
  "custom/mullvad": {
    "format": "{icon}",
    "exec": "~/your_path_to/mullvad.sh",
    "interval": 60,
    "return-type": "json",
    "on-click": "~/your_path_to//mullvad.sh toggle",
    "on-click-middle": "mullvad-vpn",
    "on-click-right": "~/your_path_to/mullvad.sh reconnect",
    "format-icons": {
      "connected": "🔒",
      "connecting": "⏳",
      "disconnected": "🔒",
    },
    "tooltip": true,
  },
```
3) Determine where Mullvad VPN Module will go in your waybar
Add "custom/mullvad", to your waybar.conf file. Typically located in ~/.config/waybar
Choose between Modules Left, Modules Center, or Modules Right"
Place only the "custom/mullvad" amongst where you want it in your waybar order
```
// Modules Right    
    "modules-right": [
        "custom/updates",
        "pulseaudio",
        "network",
        "custom/mullvad",
        "tray",
        "clock"
    ]
```
4)  Add the Mullvad Config Module.css wherever your waybar .css file is. Typically in the same foler as your waybar.conf and waybar.json file in ~./config/waybar
Feel free to change the colors under define color after the hashtag for the specific color you would like
You can also change the width, margins, fontsize, etc to fit your waybar aesthetic 
```
@define-color error #F96184;
@define-color warning #F6B016;
@define-color success #01D38F;

#custom-mullvad {
  min-width: 16px;
  margin: 0 10px;
}

#custom-mullvad.connecting {
  color: @warning;
  font-size: 16px;
  margin: 0px 10px 0px 0px;
}
#custom-mullvad.connected {
  color: @success;
  font-size: 16px;
  margin: 0px 10px 0px 0px;
}
#custom-mullvad.disconnected {
  font-size: 16px;
  margin: 0px 10px 0px 0px;
  color: @error;
}
```


5) Kill and restart your waybar

```
killall waybar && waybar &
```

## Notes

I created this code from tons of different github projects I saw and put what I liked together. Good luck people. Sorry for the bad format. I am new to posting to github and will fix in the future.

Thank you, Mullvad, the VPN I trust!

https://mullvad.net/en

This wouldn't be possible without!

https://github.com/Alexays/Waybar

## Project I pulled from
Thank you 
https://github.com/Jonathandah/mullvad-waybar-module

## Contribute or Leave Comments
Feel free to submit any issues or your own versions! 
Thank you, OpenSource Community!

