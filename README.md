# libretro-scummvm-backend
Libretro backend for ScummVM which can be added to backends/platform folder of ScummVM base to build a Libretro core of ScummVM. The intention is be able to apply the backend without adjusting any of base ScummVM.

## How to use
1. Clone official ScummVM base
2. Go to subfolder scummvm/backends/platform
3. Clone libretro-scummvm-backend to folder "libretro"
4. Go to folder scummvm/backends/platform/libretro/build
5. Compile libretro-scummvm core

## Patches
Some issues cannot be fixed without making adjustments to base ScummVM. These are maintained as patches in the patches folder and can be applied before compiling if needed.

#### android_fix_hopkins.patch
Fixes a timing issue with fading on Android causing Hopkins FBI to crash at the title screen

#### android_macos_fix_ags.patch
Fixes issues with the AGS engine on Android and macOS when using -O2 and -O3 compiler performance optimization

#### macos_fix_androidbuilding.patch
Fixes issues with compilation for Android on macOS where input limit for commands is exceeded

#### macos_fix_ultima.patch
Fixes struct packing issues when compiling Ultima engine on macOS Monterey


## Updating
When updating ScummVM, it's important to rebuild [scummvm.zip](aux-data/scummvm.zip) so that any auxiliary data is bundled in. The compile the new scummvm.zip, run the following command:

```
cd backends/platform/libretro/aux-data
./bundle_aux_data.bash
```
