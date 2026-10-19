# Local manifests: headless LineageOS 20.0 servers

One LineageOS 20.0 tree builds both devices:

| File | Device | Based on |
|---|---|---|
| `dream2lte.xml` | Galaxy S8+ Exynos (SM-G955F) | ivanmeler/local_manifests `lineage-20.0` (roomservice.xml), trimmed to dream2lte |
| `mido.xml` | Redmi Note 4 Snapdragon | zeelog's `lineage-20.0` trees (device, kernel 4.9, blobs) |
| `headless.xml` | both | `povidalo/android_vendor_headless`: the headless server pieces they share |

Projects with headless-server changes point to forks in this account, branch
`lineage-20.0-headless`.

    repo init -u https://github.com/LineageOS/android.git -b lineage-20.0 --git-lfs
    git clone -b lineage-20.0-headless https://github.com/povidalo/local_manifests .repo/local_manifests
    repo sync

Build: `vendor/headless/tools/build-in-vm.sh <dream2lte|mido> bacon`.
