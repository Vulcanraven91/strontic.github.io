﻿---
title: RpcPing.exe | RPC Ping Utility
excerpt: What is RpcPing.exe?
---

# RpcPing.exe 

* File Path: `C:\windows\SysWOW64\RpcPing.exe`
* Description: RPC Ping Utility

## Hashes

Type | Hash
-- | --
MD5 | `70DDB6C5BEF79AB8A6E35D1F1488579D`
SHA1 | `2CAAAB93A06D3139937FE796D044C4F96269A5AF`
SHA256 | `07E9C84FFBE387F263A86CF87FDF44D50BAE8D6F0B3A10C8F99556E85A7E34BB`
SHA384 | `9707722464DB8C72DC66AD73DF92CFD3C5E5567D87676820371EB48B150AE14495DECA1E508158629EB283273B968A59`
SHA512 | `4EEE9B72541063B4349F177D881D780056FEBC1DB787F44FE024F596DBE6725EC0A319CA15F4A054F6EF3CB285F51BE8D06C673179B2B7605F2D996FC82FA672`
SSDEEP | `384:GN7FQRTwWlCYhocHlLlOb30lxZCIlwMPWMFQhXtwoVV0MLWI0WEk:4mRxCOXZJlwM3FQhVGMP2k`

## Signature

* Status: The file C:\windows\SysWOW64\RpcPing.exe is not digitally signed. You cannot run this script on the current system. For more information about running scripts and setting execution policy, see about_Execution_Policies at http://go.microsoft.com/fwlink/?LinkID=135170
* Serial: ``
* Thumbprint: ``
* Issuer: 
* Subject: 

## File Metadata

* Original Filename: RpcPing.exe.mui
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 6.3.9600.16384 (winblue_rtm.130821-1623)
* Product Version: 6.3.9600.16384
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.



## Possible Misuse

*The following table contains possible examples of `RpcPing.exe` being misused. While `RpcPing.exe` is **not** inherently malicious, its legitimate functionality can be abused for malicious purposes.*

Source | Source File | Example | License
-- | -- | -- | --
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_rpcping.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_rpcping.yml) | `title: Capture Credentials with Rpcping.exe`{:.highlight .language-yaml} | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_rpcping.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_rpcping.yml) | `description: Detects using Rpcping.exe to send a RPC test connection to the target server (-s) and force the NTLM hash to be sent in the process.`{:.highlight .language-yaml} | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_rpcping.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_rpcping.yml) | `- https://lolbas-project.github.io/lolbas/Binaries/Rpcping/`{:.highlight .language-yaml} | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[sigma](https://github.com/Neo23x0/sigma) | [win_susp_rpcping.yml](https://github.com/Neo23x0/sigma/blob/master/rules/windows/process_creation/win_susp_rpcping.yml) | `Image\|endswith: '\rpcping.exe'`{:.highlight .language-yaml} | [DRL 1.0](https://github.com/Neo23x0/sigma/blob/master/LICENSE.Detection.Rules.md)
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Rpcping.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Rpcping.yml) | `Name: Rpcping.exe`{:.highlight .language-yaml} | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Rpcping.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Rpcping.yml) | `- Command: rpcping -s 127.0.0.1 -e 1234 -a privacy -u NTLM`{:.highlight .language-yaml} | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Rpcping.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Rpcping.yml) | `- Command: rpcping /s 10.0.0.35 /e 9997 /a connect /u NTLM`{:.highlight .language-yaml} | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Rpcping.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Rpcping.yml) | `- Path: C:\Windows\System32\rpcping.exe`{:.highlight .language-yaml} | 
[LOLBAS](https://github.com/LOLBAS-Project/LOLBAS) | [Rpcping.yml](https://github.com/LOLBAS-Project/LOLBAS/blob/master/yml/OSBinaries/Rpcping.yml) | `- Path: C:\Windows\SysWOW64\rpcping.exe`{:.highlight .language-yaml} | 

## Additional Info*

**The information below is copied from [MicrosoftDocs](https://github.com/MicrosoftDocs/windowsserverdocs), which is maintained by [Microsoft](https://opensource.microsoft.com/codeofconduct/). Available under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license.*

---

## rpcping

>Applies to: Windows Server 2022, Windows Server 2019, Windows Server 2016, Windows Server 2012 R2, Windows Server 2012

Confirms the RPC connectivity between the computer running Microsoft Exchange Server and any of the supported Microsoft Exchange Client workstations on the network. This utility can be used to check if the Microsoft Exchange Server services are responding to RPC requests from the client workstations via the network.

### Syntax

```
rpcping [/t <protseq>] [/s <server_addr>] [/e <endpoint>
        |/f <interface UUID>[,majorver]] [/O <interface object UUID]
        [/i <#_iterations>] [/u <security_package_id>] [/a <authn_level>]
        [/N <server_princ_name>] [/I <auth_identity>] [/C <capabilities>]
        [/T <identity_tracking>] [/M <impersonation_type>]
        [/S <server_sid>] [/P <proxy_auth_identity>] [/F <RPCHTTP_flags>]
        [/H <RPC/HTTP_authn_schemes>] [/o <binding_options>]
        [/B <server_certificate_subject>] [/b] [/E] [/q] [/c]
        [/A <http_proxy_auth_identity>] [/U <HTTP_proxy_authn_schemes>]
        [/r <report_results_interval>] [/v <verbose_level>] [/d]
```

#### Parameters

| Parameter | Description |
|--|--|
| /t `<protseq>` | Specifies the protocol sequence to use. Can be one of the standard RPC protocol sequences: ncacn_ip_tcp, ncacn_np, or ncacn_http.<p>If not specified, default is ncacn_ip_tcp. |
| /s `<server_addr>` | Specifies the server address. If not specified, the local machine will be pinged. |
| /e `<endpoint>` | Specifies the endpoint to ping. If none is specified, the endpoint mapper on the target machine will be pinged.<p>This option is mutually exclusive with the interface (**/f**) option. |
| /o `<binding_options>` | Specifies the binding options for the RPC ping. |
| /f `<interface UUID>[,Majorver]` | Specifies the interface to ping. This option is mutually exclusive with the endpoint option. The interface is specified as a UUID.<p>if the *majorver* is not specified, version 1 of the interface will be sought.<p>When interface is specified, **rpcping** will query the endpoint mapper on the target machine to retrieve the endpoint for the specified interface. The endpoint mapper will be queried using the options specified in the command line. |
| /O `<object UUID>` | Specifies the object UUID if the interface registered one. |
| /i `<#_iterations>` | Specifies the number of calls to make. The default is 1. This option is useful for measuring connection latency if multiple iterations are specified. |
| /u `<security_package_id>` | Specifies the security package (security provider) RPC will use to make the call. The security package is identified as a number or a name. If a number is used it is the same number as in the RpcBindingSetAuthInfoEx API. If you specify this option, you must specify an authentication level other than *none*. There's no default for this option. If it isn't specified, RPC won't use security for the ping. The list below shows the names and numbers. Names are not case sensitive:<ul><li>Negotiate / 9 or one of nego, snego or negotiate</li><li>NTLM / 10 or NTLM</li><li>SChannel / 14 or SChannel</li><li>Kerberos / 16 or Kerberos</li><li>Kernel / 20 or Kernel</li></ul> |
| /a `<authn_level>` | Specifies the authentication level to use. If this option is specified, the security package ID (**/u**) must also be specified. If this option isn't specified, RPC won't use security for the ping. There's no default for this option. Possible values are:<ul><li>connect</li><li>call</li><li>pkt</li><li>integrity</li><li>privacy</li></ul> |
| /N `<server_princ_name>` | Specifies a server principal name.<p>This field can be used only when authentication level and security package are selected. |
| /I `<auth_identity>` | Allows you to specify alternative identity to connect to the server. The identity is in the form user,domain,password. If the user name, domain, or password have special characters that can be interpreted by the shell, enclose the identity in double quotes. You can specify `\*` instead of the password and RPC will prompt you to enter the password without echoing it on the screen. If this field is not specified, the identity of the logged on user will be used.<p>This field can be used only when authentication level and security package are selected. |
| /C `<capabilities>` | Specifies a hexadecimal bitmask of flags. This field can be used only when authentication level and security package are selected. |
| /T `<identity_tracking>` | Specifies static or dynamic. If not specified, dynamic is the default.<p>This field can be used only when authentication level and security package are selected. |
| /M `<impersonation_type>` | Specifies anonymous, identify, impersonate or delegate. Default is impersonate.<p>This field can be used only when authentication level and security package are selected. |
| /S `<server_sid>` | Specifies the expected SID of the server.<p>This field can be used only when authentication level and security package are selected. |
| /P `<proxy_auth_identity>` | Specifies the identity to authenticate with to the RPC/HTTP proxy. Has the same format as for the **/I** option. You must specify security package (**/u**), authentication level (**/a**), and authentication schemes (**/H**) in order to use this option. |
| /F `<RPCHTTP_flags>` | Specifies the flags to pass for RPC/HTTP front end authentication. The flags may be specified as numbers or names The currently recognized flags are:<ul><li>Use SSL / 1 or ssl or use_ssl</li><li>Use first auth scheme / 2 or first or use_first</li></ul>You must specify security package (**/u**) and authentication level (**/a**) to use this option. |
| /H `<RPC/HTTP_authn_schemes>` | Specifies the authentication schemes to use for RPC/HTTP front end authentication. This option is a list of numerical values or names separated by comma. Example: Basic,NTLM. Recognized values are (names are not case sensitive):<ul><li>Basic / 1 or Basic</li><li>NTLM / 2 or NTLM</li><li>Certificate / 65536 or Cert</li></ul><p>You must specify security package (**/u**) and authentication level (**/a**) in order to use this option. |
| /B `<server_certificate_subject>` | Specifies the server certificate subject. You must use SSL for this option to work.<p>You must specify security package (**/u**) and authentication level (**/a**) in order to use this option. |
| /b | Retrieves the server certificate subject from the certificate sent by the server and prints it to a screen or a log file. Valid only when the Proxy echo only option (/E) and the use SSL options are specified.<p>You must specify security package (**/u**) and authentication level (**/a**) in order to use this option. |
| /R | Specifies the HTTP proxy. If *none*, the RPC proxy is used. The value *default* means to use the IE settings in your client machine. Any other value will be treated as the explicit HTTP proxy. If you do not specify this flag, the default value is assumed, that is, the IE settings are checked. This flag is valid only when the **/E** (echo Only) flag is enabled. |
| /E | Restricts the ping to the RPC/HTTP proxy only. The ping does not reach the server. Useful when trying to establish whether the RPC/HTTP proxy is reachable. To specify an HTTP proxy, use the /R flag. If an HTTP proxy is specified in the /o flag, this option will be ignored.<p>You must specify security package (**/u**) and authentication level (**/a**) in order to use this option. |
| /q | Specifies quiet mode. Does not issue any prompts except for passwords. Assumes *Y* response to all queries. Use this option with care. |
| /c | Use smart card certificate. rpcping will prompt user to choose smart card. |
| /A | Specifies the identity with which to authenticate to the HTTP proxy. Has the same format as for the /I option.<p>You must specify authentication schemes (/U), security package (**/u**) and authentication level (**/a**) in order to use this option. |
| /U | Specifies the authentication schemes to use for HTTP proxy authentication. This option is a list of numerical values or names separated by comma. Example: Basic,NTLM. Recognized values are (names are not case sensitive):<ul><li>Basic / 1 or Basic</li><li>NTLM / 2 or NTLM</li></ul>You must specify security package (**/u**) and authentication level (**/a**) in order to use this option. |
| /r | If multiple iterations are specified, this option will make **rpcping** display current execution statistics periodically instead after the last call. The report interval is given in seconds. Default is 15. |
| /v | Tells **rpcping** how verbose to make the output. Default value is 1. 2 and 3 provide more output from **rpcping**. |
| /d | Launches RPC network diagnostic UI. |
| /p | Specifies to prompt for credentials if authentication fails. |
| /? | Displays help at the command prompt. |

### Examples

To find out if the Exchange server you connect through RPC/HTTP is accessible, type:

```
rpcping /t ncacn_http /s exchange_server /o RpcProxy=front_end_proxy /P username,domain,* /H Basic /u NTLM /a connect /F 3
```

### Additional References

- [Command-Line Syntax Key](https://github.com/MicrosoftDocs/windowsserverdocs/tree/master/WindowsServerDocs/administration/windows-commands/command-line-syntax-key.md)

---



MIT License. Copyright (c) 2020-2021 Strontic.

