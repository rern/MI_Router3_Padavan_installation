### Mi Router 3 Custom Firmware
- Prepare PC
- Prepare Mi Router
- Flash firmware
- Setup Mi Router

## Prepare PC
- Install **VMware Workstation Player**: [www.vmware.com](www.vmware.com)
- Download: [VMWARE-PROMETHEUS-64-UBUNTU-EN-RU.7z](https://disk.yandex.ru/d/6EpD2EpHmB82o) > extract
- `VMware Workstation Player` > `Player` > `File` > `Open...` > select extracted folder > select `PROMETHEUS-64-U-EN.vmx`
- Select `Power on` (green play icon) > `I copt it` > `No` for connect virtual device > `No` for software update
- Wail until all downloads and environment setup finished (10+ minutes)

**Pre-compile**  
![1](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/scrrenshots/1.jpg)  
![2](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/scrrenshots/2.jpg)  
![3](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/scrrenshots/3.jpg)  
(Make sure NumLock is on for number keys.)
- Type **1** `1) Padavan-ng (Linaro)` (2 rounds)
- Wait until source cloning finished
- Type **2** `2) Xiaomi` > **4** `4) mi-3`

**Compile**  

![4](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/scrrenshots/4.jpg)
- Type **3** `Build toolchain (3)` (60+ minutes)
- Type **4** `Firmware (4)`
    - Type **2** `Apply skins (2)` > **0** - **6** `(0)-(6)` for all skins > **Q** `(Q)uit`
    - Type **3** `Build a firmware (3)` (30+ minutes)
    - Type **Q** `(Q)uit`
- Type **Q** `(Q)uit` or keep it running

## Prepare Mi Router   
(For Chinese language, use thses for guessing)  
- Download Mi's overwritable firmware: [miwifi_r3_all_55ac7_2.11.20.zip](https://www.dropbox.com/s/r09dl0or4z2iyxh/miwifi_r3_all_55ac7_2.11.20.zip?dl=1)
- Extract and flash to the router  
![2](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/scrrenshots/02.jpg)  
![3](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/scrrenshots/03.jpg)  
![4](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/scrrenshots/04.jpg)  
![5](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/scrrenshots/05.jpg)  

- Disconnect all LAN
- Connect to the router through WiFi **Xiaomi_xxxxxx** > pop-up Setup page
- Finish initial setup - remember **admin password**

## Flash firmware
![1](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/scrrenshots/01.jpg)
- Set PC network adapter:
	- Write down current settings
	- Set IP: 192.168.31.2
	- Set subnet: 255.255.255.0
- Reconnect PC to Router
- If `(Q)uit` > Run `./start.sh`
- Type **0** `SSH-hach of stock firmware (0)` > **enter** for (default - 192.168.31.1) > type **addmin password**
- Wait until SSH-hack succeeded
- Verify:
	- in heading:
    	- `Toolchain: OK`
    	- `Firmware: MI-3_X.X.X.X-XXX.trx`
	- `SSH-hach of stock firmware (0)` disappeared
- Type **4** `Firmware (4)` > **4** `Flash a firmware (4)` > type **n** no backup partition to save time
- Wait until finished > type **y** to reboot the router
- Done
- Restore PC network adapter settings

## Setup Mi Router  
Connect to the router
- LAN or WiFi: **ASUS** password: **1234567890**
- IP: 192.168.1.1
- ID: admin
- Password: admin
