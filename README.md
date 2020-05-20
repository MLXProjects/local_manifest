Manifest for Android KitKat / LineageOS 11.0
====================================
Project coriplus|GT-S5301
Thanks to bcm216xx for his work on the corsica, all my work is mostly based on his repos.

---

Manual Way:

To initialize LineageOS 11.0 Repo:

    repo init -u https://github.com/LineageOS/android.git -b cm-11.0 --no-clone-bundle --depth=1

---

To initialize Manifest:

    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.github.com/MLXProjects/local_manifest/cm-11.0/local_manifest.xml

---

Sync the repo:

    repo sync -j$( nproc --all ) --force-sync -c --no-clone-bundle --no-tags --optimized-fetch --prune

---

Apply Pacht

	git clone https://github.com/bcm216xx-LOS/android_patches_los11.git
	sh android_patches_los11/apply-patches.sh

Initialize the environment:

    source build/envsetup.sh

---

To build:

    brunch coriplus
