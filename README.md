# Information about VM/370 in the modern era

A number of people are discovering VM/370 thanks to the system currently known
as _VM/370 Community Edition_, which is based on IBM's _VM/370 R6 PLC ?_ system.
I discovered it in 1978 as a computer operator at the New Jersey Educational
Computer Network (NJECN), where we ran VM/370 R6 PLC 12 with IBM's _System Extensions
Program Product_ (SEPP).  I then worked with various versions for 20 years, very
intensively.  Here is a collection of information that may be useful to me after
a 20 year break from VM, and maybe others.

# VM/370 Community Edition and predecessors

TODO say something here about Sixpack, and Fourpack

## Distribution	
VM/370 CE is distributed from [vm370.org](http://www.vm370.org/vm).  The distribution
is a ZIP file (_e.g._, [VM370CE.V1.R1.2.zip](http://www.vm370.org/sites/default/files/2022-07/VM370CE.V1.R1.2.zip)
organized for deployment using the Hercules System/370 emulator.

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

* ["VM370/R6 SixPack" version 1.2](documentation/release_notes/sixpack_1.2_readme.txt), dated 2010-10
* ["VM370/R6 SixPack" version 1.3](documentation/release_notes/sixpack_1.3_readme.txt), dated sometime between 2010 and 2021
* ["VM/370 Community Edition" version 1.0](documentation/release_notes/vmce_1.1.0_readme.txt), dated 2021-03-22
* ["VM/370 Community Edition" version 1.1](documentation/release_notes/vmce_1.1.1_readme.txt), dated 2021-05-04
* ["VM/370 Community Edition" version 1.2](documentation/release_notes/vmce_1.1.2_readme.txt), dated 2022-07-22

## Major changes

### CP
HRC001DK V01 RECALL LAST COMMAND(S) VIA PF KEY
HRC003DK V01 LEAVE OPTION ON DETACH COMMAND
HRC004DK V01 ENABLE SUPPORT FOR 4K STORAGE KEYS
HRC006DK V01 FIX TO TRAP AND HIDE DSP003 ABENDS
HRC009DK V01 DISPLAY REAL VOL FOR TDSK DISK RATHER THAN TDSK
HRC011DK V01 ADD 3380 MDISK/DEDICATED DEVICE SUPPORT
HRC012DK V01 3380 SUPPORT FOR DDR
HRC013DK V01 UNIVERSITY OF MAINE P.E.R. TRACE FACILITY
HRC014DK V01 LNKNOPAS DIRECTORY OPTION
HRC016DK V01 CHANGE NAME OF USER TO BE AUTOLOGGED TO "AUTOLOG1-9"
HRC017DK V01 ELIMINATE TRAILER AND ALARM FOR MSGNOH COMMAND
HRC022DK V01 IMPLEMENT THE ENHANCED TRANSFER COMMAND
HRC026DK V01 RE-CLASSIFY CERTAIN COMMAND PRIVILEGES
HRC027DK V01 CHANGE CYLINDER FROM HEX TO DECIMAL.
HRC035DK V01 ADD SUPPORT FOR FRET TRAP
HRC036DK V01 ADD SYSIPL MACRO FOR DEFAULT START
HRC058DK V03 DIAG 58 SUPPORT
HRC065DK V01 LOGICAL DEVICE SUPPORT FACILITY
HRC068DK V01 Shadow table bypass support
HRC075DK V01 Alternate nucleus support
HRC076DK V01 SHUTDOWN REIPL support
HRC101DK V02 TERMINAL ENHANCEMENTS LIKE Z/VM
HRC107DK H40 Add QUERY USERID command
HRC108DK H40 Implement SYSID
HRC450DK V01 Support APL character set for 3278 emulators
HRC451DK V01 Show lowercase alphabetics in DISPLAY storage cmds
HRC452DK V01 Support ;BASE specification on DISPLAY command
HRC700DK V01 Support for DIAG00 to return timezone offset

### CMS
UPDTVMCF - Switch SMSG from IUCV to VMCF for VM/370
HRC001DS V01 ADD QUERY CMSLEVEL         TO MATCH VM/SP - QUERY
HRC002DS V01 ADD MORE MINIDISKS & TAPES TO MATCH VM/SP
HRC003DS V01 ENHANCE Q DISK             TO MATCH VM/SP - QUERY
HRC004DS V01 ADD SUPPORT FOR D/T3380
HRC005DS V01 ADD FULL DATE SUPPORT
HRC008DS V01 ALLOW CERTAIN COMMANDS TO WORK UPWARDS AS WELL AS FORWARD
HRC009DS V01 IMPLEMENT SUPPORT FOR SET ABEND COMMAND
HRC010DS V01 ACCESS EMPTY R/O DISK & R/O MODE 0
HRC011DS V01 CHANGE READY PROMPT TO MATCH CURRENT FLAVORS OF CMS
HRC012DS V01 ADD ADDITIONAL CHARACTERS FOR FILE NAME
HRC073DS V01 ADD EDIT SUPPORT OF 3278 MODEL 5 TERMINALS
HRC101DS V02 IMPLEMENT SUPPORT FOR STACK OPTION
HRC105DS H40 Extend FSTD / STATEFST for greater VM/SP compatibility
HRC106DS H40 Accept FORM=E for greater VM/SP compatibility
HRC309DS V03 supply extended PLIST to CMS commands
HRC321DS v03 add FIFO and LIFO options
HRC322DS V03 CMSLEVEL now obeys stack optn, all msgs lowercase
HRC350DS v03 Add FIFO, LIFO, DISCARD operand to CP command.
HRC371DS 1.2 Support execution of REXX programs as filetype EXEC
HRC371DS V03 Invoke SYSPROF EXEC (it it exists) before PROFILE EXEC.
HRC400DS V01 add Halt Interpretor, Trace Start, and Trace End cmds
HRC401DS V01 SUPPORT SET INPUT AND SET OUTPUT TABLES IN EDIT
HRC402DS V01 Support execution of REXX programs as filetype EXEC
HRC404DS V01 NUCEXT and SUBCOM support
HRC406DS V01 Support for MAKEBUF, DROPBUF, and SENTRIES
HRC407DS V01 Add SET EXECTRAC command for REXX
HRC408DS V01 Support call type X'05' for REXX functions
HRC411DS V01 Add EXECIO command to VM/370
HRC415DS V01 Reorganize CMS Nucleus to reside in High Memory
HRC416DS V01 Support for IDENTIFY command
HRC417DS V01 Support RDTERM TYPE=DIRECT for REXX tracing
HRC425DS V01 QUERY CMSTYPE and SET CMSTYPE
HRC431DS V01 Support NUCXMAP name operand, STACK, and ATTRIBUTE options

### RSCS
None.

# VM/370 Release 6 from IBM

