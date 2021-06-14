# nation_bennys
- FIVEM Mechanic Menu
![alt text](https://i.imgur.com/wpr9IVh.png)
- Info: a lot of people are requesting this, so here is my version, this is actually made few months ago now i am sharing it.

- All Events needed are converted from VRPEX to ESX (TESTED v1 final)

- if you found a bug i will fixed it when i have a time:

- Added Society Money Option at config: Mechanic can earn money from the script to their society money.
- Money being used is either bank or

- Dependencies: Esx Datastore, Mysql, esx_society, progressbar
also take note: this script uses rgb on paint and neons.
if your esx does not support it, it wont save the colors of paint.

heres what you can do to make the paint save.

edit functions.lua at es_extended/client/functions.lua

Find:

ESX.Game.GetVehicleProperties = function(vehicle)

add: after color2

rgb = table.pack(GetVehicleCustomPrimaryColour(vehicle)),
rgb2 = table.pack(GetVehicleCustomSecondaryColour(vehicle)),


Find:

ESX.Game.SetVehicleProperties = function(vehicle, props)

add : after props.dirtlevel

if props.rgb then SetVehicleCustomPrimaryColour(vehicle, props.rgb[1], props.rgb[2], props.rgb[3]) end
if props.rgb2 then SetVehicleCustomSecondaryColour(vehicle, props.rgb[1], props.rgb[2], props.rgb[3]) end
