# lg-g4-build-lineage
I tried on Manjaro xfce.
```
sudo pacman -S repo
```
Make default python2 globally

```
sudoedit /usr/local/bin/python
```
Paste this inside and save the file:
```
#!/bin/bash
exec python2 "$@"
```
Don't forget to make it executable:
```
sudo chmod +x /usr/local/bin/python
```
```
mkdir android
cd android
mkdir lineage
cd lineage
repo init -u git://github.com/LineageOS/android.git -b lineage-16.0
```

```
repo sync
```
After that,
```
cd ~/android/lineage
source build/envsetup.sh
breakfast h815
```

```
cd ~/android/lineage/device/lge/h815

./extract-files.sh

export ANDROID_JACK_VM_ARGS="-Dfile.encoding=UTF-8 -XX:+TieredCompilation -Xmx4G"


croot
brunch h815
```
