Manifest for Android Nougat / LineageOS 14.1
====================================
Project coriplus|GT-S5301
Thanks to bcm216xx for his work on the corsica and chijure for this repo, all my work is mostly based on their repos.

---

Manual Way:

To initialize LineageOS 14.1 Repo:

    repo init -u https://github.com/LineageOS/android.git -b cm-14.1 --no-clone-bundle --depth=1

---

To initialize Manifest:

    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.github.com/MLXProjects/local_manifest/cm-14.1/local_manifest.xml

---

Sync the repo:

    repo sync -j$( nproc --all ) --force-sync -c --no-clone-bundle --no-tags --optimized-fetch --prune

---

Apply Patch

	Run "git clone https://github.com/MLXProjects/build_tools.git -b cm-14.1" in root of ROM sources directory.
	cd rom_sources
	sources build_tools/patch


Initialize the environment:

    source build/envsetup.sh

---

To build:

    brunch coriplus
