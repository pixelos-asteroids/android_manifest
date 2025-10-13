mkdir VoltageOS && cd VoltageOS

repo init -u https://github.com/VoltageOS/manifest.git -b 16 --git-lfs

mkdir .repo/local_manifests && wget https://raw.githubusercontent.com/voltageos-oneplus9/manifest/16/OnePlus9Series.xml -O .repo/local_manifests/OnePlus9Series.xml

repo sync

#To build for OnePlus 9 Pro aka lemonadep

. build/envsetup.sh

brunch lemonadep

#To build for OnePlus 9 aka lemonade

. build/envsetup.sh

brunch lemonade
