## Overview

Here is ACPI dump produced by acpidump (man 8 acpidump) from HP Probook 455G7:
 * acpdump.aml
 * acpdump.asl

Here is patched version with slight fix:
 * my.aml
 * my.asl
 
The subtle is increase of array for thermal zone to avoid error like:
```
[1273] Firmware Error (ACPI): AE_AML_PACKAGE_LIMIT, Index (0x000000005) is beyond end of object (length 0x5) (20210930/exoparg2-569)
[1273] ACPI Error: Aborting method \134_TZ.GTTP due to previous error (AE_AML_PACKAGE_LIMIT) (20210930/psparse-689)
[1273] ACPI Error: Aborting method \134_TZ.CHGZ._TMP due to previous error (AE_AML_PACKAGE_LIMIT) (20210930/psparse-689)
```

To get more details about usage, please check OS documentation. 
In case of FreeBSD here is: 

[https://docs.freebsd.org/en/books/handbook/config/#_overriding_the_default_aml]

THIS MAY DAMAGE YOUR COMPUTER! USE AT YOUR OWN RISK.
