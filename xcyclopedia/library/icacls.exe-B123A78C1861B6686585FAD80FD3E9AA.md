﻿
# icacls.exe 
* File Path: `C:\Windows\SysWOW64\icacls.exe`
* Description: 
* Comments: 

## Hashes
Type | Hash
-- | --
MD5 | `B123A78C1861B6686585FAD80FD3E9AA`
SHA1 | `95D063153A3535F3C1F0AABEB3ED396D04E5E5C1`
SHA256 | `A1BD6ADB57EFD737C0ABC1BE4D4E732B54AFAAED42FC4E077522FA4DC88B5CA6`
SHA384 | `42D2190C82E9D487F11900A419C07401E1986CDFA67ECE261B83969309306E70F9958BF32700E5458C0D153F1C1B3420`
SHA415 | `38867CB3195D0D09E958AE9F96B88ABA0333473BF597CF0856B26E9E05E74C3944D1E009289034DBF2B781563E23D6F07FE07CBC752C9F430A910A3468657FB8`
SSDEEP | `768:kv0pBuur32t8DPh+vT2CdCCGfEBLlYXD:kGBXmtyP6TSEBLlY`

## Runtime Data
### Usage (stdout):
```Batchfile

ICACLS name /save aclfile [/T] [/C] [/L] [/Q]
    stores the DACLs for the files and folders that match the name
    into aclfile for later use with /restore. Note that SACLs,
    owner, or integrity labels are not saved.

ICACLS directory [/substitute SidOld SidNew [...]] /restore aclfile
                 [/C] [/L] [/Q]
    applies the stored DACLs to files in directory.

ICACLS name /setowner user [/T] [/C] [/L] [/Q]
    changes the owner of all matching names. This option does not
    force a change of ownership; use the takeown.exe utility for
    that purpose.

ICACLS name /findsid Sid [/T] [/C] [/L] [/Q]
    finds all matching names that contain an ACL
    explicitly mentioning Sid.

ICACLS name /verify [/T] [/C] [/L] [/Q]
    finds all files whose ACL is not in canonical form or whose
    lengths are inconsistent with ACE counts.

ICACLS name /reset [/T] [/C] [/L] [/Q]
    replaces ACLs with default inherited ACLs for all matching files.

ICACLS name [/grant[:r] Sid:perm[...]]
       [/deny Sid:perm [...]]
       [/remove[:g|:d]] Sid[...]] [/T] [/C] [/L] [/Q]
       [/setintegritylevel Level:policy[...]]

    /grant[:r] Sid:perm grants the specified user access rights. With :r,
        the permissions replace any previously granted explicit permissions.
        Without :r, the permissions are added to any previously granted
        explicit permissions.

    /deny Sid:perm explicitly denies the specified user access rights.
        An explicit deny ACE is added for the stated permissions and
        the same permissions in any explicit grant are removed.

    /remove[:[g|d]] Sid removes all occurrences of Sid in the ACL. With
        :g, it removes all occurrences of granted rights to that Sid. With
        :d, it removes all occurrences of denied rights to that Sid.

    /setintegritylevel [(CI)(OI)]Level explicitly adds an integrity
        ACE to all matching files.  The level is to be specified as one
        of:
            L[ow]
            M[edium]
            H[igh]
        Inheritance options for the integrity ACE may precede the level
        and are applied only to directories.

    /inheritance:e|d|r
        e - enables inheritance
        d - disables inheritance and copy the ACEs
        r - remove all inherited ACEs


Note:
    Sids may be in either numerical or friendly name form. If a numerical
    form is given, affix a * to the start of the SID.

    /T indicates that this operation is performed on all matching
        files/directories below the directories specified in the name.

    /C indicates that this operation will continue on all file errors.
        Error messages will still be displayed.

    /L indicates that this operation is performed on a symbolic link
       itself versus its target.

    /Q indicates that icacls should suppress success messages.

    ICACLS preserves the canonical ordering of ACE entries:
            Explicit denials
            Explicit grants
            Inherited denials
            Inherited grants

    perm is a permission mask and can be specified in one of two forms:
        a sequence of simple rights:
                N - no access
                F - full access
                M - modify access
                RX - read and execute access
                R - read-only access
                W - write-only access
                D - delete access
        a comma-separated list in parentheses of specific rights:
                DE - delete
                RC - read control
                WDAC - write DAC
                WO - write owner
                S - synchronize
                AS - access system security
                MA - maximum allowed
                GR - generic read
                GW - generic write
                GE - generic execute
                GA - generic all
                RD - read data/list directory
                WD - write data/add file
                AD - append data/add subdirectory
                REA - read extended attributes
                WEA - write extended attributes
                X - execute/traverse
                DC - delete child
                RA - read attributes
                WA - write attributes
        inheritance rights may precede either form and are applied
        only to directories:
                (OI) - object inherit
                (CI) - container inherit
                (IO) - inherit only
                (NP) - don't propagate inherit
                (I) - permission inherited from parent container

Examples:

        icacls c:\windows\* /save AclFile /T
        - Will save the ACLs for all files under c:\windows
          and its subdirectories to AclFile.

        icacls c:\windows\ /restore AclFile
        - Will restore the Acls for every file within
          AclFile that exists in c:\windows and its subdirectories.

        icacls file /grant Administrator:(D,WDAC)
        - Will grant the user Administrator Delete and Write DAC
          permissions to file.

        icacls file /grant *S-1-1-0:(D,WDAC)
        - Will grant the user defined by sid S-1-1-0 Delete and
          Write DAC permissions to file.

```

### Usage (stderr):
```Batchfile
First parameter must be a file name pattern or "/?"

```

### Child Processes:


## Signature

* Status: Signature verified.
* Serial: 33000000BCE120FDD27CC8EE930000000000BC
* Thumbprint: E85459B23C232DB3CB94C7A56D47678F58E8E51E
* Issuer: CN=Microsoft Windows Production PCA 2011, O=Microsoft Corporation, L=Redmond, S=Washington, C=US
* Subject: CN=Microsoft Windows, O=Microsoft Corporation, L=Redmond, S=Washington, C=US

## File Metadata

* Original Filename: iCACLS.EXE.MUI
* Product Name: Microsoft Windows Operating System
* Company Name: Microsoft Corporation
* File Version: 10.0.14393.0 (rs1_release.160715-1616)
* Product Version: 10.0.14393.0
* Language: English (United States)
* Legal Copyright:  Microsoft Corporation. All rights reserved.

