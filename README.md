# Information about VM/370 in the modern era

A number of people are discovering VM/370 thanks to the system currently known
as _VM/370 Community Edition_, which is based on IBM's _VM/370 R6 PLC ?_ system.
I discovered it in 1978 as a computer operator at the New Jersey Educational
Computer Network (NJECN), where we ran VM/370 R6 PLC 12 with IBM's _System Extensions
Program Product_ (SEPP).  I then worked with various versions for 20 years, very
intensively.  Here is a collection of information that may be useful to me after
a 20 year break from VM, and maybe others.

# VM/370 Community Edition and predecessors

## History
Most of this history section started with Dave Wade's VM/370 page at
http://www.smrcc.org.uk/members/g4ugm/VM370.htm, which is offline as of 2024-04-05,
but which the [Internet Archive](https://archive.org) saved on 
[2022-12-07](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/VM370.htm).

As Dave says there:

*** Important *** Please use VM/CE, which you will find [HERE](http://vm370.org/vm),
as it contains new features and fixes ****

### Bob Abeles's Original 3-Pack System
This is Bob Abeles's original distribution. Unlike the later systems which are
distributed as "ready to IPL" DASD, this system is distributed as [AWS](???) tapes
that need to be restored to 3330 packs. A couple of extra things to note:

1. Due an incompatibility between Hercules (and P/370 & P/390 systems) and DDR if
you follow Bob's original instructions Hercules will loop at the end of each
restore. Simply re-wind and re-ipl the DDR tape or add the `(leave` option to the
DDR `input` statement cards.

1. Recent releases of Hercules default to ESA architecture. An `ARCHMODE S/370`
or `ARCHLEVEL S/370` statement needs to be added to the Hercules configuraton,
as VM/370 does not understand ESA machines.

You need these files to get a system up and running:-

* [vm370r6-essentials.tar.gz](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/vm370r6-essentials.tar.gz)
* [CPR6L0.ddr.aws.bz2](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/CPR6L0.ddr.aws.bz2)
* [VMREL6.ddr.aws.bz2](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/VMREL6.ddr.aws.bz2)
* [README.txt](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/README.txt)

These are optional:

* [base-source.aws.bz2](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/base-source.aws.bz2)
* [ptf-616.aws.bz2](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/ptf-616.aws.bz2)
* [starter-3330.aws.bz2](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/starter-3330.aws.bz2)
* [waterloo.aws.bz2](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/waterloo.aws.bz2)

You will also need [BZIP2](http://www.bzip.org/) to unpack those downloaded files.

### Andy Norrie's 4-Pack system

Andy Norrie built atop Bob Abeles's system.  He put a lot of effort into re-working
and cross checking the patches.

* [vmsys.zip](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/vmsys.zip)

### Paul Gorlinsky's 5-Pack System

In 2006, Paul Gorlinsky released the "5-Pack" VM/370 system.  As Dave wrote, "_It has all of Andy's fixes, plus many enhancements that make it an almost useable system_."

* [VMDIST.zip](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/VMDIST.zip),
released in 2006.

### Robert O'Hara's Six Pack
In 2009, Bob O'Hara, one of the early IBM VM/370 programmers, [announced](https://h390-vm.yahoogroups.narkive.com/j5oaE1OC/announcing-the-vm-370-sixpack-version-1-0)
Release 1.0 of the "SixPack" system.  As he wrote, it '_rolls up all of the modifications
posted on the H390-VM and Hercules-os380 Yahoo groups since the "5-pack" system was released
in 2006._'  As with earlier systems, the name comes from the fact that it is organized as
6 3350 disks.  Bob's annoucement credited "_Robert O'Hara, Paul Edwards, and Dave Wade. It is based on earlier versions of VM/370 for Hercules developed by Andy Norrie and Paul Gorlinsky._"

Bob delivered 3 versions of the SixPack:
* [vm370sixpack-1_0.zip](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/vm370sixpack-1_0.zip), Release 1.0, dataed 2009.
* [vm370sixpack1_1.zip[(https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/vm370sixpack1_1.zip), Release 1.1, dated ???
* [vm370sixpack-1_2.zip](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/vm-370/vm370sixpack-1_2.zip), Release 1.2, dated ???

### VM/370 Community Edition
In 2021, several folks were preparing a new update to the SixPack system.  A [discussion](https://groups.io/g/h390-vm/topic/what_do_we_call_it/79201407)
ensued about how to name the new system, and they settled on "VM/370 Community Edition".  The most
recent distribution is from 2022-07-22, and is available at the [vm370.org](http://www.vm370.org/vm)
website.  Like the the 4, 5, and 6-pack systems, the distribution is a ZIP file (_e.g._,
[VM370CE.V1.R1.2.zip](http://www.vm370.org/sites/default/files/2022-07/VM370CE.V1.R1.2.zip)
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

* [Bob Abeles' ThreePack](documentation/release_notes/threepack_readme.txt), undated
* ["VM370/R6 SixPack" version 1.2](documentation/release_notes/sixpack_1.2_readme.txt), dated 2010-10
* ["VM370/R6 SixPack" version 1.3](documentation/release_notes/sixpack_1.3_readme.txt), dated sometime between 2010 and 2021
* ["VM/370 Community Edition" version 1.0](documentation/release_notes/vmce_1.1.0_readme.txt), dated 2021-03-22
* ["VM/370 Community Edition" version 1.1](documentation/release_notes/vmce_1.1.1_readme.txt), dated 2021-05-04
* ["VM/370 Community Edition" version 1.2](documentation/release_notes/vmce_1.1.2_readme.txt), dated 2022-07-22

## Major changes

### CP
* HRC001DK V01 RECALL LAST COMMAND(S) VIA PF KEY
* HRC003DK V01 LEAVE OPTION ON DETACH COMMAND
* HRC004DK V01 ENABLE SUPPORT FOR 4K STORAGE KEYS
* HRC006DK V01 FIX TO TRAP AND HIDE DSP003 ABENDS
* HRC009DK V01 DISPLAY REAL VOL FOR TDSK DISK RATHER THAN TDSK
* HRC011DK V01 ADD 3380 MDISK/DEDICATED DEVICE SUPPORT
* HRC012DK V01 3380 SUPPORT FOR DDR
* HRC013DK V01 UNIVERSITY OF MAINE P.E.R. TRACE FACILITY
* [HRC014DK](hrc_mods/HRC014DK.MEMO.txt) V01 LNKNOPAS DIRECTORY OPTION

  Users with this option bypass PASSWORD checking for minidisk links.
* HRC016DK V01 CHANGE NAME OF USER TO BE AUTOLOGGED TO "AUTOLOG1-9"
* HRC017DK V01 ELIMINATE TRAILER AND ALARM FOR MSGNOH COMMAND
* HRC022DK V01 IMPLEMENT THE ENHANCED TRANSFER COMMAND
* HRC026DK V01 RE-CLASSIFY CERTAIN COMMAND PRIVILEGES
* HRC027DK V01 CHANGE CYLINDER FROM HEX TO DECIMAL.
* HRC035DK V01 ADD SUPPORT FOR FRET TRAP
* HRC036DK V01 ADD SYSIPL MACRO FOR DEFAULT START
* HRC058DK V03 DIAG 58 SUPPORT
* HRC065DK V01 LOGICAL DEVICE SUPPORT FACILITY
* HRC068DK V01 Shadow table bypass support
* HRC075DK V01 Alternate nucleus support
* HRC076DK V01 SHUTDOWN REIPL support
* HRC101DK V02 TERMINAL ENHANCEMENTS LIKE Z/VM
* HRC107DK H40 Add QUERY USERID command
* HRC108DK H40 Implement SYSID
* HRC450DK V01 Support APL character set for 3278 emulators
* HRC451DK V01 Show lowercase alphabetics in DISPLAY storage cmds
* HRC452DK V01 Support ;BASE specification on DISPLAY command
* HRC700DK V01 Support for DIAG00 to return timezone offset

### CMS
* UPDTVMCF - Switch SMSG from IUCV to VMCF for VM/370
* HRC001DS V01 ADD QUERY CMSLEVEL         TO MATCH VM/SP - QUERY
* HRC002DS V01 ADD MORE MINIDISKS & TAPES TO MATCH VM/SP
* HRC003DS V01 ENHANCE Q DISK             TO MATCH VM/SP - QUERY
* HRC004DS V01 ADD SUPPORT FOR D/T3380
* HRC005DS V01 ADD FULL DATE SUPPORT
* HRC008DS V01 ALLOW CERTAIN COMMANDS TO WORK UPWARDS AS WELL AS FORWARD
* HRC009DS V01 IMPLEMENT SUPPORT FOR SET ABEND COMMAND
* HRC010DS V01 ACCESS EMPTY R/O DISK & R/O MODE 0
* HRC011DS V01 CHANGE READY PROMPT TO MATCH CURRENT FLAVORS OF CMS
* HRC012DS V01 ADD ADDITIONAL CHARACTERS FOR FILE NAME
* HRC073DS V01 ADD EDIT SUPPORT OF 3278 MODEL 5 TERMINALS
* HRC101DS V02 IMPLEMENT SUPPORT FOR STACK OPTION
* HRC105DS H40 Extend FSTD / STATEFST for greater VM/SP compatibility
* HRC106DS H40 Accept FORM=E for greater VM/SP compatibility
* HRC309DS V03 supply extended PLIST to CMS commands
* HRC321DS v03 add FIFO and LIFO options
* HRC322DS V03 CMSLEVEL now obeys stack optn, all msgs lowercase
* HRC350DS v03 Add FIFO, LIFO, DISCARD operand to CP command.
* HRC371DS 1.2 Support execution of REXX programs as filetype EXEC
* HRC371DS V03 Invoke SYSPROF EXEC (it it exists) before PROFILE EXEC.
* HRC400DS V01 add Halt Interpretor, Trace Start, and Trace End cmds
* HRC401DS V01 SUPPORT SET INPUT AND SET OUTPUT TABLES IN EDIT
* HRC402DS V01 Support execution of REXX programs as filetype EXEC
* HRC404DS V01 NUCEXT and SUBCOM support
* HRC406DS V01 Support for MAKEBUF, DROPBUF, and SENTRIES
* HRC407DS V01 Add SET EXECTRAC command for REXX
* HRC408DS V01 Support call type X'05' for REXX functions
* HRC411DS V01 Add EXECIO command to VM/370
* HRC415DS V01 Reorganize CMS Nucleus to reside in High Memory
* HRC416DS V01 Support for IDENTIFY command
* HRC417DS V01 Support RDTERM TYPE=DIRECT for REXX tracing
* HRC425DS V01 QUERY CMSTYPE and SET CMSTYPE
* HRC431DS V01 Support NUCXMAP name operand, STACK, and ATTRIBUTE options

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
