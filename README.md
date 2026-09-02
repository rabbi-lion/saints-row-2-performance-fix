# Saints Row 2 Performance Fix

A guide for improving the performance and stability of the Saints Row 2 PC port on modern systems.

The main fix used by this guide is the Saints Row 2 Juiced Patch.

## Saints Row 2 Juiced Patch

Juiced Patch is a community patch that fixes and improves many parts of the Saints Row 2 PC port.

Among its fixes and improvements are:

- improved CPU performance
- improved thread synchronization
- reduced CPU usage
- loading improvements
- crash fixes
- input fixes
- graphical fixes
- additional configuration options
- improved mod support

Download the latest release of **Saints Row 2 Juiced Patch** from its official GitHub repository.

## Prerequisites

Juiced Patch requires the Microsoft Visual C++ runtime components used by Saints Row 2 and the patch itself.

Make sure the following are installed:

- Microsoft Visual C++ 2010 Redistributable
- Microsoft Visual C++ 2015–2022 Redistributable

## Install Juiced Patch

Open the Saints Row 2 installation directory.

For a default Steam installation, this is normally:

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

After extracting the patch, run:

```text
SR2_pc.exe
```

as Administrator once.

This allows Juiced Patch to perform its initial executable patching.

Juiced should also create a backup of the original executable named:

```text
sr2_pc_unpatched.exe
```

After the initial setup has completed, launch the game normally.

## Configure Juiced Patch

Juiced Patch is configured through:

```text
juiced.ini
```

The default configuration already enables the important performance fixes.

Three important options are:

```ini
FixPerformance=1
sync_shadows_threads=1
FastMath=1
```

`FixPerformance` improves synchronization between the game's main and rendering threads.

`sync_shadows_threads` improves synchronization of shadow-related jobs and can significantly reduce unnecessary CPU usage.

`FastMath` replaces some of the game's older mathematical routines with more optimized implementations.

Unless you have a specific reason to change them, leave the performance-related defaults enabled.

## Optional: DXVK

Juiced Patch does not require DXVK.

However, the Juiced developers note that the benefits of `FixPerformance` can be greater when the game is used with DXVK.

DXVK is therefore an optional additional performance tweak rather than a required part of this guide.

Because DXVK versions and compatibility can change over time, follow the current DXVK and Juiced Patch documentation rather than relying on an old version-specific installation procedure.

## Gentlemen of the Row

Gentlemen of the Row, commonly known as GotR, is an optional Saints Row 2 mod compilation originally created by IdolNinja and other contributors.

It includes a large collection of fixes, improvements and optional modifications.

Modern versions of Juiced Patch support loose-file mod loading, which changes how older Saints Row 2 mods should be installed.

Older GotR installation methods and patch-builder workflows can conflict with Juiced or other modern mods.

If you want to use GotR together with Juiced Patch, follow the current Juiced/GotR compatibility instructions rather than older guides that manually replace game files without checking compatibility.

If you only want performance and stability improvements, Juiced Patch can be used without installing Gentlemen of the Row.

## Save files

Back up your Saints Row 2 saves before installing or changing major mods.

The default save location is normally:

```text
%LOCALAPPDATA%\THQ\Saints Row 2
```

Keep a backup somewhere outside the Saints Row 2 installation and save directories before making major changes.

## Troubleshooting

If the game becomes unstable after installing additional modifications:

1. Remove recently added mods.
2. Replace `juiced.ini` with a fresh copy from the current Juiced Patch release.
3. Verify the game files through Steam if necessary.
4. Reinstall the latest Juiced Patch release.
5. Run `SR2_pc.exe` as Administrator once again if the executable has been restored or replaced.
6. Test the game before adding other modifications again.

Avoid combining old Saints Row 2 performance fixes with Juiced unless their current documentation specifically states that they are compatible.

If Steam file verification restores the original executable or removes files modified by Juiced, reinstall Juiced Patch afterward.

## Notes

Saints Row 2 is an old PC port with significant technical problems, so Juiced Patch may greatly improve performance and stability without eliminating every possible crash or issue.

Performance can still vary depending on hardware, drivers, operating-system configuration and installed modifications.

## License

Made by rabbi-lion.

Original text in this repository is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License.

Referenced projects, games, mods and third-party material retain their respective rights and licenses.

See `LICENSE` for the full license text.
