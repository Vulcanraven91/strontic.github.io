﻿
# MpCmdRun.exe 
* File Path: `C:\ProgramData\Microsoft\Windows Defender\platform\4.18.2004.6-0\X86\MpCmdRun.exe`
* Description: Microsoft Malware Protection Command Line Utility
* Comments: 

## Hashes
Type | Hash
-- | --
MD5 | `309668978FAD5EFE13304BBA3120E9D2`
SHA1 | `2A3D353B0C14496BBF09C5C59631B032613CBAC0`
SHA256 | `9909DDC3158721BD4C09A6BCDEB1A32CB7BDD12A29FCAE56CB5F4BDC0A141296`
SHA384 | `A88930CAF947FF0A45311C77E98816703A6CCB29B487CDA5EB372253FF09AC768D549F4148BA0325F3F02F0AAE2F886A`
SHA415 | `C99456D1DDE967A04C91E87930368A22E77A3D9C1B86CC80192F464B21B7FFE3C1A371274DE42C436BA61904392DB996A0380838D513BB498585326D39819BBB`
SSDEEP | `6144:beL9BpPxovL28CE7S3Cs4qRo34tmNUpAOG:VvL28CBo36tAP`

## Runtime Data
### Usage (stdout):
```Batchfile
Microsoft Antimalware Service Command Line Utility (c) 2006-2018 Microsoft Corp
Use this tool to automate and troubleshoot Microsoft Antimalware Service

Usage:
MpCmdRun.exe [command] [-options]

Command Description
   -? / -h                                    Displays all available options
                                              for this tool
   -Scan [-ScanType #] [-File <path> [-DisableRemediation] [-BootSectorScan] [-CpuThrottling]]
         [-Timeout <days>]
         [-Cancel]
                                              Scans for malicious software
   -Trace [-Grouping #] [-Level #]            Starts diagnostic tracing
   -GetFiles                                  Collects support information
   -GetFilesDiagTrack                         Same as Getfiles but outputs to 
                                              temporary DiagTrack folder 
   -RemoveDefinitions [-All]                  Restores the installed
                                              signature definitions
                                              to a previous backup copy or to
                                              the original default set of
                                              signatures
                      [-Engine]               Restore the installed engine to
                                              the previous version saved
                      [-DynamicSignatures]    Removes only the dynamically
                                              downloaded signatures
   -SignatureUpdate [-UNC | -MMPC]            Checks for new definition updates
   -Restore  [-ListAll | [[-Name <name>] [-All] | [-FilePath <filePath>]] [-Path <path>]]  Restore or list
                                                               quarantined item(s)
   -AddDynamicSignature [-Path]               Loads a dynamic signature
   -ListAllDynamicSignatures                  List the loaded dynamic signatures
   -RemoveDynamicSignature [-SignatureSetID]  Removes a dynamic signature
   -CheckExclusion -path <path>               Checks whether path is excluded

Additional Information:

Support information will be in the following directory:
C:\ProgramData\Microsoft\Windows Defender\Support

   -Scan [-ScanType value]
        0  Default, according to your configuration
        1  Quick scan
        2  Full system scan
        3  File and directory custom scan

           [-File <path>]
                Indicates the file or directory  to be scanned, only valid for custom scan.

           [-DisableRemediation]
                This option is valid only for custom scan.
                When specified:
                  - File exclusions are ignored.
                  - Archive files are scanned.
                  - Actions are not applied after detection.
                  - Event log entries are not written after detection.
                  - Detections from the custom scan are not displayed in the user interface.
                  - The console output will show the list of detections from the custom scan.

           [-BootSectorScan]
                Enables boot sector scanning; only valid for custom scan.

           [-Timeout <days>]
                Timeout in days; maximum value is 30.
                If this parameter is not specified, default value is 7 days for full scan and 1 day for all other scans.

           [-Cancel]
                Try to cancel any ongoing quick or full scan.

           [-CpuThrottling]
                When specified:
                  - Will ensure that the scan obeys the CPU throttling as defined in the policy (Default 50).

      Return code is
      0    if no malware is found or malware is successfully remediated and no additional user action is required
      2    if malware is found and not remediated or additional user action is required to complete remediation or there is error in scanning.  Please check History for more information.

   -Trace [-Grouping value] [-Level value]
        Begins tracing Microsoft Antimalware Service's actions.
        You can specify the components for which tracing is enabled and
        how much information is recorded.
        If no component is specified, all the components will be logged.
        If no level is specified, the Error, Warning and Informational levels
        will be logged. The data will be stored in the support directory
        as a file having the current timestamp in its name and bearing
        the extension BIN.

        [-Grouping]
        0x1    Service
        0x2    Malware Protection Engine
        0x4    User Interface
        0x8    Real-Time Protection
        0x10   Scheduled actions
        0x20   WMI
        0x40   NIS/GAPA
        0x80   Windows Security Center
        0x100  DLP external

        [-Level]
        0x1    Errors
        0x2    Warnings
        0x4    Informational messages
        0x8    Function calls
        0x10   Verbose
        0x20   Performance

   -CaptureNetworkTrace -path <path>
       Captures all the network input into the Network Protection service and 
       saves it to a file at <path>. Supply an empty path to stop tracing
       Note: The specified path must be writable by LocalService
       ex: C:\Users\Public\Downloads 

   -GetFiles
        Gathers the following log files and packages them together in a 
        compressed file in the support directory

        - Any trace files from Microsoft Antimalware Service
        - The Windows Update history log
        - All Microsoft Antimalware Service events from the System event log
        - All relevant Microsoft Antimalware Service registry locations
        - The log file of this tool
        - The log file of the signature update helper tool

   -GetFilesDiagTrack
        Same as GetFiles, but outputs the CAB file to the temp DiagTrack 
        directory

   -RemoveDefinitions
        Restores the last set of signature definitions

        [-Engine]
        Restores the last saved engine
        Use this option to restore the previous engine.

        [-All]
        Removes any installed signature and engine files. Use this 
        option if you have difficulties trying to update signatures.

        [-DynamicSignatures]
        Removes all Dynamic Signatures. 

   -SignatureUpdate
        Checks for new definition updates

        [-UNC [-Path <path>]]
        Performs update directly from UNC file share specified in <path>
        If -Path is not specified, update will be performed directly from the
             preconfigured UNC location

        [-MMPC]
        Performs update directly from Microsoft Malware Protection Center

   -Restore
        [-ListAll]
        List all items that were quarantined

        [-Name <name>]
        Restores the most recently quarantined item based on threat name
        One Threat can map to more than one file

        [-All]
        Restores all the quarantined items based on name

        [-FilePath <filePath>]
        Restores quarantined item based on file path

        [-Path]
        Specify the path where the quarantined items will be restored.
        If not specified, the item will be restored to the original path.
   -AddDynamicSignature -Path <path> 
        Adds a Dynamic Signature specified by <path>

   -ListAllDynamicSignatures
        Lists SignatureSet ID's of all Dynamic Signatures added to the client
        via MAPS and MPCMDRUN -AddDynamicSignature

   -RemoveDynamicSignature -SignatureSetID <SignatureSetID> 
        Removes a Dynamic Signature specified by <SignatureSetID>

   -CheckExclusion -path <path>
        Checks whether <path> is excluded. It can be either a path, or a file.


```

### Usage (stderr):
```Batchfile

```

### Child Processes:
RdpSa.exe

## Signature

* Status: Signature verified.
* Serial: 330000024A0E8AFDF15C662D2B00000000024A
* Thumbprint: 96384A7F5F1C438F32E2454697DC6D312A74517B
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows Publisher, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: MpCmdRun.exe
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 4.18.2004.6 (WinBuild.160101.0800)
* Product Version: 4.18.2004.6
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.

