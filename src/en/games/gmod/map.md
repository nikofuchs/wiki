

# <GmodLogo>Changing The Startup Map</GmodLogo>

A quick guide to changing the default map on your Garry's Mod game server.

## Setting a Variable in Startup Parameters

Go to the management page of your server.

Navigate to the server startup parameters and find the "Map" parameter.

Enter the full name of the map, for example `gm_construct`.

![map in startup parameters](/images/games/gmod/map.png){data-zoomable}

Done! Now the server will load with this map every time it starts.

## Listing available maps on the server

If you are unsure which maps you have installed on the server, you can easily find out the full list (including Workshop addons) by using the `maps *` command through the Console.

![map list through a console command](/images/games/gmod/map_list.png){data-zoomable}

## Installing Maps from Steam Workshop

If you're using a map from the Steam Workshop, it's recommended to download it manually and upload it to the `/garrysmod/maps/` path, otherwise the server may not start.

You can do this using the [SteamWorkshopDownloader](https://steamworkshopdownloader.io) utility - go to the website, enter the link to the map page in the Steam Workshop, and download the files to your PC.

Extract the archive, go to the `maps` folder, and upload all files from it to the `/garrysmod/maps/` folder.

Set the map variable in the startup parameters the same way as described above.
