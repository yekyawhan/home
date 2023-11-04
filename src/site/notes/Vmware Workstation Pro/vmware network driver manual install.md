---
{"tags":["vmware"],"dg-publish":true,"permalink":"/vmware-workstation-pro/vmware-network-driver-manual-install/","dgPassFrontmatter":true,"noteIcon":""}
---


## pnputil

- Run below command as administrator:

pnputil /add-driver _<a full path to the inf file>_ /install    _or_    pnputil -i -a _<a full path to the inf file>_

![VMware_drivers_7](https://kb.vmware.com/servlet/rtaImage?eid=ka05G000001hhSz&feoid=00Nf400000Tyi5M&refid=0EM5G000007YBuj)

  
**Note:**  
System reboot may be required to complete the operation.

#### Notes

- _Some drivers may requires restart OS after install driver successfully._
- _Verify if your driver runs normally (in Device Manager or System Information) after installing please._

## Uninstall

## Device Manager

1. Launch Device Manager.
2. Right-click the device you want to uninstall.
3. Click Uninstall.
4. Windows will prompt you to confirm the device’s removal. Check "Delete the driver software for this device", click OK to remove the driver.

## **pnputil**

- Run below command as administrator:

pnputil /delete-driver <the .inf file of the driver to be uninstalled, it is named like oem#.inf> /uninstall /force