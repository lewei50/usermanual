# Quick Start
# 1 Add a new device
For getting started on DeviceBit platform, the first step is to add a new device.
Log into the IOT platform (If you don’t have the account you need to sign up first).
Sign up a DeviceBit Account ([www.devicebit.com](/www.devicebit.com))
![home.jpg](https://upload-images.jianshu.io/upload_images/5875248-a27982f0be2f9336.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


Pic.1 Sign Up
As shown in Pic2, go to ***My Devices -> Devices -> Add A device***, fill in the information and then save.
![1.jpg](https://upload-images.jianshu.io/upload_images/5875248-63d4f8279169e18c.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

Pic.2 Create a new device
# 2 Add sensors & controllers
The next step is to add a new sensor or controller connected to your device.
## 2.1 Add a new sensor
As shown in Pic3, go to ***My Devices -> Sensors&Controllers ->Sensors, ***and then click on ***Add*** button to create a new sensor.
![2.jpg](https://upload-images.jianshu.io/upload_images/5875248-69f419f407b41109.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Pic.1 Add a new sensor
![3.jpg](https://upload-images.jianshu.io/upload_images/5875248-5bdbebbe22f00fa0.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 2.2 Add a new controller
As shown in Pic4, go to ***My Devices -> Sensors&Controllers ->Controllers, ***and then click on ***Add*** button to create a new controller.
![4.jpg](https://upload-images.jianshu.io/upload_images/5875248-59e0dbbd77008921.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![5.jpg](https://upload-images.jianshu.io/upload_images/5875248-d7dc16e0ac309b07.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
# 3 Data Upload Simulation

This tutorial mainly introduces how to simulate data upload by using API testing tool.
**Hardware**
No hardware is required. Only simulate data upload by API testing tool provided by Devicebit platform.
**Procedure：**
## 3.1 Add My Device, Sensors: Humidity and Temperature
(The steps are as follows. Note: note down the ID, for it will be used in Api calling.)
## 3.2 Add A Device
After login, go to My Devices -> Devices->Add a Device
First, click on Devices -> Add A Device , as the picture1 below. After entering the related information, click on Save.
![1.jpg](https://upload-images.jianshu.io/upload_images/5875248-63d4f8279169e18c.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
## 3.3 Add Humidity
The next step is to add the humidity sensor. Go to**My Devices-> Sensors&Controllers->Sensor**, click on **Add**.

![2.jpg](https://upload-images.jianshu.io/upload_images/5875248-69f419f407b41109.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Pic.3 Sensors
Then there will be the ***Add A Sensor*** page.
![3.jpg](https://upload-images.jianshu.io/upload_images/5875248-5bdbebbe22f00fa0.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Pic.4 Add Humidity


## 3.3 Add Temperature
Add the ***Temperature*** sensor in the same way. Please see the following picture.
![3-T.jpg](https://upload-images.jianshu.io/upload_images/5875248-d268286302be8be7.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Pic.5 Add Temperature
After setting up, as picture 5 shows, note down the ***ID*** because it will be used in Api calling.
![3-2.jpg](https://upload-images.jianshu.io/upload_images/5875248-eb5f8fa8d99d258c.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

Pic.6 Sensor ID

## 3.4 Data Simulation
Now, let's move on to simulate data upload by using Api testing tool.
At the home page (the website is www.devicebit.com) click on ***Documentation***

Pic.7 Home Page
and then go to **API Directory-> Sensor ->Upload Sensor Data**
![3-API.jpg](https://upload-images.jianshu.io/upload_images/5875248-fd5034c086bb6020.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Pic.8 API Directory
Website https://www.devicebit.com/dev/apitest/203



![](http://upload-images.jianshu.io/upload_images/5875248-43385cd3c136c6d7.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Pic.9 On-line test
Click on ***on-line test***
![](http://upload-images.jianshu.io/upload_images/5875248-9189516a45c179fb.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Pic.10 API Testing Tool
Enter your **Userkey**
Enter ***Device ID*** at API URL
http://www.devicebit.com/api/V1/gateway/UpdateSensors/{device ID}
[（01 for exampe）](http://www.lewei50.com/api/V1/gateway/UpdateSensors/%E4%BD%A0%E7%9A%84%E7%BD%91%E5%85%B3%E5%8F%B7)
After entering the device ID, the APIURL is: http://www.devicebit.com/api/V1/gateway/UpdateSensors/01

![](http://upload-images.jianshu.io/upload_images/5875248-4d20a426fb793a29.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Pic.11 Userkey & Device No.
Change ***T1*** to ***Temperature*** for ***Name***; change ***1*** to ***32*** for **Value***;
Change ***01H1*** to ***Humidity*** for ***Name***; change ***96.2*** to ***75*** for ***Value***.
![](http://upload-images.jianshu.io/upload_images/5875248-8bd1cebcac05e996.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Pic.12 Post Data
Click on ***Run***, and then the request detail will be displayed.
![](http://upload-images.jianshu.io/upload_images/5875248-155ac589f0f24f1c.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Pic.13 Request Detail
At last, Go to ***My IOT -> Sensors&Controllers->Sensor List***, you will see the following value.
![](http://upload-images.jianshu.io/upload_images/5875248-25994a4da11d5380.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Pic.14 The Value
Well Done! Your data upload is successfully simulated by using API testing tool!
The following part will introduce how to set Notice Groups, and receive email alerts

# 4 Alert
The following part will introduce how to set Notice Groups, and receive email alerts.
## 4.1 Add A New Contact

Click on Notice Groups -> Contacts -> New Contact

![w1.jpg](http://upload-images.jianshu.io/upload_images/5875248-d35b662cfdedf98e.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


Enter the name, Email etc. of this contact and then click on Save.

![w2.jpg](http://upload-images.jianshu.io/upload_images/5875248-3329c5d6c69fac1c.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

Add more contacts in the same way.


![w3.jpg](http://upload-images.jianshu.io/upload_images/5875248-91c804f86585df59.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 4.2 Add A New Group

Go to Notice Groups -> Add Group

![w5.jpg](http://upload-images.jianshu.io/upload_images/5875248-30088f3b3243b34c.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

Enter the group name, tick the contacts, and save.

![w6.jpg](http://upload-images.jianshu.io/upload_images/5875248-84abedff39e82e90.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)