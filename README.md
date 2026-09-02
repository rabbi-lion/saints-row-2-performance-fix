# Saints Row 2 Performance Fix

A guide for improving the performance and stability of the Saints Row 2 PC port on modern systems.

The main fix used by this guide is the Saints Row 2 Juiced Patch.

## Saints Row 2 Juiced Patch

Juiced Patch is a community patch that fixes and improves many parts of the Saints Row 2 PC port.

Among its fixes are:

- improved CPU performance
- improved thread synchronization
- reduced CPU usage
- loading improvements
- crash fixes
- input fixes
- graphical fixes
- additional configuration options

Download the latest release of **Saints Row 2 Juiced Patch** from its official GitHub repository.

## Install Juiced Patch

Open the Saints Row 2 installation directory.

For a default Steam installation this is normally:

```text
C:\Program Files (x86)\Steam\steamapps\common\Saints Row 2
```

You can also locate it through Steam:

```text
Saints Row 2 → Properties → Installed Files → Browse
```

Extract the contents of the Juiced Patch release into the Saints Row 2 directory.

The Juiced files should be located alongside:

```text
SR2_pc.exe
```

Launch the game normally after installation.

## Configure Juiced Patch

Juiced Patch is configured through:

```text
juiced.ini
```

The default configuration already enables important performance fixes.

Two important options are:

```ini
FixPerformance=1
sync_shadows_threads=1
```

These improve synchronization between the game's threads and reduce unnecessary CPU usage.

Unless you have a specific reason to change them, leave the performance-related defaults enabled.

## Gentlemen of the Row

Gentlemen of the Row is an optional Saints Row 2 mod compilation originally created by IdolNinja and other contributors.

It includes a large number of fixes, improvements and optional modifications.

The current Juiced Patch ecosystem supports loading mods more cleanly than older Saints Row 2 setups, so follow the current Juiced/GotR installation documentation rather than older instructions that manually replace files without checking compatibility.

If you only want performance and stability improvements, Juiced Patch can be used without installing Gentlemen of the Row.

## Save files

Back up your Saints Row 2 saves before installing or changing major mods.

The default save location is normally under:

```text
%LOCALAPPDATA%\THQ\Saints Row 2
```

## Troubleshooting

If the game becomes unstable after installing additional modifications:

1. Remove recently added mods.
2. Restore the default `juiced.ini`.
3. Verify the game files through Steam if necessary.
4. Reinstall the latest Juiced Patch release.
5. Test the game before adding other modifications again.

Avoid combining old performance fixes with Juiced unless their current documentation specifically says they are compatible.

## License

Made by rabbi-lion.

Original text in this repository is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License.

Referenced projects, games, mods and third-party material retain their respective rights and licenses.

See `LICENSE` for the full license text.
