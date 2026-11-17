# Pokédex Merger for Nintendo 3DS

**Latest prototype: v0.3**. Merge Pokédex seen/caught progress from Pokémon Platinum or Pokémon Black into a Pokémon Black 2 save, one source at a time.

## Download

[Get the compiled v0.3 app (GitHub Actions)](https://github.com/jemmart6-prog/PokedexMerger-3DS/actions/runs/43992271749)

Open the successful run, download the **PokedexMerger-3DSX** artifact, extract `PokedexMerger.3dsx` from the ZIP, then copy it to `SD:/3ds/PokedexMerger.3dsx`. Start the Homebrew Launcher.

## How to use

1. Choose a **source**: Pokémon Platinum or Pokémon Black.
2. Choose your **Black 2 destination** save.
3. Press **X** to preview additions.
4. Press **Y** then **A** to confirm writing back to the **selected destination file in its original folder, with its original name**.
5. To merge the other game, choose the next source and repeat. The destination stays selected.

Use the touch screen or physical buttons. File selection begins with quick shortcuts for TWiLight Menu++ saves, Checkpoint backups, your last folder, or SD card browsing.

**Optional extra backup is OFF by default.** Press **SELECT** to toggle it. Saving uses a temporary file and rollback mechanism, not a renamed export. A lingering `.dexmerge.rollback` file contains recoverable original data; do not delete it after any failed write.

## Compatibility and limitations

Works on raw 512 KiB save files stored on the SD card. The picker accepts Checkpoint's save filenames even without a `.sav` suffix. It does *not* read or write physical DS cartridge memory directly. To restore to a physical cartridge, first use a save manager such as Checkpoint to work with cartridge backups.

**Experimental:** compiler build and synthetic-save tests passed, but this version has not been fully validated with genuine save files on 3DS hardware. Test with disposable save copies before updating anything irreplaceable. Close the games while saving and do not eject the SD card during writes.

The built source is stored in `PokedexMerger_3DS_Source.tar.xz.b64` and unpacked by the automated build workflow. Refer to the archive's included README for details.

Independent homebrew project. No game ROMs or save files are included.
