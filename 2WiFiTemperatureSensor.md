This article will take about 10 minutes to read. It mainly introduces an open source WiFi  temperature sensor (DS18B20) based on nodemcu (esp8266) which can be used on DeviceBit.
[toc]




# 1 Hardware & Software
|No.   |Sort |Name|Description|
|---|---|---|---|
|1   | Hardware |Nodemcu DS18B20|![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifi-ht-20180913-8.jpg)|
|2   | Software|[FLASH_DOWNLOAD_TOOLS_V3.6.4](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/software/FLASH_DOWNLOAD_TOOLS_V3.6.4.rar)| Nodemcu Download tool |


# 2 Hardware

## 2.1 Wire Connection

As the picture shown below, supply power to the 18b20 with nodemcu and connect the 18B20 data cable to D5 pin of ndoemcu.
![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifi-ht-20180913-8.jpg)

Hardware schematic：[Hardware schematic](https://github.com/lewei50/lua-on-nodemcu/blob/master/demo/ESP8266-DS18B20/esp-tUSB-201808D2.PDF)

## 2.2 Download firmware

[Firmware download software：FLASH_DOWNLOAD_TOOLS_V3.6.4](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/software/FLASH_DOWNLOAD_TOOLS_V3.6.4.rar)

Firmware ：https://github.com/lewei50/lua-on-nodemcu/tree/master/demo/ESP8266-DS18B20/bin

Download firmware：
![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifiht-20180923-5.jpg)

After the download is complete, restart the device

# 3 Configuration on DeviceBit

Log in to [https://www.lewei50.com ](https://www.lewei50.com ), sign up and then sign in.

## 3.1 Add A Device with wifiHT Template

Note: to select the correct template.
![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifiht-20180923-1.jpg)
Click on ***Save***
 ![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifiht-20180923-2.jpg)
There will be three sensors on the sensor page after click on ***Save*** successfully.
 ![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifiht-20180923-3.jpg)

<h2 id="3.2"> 3.2 Record the related parameters of your account </h2>
Each account has a userkey, and each device has an ID. Record the userkey_ID of the newly created template device, as shown below.


 ![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifiht-20180923-4.jpg)

# 4 Nodemcu settings & Configuration on DeviceBit
## Restart, and connect to AP
Restart nodemcu，find the following ap of ssid, and connect to it. The password is 12345678.

![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifi-ht-20180913-1.jpg)

## WiFi Configuration（http://192.168.4.1/dev）
Visit http://192.168.4.1/dev ，see the following page
 ![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifiht-20180923-8.jpg)
TcpServer：User's own server address (described later, optional)
SN：The userkey_ID of the user account of the platform (introduced in Chapter 3.2), shown as follows:
 ![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifiht-20180923-4.jpg)
Click on ***Save*** when the configuration is done.
 ![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifiht-20180923-9.jpg)

## WiFi Configuration（http://192.168.4.1）
Visit 192.168.4.1 to configure related wifi parameters, and then click on ***Save***.
 ![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifiht-20180923-10.jpg)


The device will restart automatically. If everything is normal, you will see  there is one more device in the network of the windows system. Its name is DS18B20_SN. You can modify the configuration at any time.
![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifi-ht-20180913-6.jpg)

# 5 Monitor on DeviceBit & Alert

![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifiht-20180923-11.jpg)



# 6 Other features of open source wifi HT
This open source WiFi HT is not bound to the cloud platform. In addition to uploading data to the platform, it can also implement the following applications.
## 6.1 Serve as http server to provide  get interface
Mainly for LAN applications without internet

![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifi-ht-20180913-10.jpg)

Inside the data array is the temperature value, which is updated in 10 seconds.
## 6.2 Custom socket; data is sent to the personal server
![](https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/wifiht-20180923-7.jpg)
The firmware periodically sends {"status": "succeed", "data": [28.1875], "mac": "18fe34e0b7d8"} every minute as a heartbeat packet.
The firmware responds to the read command and returns {"status":"succeed","data":[28.1875],"mac":"18fe34e0b7d8"}
(The data in the data array is the real-time temperature value.)
