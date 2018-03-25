Manifest for Android Lollipop / LineageOS 12.1
====================================
Project corsica|GT-S5310/GT-S5312

---

Manual Way:

To initialize LineageOS 12.1 Repo:

    repo init -u https://github.com/LineageOS/android.git -b cm-12.1 --no-clone-bundle --depth=1

---

To initialize Manifest:

    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.github.com/bcm216xx-LOS/local_manifest/cm-12.1/local_manifest.xml

---

Sync the repo:

    repo sync -j$( nproc --all ) --force-sync -c --no-clone-bundle --no-tags --optimized-fetch --prune

---

Sync prebuilts:

    cd vendor/cm
    ./get-prebuilts
    cd ../..

---

Initialize the environment:

    source build/envsetup.sh

---

To build:

    brunch corsica
