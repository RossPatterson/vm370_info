# Information about VM/370 in the modern era

A number of people are discovering VM/370 thanks to the system currently known
as _VM/370 Community Edition_, which is based on IBM's _VM/370 R6 PLC ?_ system.
I discovered it in 1978 as a computer operator at the New Jersey Educational
Computer Network (NJECN), where we ran VM/370 R6 PLC 12 with IBM's _System Extensions
Program Product_ (SEPP).  I then worked with various versions for 20 years, very
intensively.  Here is a collection of information that may be useful to me after
a 20 year break from VM, and maybe others.

# VM/370 Community Edition

## History
There is a history of public VM releases available [here](documentation/history.md).

## Bugs
Bugs can be reported by opening an issue at Harold Grovesteen's [vm370 GitHub repository](https://github.com/s390guy/vm370/issues).

# Differences from IBM's original VM/370 Release 6


# Documentation

## IBM Documentation

Most of the [original VM/370 Release 6 documentation](documentation/library.md) is
available in PDF form from bitsavers.org at https://bitsavers.org/pdf/ibm/370/VM/370/Release_6/,
albeit at a variety of Program Level Change (PLC) levels.

## Release Notes
Release notes for some of the post-IBM releases of VM/370 are stored on the web, and
are also included in the VM/370 Community Edition distribution ZIP files (_e.g._,
VM370CE.V1.R1.2/readme-1_2.txt).

* [Bob Abeles' ThreePack](documentation/release_notes/threepack_readme.txt), dated 2000-11
* ["VM370/R6 SixPack" version 1.2](documentation/release_notes/sixpack_1.2_readme.txt), dated 2010-10
* ["VM370/R6 SixPack" version 1.3](documentation/release_notes/sixpack_1.3_readme.txt), dated sometime between 2010 and 2021
* ["VM/370 Community Edition" version 1.0](documentation/release_notes/vmce_1.1.0_readme.txt), dated 2021-03-22
* ["VM/370 Community Edition" version 1.1](documentation/release_notes/vmce_1.1.1_readme.txt), dated 2021-05-04
* ["VM/370 Community Edition" version 1.2](documentation/release_notes/vmce_1.1.2_readme.txt), dated 2022-07-22

## Major changes

### CP
* [HRC001DK](hrc_mods/HRC001DK.MEMO.txt) RECALL LAST COMMAND(S) VIA PF KEY
* [HRC002DK](hrc_mods/HRC002DK.MEMO.txt) POWEROFF AT SHUTDOWN
* [HRC003DK](hrc_mods/HRC003DK.MEMO.txt) LEAVE OPTION ON DETACH COMMAND
* [HRC004DK](hrc_mods/HRC004DK.MEMO.txt) ENABLE SUPPORT FOR 4K STORAGE KEYS
* [HRC006DK](hrc_mods/HRC006DK.MEMO.txt) FIX TO TRAP AND HIDE DSP003 ABENDS
* [HRC009DK](hrc_mods/HRC009DK.MEMO.txt) DISPLAY REAL VOL FOR TDSK DISK RATHER THAN TDSK
* [HRC011DK](hrc_mods/HRC011DK.MEMO.txt) ADD 3380 MDISK/DEDICATED DEVICE SUPPORT
* [HRC012DK](hrc_mods/HRC012DK.MEMO.txt) 3380 SUPPORT FOR DDR
* [HRC013DK](hrc_mods/HRC013DK.MEMO.txt) UNIVERSITY OF MAINE P.E.R. TRACE FACILITY
* [HRC014DK](hrc_mods/HRC014DK.MEMO.txt) LNKNOPAS DIRECTORY OPTION
* [HRC016DK](hrc_mods/HRC016DK.MEMO.txt) CHANGE NAME OF USER TO BE AUTOLOGGED TO "AUTOLOG1-9"
* [HRC017DK](hrc_mods/HRC017DK.MEMO.txt) ELIMINATE TRAILER AND ALARM FOR MSGNOH COMMAND
* [HRC018DK](hrc_mods/HRC018DK.MEMO.txt) IMPLEMENT EXTENDED HRC SET FUNCTIONS
* [HRC019DK](hrc_mods/HRC019DK.MEMO.txt) IMPLEMENT EXTENDED HRC SET FUNCTIONS
* [HRC021DK](hrc_mods/HRC021DK.MEMO.txt) SUPPORT PREFIX PERIOD CONSOLE OUTPUT SUPPRESSION
* [HRC022DK](hrc_mods/HRC022DK.MEMO.txt) IMPLEMENT THE ENHANCED TRANSFER COMMAND
* [HRC026DK](hrc_mods/HRC026DK.MEMO.txt) RE-CLASSIFY CERTAIN COMMAND PRIVILEGES
* [HRC027DK](hrc_mods/HRC027DK.MEMO.txt) CHANGE CYLINDER FROM HEX TO DECIMAL.
* [HRC030DK](hrc_mods/HRC030DK.MEMO.txt) QUERY ALLOC COMMAND
* [HRC035DK](hrc_mods/HRC035DK.MEMO.txt) ADD SUPPORT FOR FRET TRAP
* [HRC058DK](hrc_mods/HRC058DK.MEMO.txt) DIAG 58 SUPPORT
* [HRC065DK](hrc_mods/HRC065DK.MEMO.txt) LOGICAL DEVICE SUPPORT FACILITY
* [HRC068DK](hrc_mods/HRC068DK.MEMO.txt) Shadow table bypass support
* [HRC075DK](hrc_mods/HRC075DK.MEMO.txt) Alternate nucleus support
* [HRC076DK](hrc_mods/HRC076DK.MEMO.txt) SHUTDOWN REIPL support
* [HRC101DK](hrc_mods/HRC101DK.MEMO.txt) TERMINAL ENHANCEMENTS LIKE Z/VM
* [HRC107DK](hrc_mods/HRC107DK.MEMO.txt) Add QUERY USERID command
* [HRC108DK](hrc_mods/HRC108DK.MEMO.txt) Implement SYSID
* [HRC450DK](hrc_mods/HRC450DK.MEMO.txt) Support APL character set for 3278 emulators
* [HRC451DK](hrc_mods/HRC451DK.MEMO.txt) Show lowercase alphabetics in DISPLAY storage cmds
* HRC452DK Support ;BASE specification on DISPLAY command
* HRC700DK Support for DIAG00 to return timezone offset

### CMS
* [HRC001DS](hrc_mods/HRC001DS.MEMO.txt) ADD QUERY CMSLEVEL         TO MATCH VM/SP - QUERY
* [HRC002DS](hrc_mods/HRC002DS.MEMO.txt) ADD MORE MINIDISKS & TAPES TO MATCH VM/SP
* [HRC003DS](hrc_mods/HRC003DS.MEMO.txt) ENHANCE Q DISK             TO MATCH VM/SP - QUERY
* [HRC005DS](hrc_mods/HRC005DS.MEMO.txt) ADD FULL DATE SUPPORT
* [HRC009DS](hrc_mods/HRC009DS.MEMO.txt) IMPLEMENT SUPPORT FOR SET ABEND COMMAND
* [HRC010DS](hrc_mods/HRC010DS.MEMO.txt) ACCESS EMPTY R/O DISK & R/O MODE 0
* [HRC012DS](hrc_mods/HRC012DS.MEMO.txt) ADD ADDITIONAL CHARACTERS FOR FILE NAME
* [HRC101DS](hrc_mods/HRC101DS.MEMO.txt) IMPLEMENT SUPPORT FOR STACK OPTION
* [HRC105DS](hrc_mods/HRC105DS.MEMO.txt) Extend FSTD / STATEFST for greater VM/SP compatibility
* [HRC106DS](hrc_mods/HRC106DS.MEMO.txt) Accept FORM=E for greater VM/SP compatibility
* [HRC309DS](hrc_mods/HRC309DS.MEMO.txt) supply extended PLIST to CMS commands
* [HRC321DS](hrc_mods/HRC321DS.MEMO.txt) add FIFO and LIFO options
* [HRC322DS](hrc_mods/HRC322DS.MEMO.txt) CMSLEVEL now obeys stack optn, all msgs lowercase
* [HRC350DS](hrc_mods/HRC350DS.MEMO.txt) Add FIFO, LIFO, DISCARD operand to CP command.
* [HRC371DS](hrc_mods/HRC371DS.MEMO.txt) Support execution of REXX programs as filetype EXEC
* [HRC371DS](hrc_mods/HRC371DS.MEMO.txt) Invoke SYSPROF EXEC (it it exists) before PROFILE EXEC.
* [HRC400DS](hrc_mods/HRC400DS.MEMO.txt) add Halt Interpretor, Trace Start, and Trace End cmds
* [HRC402DS](hrc_mods/HRC402DS.MEMO.txt) Support execution of REXX programs as filetype EXEC
* [HRC404DS](hrc_mods/HRC404DS.MEMO.txt) NUCEXT and SUBCOM support
* [HRC406DS](hrc_mods/HRC406DS.MEMO.txt) Support for MAKEBUF, DROPBUF, and SENTRIES
* [HRC407DS](hrc_mods/HRC407DS.MEMO.txt) Add SET EXECTRAC command for REXX
* [HRC408DS](hrc_mods/HRC408DS.MEMO.txt) Support call type X'05' for REXX functions
* [HRC411DS](hrc_mods/HRC411DS.MEMO.txt) Add EXECIO command to VM/370
* [HRC415DS](hrc_mods/HRC415DS.MEMO.txt) Reorganize CMS Nucleus to reside in High Memory
* [HRC416DS](hrc_mods/HRC416DS.MEMO.txt) Support for IDENTIFY command
* [HRC417DS](hrc_mods/HRC417DS.MEMO.txt) Support RDTERM TYPE=DIRECT for REXX tracing
* [HRC425DS](hrc_mods/HRC425DS.MEMO.txt) QUERY CMSTYPE and SET CMSTYPE
* HRC431DS Support NUCXMAP name operand, STACK, and ATTRIBUTE options

### RSCS
None.

# VM/370 Release 6 from IBM

# Stuff from the VM Community

## The "Waterloo" tapes

## The "VM Workshop" tapes

## VMSHARE

http://vm.marist.edu/~vmshare/

http://vm.marist.edu/~vmshare/browse.cgi?fn=$AD&ft=MEMO

## Interesting websites

* The "Wizard Of Odd CODEX"'s section on [IBM 360/370 Mainframe Architectures](https://codex.sjzoppi.com/ibm360-370:start)
is largely focused on VM/370 systems running under Hercules.
* Jay Maynard's site: https://www.ibiblio.org/jmaynard/
