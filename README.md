# XHC-USB-Kext-Library

A XHC USB kexts basically performs the USB port-count, USB port type and USB port injections for one particular motherboard of a particular brand. Users of the same motherboard naturally can share the same XHC USB kext, if fully and properly implemented.

This library contains a set of fully implemented board-specfic XHC USB Kexts to be used with any SMBIOS under any macOS Version, always provided a working USB port limit kext patch to cirumvent Apple's 15 port USB limit. Fully implemented board-specfic XHC USB Kexts usually exceed Apple's 15 port USB limit, as usually more then 15 HS/SS ports are implemented.

In general it is recommended to stay away from any USB port limit patch (disable) and to always use a truncated 15-port kext also under macOS versions with a working port limit patch, as the latter approach makes our systems even more vanilla and resistent against respective macOS updates and also avoids buffer overruns, which can also severaly affect sleep/wake functionality. The kext truncation to max. 15 HS/SS ports however many times implies to scarify e.g. one entire internal USB3.0 onboard connector (2x HS, 2x SS) and one external USB2.0 connector (1x HS). By providing fully implemented XHC USB kexts,the decision about which onboard connectors and assigned HS and SS ports to be dropped is still left to the respective user. However, one can also directly download and implement the respective truncated 15-port XHC USB from the respective sub-directory of this Library.  

For the proper use of the distributed kexts with a SMBIOS different than implemented, edit the kext with Xcode and replace at all locations the implemented SMBIOS defintions by the desired SMBIOS definition. 

Experienced users are invited to use my XHC USB kext creation guideline https://www.tonymacx86.com/threads/xhc-usb-kext-creation-guideline.242999/ for developing new board-specfic XHC USB kexts not yet being part fo this library. They are kindly asked to subsqeuntly provide both fully implemented and truncated 15-port XHC USB kexts for their particular motherboard to help growing this library. 

Credits to Brumbear for initally devloping the XHC USB Kext approach.  
