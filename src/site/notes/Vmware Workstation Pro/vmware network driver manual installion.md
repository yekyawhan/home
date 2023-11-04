---
{"tags":["vmware"],"dg-publish":true,"permalink":"/vmware-workstation-pro/vmware-network-driver-manual-installion/","dgPassFrontmatter":true,"noteIcon":""}
---

# pnputil

- Run below command as administrator:
- pnputil /add-driver  /install    _or_    pnputil -i -a

![VMware_drivers_7](https://kb.vmware.com/servlet/rtaImage?eid=ka05G000001hhSz&feoid=00Nf400000Tyi5M&refid=0EM5G000007YBuj)

**Note:**  
- System reboot may be required to complete the operation.
- Some drivers may requires restart OS after install driver successfully.
- Verify if your driver runs normally (in Device Manager or System Information) after installing please.


# Uninstall

##### Device Manager

1. Launch Device Manager.
2. Right-click the device you want to uninstall.
3. Click Uninstall.
4. Windows will prompt you to confirm the device’s removal. Check "Delete the driver software for this device", click OK to remove the driver.


- Run below command as administrator:

```shell
pnputil /delete-driver <the .inf file of the driver to be uninstalled, it is named like oem#.inf> /uninstall /force
```