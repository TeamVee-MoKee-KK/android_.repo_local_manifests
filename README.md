Manifest for Android KitKat / Mokee KK
====================================
Project M4|L5 / Project U0|L7 / Project V1|L1II / Project Vee3|L3II

---

Automatic Way:

script to download manifests, sync repo and build:

    curl --create-dirs -L -o build.sh -O -L https://raw.github.com/TeamVee-MoKee-KK/android_.repo_local_manifests/kk_mkt/build.sh

To use:

    source build.sh

---

Manual Way:

To initialize Mokee KK Repo:

    repo init -u https://github.com/MK-KK/android.git -b kk_mkt -g all,-notdefault,-darwin

---

To initialize MSM7x27a Manifest for all devices:

    curl --create-dirs -L -o .repo/local_manifests/msm7x27a_manifest.xml -O -L https://raw.github.com/TeamVee-MoKee-KK/android_.repo_local_manifests/kk_mkt/msm7x27a_manifest.xml

---

To initialize Manifest for L5/L7:

    curl --create-dirs -L -o .repo/local_manifests/gen1_manifest.xml -O -L https://raw.github.com/TeamVee-MoKee-KK/android_.repo_local_manifests/kk_mkt/gen1_manifest.xml

---

To initialize Manifest for L1II/L3II:

    curl --create-dirs -L -o .repo/local_manifests/gen2_manifest.xml -O -L https://raw.github.com/TeamVee-MoKee-KK/android_.repo_local_manifests/kk_mkt/gen2_manifest.xml

---

# Never use 'L5/L7' Manifest with 'L1II/L3II' Manifest

---

Sync the repo:

    repo sync -c --force-sync

---

Initialize the environment:

    source build/envsetup.sh

---

To build for L5:

    . mk e610

---

To build for L7:

    . mk p700

---

To build for L1II:

    sh device/lge/v1/patches/apply.sh
    . mk v1

---

To build for L3II:

    sh device/lge/vee3/patches/apply.sh
    . mk vee3
