---
title: "Installing Minecraft Plugins"
description: "Guide for installing and configuring plugins on a Minecraft server. Support for PaperMC, CraftBukkit, Mohist, and other popular cores."
head:
  - - meta
    - name: keywords
      content: minecraft, plugins, bukkit, spigot, paper, mohist, minecraft plugins
  - - meta
    - property: og:title 
      content: "Minecraft - Installing Plugins"
  - - meta
    - property: og:description
      content: "Guide for installing and configuring plugins on a Minecraft server. Support for PaperMC, CraftBukkit, Mohist, and other popular cores."
---



# <MinecraftLogo>Installing Plugins</MinecraftLogo>

A quick guide to installing plugins on your Minecraft server.

***

::: tip
Plugins require compatible server software (core) to function, such as [PaperMC](https://papermc.io/), [CraftBukkit](https://getbukkit.org/), [Mohist](https://mohistmc.com/), or [Fabric](https://fabricmc.net/). For instructions on installing these server types, see our [custom server software guide](/games/minecraft/software).
:::

Each plugin is designed for a particular Minecraft core. For instance, Paper plugins will not work with CraftBukkit, and the reverse is also true. Always check that any plugin you download is compatible with your server’s core and game version.

To ensure stability and avoid broken or malicious plugins, download plugins from official or trusted sources:
- [Hangar (PaperMC)](https://hangar.papermc.io/)
- [Bukkit Plugins (CraftBukkit)](https://dev.bukkit.org/bukkit-plugins)
- [Spigot Resources (Spigot)](https://www.spigotmc.org/resources/categories/spigot.4/)
- [Modrinth (multi-platform)](https://modrinth.com/plugins)

### Downloading Plugins

In this tutorial, we'll use [Modrinth](https://modrinth.com/plugins) as an example because of its simplicity and the wide range of plugins available.

Filtering by server type (platform/core) and game version is highly recommended to ensure compatibility.

![plugin filters](/images/games/minecraft/plugins/filters.png){data-zoomable}

Once you've found your desired plugin, open its page and click the "Download" button.

![plugin download button](/images/games/minecraft/plugins/plugin-download-button.png){data-zoomable}

A popup will prompt you to pick the version and core (platform). Choose the ones that match your server setup.

![plugin download popup](/images/games/minecraft/plugins/plugin-download-popup.png){data-zoomable}

### Installing the Plugin on the Server

After downloading the plugin, access your server's file manager and open the `plugins` directory. Upload the downloaded `.jar` file here (for example, `worldedit-bukkit-7.3.6.jar`).

![plugin upload to the server](/images/games/minecraft/plugins/file-upload.png){data-zoomable}

### Testing That the Plugin Works

Restart your Minecraft server to load the new plugin. Once the server is running, type the `plugins` command in the server console. If you see your newly added plugin listed, the installation was successful!

![plugin working](/images/games/minecraft/plugins/plugin-working.png){data-zoomable}
