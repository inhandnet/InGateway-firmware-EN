# InGateway502 Quick Start Manual
This document is used to explain the basic configuration operations of InGateway502 (IG502 for short) networking, software version update, etc., so that users can master the basic configuration of IG502 and the use of common functions.

  - [1. Configure IG502 Network Parameters](#configure-ig502-network-parameters)
    - [1.1 Access the IG502](#set-lan-parameters)
    - [1.2 Connect IG502 to the Internet](#set-wan-parameters)
  - [2. Update the Software](#update-the-software)
    - [2.1 Update the IG502 firmware](#update-the-firmware-software)
    - [2.2 Upgrade the Python SDK of IG502](#update-the-sdk-software)
  - [3. Python Edge Computing](#use-python-edge-computing)
    - [3.1 Install and run Python App](#install-and-run-python-app)
    - [3.2 Update Configuration File for App](#update-configuration-file-for-app)
    - [3.3 Update Python App version](#update-python-app-version)
    - [3.4 Enable the Debug Mode](#enable-the-debug-mode)
  - [4. InHand Cloud](#inhand-cloud)
  - [5. Data Collection And Upload To The Cloud](#data-collection-and-upload-to-the-cloud)
  - [Appendix](#appendix)
    - [Factory reset](#factory-reset)

<a id="configure-ig502-network-parameters"> </a>  

## 1. Configure IG502 Network Parameters

<a id="set-lan-parameters"> </a>  

### 1.1 Access the IG502
- Step 1: By default, the IP address of WAN on IG502 is 192.168.1.1; the IP address of LAN on IG502 is 192.168.2.1. This document uses the LAN port to access the IG502 as an example. Set the PC’s IP address to be on the same subnet with LAN.   
    
  - Method 1: Enable the PC to obtain an IP address automatically (recommended)  

    ![](images/2020-01-02-09-55-52.png)  

  - Method 2: Set a fixed IP address  
  
    Select Use the following IP address, enter an IP address (By default,any from 192.168.2.2 to 192.168.2.254), subnet mask (By default,255.255.255.0), default gateway (By default,192.168.2.1), and DNS server address, and click OK.   

    ![](images/2020-01-21-15-57-32.png)  

- Step 2: Launch the browser on the PC and access the IP address of LAN. Enter the login user name and password. The default user name and password are adm and 123456 respectively.  

  ![](images/2021-01-20-20-40-59.png)   

- Step 3: After successful login, you can see the web page as shown below:   

  ![](images/2021-01-20-20-41-38.png)  

- Step 4: To change the user name and password for logging in to the web management interface of IG502, choose System > User Management page of IG502 and set the new user name and password.   

  ![](images/2021-01-20-20-42-06.png)  

- Step 5: To change the IP address of LAN, choose Network > Network Interfaces > LAN page of IG502 to configure LAN.  

  ![](images/2021-01-20-20-43-43.png)  

<a id="set-wan-parameters"> </a>  

### 1.2 Connect IG502 to the Internet
  - Method 1: Connect to the Internet by SIM card
    - Step 1: Insert the SIM card. (Note: Before inserting or removing the SIM card, unplug the power cable; otherwise, the operation may cause data loss or damage the IG502.) After inserting the SIM card, connect the 4G LTE antenna to the ANT interface and power on the IG502.  

      ![](images/2021-01-20-20-47-15.png)  

    - Step 2: Choose Network > Network Interfaces > Cellular page of IG502 and select Enable Cellular and click Submit.  

      ![](images/2021-01-20-20-48-32.png)  

      When the network connection status is Connected and an IP address has been allocated, the IG502 has been connected to the Internet with the SIM card.   

      ![](images/2021-01-20-20-49-31.png)  

  - Method 2: Connect to the Internet by Ethernet  
    - Step 1: Use the Ethernet cable to connect the WAN and LAN ports of the IG502 respectively, as shown below:   
 
      ![](images/2021-01-20-20-51-27.png)  

    - Step 2: Choose Network > Network Interface > WAN page of IG502 to configure the IP address of the WAN port and click Submit. (When the network type is a static IP address, you need to configure the IP, subnet mask, and other information according to the site network conditions.)  

      ![](images/2021-01-21-17-54-55.png)  

      ![](images/2021-01-21-17-55-19.png)  

    - Step 3: Choose Network > Routing > Static Routing page of IG502 to add a static route for WAN port and click Submit. (Select "WAN" for the interface item, and configure the other items according to the site network conditions.)  

      ![](images/2021-01-21-17-57-29.png)  

    - Step 4: Choose System > Network Tools page of IG502 and use the Ping tool to check whether the IG502 has successfully connected to the Internet. The following figure shows that IG502 have successfully connected to the Internet:  

      ![](images/2021-01-21-17-59-49.png)

<a id="update-the-software"> </a>  

## 2. Update the Software
To obtain the latest software version of IG502 and updated functions, contact the customer service center. To update the IG502 software version, do as follows.  

<a id="update-the-firmware-software"> </a>  

## 2.1 Update the IG502 firmware.  
  
  Choose System > Firmware Upgrade. Select a firmware file and click Start Upgrading. After the update is completed, you are prompted to restart the system to Apply the new firmware.  

  ![](images/2021-01-21-18-01-47.png)  
   
<a id="update-the-sdk-software"> </a>  

## 2.2 Upgrade the Python SDK of IG502.   
  
  Choose Edge Computing > Python Edge Computing. Select Python Engine, select an Python SDK file, and click Upgrade; when the upgrade confirmation window pops up, click Confirm. Then the IG502 automatically performs the upgrade.  

  ![](images/2021-01-21-18-03-20.png)  

<a id="use-python-edge-computing"> </a>  

## 3. Python Edge Computing

<a id="install-and-run-python-app"> </a>  

### 3.1 Install and run Python App
To install and run Python App (App for short) in IG502,  please refer to the following process, this document takes **Device Supervisor** as an example:
- Step 1: Install the App  
  
  Before installing the App, you need to ensure that the Python Edge Computing Engine is enabled and the Python SDK is installed, as shown in the following figure:  

  ![](images/2021-01-21-18-35-36.png)  

  Choose Edge Computing > Python Edge Computing. click the Add button and select the App package file to be installed, then click Confirm.  

  ![](images/2021-01-21-18-37-53.png)  

  After importing, you can view the imported Apps, as shown in the following figure:  

  ![](images/2021-01-21-18-38-38.png)  
   
- Step 2: Run the App   
  
  Select enable App and click Submit.  

  ![](images/2021-01-21-18-40-16.png)  

  Once enabled, the App automatically runs and will run every time the IG502 is started.  

  ![](images/2021-01-21-18-41-07.png)

<a id="update-configuration-file-for-app"> </a>  

### 3.2 Update Configuration File for App
If the installed App supports importing configuration files to modify the running mode, you can update the App running configuration by referring to the following process:
- Step 1: Choose Edge Computing > Python Edge Computing,  click the Import Configuration button and select the configuration file to be imported, then click Confirm.  

  ![](images/2021-01-21-18-42-41.png)  
   
- Step 2: Restart the App after the import is successful. After the App restarts, it will runing according to the imported configuration file.  

  ![](images/2021-01-21-18-43-16.png)  

<a id="update-python-app-version"> </a>  

### 3.3 Update Python App version
Generally, if you need to update the Python App version, you only need to import the new version of the App on the Edge Computing > Python Edge Computing page.  

![](images/2021-01-21-18-43-52.png)  

After the update is completed, as shown below：  

![](images/2021-01-21-19-02-16.png)

<a id="enable-the-debug-mode"> </a>  

### 3.4 Enable the Debug Mode
To run and debug Python code on IG502, you need to enable IG502's debug mode.  Choose Edge Computing > Python Edge Computing, select Enable Debug Mode. After enabling, you can develop IG502 through VS Code. How to use VS Code for Python development of IG502, please refer to [Quick Start for MobiusPi Python Development](http://sdk.ig.inhandnetworks.com/en/latest/MobiusPi-Python-QuickStart-EN.html).  

![](images/2021-01-21-19-02-41.png)  

After the debugging mode is enabled, IG502 will start an SSH server to listen on port 222 of LAN (default IP address being 192.168.2.1). The user name and password of the SSH server are displayed on the previous web page. A random password is generated every time the debugging mode is enabled or the IG502 is restarted to ensure security.

<a id="inhand-cloud"> </a>  

## 4. InHand Cloud
The InHand Cloud developed by InHand supports functions such as monitoring IG502 status, remote maintenance of equipment, remote batch delivery of IG502 configuration, and IG502 batch upgrade, helping users to conveniently and efficiently manage IG502 and field devices. In order to enable the InHand Cloud to remotely manage the IG502 and field devices, the IG502 needs to be connected to the cloud platform. The connection method is as follows:  
Choose System Management > InHand Cloud, tick Enable InHand Cloud and configure the corresponding server address and registered account, and click Submit after the configuration is complete. The **InHand Connect Service** platform mainly provides users with remote maintenance channels, and the **InHand Device Manager** platform mainly provides users with gateway management services (such as batch remote upgrades, etc.).  
- Server address: the address of the InHand Cloud. 
- Registered account: the InHand Cloud account associated with the IG502 device (if you have not registered an account, you need to register an account first)  
- Advanced settings: Contains configurations such as heartbeat interval. Generally, you can use the default configuration.  

![](images/2021-01-21-19-12-46.png)   

After the IG502 is successfully connected to the InHand Device Manager, the status is described as Connection Accepted.  

![](images/2021-01-21-19-13-42.png)  

<a id="data-collection-and-upload-to-the-cloud"> </a>  

## 5. Data Collection And Upload To The Cloud

- Step 1: Connect PLC

  Use Ethernet or serial cable to connect IG502 and PLC, the following figure describes how to connect serial port terminals of IG502:  

  ![](images/2020-07-13-11-36-38.png)  

- Step 2: Install and run Device Supervisor

  Please refer to [3.1 Install and Run Python App](#install-and-run-python-app) for how to install and run Device Supervisor.  

- Step 3: Add a PLC
  
  Choose **Edge Computing > Device Supervisor > Device List**, and click **Add**. On the device adding page, select the PLC protocol and configure the PLC communication parameters. The following figure is an example of adding S7-1200 PLC:  

  ![](images/2020-06-02-14-19-45.png)  

- Step 4: Add variable
  
  On the **Device List** page, click **Add** variable, and configure the variable parameters in the pop-up box.  

  ![](images/2020-06-02-14-38-18.png)  

- Step 5: Configure a cloud service to report and receive data

  Choose Edge Computing > Device Supervisor > Cloud. Select Enable Cloud Service, configure the MQTT connection parameters and publish and subscribe messages (this document takes the configuration of publish messages as an example), and then click Submit. After the above configuration is correctly completed, the collected data can be monitored in the gateway and cloud platform.  

  ![](images/2020-09-30-15-51-28.png)  

  ![](images/2020-06-22-11-59-03.png)

## Appendix
### Factory reset
There are two ways to restore the IG502 to factory settings: hardware factory reset and software factory reset.
- Hardware factory reset  
  - Step 1: After the device is powered on and the ERR light is off, press and hold the RESET key;  
  - Step 2: When the ERR light is always on, release the RESET key;  
  - Step 3: After the ERR light goes out, press and hold the RESET key again, and release the RESET key when the ERR light flashes; wait for the ERR light to go out, indicating that the factory reset was successful.  
   
- Software factory reset  
  
  Choose System Management > Configuration Management, click the reset button and select OK. IG502 will complete the factory reset operation by itself.  

  ![](images/2021-01-21-19-15-01.png)