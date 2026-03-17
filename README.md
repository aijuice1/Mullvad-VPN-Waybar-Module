# Mullvad-VPN-Waybar-Module
##Mullvad VPN Waybar Module

## Dependencies
'''bash
Mullvad-vpn or Mullvad-vpn-cli
'''

## Getting Started
What you will need. Files available above.
1) Mullvad.sh script
2) Mullvad Module.json
3) Mullvad Config Module.css
4) Mullvad Config Module Location.conf

## Installation

Place your Mullvad.sh file wherever you want it to pull from. I personally put my Mullvad.sh in ~/.config/scripts foler that I created

Find your waybar config. Typically ~/.config/waybar folder



Add the script to your waybar.json file. Make sure to place your path to wherever you put your Mullvad.sh file


Add "custom/mullvad", to your waybar.conf file 

Check Mullvad Config Module Location file for more details


Add the Mullvad Config Module.css wherever your waybar .css file is. Typically in the same foler as your waybar.conf and waybar.json file in ~./config/waybar


Lastly, kill and restart your waybar to see the changes.


killall waybar && waybar &


You can change the colors, modeule location, size, font, etc to fit yours. Feel Free to change the icon as well. Nerdfonts.com is a great place to look.


I created this code from tons of different github projects I saw and put what I liked together. Good luck people. Sorry for the bad format. I am new to posting to github and will fix in the future.
