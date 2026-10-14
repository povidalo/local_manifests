# Local manifest: Galaxy S8+ Exynos (dream2lte), headless LineageOS 20.0

Based on ivanmeler/local_manifests `lineage-20.0` (roomservice.xml), trimmed to
dream2lte. Projects with headless-server changes point to forks in this account,
branch `lineage-20.0-headless`.

    repo init -u https://github.com/LineageOS/android.git -b lineage-20.0 --git-lfs
    git clone -b lineage-20.0-headless https://github.com/povidalo/local_manifests .repo/local_manifests
    repo sync
