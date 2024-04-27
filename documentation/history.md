# History of VM/370 Community Edition and its predecessors

## Sources
Most of this history started with Dave Wade's VM/370 page at
http://www.smrcc.org.uk/members/g4ugm/VM370.htm, which is offline as of 2024-04-05,
but which the [Internet Archive](https://archive.org) saved on 
[2022-12-07](https://web.archive.org/web/20221217015227/http://www.smrcc.org.uk/members/g4ugm/VM370.htm).

As Dave says there:

> *** Important *** Please use VM/CE, which you will find [HERE](http://vm370.org/vm),
> as it contains new features and fixes ****

Some of it came from WELCOME HELPOLD2 on MAINT 19D from VM/CE 1.2.

## Distributions

### IBM VM/370 Release 6
Everything started with the last publicly-available release of VM/370 from IBM.
IBM packaged "Program Level Change" (PLC) updates for VM/370, but it isn't clear
which R6 PLC was the starting point for all these systems.

### Bob Abeles's Original System
In 2000-11, Bob Abeles released a copy of the IBM VM/370 R6 distribution in
its original form - two "tapes" created with the VM/370 _DASD Dump Restore_ (DDR)
program, which need to be restored to 3330 disks.  This is exactly how a new IBM
customer would have installed VM on their new System/370.  The original IBM
distribution tapes are stored as [AWS](https://xmi.readthedocs.io/en/latest/virtualtape.html)
tapes that Hercules and other S/370`emulators can process.

A couple of extra things to note:

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
