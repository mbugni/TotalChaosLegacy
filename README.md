<img align="right" width="155" src="retro_banner.png" alt="TotalChaos Retro Banner" />

# Total Chaos Legacy - Flatpak Build

###  Retro Edition v1.40 on GZDoom Legacy v3.8.2

This project contains files to build [Total Chaos - Retro Edition](https://www.moddb.com/mods/total-chaos/downloads/total-chaos-directors-cut-retro-edition-140) as a Flatpak app.

Retro Edition has reduced texture resolution and poly-counts for improved performance. Save files from other versions of Total Chaos are not compatible.

The game runs using the [GZDoom Legacy v3.8.2](https://zdoom.org/) engine to ensure more compatibility with old computers. It requires OpenGL 2.1 or later and at least 1GB of free RAM.

This project is based on [com.moddb.TotalChaos](https://github.com/flathub/com.moddb.TotalChaos).

## How To Build and Run the Game

### 1 - Prepare the environment
Ensure you have the following commands installed on your system:
- `git`
- `flatpak`
- `flatpak-builder`

Ensure you have the `flathub` repo enabled:

```shell
$ flatpak remote-add --user --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

Clone this project on your computer:

```shell
$ git clone https://github.com/mbugni/TotalChaosLegacy.git
```

### 2 - Build and install the app
From the project directory run the command:

```shell
$ flatpak-builder --user --verbose --install --install-deps-from=flathub --force-clean build \
  io.github.mbugni.TotalChaosLegacy.yaml
```

See [flatpak documentation](https://docs.flatpak.org/) for more info.

The build can take a while (20 minutes or more), it depends on your machine performances. It compile and install the app, making it available for all users in your system.

*NOTE:* if you want to install the app system wide, remove the `--user` option and the use `sudo` command.

### 3 - Run the game
You can run the game launching it from your favorite desktop, or manually by using the `flatpak` command:

```shell
$ flatpak run io.github.mbugni.TotalChaosLegacy
```

#### Tips for gaming
- Skip the intro by pressing the `E` button

#### GZDoom options
 GZDoom engine defaults are in file `~/.var/app/io.github.mbugni.TotalChaosLegacy/.config/gzdoom/gzdoom.ini`

|  Option       | Descritipn                                              |
|---------------|---------------------------------------------------------|
| `vid_adapter` | Sets the primary display (when using multiple monitors) |
