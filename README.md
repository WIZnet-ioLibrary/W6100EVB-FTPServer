# Index
- [FTP Server Example for W6100-EVB](#FTP Server-Example-for-W6100-EVB)
- [Hardware Environment](#Hardware-Environment)
- [Software Environments](#Software-Environment)
- [Run](#Run)
- [Code review](#Code-review)
  - [Test packet capture file](#Test-packet-capture-file)


------
# FTP Server Example for W6100-EVB
Common to Any MCU, Easy to Add-on. Internet Offload co-Processor, HW TCP/IP chip,
best fits for low-end Non-OS devices connecting to Ethernet for the Internet of Things. These will be updated continuously.

## Hardware Environment
* W6100EVB
  - connecting Micro usb.
  - connecting Ethernet cable. <br>
<p align="center">
  <img width="60%" src="https://wizwiki.net/wiki/lib/exe/fetch.php?w=600&tok=eabde4&media=products:w6100:w6100_evb:w6100-evb_callout.png" />
</p>

## Software Environment
In case of used to TureSTUDIO,it it the same as HTTP Server example.
 - Link : [Software Environment of W6100EVB-HTTP_Server](https://github.com/WIZnet-ioLibrary/W6100EVB-HTTP_Server#Software-Environment)


## Run
* Demo Environment & Program <br>

  - Windows 7 <br>
  - Hercules <br>
  - [WinSCP (FTP Client Program)](https://winscp.net/download/WinSCP-5.15.1-Setup.exe) <br>

* Demo Result <br>
  - Power On and push Reset button to start Program<br>
  - Program Run Serial display <br>
  <p align="center">
    <img width="60%" src="https://user-images.githubusercontent.com/24927447/56946286-a0315500-6b64-11e9-9fb5-1bb8047fa78e.PNG" />
  </p>

  - You can connect to the W6100 FTP Server using the FTP Client program.

  <p align="center">
    <img width="60%" src="https://user-images.githubusercontent.com/24927447/56948336-c954e400-6b6a-11e9-964e-e99860a3a187.PNG" />
  </p>

  - You can connect to the server after you enter the IP, port password, etc. and try to connect.

  <p align="center">
    <img width="60%" src="https://user-images.githubusercontent.com/24927447/56948426-0faa4300-6b6b-11e9-925b-1dcf7f6ef17b.PNG" />
  </p>

  - Since W6100 FTP Server is TCP Dual Mode, it can access to IPv6..

  <p align="center">
    <img width="60%" src="https://user-images.githubusercontent.com/24927447/56949746-a0365280-6b6e-11e9-8531-5aff6b54a142.PNG" />
  </p>
  
  
  ## Code review
  * main.c  <br>
  - Set the Network Information & FTP Server User ID, Password and port number
  <p align="center">
    <img width="80%" src="https://user-images.githubusercontent.com/24927447/56950614-db398580-6b70-11e9-9f87-d4c2267c86a5.PNG" />
    <img width="50%" src="https://user-images.githubusercontent.com/24927447/56950615-db398580-6b70-11e9-820b-affc84c15210.PNG" />
  </p>
  
  * wizchip_conf.h  <br>
  - Set the IO Mode
  <p align="center">
    <img width="50%" src="https://user-images.githubusercontent.com/24927447/56950925-81858b00-6b71-11e9-9ed7-da0cb12d5a12.PNG" />
  </p>
  
 * ftpd.c <br>
 - In the current code, FTP Server's files and directories are simply implemented. If you want to send a specific file to the client, you need to modify ftpd_listcmd (), ftpd_retrcmd (), and so on.

   ## Test packet capture file
   <p align="center">
   <img width="100%" src="https://user-images.githubusercontent.com/24927447/56949968-4c783900-6b6f-11e9-9e8e-4be5a0d8e92a.PNG" />
   <img width="100%" src="https://user-images.githubusercontent.com/24927447/56949969-4c783900-6b6f-11e9-93cf-1d561961e480.PNG" />
    </p>

    -Test packet capture file : [FTP Server_Packet Capture file.zip](https://github.com/WIZnet-ioLibrary/W6100EVB-FTPServer/files/3130489/FTPServer_Packet.zip)

