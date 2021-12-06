# VyOS ISO Automation Build

Automate build VyOS v1.2 LTS, v1.3 LTS Release and v1.4 Rolling Release ISO files.

## About this repository

Use the official build script provided by VyOS [https://github.com/vyos/vyos-build](https://github.com/vyos/vyos-build).

Manual build VyOS instructions can be found in VyOS official [Documentation - Build VyOS](https://docs.vyos.io/en/latest/contributing/build-vyos.html).

## Github Action workflow files

Github Action automate the build process and save you some times.

There are two workflow files:

[vyos-v1.2.x-crux.yml](.github/workflows/vyos-v1.2.x-crux.yml)

For VyOS v1.2.x LTS release, action trigger by a tag push. It will build the ISO and VM image files, create a release and upload the release asset.

[vyos-v1.3.x-equuleus.yml](.github/workflows/vyos-v1.3.x-equuleus.yml)

For VyOS v1.3.x LTS release, action trigger by a tag push. It will build the ISO and VM image files, create a release and upload the release asset.

[vyos-v1.4-rolling-release.yml](.github/workflows/vyos-v1.4-rolling-release.yml)

For VyOs v1.4 rolling release, action trigger on schedule every day. ISO file can be found in the Action Artifacts section.

You can edit the workflow files to modify the trigger conditions to suit your needs.

## Generate your own private key for signing vmware image

```bash
openssl req -x509 -nodes -sha256 -newkey rsa:2048 -keyout private_key_for_signing_vmware_image.pem -out private_key_for_signing_vmware_image.pem
```
