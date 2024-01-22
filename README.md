## KickrBikeGearsS4ZMod

An implementation of of a [sauce4zwift](https://www.sauce.llc/products/sauce4zwift/) "mod" that will provide Wahoo Kickr Bike Gear information 
to Sauce for Zwift.

At this time (Jan 19, 2024), you must be running version 1.0.11-alpha (or later) version of [sauce4zwift](https://www.sauce.llc/products/sauce4zwift/)
for this mod to work.

You will also need [KickrBikeInterceptor](https://github.com/pwfulghum/KickrBikeInterceptor-Releases) for the actual data to be injected into [sauce4zwift](https://www.sauce.llc/products/sauce4zwift/).
You can have programming/building your own Lilygo ESP32 IOT device as discussed on [zwiftforrum](https://forums.zwift.com/t/wahoo-kickr-bike-external-gear-display/597907) or just use the PC based software solution.

This mod simply lets you access the data once it is there.

## This mod will act on this injected data (into the "self" athelete)
```
["self", { "gears" : {"chainring": "<frontgear>", "cassette": "<reargear>" }}]
```

NOTE: If you are using https://github.com/gazhay/kickrbike_display (or similar) running on an ESP32 dongle as mentioned on [zwift forums](https://forums.zwift.com/t/wahoo-kickr-bike-external-gear-display/597907) to get your gear data into sauce, you will have to change either the sketch or contents/add_a_data_field.js to match.

## Basics

A Sauce for Zwift "Mod" is a directory placed in `~/Documents/SauceMods`.  NOTE: "Documents"
may be called "My Documents" on some platforms.  For first time mod users they should create
an empty **SauceMods** folder first.  Then each Mod will be a sub directory in there such as...
```
Documents
└── SauceMods
    ├── KickBikeGearsS4ZMod
    └── super_duper_theme_mod
```

To install this mod, just place the extracted files from the "release" zip in the directory structure as shown above and restart 
Sauce For Zwift.    You will now see new data type available when you add data to a window.

![Opps - You should See an image](https://github.com/pwfulghum/KickrBikeGearsS4ZMod/blob/main/NewDataCategory.jpg?raw=true)
