# libretro-scummvm-backend
Libretro backend for ScummVM which can be added to backends folder of ScummVM base

## Updating

When updating ScummVM, it's important to rebuild [scummvm.zip](aux-data/scummvm.zip) so that any auxiliary data is bundled in. The compile the new scummvm.zip, run the following command:

```
cd backends/platform/libretro/aux-data
./bundle_aux_data.bash
```
