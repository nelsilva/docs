﻿# PKI Express changelog

<a name="v1-15-0" />
### 1.15.0 (2020-06-17)

- Add field "customSignatureFieldName" in PAdES signature
- Update PKI SDK to [2.7.2](../pki-sdk/changelog.md#v2-7-2)

<a name="v1-14-0" />
### 1.14.0 (2020-06-09)

- Add support for signature (CAdES, PAdES and XAdES) using key stored on Azure Key Vault
- Update PKI SDK to [2.7.0](../pki-sdk/changelog.md#v2-7-0)

<a name="v1-13-2" />
### 1.13.2 (2019-08-21)

- Update PKI SDK to [2.5.3](../pki-sdk/changelog.md#v2-5-3)

<a name="v1-13.1" />
### 1.13.1 (2019-07-31)

- Add the option of not showing the default visual representation on a PAdES signature with `--suppress-default-visual-rep` enabled

<a name="v1-13-0" />
### 1.13.0 (2019-07-19)

- Add integration with LAPP service
- Add support for signer's reason for a PAdES signature with `--reason` enabled
- Update PKI SDK to [2.5.1](../pki-sdk/changelog.md#v2-5-1)

<a name="v1-12-3" />
### 1.12.3 (2019-05-20)

- Compilation changes

<a name="v1-12-2" />
### 1.12.2 (2019-04-01)

- Add support to timeout configuration for CRLs and CA issuers download
- Add support to timeout configuration for timestamp request
- Update PKI SDK to [2.3.0](../pki-sdk/changelog.md#v2-3-0)

<a name="v1-12-0" />
### 1.12.0 (2019-02-05)

- Add support to PKI-Brazil policies on PAdES signatures (policies `adrb`, `adrb-ltv`, and `adrt`)
- Update PKI SDK to [2.2.7](../pki-sdk/changelog.md#v2-2-7)

<a name="v1-11-0" />
### 1.11.0 (2018-12-04)

- Add support for key generation (command `gen-key`)
- Add support for PKCS #12 certificate generation (command `create-pfx`)

<a name="v1-10-0" />
### 1.10.0 (2018-10-31)

- Add support for setting culture and timezone with `--culture` and `--timezone` enabled on the signatures
- Add support for setting date time format on PAdES visual representation
- Add support for listing available timezones on the system (command `list-timezones`)

<a name="v1-9-0" />
### 1.9.0 (2018-10-05)

- Add support for merging CMS/CAdES signatures (command `merge-cms`).
- Improve PAdES and CAdES signatures validation to support policies with timestamp.

<a name="v1-8-0" />
### 1.8.0 (2018-09-25)

- Add support for returning the signer certificate after a signature.
- Update PKI SDK to [2.1.3](../pki-sdk/changelog.md#v2-1-3)

<a name="v1-7-0" />
### 1.7.0 (2018-09-20)

- Add support for timestamping (command `stamp-pdf`) on PDF files.

<a name="v1-6-2" />
### 1.6.2 (2018-07-20)

- Fix bug on manual activation with new license
- Update PKI SDK to [2.1.0](../pki-sdk/changelog.md#v2-1-0)

<a name="v1-6-1" />
### 1.6.1 (2018-07-11)

- Fixed bug on activation that affected installation on Docker containers

<a name="v1-6-0" />
### 1.6.0 (2018-06-18)

- Add support for *Certificación de Origen Digital* (COD) signature policy on XML signatures.

<a name="v1-5-0" />
### 1.5.0 (2018-05-18)

- Add support for choosing a signature policy with `--policy` enabled on the signatures
- Add support for performing signatures with timestamp (support for PAdES, CAdES and XAdES)
- Update PKI SDK to [1.20.16](../pki-sdk/changelog.md#v1-20-16), fixing certificate chain filling bug on PAdES

<a name="v1-4-1" />
### 1.4.1 (2018-05-14)

- Update PKI SDK to [1.20.15](../pki-sdk/changelog.md#v1-20-15)

<a name="v1-4-0" />
### 1.4.0 (2018-04-10)

- Add support for authentication with certificate (commands `start-auth` and `complete-auth`)

<a name="v1-3-0" />
### 1.3.0 (2018-03-02)

- Add support for opening and validating PAdES and CAdES signatures (commands `open-pades` and `open-cades`)
- Add support for editing PDFs (command `edit-pdf`), enabling generation of "printer-friendly versions"
- Add support for server signatures using PKCS #12 files (.pfx)
- Add support for [using a web proxy](config/proxy.md)
- Update PKI SDK to 2.0.13


<a name="v1-2-1" />
### 1.2.1 (2018-01-18)

- Update PKI SDK to 2.0.11, thus fixing bug that caused network delays even with `--offline` enabled


<a name="v1-2-0" />
### 1.2.0 (2018-01-17)

- Add global flag `--offline` to allow offline operations
- Fix bug that caused activation to be required for `help` command
- Update PKI SDK to 2.0.10


<a name="v1-1-0" />
### 1.1.0 (2017-12-06)

- Add activation mechanism, relieving applications from passing the license file on every call
- Improve logging
- Add `config` command
- Update PKI SDK to 2.0.7, fixing CRL cache bug on Linux


<a name="v1-0-3" />
### 1.0.3 (2017-11-15)

- Update PKI SDK to 2.0.3, fixing *PlatformNotSupportedException bug* on certain Linux distributions


<a name="v1-0-2" />
### 1.0.2 (2017-11-07)

- First version released for both Linux and Windows
- Update PKI SDK to 2.0.2
- Add version information on `help` command


<a name="v1-0-1" />
### 1.0.1 (2017-10-27)

- Fixed bug on compilation which caused unnecessary files to be included on the package

*This version was only released for Linux*


<a name="v1-0-0" />
### 1.0.0 (2017-10-26)

- First version released publicly
- Commands available on this version:
  - `list-certs`
  - `read-cert`
  - `import-pfx`
  - `sign-data`
  - `sign-hash`
  - `sign-cades`
  - `sign-pades`
  - `sign-xml`
  - `start-cades`
  - `start-pades`
  - `start-xml`
  - `complete-sig`
  - `help`

*This version was only released for Linux*
