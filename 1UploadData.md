# Quick Start
# 1 Add a new device
For getting started on DeviceBit platform, the first step is to add a new device.
Log into the IOT platform (If you don’t have the account you need to sign up first).
Sign up a DeviceBit Account ([www.devicebit.com](/www.devicebit.com))
![][1]
Pic.1 Sign Up
As shown in Pic2, go to ***My Devices -> Devices -> Add A device***, fill in the information and then save.
![][2]

Pic.2 Create a new device
# 2 Add sensors & controllers
The next step is to add a new sensor or controller connected to your device.
## 2.1 Add a new sensor
As shown in Pic3, go to ***My Devices -> Sensors&Controllers ->Sensors, ***and then click on ***Add*** button to create a new sensor.
![][3]
Pic.1 Add a new sensor
![][4]


# 3 Data Upload Simulation

This tutorial mainly introduces how to simulate data upload by using API testing tool.
**Hardware**
No hardware is required. Only simulate data upload by API testing tool provided by Devicebit platform.
**Procedure：**
1 Sign up a DeviceBit Account ([www.devicebit.com](/www.devicebit.com))
![home.jpg][1]

Pic.1 Sign Up
## 3.1 Add My Device, Sensors: Humidity and Temperature
(The steps are as follows. Note: note down the ID, for it will be used in Api calling.)
## 3.2 Add A Device
After login, go to My Devices -> Devices->Add a Device
First, click on Devices -> Add A Device , as the picture1 below. After entering the related information, click on Save.
![][2]
## 3.3 Add Humidity
The next step is to add the humidity sensor. Go to**My Devices-> Sensors&Controllers->Sensor**, click on **Add**.

![][3]
Pic.3 Sensors
Then there will be the ***Add A Sensor*** page.
![][7]
Pic.4 Add Humidity


## 3.3 Add Temperature
Add the ***Temperature*** sensor in the same way. Please see the following picture.
![][8]
Pic.5 Add Temperature
After setting up, as picture 5 shows, note down the ***ID*** because it will be used in Api calling.
![][9]

Pic.6 Sensor ID

## 3.4 Data Simulation
Now, let's move on to simulate data upload by using Api testing tool.
At the home page (the website is www.devicebit.com) click on ***Documentation***

Pic.7 Home Page
and then go to **API Directory-> Sensor ->Upload Sensor Data**
![][10]
Pic.8 API Directory
Website
https://www.devicebit.com/dev/apitest/203



![][11]
Pic.9 On-line test
Click on ***on-line test***
![][12]
Pic.10 API Testing Tool
Enter your **Userkey**
Enter ***Device ID*** at API URL
http://www.devicebit.com/api/V1/gateway/UpdateSensors/{device ID}
[（01 for exampe）](http://www.lewei50.com/api/V1/gateway/UpdateSensors/%E4%BD%A0%E7%9A%84%E7%BD%91%E5%85%B3%E5%8F%B7)
After entering the device ID, the APIURL is: http://www.devicebit.com/api/V1/gateway/UpdateSensors/01
![][13]
Pic.11 Userkey & Device No.
Change ***T1*** to ***Temperature*** for ***Name***; change ***1*** to ***32*** for **Value***;
Change ***01H1*** to ***Humidity*** for ***Name***; change ***96.2*** to ***75*** for ***Value***.
![][14]
Pic.12 Post Data
Click on ***Run***, and then the request detail will be displayed.
![][15]
Pic.13 Request Detail
At last, Go to ***My IOT -> Sensors&Controllers->Sensor List***, you will see the following value.
![][16]
Pic.14 The Value
Well Done! Your data upload is successfully simulated by using API testing tool!



The following part will introduce how to set Notice Groups, and receive email alerts

# 4 Alert
The following part will introduce how to set Notice Groups, and receive email alerts.
# 4.1 Add A New Contact

Click on Notice Groups -> Contacts -> New Contact
![][17]


Enter the name, Email etc. of this contact and then click on Save.
![][18]

Add more contacts in the same way.


![][19]

# 4.2 Add A New Group

Go to Notice Groups -> Add Group

![][20]

Enter the group name, tick the contacts, and save.

![][21]

![][22]


# 4.3 Alarm Settings

Go to List, and click on Edit.


![][23]
![][24]


Set the normal temperature range for your device and select the notice group, e.g. the Temperature group which is just set.
Then, set the normal humidity range in the same way.




Then, click on Save and the settings are successfully saved. Please remember the ID of the sensors (H1, T1), for they will be used in the following calling step.


![][25]


After settings, simulate data upload as the last chapter mentioned.

![][26]


Meanwhile, you will receive the following alarms by Email.

![][27]

[17]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-17.jpg
[18]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-18.jpg
[19]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-19.jpg
[20]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-20.jpg
[21]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-21.jpg
[22]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-22.jpg
[23]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-23.jpg
[24]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-24.jpg
[25]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-25.jpg
[26]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-26.jpg
[27]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-27.jpg
[28]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-28.jpg
[29]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-29.jpg
[30]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-30.jpg
[31]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-31.jpg
[32]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-32.jpg
[33]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-33.jpg
[34]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-34.jpg
[35]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-35.jpg
[36]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-36.jpg
[37]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-37.jpg
[38]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-38.jpg
[39]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-39.jpg
[40]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-40.jpg
[41]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-41.jpg
[42]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-42.jpg

[43]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-43.jpg
[44]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-44.jpg
[45]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-45.jpg
[46]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-46.jpg
[47]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-47.jpg
[48]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-48.jpg
[49]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-49.jpg
[50]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-50.jpg
[51]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-51.jpg
[52]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-52.jpg
[55]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-55.jpg
[56]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-56.jpg
[57]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-57.jpg
[58]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-58.jpg
[59]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-59.jpg
[60]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-60.jpg
[53]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-53.jpg
[54]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-54.jpg

[3]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-3.jpg
[1]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-1.jpg
[2]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-2.jpg
[5]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-5.jpg
[6]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-6.jpg
[7]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-7.jpg
[8]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-8.jpg
[9]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-9.jpg
[10]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-10.jpg
[11]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-11.jpg
[12]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-12.jpg
[13]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-13.jpg
[14]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-14.jpg
[15]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-15.jpg
[16]: https://leweidoc.oss-cn-hangzhou.aliyuncs.com/lewei50/img/devicebitmanual-xj-20180930-16.jpg