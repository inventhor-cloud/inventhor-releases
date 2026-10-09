# Viktorija Android — GitHub releases

This public repository is the download/update distribution point. Viktorija is a standalone education application, separate from INVENTHOR's private owner application.

**Status: no stable Viktorija APK has been approved for publication.** Do not upload development/debug builds, old signed APKs, APKs with a mismatched signing certificate, signing keys, credentials or student data.

## Stable Android release convention

- Product ID: `INV_VIKTORIJA`
- Android package: `com.inventhor.viktorija`
- Release tag: `viktorija-android-vc<VERSION_CODE>` (for example, `viktorija-android-vc3`)
- APK asset filename: `viktorija-android.apk`
- The GitHub release must be **published**, non-draft and non-prerelease, with an uploaded APK asset exposing a SHA-256 digest.
- Increment `versionCode` monotonically; retain the **same authorized release signing identity** across updates.
- Include human-readable changes, known issues, test and device acceptance evidence, hash/signature identity and rollback plan.

The Android app checks the public GitHub Releases API, searches only its own strictly named product tags and APK assets, and can notify the user if a newer version exists. The user taps **Güvenli güncellemeyi indir ve kur** in Settings, or opens an Android notification leading to the same in-app card. The app downloads only through an allowlisted GitHub HTTPS redirect chain, checks the GitHub asset SHA-256 digest, the expected package ID, strictly newer version code, and the installed-app signing certificate before opening the Android package installer. Android requires user approval and, where applicable, permission to install from this source. GitHub is not a silent installer.

Other user-facing apps can share this repository by using their **own** product-scoped release tags and asset names, without sharing account data, credentials, package IDs or signing keys. The existing shared `INV_APP_UPDATE_CORE` remains the versioning and verification contract.

## Publication gate

Do not publish the first stable release until teacher/student runtime acceptance, HTTPS, signing configuration, content/permission testing, APK integrity and release-management review pass. A successful debug build or unit test suite is not a release decision.

Links: [Public releases](https://github.com/inventhor-cloud/inventhor-releases/releases) · [Repository](https://github.com/inventhor-cloud/inventhor-releases).
