# Serial to TCP Tool for Windows

 DeviceBit

---

## Software introduction
If you don't have a DTU device to connect your device to DeviceBit, you can try TCP to serial tool software. By using this software, you can quickly connect your device to DeviceBit for testing.
The running operation system is Windows.

## 1. Add your device on DeviceBit
Sign up on DeviceBit if you don't have an account. Then Add you device to DeviceBit. Refer to previous chapter [Add a device][h1]
Log into DeviceBit, go to "My account"-"Account settings", copy your userkey down for the following step.
![Userkey][1]
## 2. Connect your device to your PC
Connect your device or sensor to your PC accoring to their communication port. And check which serial port of you PC is connected.
>>Note: You may need a serial to USB driver software if you connect your device to USB port of your PC.
## 3. Download the software and configure
Download [Serial to TCP tool][h2]. You can select the language on the letf bottom.
You need to configure the below settings
a.Set the serial port, buadrate as shown in the picture according to actual condition. 
b.Set the SOCKET information, including address, port as shown in the picture
c.Set the Userkey_DeviceID (or SN_DeviceID).
![software configuration][2]
## 4. View the data uploaded to DeviceBit
Log into DeviceBit, go to "My Devices"-"Real-time Data", you can view your device's data.
![View you data][3]

  [h1]: https://devicebit.gitbook.io/devicebit/user-manual/1
  [h2]: https://cdn.lewei50.com/downloads/LeweiTcp.zip
  [1]:https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-DTUtool-20180930-1.jpg
  [2]:http://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-DTUtool-20180930-2.jpg
  [3]:http://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-DTUtool-20180930-3.jpg