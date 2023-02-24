### Mi Router 3 Custom Firmware Installation
How to use [Prometheus tool](http://prometheus.freize.net/) to install [Padavan's custom firmware](https://github.com/andy-padavan/rt-n56u) on Mi Router 3.
- Prepare PC
- Prepare Mi Router
- Flash firmware
- Setup Mi Router

## Prepare PC
- Install **VMware Workstation Player**: [www.vmware.com]((https://www.vmware.com)
- Download: [VMWARE-PROMETHEUS-64-UBUNTU-EN-RU.7z](https://disk.yandex.ru/d/6EpD2EpHmB82o) > extract  

![0](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/0.jpg)
- `VMware Workstation Player` > `Player` > `File` > `Open...` > select extracted folder > select `PROMETHEUS-64-U-EN.vmx`
- Select `PROMETHEUS-64-U-EN` > `Play virtual machine` > `I copy it` > `No` for connect virtual device > `No` for software update
- Wail until all downloads and environment setup finished (10+ minutes)

**Pre-compile**  
(Make sure NumLock is on for number keys.)  
- ![1](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/1.jpg)  
- Type **1** `1) Padavan-ng (Linaro)` (2 rounds)
- Wait until source cloning finished  
- ![2](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/2.jpg)  
- Type **2** `2) xiaomi`
- ![3](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/3.jpg)  
- Type **4** `4) mi-3`

**Compile**  

![4](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/4.jpg)
- Type **3** `Build toolchain (3)`
- Wait until finished (60+ minutes)
- Type **4** `Firmware (4)`  

    - ![6](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/6.jpg)
    - Type **2** `Apply skins (2)`  
    
    	- ![7](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/7.jpg)
    	- Type **0** to **6** `(0) - (6)` to select all skins  
		- Type **Q** `(Q)uit`  
		
    - Type **3** `Build a firmware (3)`
    - Wait until finished (30+ minutes)
    - Type **Q** `(Q)uit`  
    
- Keep main menu running

## Prepare Mi Router   
(For Chinese language, use these for guessing)  
- Download Mi's overwritable firmware: [miwifi_r3_all_55ac7_2.11.20.zip](https://www.dropbox.com/s/r09dl0or4z2iyxh/miwifi_r3_all_55ac7_2.11.20.zip?dl=1)
- Extract and flash to the router  

![2](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/02.jpg)  
![3](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/03.jpg)  
![4](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/04.jpg)  
![5](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/05.jpg)
- Disconnect LAN - PC to router
- Connect to the router through WiFi **Xiaomi_xxxxxx** > pop-up Setup page
- Finish initial setup
- write down **admin password**

## Flash firmware  
- Set PC network adapter:
	- Write down current settings
	- Set IP: 192.168.31.2
	- Set subnet: 255.255.255.0
- Reconnect LAN - PC to router
- If main menu was closed, Run `./start.sh` again.  

![1](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/01.jpg)
- Type **0** `SSH-hach of stock firmware (0)`
	- **Enter** for (default - 192.168.31.1)
	- Type **addmin password**
- Wait until SSH-hack succeeded
- Verify
	- In heading: `Toolchain: OK Firmware: MI-3_X.X.X.X-XXX.trx`
	- `SSH-hach of stock firmware (0)` disappeared
- Type **4** `Firmware (4)`

![6](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/6.jpg)
- Type **4** `Flash a firmware (4)`
	- Type **n** no backup partition to save time

![5](https://github.com/rern/MI_Router3_Padavan_installation/blob/master/screenshots/5.jpg)
- Wait until finished
- Type **y** to reboot the router

## Done
- Restore PC network adapter settings

## Setup Mi Router  
- Connect to the router  
	- LAN
	- or WiFi
		- SSID: ASUS
		- Password: 1234567890
- Login
	- IP: 192.168.1.1
	- ID: admin
	- Password: admin
