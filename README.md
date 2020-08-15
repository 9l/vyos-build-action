# VyOS ISO Automation Build

Automate build VyOS v1.2 LTS Release and v1.3 Rolling Release ISO files.

# About this repository

Use the official build script provided by VyOS [https://github.com/vyos/vyos-build](https://github.com/vyos/vyos-build).

Manual build VyOS instructions can be found in VyOS official [Documentation - Build VyOS](https://docs.vyos.io/en/latest/contributing/build-vyos.html).

# Github Action workflow files

Github Action automate the build process and save you some times.

There are two workflow files:

[vyos-v1.2-lts-release.yml](.github/workflows/vyos-v1.2-lts-release.yml)

For VyOS v1.2 release, action trigger by a tag push. It will build the ISO file, create a release and upload the release asset.

[vyos-1.3-rolling-release.yml](.github/workflows/vyos-1.3-rolling-release.yml)

For VyOs rolling release, action trigger on schedule every day. ISO file can be found in Action Artifacts section.

You can edit the file to modify the trigger conditions to suit your needs.
