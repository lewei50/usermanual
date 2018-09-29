[toc]
#  1 Introduction

This article mainly introduces how to connect the Modbus RTU device to DeviceBit through DTU without programming. The entire tutorial will take about 15 minutes.

![](http://doc-resources.lewei50.com/lewei50/img/DTU-lewei50-20170707-10.png)





# 2 Modbus Connecting Steps

To connect modbus device to DeviceBit requires the following 3 steps,
1. Sign up one account on DeviceBit; Write account information in DTU as a registration package.
2. Set registers for modbus device on DeviceBit.
3. Connect DTU with modbus device.
Now let's briefly explain the process. For simplicity, we use software to simulate the function of DTU.[DTU Software download link](https://cdn.lewei50.com/downloads/LeweiTcp.zip) 
The main function of the software DTU is to implement serial<->tcp. The interface is shown below:
![](http://doc-resources.lewei50.com/lewei50/img/qs20180926-1.jpg)
## 2.1 First simulate one modbus device, as the following picture shows. Two register addresses :0 1, and the values are 12 13 separately.

![modbus slave](http://doc-resources.lewei50.com/lewei50/img/DTU-lewei50-20170707-1.jpg)

## 2.2 Sign up an account, add a new device, and pay attention to all the settings.
![](http://doc-resources.lewei50.com/lewei50/img/qs20180926-2.jpg)
## 2.3 Get the registration package from the account and write it in DTU.
The registration package is in the mode of userkey_ID mode, and the following picture shows how to get userkey and ID.
![](http://doc-resources.lewei50.com/lewei50/img/qs20180926-3.jpg)

## 2.4 Connect modbus device with DTU


## 2.5 Test by modbus console
You can see that the simulated modbus data is already readable on the modbus console.
![](http://doc-resources.lewei50.com/lewei50/img/qs20180926-4.jpg)

## 2.6 Add sensors to collect data automatically

The sensor naming rule is the S + register address. For example, the register 0 is S0, and if the register has two addresses, such as register 1-2, the name is S1-2.
![](http://doc-resources.lewei50.com/lewei50/img/qs20180926-5.jpg)
![](http://doc-resources.lewei50.com/lewei50/img/qs20180926-6.jpg)
Please see the following sensor page after the devices are added successfully.
![](http://doc-resources.lewei50.com/lewei50/img/qs20180926-7.jpg)
## 2.7 2.7 Reconnect after adding the sensors.
![](http://doc-resources.lewei50.com/lewei50/img/qs20180926-8.jpg)
## 2.8 Wait to see the data collected automatically.
![](http://doc-resources.lewei50.com/lewei50/img/qs20180926-9.jpg)





