# Epic file system quest files
## FANF
**Flag:** `   pwn.college{Q0dUM-CLHmp6LURaVkcqriit2aT.QX5IDO0wCOzAzNzEzW}

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.
```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
MESSAGE  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat MESSAGE
Yahaha, you found me!
The next clue is in: /usr/share/racket/pkgs/html-doc/html

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/racket/pkgs/html-doc/html/NUGGET-TRAPPED
Great sleuthing!
The next clue is in: /usr/share/icons/hicolor/192x192/devices

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/icons/hicolor/192x192/devices
cat: /usr/share/icons/hicolor/192x192/devices: Is a directory
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/icons/hicolor/192x192/devices/.CUE
Tubular find!
The next clue is in: /opt/linux/linux-5.4/drivers/mtd/nand/raw

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/drivers/mtd/nand/raw
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/mtd/nand/raw$ ls
BLUEPRINT      cmx270_nand.c    fsl_ifc_nand.c  lpc32xx_slc.c   nand_amd.c    nand_legacy.c    omap2.c        s3c2410.c          tegra_nand.c
Kconfig        cs553x_nand.c    fsl_upm.c       marvell_nand.c  nand_base.c   nand_macronix.c  omap_elm.c     sh_flctl.c         tmio_nand.c
Makefile       davinci_nand.c   fsmc_nand.c     meson_nand.c    nand_bbt.c    nand_micron.c    orion_nand.c   sharpsl.c          txx9ndfmc.c
ams-delta.c    denali.c         gpio.c          mpc5121_nfc.c   nand_bch.c    nand_onfi.c      oxnas_nand.c   sm_common.c        vf610_nfc.c
atmel          denali.h         gpmi-nand       mtk_ecc.c       nand_ecc.c    nand_samsung.c   pasemi_nand.c  sm_common.h        xway_nand.c
au1550nd.c     denali_dt.c      hisi504_nand.c  mtk_ecc.h       nand_esmt.c   nand_timings.c   plat_nand.c    socrates_nand.c
bcm47xxnflash  denali_pci.c     ingenic         mtk_nand.c      nand_hynix.c  nand_toshiba.c   qcom_nandc.c   stm32_fmc2_nand.c
brcmnand       diskonchip.c     internals.h     mxc_nand.c      nand_ids.c    nandsim.c        r852.c         sunxi_nand.c
cafe_nand.c    fsl_elbc_nand.c  lpc32xx_mlc.c   mxic_nand.c     nand_jedec.c  ndfc.c           r852.h         tango_nand.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/mtd/nand/raw$ cat nand_timings.c
// SPDX-License-Identifier: GPL-2.0-only
/*
 *  Copyright (C) 2014 Free Electrons
 *
 *  Author: Boris BREZILLON <boris.brezillon@free-electrons.com>
 */
#include <linux/kernel.h>
#include <linux/err.h>
#include <linux/export.h>

#include "internals.h"

#define ONFI_DYN_TIMING_MAX U16_MAX

static const struct nand_data_interface onfi_sdr_timings[] = {
        /* Mode 0 */
        {
                .type = NAND_SDR_IFACE,
                .timings.sdr = {
                        .tCCS_min = 500000,
                        .tR_max = 200000000,
                        .tADL_min = 400000,
                        .tALH_min = 20000,
                        .tALS_min = 50000,
                        .tAR_min = 25000,
                        .tCEA_max = 100000,
                        .tCEH_min = 20000,
                        .tCH_min = 20000,
                        .tCHZ_max = 100000,
                        .tCLH_min = 20000,
                        .tCLR_min = 20000,
                        .tCLS_min = 50000,
                        .tCOH_min = 0,
                        .tCS_min = 70000,
                        .tDH_min = 20000,
                        .tDS_min = 40000,
                        .tFEAT_max = 1000000,
                        .tIR_min = 10000,
                        .tITC_max = 1000000,
                        .tRC_min = 100000,
                        .tREA_max = 40000,
                        .tREH_min = 30000,
                        .tRHOH_min = 0,
                        .tRHW_min = 200000,
                        .tRHZ_max = 200000,
                        .tRLOH_min = 0,
                        .tRP_min = 50000,
                        .tRR_min = 40000,
                        .tRST_max = 250000000000ULL,
                        .tWB_max = 200000,
                        .tWC_min = 100000,
                        .tWH_min = 30000,
                        .tWHR_min = 120000,
                        .tWP_min = 50000,
                        .tWW_min = 100000,
                },
        },
        /* Mode 1 */
        {
                .type = NAND_SDR_IFACE,
                .timings.sdr = {
                        .tCCS_min = 500000,
                        .tR_max = 200000000,
                        .tADL_min = 400000,
                        .tALH_min = 10000,
                        .tALS_min = 25000,
                        .tAR_min = 10000,
                        .tCEA_max = 45000,
                        .tCEH_min = 20000,
                        .tCH_min = 10000,
                        .tCHZ_max = 50000,
                        .tCLH_min = 10000,
                        .tCLR_min = 10000,
                        .tCLS_min = 25000,
                        .tCOH_min = 15000,
                        .tCS_min = 35000,
                        .tDH_min = 10000,
                        .tDS_min = 20000,
                        .tFEAT_max = 1000000,
                        .tIR_min = 0,
                        .tITC_max = 1000000,
                        .tRC_min = 50000,
                        .tREA_max = 30000,
                        .tREH_min = 15000,
                        .tRHOH_min = 15000,
                        .tRHW_min = 100000,
                        .tRHZ_max = 100000,
                        .tRLOH_min = 0,
                        .tRP_min = 25000,
                        .tRR_min = 20000,
                        .tRST_max = 500000000,
                        .tWB_max = 100000,
                        .tWC_min = 45000,
                        .tWH_min = 15000,
                        .tWHR_min = 80000,
                        .tWP_min = 25000,
                        .tWW_min = 100000,
                },
        },
        /* Mode 2 */
        {
                .type = NAND_SDR_IFACE,
                .timings.sdr = {
                        .tCCS_min = 500000,
                        .tR_max = 200000000,
                        .tADL_min = 400000,
                        .tALH_min = 10000,
                        .tALS_min = 15000,
                        .tAR_min = 10000,
                        .tCEA_max = 30000,
                        .tCEH_min = 20000,
                        .tCH_min = 10000,
                        .tCHZ_max = 50000,
                        .tCLH_min = 10000,
                        .tCLR_min = 10000,
                        .tCLS_min = 15000,
                        .tCOH_min = 15000,
                        .tCS_min = 25000,
                        .tDH_min = 5000,
                        .tDS_min = 15000,
                        .tFEAT_max = 1000000,
                        .tIR_min = 0,
                        .tITC_max = 1000000,
                        .tRC_min = 35000,
                        .tREA_max = 25000,
                        .tREH_min = 15000,
                        .tRHOH_min = 15000,
                        .tRHW_min = 100000,
                        .tRHZ_max = 100000,
                        .tRLOH_min = 0,
                        .tRR_min = 20000,
                        .tRST_max = 500000000,
                        .tWB_max = 100000,
                        .tRP_min = 17000,
                        .tWC_min = 35000,
                        .tWH_min = 15000,
                        .tWHR_min = 80000,
                        .tWP_min = 17000,
                        .tWW_min = 100000,
                },
        },
        /* Mode 3 */
        {
                .type = NAND_SDR_IFACE,
                .timings.sdr = {
                        .tCCS_min = 500000,
                        .tR_max = 200000000,
                        .tADL_min = 400000,
                        .tALH_min = 5000,
                        .tALS_min = 10000,
                        .tAR_min = 10000,
                        .tCEA_max = 25000,
                        .tCEH_min = 20000,
                        .tCH_min = 5000,
                        .tCHZ_max = 50000,
                        .tCLH_min = 5000,
                        .tCLR_min = 10000,
                        .tCLS_min = 10000,
                        .tCOH_min = 15000,
                        .tCS_min = 25000,
                        .tDH_min = 5000,
                        .tDS_min = 10000,
                        .tFEAT_max = 1000000,
                        .tIR_min = 0,
                        .tITC_max = 1000000,
                        .tRC_min = 30000,
                        .tREA_max = 20000,
                        .tREH_min = 10000,
                        .tRHOH_min = 15000,
                        .tRHW_min = 100000,
                        .tRHZ_max = 100000,
                        .tRLOH_min = 0,
                        .tRP_min = 15000,
                        .tRR_min = 20000,
                        .tRST_max = 500000000,
                        .tWB_max = 100000,
                        .tWC_min = 30000,
      ◘  struct nand_data_interface *iface = &chip->data_interface;
                        .tWH_min = 10000,
                        .tWHR_min = 80000,
                        .tWP_min = 15000,
                        .tWW_min = 100000,
                },
        },
        /* Mode 4 */
        {
                .type = NAND_SDR_IFACE,
                .timings.sdr = {
                        .tCCS_min = 500000,
                        .tR_max = 200000000,
                        .tADL_min = 400000,
                        .tALH_min = 5000,
                        .tALS_min = 10000,
                        .tAR_min = 10000,
                        .tCEA_max = 25000,
                        .tCEH_min = 20000,
                        .tCH_min = 5000,
                        .tCHZ_max = 30000,
                        .tCLH_min = 5000,
                        .tCLR_min = 10000,
                        .tCLS_min = 10000,
                        .tCOH_min = 15000,
                        .tCS_min = 20000,
                        .tDH_min = 5000,
                        .tDS_min = 10000,
                        .tFEAT_max = 1000000,
                        .tIR_min = 0,
                        .tITC_max = 1000000,
                        .tRC_min = 25000,
                        .tREA_max = 20000,
                        .tREH_min = 10000,
                        .tRHOH_min = 15000,
                        .tRHW_min = 100000,
                        .tRHZ_max = 100000,
                        .tRLOH_min = 5000,
                        .tRP_min = 12000,
                        .tRR_min = 20000,
                        .tRST_max = 500000000,
                        .tWB_max = 100000,
                        .tWC_min = 25000,
                        .tWH_min = 10000,
                        .tWHR_min = 80000,
                        .tWP_min = 12000,
                        .tWW_min = 100000,
                },
        },
        /* Mode 5 */
        {
                .type = NAND_SDR_IFACE,
                .timings.sdr = {
                        .tCCS_min = 500000,
                        .tR_max = 200000000,
                        .tADL_min = 400000,
                        .tALH_min = 5000,
                        .tALS_min = 10000,
                        .tAR_min = 10000,
                        .tCEA_max = 25000,
                        .tCEH_min = 20000,
                        .tCH_min = 5000,
                        .tCHZ_max = 30000,
                        .tCLH_min = 5000,
                        .tCLR_min = 10000,
                        .tCLS_min = 10000,
                        .tCOH_min = 15000,
                        .tCS_min = 15000,
                        .tDH_min = 5000,
                        .tDS_min = 7000,
                        .tFEAT_max = 1000000,
                        .tIR_min = 0,
                        .tITC_max = 1000000,
                        .tRC_min = 20000,
                        .tREA_max = 16000,
                        .tREH_min = 7000,
                        .tRHOH_min = 15000,
                        .tRHW_min = 100000,
                        .tRHZ_max = 100000,
                        .tRLOH_min = 5000,
                        .tRP_min = 10000,
                        .tRR_min = 20000,
                        .tRST_max = 500000000,
                        .tWB_max = 100000,
                        .tWC_min = 20000,
                        .tWH_min = 7000,
                        .tWHR_min = 80000,
                        .tWP_min = 10000,
                        .tWW_min = 100000,
                },
        },
};

/**
 * onfi_fill_data_interface - [NAND Interface] Initialize a data interface from
 * given ONFI mode
 * @mode: The ONFI timing mode
 */
int onfi_fill_data_interface(struct nand_chip *chip,
                             enum nand_data_interface_type type,
                             int timing_mode)
{
        struct onfi_params *onfi = chip->parameters.onfi;

        if (type != NAND_SDR_IFACE)
                return -EINVAL;

        if (timing_mode < 0 || timing_mode >= ARRAY_SIZE(onfi_sdr_timings))
                return -EINVAL;

        *iface = onfi_sdr_timings[timing_mode];

        /*
         * Initialize timings that cannot be deduced from timing mode:
         * tPROG, tBERS, tR and tCCS.
         * These information are part of the ONFI parameter page.
         */
        if (onfi) {
                struct nand_sdr_timings *timings = &iface->timings.sdr;

                /* microseconds -> picoseconds */
                timings->tPROG_max = 1000000ULL * onfi->tPROG;
                timings->tBERS_max = 1000000ULL * onfi->tBERS;
                timings->tR_max = 1000000ULL * onfi->tR;

                /* nanoseconds -> picoseconds */
                timings->tCCS_min = 1000UL * onfi->tCCS;
        } else {
                struct nand_sdr_timings *timings = &iface->timings.sdr;
                /*
                 * For non-ONFI chips we use the highest possible value for
                 * tPROG and tBERS. tR and tCCS will take the default values
                 * precised in the ONFI specification for timing mode 0,
                 * respectively 200us and 500ns.
                 */

                /* microseconds -> picoseconds */
                timings->tPROG_max = 1000000ULL * ONFI_DYN_TIMING_MAX;
                timings->tBERS_max = 1000000ULL * ONFI_DYN_TIMING_MAX;
                timings->tR_max = 1000000ULL * 200000000ULL;

                /* nanoseconds -> picoseconds */
                timings->tCCS_min = 1000UL * 500000;
        }

        return 0;
}
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/mtd/nand/raw$ cat BLUEPRINT
Lucky listing!
The next clue is in: /usr/share/racket/pkgs/srfi-lib/srfi/%3a64/compiled
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/mtd/nand/raw$ ls /usr/share/racket/pkgs/srfi-lib/srfi/%3a64/compiled
DOSSIER  testing_rkt.dep  testing_rkt.zo
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/mtd/nand/raw$ cat  /usr/share/racket/pkgs/srfi-lib/srfi/%3a64/compiled/DOSSI
ER
Great sleuthing!
The next clue is in: /opt/libslub/.git/objects/78

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/mtd/nand/raw$ cd /opt/libslub/.git/objects/78
hacker@commands~an-epic-filesystem-quest:/opt/libslub/.git/objects/78$ ls
02396e41d769ed7a11acba98cc0e750cf16f0e  EVIDENCE
hacker@commands~an-epic-filesystem-quest:/opt/libslub/.git/objects/78$ cat EVIDENCE
Yahaha, you found me!
The next clue is in: /usr/share/perl/5.30.0/unicore/lib/Ccc

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/libslub/.git/objects/78$ cd /usr/share/perl/5.30.0/unicore/lib/Ccc
hacker@commands~an-epic-filesystem-quest:/usr/share/perl/5.30.0/unicore/lib/Ccc$ ls
A.pl  AL.pl  AR.pl  ATAR.pl  B.pl  BR.pl  DB.pl  NK.pl  NR.pl  OV.pl  VR.pl  WHISPER
hacker@commands~an-epic-filesystem-quest:/usr/share/perl/5.30.0/unicore/lib/Ccc$ cat WHISPER
Tubular find!
The next clue is in: /usr/lib/python3/dist-packages/werkzeug/debug/shared

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/perl/5.30.0/unicore/lib/Ccc$ ls -a /usr/lib/python3/dist-packages/werkzeug/debug/shared
.  ..  .README  console.png  debugger.js  jquery.js  less.png  more.png  source.png  style.css
hacker@commands~an-epic-filesystem-quest:/usr/share/perl/5.30.0/unicore/lib/Ccc$ cat  /usr/lib/python3/dist-packages/werkzeug/debug/shared/.README
Congratulations, you found the clue!
The next clue is in: /usr/share/doc/libavahi-common-data

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/perl/5.30.0/unicore/lib/Ccc$ ls -a /usr/share/doc/libavahi-common-data
.  ..  .ALERT  NEWS.gz  README  changelog.Debian.gz  copyright
hacker@commands~an-epic-filesystem-quest:/usr/share/perl/5.30.0/unicore/lib/Ccc$ cat  /usr/share/doc/libavahi-common-data/README
Avahi is a free, LGPL mDNS/DNS-SD implementation.

Copyright 2004-2009 by the Avahi developers.

        http://avahi.org/

Avahi has a mailing list:

        http://lists.freedesktop.org/mailman/listinfo/avahi

You have a chance to meet the developers on

        #avahi on irc.freenode.org

Please report bugs to the freedesktop.org bugzilla:

        http://bugs.freedesktop.org/

Avahi's SVN repository is freely accessible:

        svn checkout svn://svn.0pointer.de/avahi/trunk avahi

        http://0pointer.de/cgi-bin/viewcvs.cgi/?root=avahi

Avahi has the following requirements:
        - glib2
        - expat
        - libdaemon (http://0pointer.de/lennart/projects/libdaemon/)
        - Linux 2.4 or 2.6
        - DBUS 0.3x (optional, if you disable this, the daemon is not
          accessible over IPC to other applications!)
        - gtk2 + glade (optional, needed for avahi-discover-standalone)
        - doxygen (optional, needed for he API documentaton)
        - Python 2.4, pygtk2 (optional, needed by all client tools)
        - python-twisted (optional, needed by avahi-bookmarks)
    - xmltoman (if building from SVN rather than a tarball)
      If you are not using debian or ubuntu, the upstream authors page has
      disappeared, but you can get the source from debian here
      http://ftp.debian.org/debian/pool/main/x/xmltoman/xmltoman_0.3.orig.tar.gz

Please make sure to read the currently available documentation for avahi before
asking for support on the mailing list:

        - INSTALL
        - Man pages
        - Homepage http://avahi.org/
        - Mailing list archive http://lists.freedesktop.org/archives/avahi/
hacker@commands~an-epic-filesystem-quest:/usr/share/perl/5.30.0/unicore/lib/Ccc$ cat  /usr/share/doc/libavahi-common-data/.ALERT
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{Q0dUM-CLHmp6LURaVkcqriit2aT.QX5IDO0wCOzAzNzEzW}
hacker@commands~an-epic-filesystem-quest:/usr/share/perl/5.30.0/unicore/lib/Ccc$ ^C
hacker@commands~an-epic-filesystem-quest:/usr/share/perl/5.30.0/unicore/lib/Ccc$ ^C
hacker@commands~an-epic-filesystem-quest:/usr/share/perl/5.30.0/unicore/lib/Ccc$ 
```
Rep...
## What I learned
Sometimes --ending-- yourself is not a bad option
## References 
.