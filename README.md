# android-appstubs

Stub OS X applications for Android (emulator, avd, sdk)

## Instructions ##

To generate these applications, you must have [platypus](http://sveinbjorn.org/platypus) installed.

### Android AVD Manager ###
```bash
echo "source /etc/profile; android avd" | \
platypus -o None -i android-avd.icns -B -R -y -p /bin/bash - "apps/Android AVD Manager"
```

### Android SDK Manager ###
```bash
echo "source /etc/profile; android sdk" | \
platypus -o None -i android-sdk.icns -B -R -y -p /bin/bash - "apps/Android SDK Manager"
```

### Android Emulator ###

Note: The name of the emulator that is launched is "default" - you can modify this call for a different emulator

```bash
echo "source /etc/profile; emulator @default -partition-size 1024 -gpu on" | \
platypus -o None -i android-emulator.icns -B -R -y -p /bin/bash - "apps/Android Emulator"
```

### Android Emulator (Wiped) ###

Note: The name of the emulator that is launched is "default" - you can modify this call for a different emulator

```bash
echo "source /etc/profile; emulator @default -partition-size 1024 -gpu on -wipe-data" | \
platypus -o None -i android-emulator.icns -B -R -y -p /bin/bash - "apps/Android Emulator (Wiped)"
```

