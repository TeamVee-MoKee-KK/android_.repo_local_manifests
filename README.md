Mokee KK Manifests
========================
Project V1 / Project Vee3

Local manifests to build Android KitKat 4.4 to L1II and L3II

To initialize Mokee Repo:

    repo init -u https://github.com/MK-KK/android.git -b kk_mkt -g all,-notdefault,-darwin

To initialize Repo's:

    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.github.com/TeamVee-MoKee-KK/android_.repo_local_manifests/kk_mkt/local_manifest.xml

To sync:

    repo sync

To apply patchs:

    device/lge/vee-common/patches/apply.sh

To build for L1 II:

    . mk v1

To build for L3 II:

    . mk vee3
