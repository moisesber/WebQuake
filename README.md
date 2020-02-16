# Docker WebQuake

Docker WebQuake is a Docker version of the the WebQuake port made by [Triangl3](https://github.com/Triang3l) and can be found [here](https://github.com/Triang3l/WebQuake).
**WebQuake** is an HTML5 WebGL port of the game Quake by id Software.


[Online demo by SpiritQuaddicted](http://quaddicted.com/forum/viewtopic.php?pid=438).

# Installing and running

Follow these steps to install Docker WebQuake:

1. Configure your docker environment. (https://www.docker.com/products/docker-desktop)
2. Build the docker image:

```console
docker build -t quake-web .
```

3. Run the docker image mounting the `id1` folder accordingly:

```console
docker run -it -p 8080:80 -v <path_to_your_id1_folder>:/usr/local/apache2/htdocs/client/id1/ quake-web
```

4. (Optional) If you have any mods or extra content, repeat 3 with the extra folders:

```console
docker run -it -p 8080:80 -v <path_to_your_mod_folder>:/usr/local/apache2/htdocs/client/mod_name quake-web
```

To launch WebQuake, go to (http://localhost:8080/client/index.htm) in your browser.

To launch the game with command line arguments, add ? after the address and put the arguments after it in the same format as you use for Quake.

For Scourge of Armagon, add `-hipnotic` command line argument. For Dissolution of Eternity, add `-rogue`.

To launch mods, copy the mod folder into the folder containing index.htm and add `-game MOD_NAME_HERE` command line argument. Ensure step 6 of the installing instructions for the mod folder.

To use browser hotkeys (such as F5, Ctrl+T and Ctrl+W), click the address bar, and when you're done, click the game.

# Playing multiplayer

If you want to join a multiplayer game, do one of the following steps, go to Multiplayer menu in the main menu, type the IP in "Join game at" field and press Enter, or type `connect ws://ip:port` in the console.

You can also play WebQuake games in a native Quake (not QuakeWorld) client such as WinQuake or GLQuake. Choose TCP/IP in the Join Game menu.

You cannot join multiplayer games if the client is installed on https:// protocol, however.

