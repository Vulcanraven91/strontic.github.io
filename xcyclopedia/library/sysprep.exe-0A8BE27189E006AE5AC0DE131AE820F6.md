﻿---
title: sysprep.exe | System Preparation Tool
---

# sysprep.exe 

* File Path: `C:\Windows\system32\Sysprep\sysprep.exe`
* Description: System Preparation Tool
* Comments: 

## Hashes

Type | Hash
-- | --
MD5 | `0A8BE27189E006AE5AC0DE131AE820F6`
SHA1 | `B1CAC636C1F71439D06D17FB001933D008CB2973`
SHA256 | `5E65918023ADD10E63533950F9914BFC09F5EAF46D28CCC73CCE833B1725A498`
SHA384 | `2C53F5975FF17ACB3B327745DD9890DBEDA97BA08D527B839434C307184F0CD4ACC81423B10587C016D417F72A828F8D`
SHA512 | `B53BEA9DAA68B279A05C17B33251D956120A6AD9B571407CA4621EBC7172963235A317AB9DA955A2175042C40E55C99C901B4ACAAA875BA29D033401195E84C5`
SSDEEP | `12288:CPOLi3zc4LDKGvFIwUzOQyZ4y8YN6totkehMyoGf5kD:CPxxDKGvFI9z089e9k`

## Runtime Data

### Usage (stdout):
```Batchfile

```

### Usage (stderr):
```Batchfile

```

### Child Processes:


## Signature

* Status: Signature verified.
* Serial: `330000023241FB59996DCC4DFF000000000232`
* Thumbprint: `FF82BC38E1DA5E596DF374C53E3617F7EDA36B06`
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: sysprep.EXE.MUI
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.19041.1 (WinBuild.160101.0800)
* Product Version: 10.0.19041.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.


## Possible Misuse

*The following table contains possible examples of `sysprep.exe` being misused. While `sysprep.exe` is **not** inherently malicious, its legitimate functionality can by abused for malicious purposes.*

Source | Source File | Example | License
-- | -- | -- | --
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_sysprep_appdata.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_sysprep_appdata.yml) | `title: Sysprep on AppData Folder` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_sysprep_appdata.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_sysprep_appdata.yml) | `description: Detects suspicious sysprep process start with AppData folder as target (as used by Trojan Syndicasec in Thrip report by Symantec)` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_sysprep_appdata.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_sysprep_appdata.yml) | `            - '*\sysprep.exe *\AppData\\*'` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_sysprep_appdata.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_sysprep_appdata.yml) | `            - sysprep.exe *\AppData\\*` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)



MIT License. Copyright (c) 2020 Strontic.

