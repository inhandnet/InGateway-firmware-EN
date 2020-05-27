# InGateway501 Quick Start Manual
This document is used to explain the basic configuration operations of InGateway501 (IG501 for short) networking, software version update, etc., so that users can master the basic configuration of IG501 and the use of common functions.

  - [1. Configure IG501 Network Parameters](#configure-ig902-network-parameters)
    - [1.1 Set LAN Parameters: Access the IG501 Through LAN](#set-lan-parameters)
    - [1.2 Set WAN Parameters: Connect IG501 to the Internet](#set-wan-parameters)
  - [2. Update the Software](#update-the-software)
  - [3. Use Python Edge Computing](#use-python-edge-computing)
    - [3.1 Install and run Python App](#install-and-run-python-app)
    - [3.2 Update Configuration File for App](#update-configuration-file-for-app)
    - [3.3 Update Python App version](#update-python-app-version)
    - [3.4 Enable the Debug Mode](#enable-the-debug-mode)
  - [4. Device Manager](#device-manager)
  - [Appendix](#appendix)
    - [Factory reset](#factory-reset)

<a id="configure-ig902-network-parameters"> </a>  

## 1. Configure IG501 Network Parameters

<a id="set-lan-parameters"> </a>  

### 1.1 Set LAN Parameters: Access the IG501 Through LAN
- Step 1: Set the PC’s IP address to be on the same subnet with FE 0/1. By default, the IP address of FE 0/1 on IG501 is 192.168.1.1.   
  - Method 1: Enable the PC to obtain an IP address automatically (recommended)  

     ![](images/2020-01-02-09-55-52.png)  

  - Method 2: Set a fixed IP address   
  
     Select Use the following IP address, enter an IP address (By default,any from 192.168.1.2 to 192.168.1.254), subnet mask (By default,255.255.255.0), default gateway (By default,192.168.1.1), and DNS server address, and click OK.   

    ![](images/2020-01-21-15-57-32.png)  

- Step 2: Launch the browser on the PC and access the IP address of FE 0/1. Enter the login user name and password. The default user name and password are adm and 123456 respectively.  

  ![](images/2020-02-14-16-28-07.png)   

- Step 3: After successful login, you can see the web page as shown below:   

  ![](images/2020-02-14-10-03-48.png)  

- Step 4: To change the user name and password for logging in to the web management interface of IG501, choose System > User Management page of IG501 and set the new user name and password.   

  ![](images/2020-01-21-10-37-54.png)  

- Step 5: To change the IP address of FE 0/1, choose Network > Network Interfaces > Ethernet page of IG501 to configure FE 0/1.  

  ![](images/2020-01-21-10-42-52.png)  

<a id="set-wan-parameters"> </a>  

### 1.2 Set WAN Parameters: Connect IG501 to the Internet
- Step 1: Insert the SIM card. (Note: Before inserting or removing the SIM card, unplug the power cable; otherwise, the operation may cause data loss or damage the IG501.) After inserting the SIM card, connect the 4G LTE antenna to the ANT interface and power on the IG501.  

  ![](images/2020-01-02-10-10-25.png)  

- Step 2: Choose Network > Network Interfaces > Cellular and select Enable Cellular.  

  ![](images/2020-02-13-14-36-40.png)  

  When the network connection status is Connected and an IP address has been allocated, the IG501 has been connected to the Internet with the SIM card.  

  ![](images/2020-02-14-10-21-15.png)

<a id="update-the-software"> </a>  

## 2. Update the Software
To obtain the latest software version of IG501 and updated functions, contact the customer service center. To update the IG501 software version, do as follows:  
- Update the IG501 firmware.   
  
  Choose System > Firmware Upgrade. Select a firmware file and click Start Upgrading. After the update is completed, you are prompted to restart the system to Apply the new firmware.  

  ![](images/2020-01-21-14-20-39.png)  
   
- Upgrade the Python SDK of IG501.   
  
  Choose Edge Computing > Python Edge Computing. Select Python Engine, select an Python SDK file, and click Upgrade; when the upgrade confirmation window pops up, click Confirm. Then the IG501 automatically performs the upgrade.  

  ![](images/2020-02-12-14-09-43.png)  

<a id="use-python-edge-computing"> </a>  

## 3. Use Python Edge Computing

<a id="install-and-run-python-app"> </a>  

### 3.1 Install and run Python App
To install and run Python App (App for short) in IG501,  please refer to the following process:  
- Step 1: Install the App  
  
  Before installing the App, you need to ensure that the Python Edge Computing Engine is enabled and the Python SDK is installed, as shown in the following figure:  

  ![](images/2020-02-12-14-41-48.png)  

  Choose Edge Computing > Python Edge Computing. click the Add button and select the App package file to be installed, then click OK.  

  ![](images/2020-02-12-14-51-36.png)   

  After importing, you can view the imported Apps, as shown in the following figure:  

  ![](images/2020-02-12-14-53-53.png)   
   
- Step 2: Run the App   
  
  Select enable App and click Submit.  

  ![](images/2020-02-12-14-56-05.png)  

  Once enabled, the App automatically runs and will run every time the IG501 is started.  

  ![](images/2020-02-12-15-00-59.png)

<a id="update-configuration-file-for-app"> </a>  

### 3.2 Update Configuration File for App
If the installed App supports importing configuration files to modify the running mode, you can update the App running configuration by referring to the following process:  
- Step 1: Choose Edge Computing > Python Edge Computing, click the Import Configuration button and select the configuration file to be imported, then click Confirm.  
  
  ![](images/2020-02-12-15-01-54.png)   
   
- Step 2: Restart the App after the import is successful. After the App restarts, it will runing according to the imported configuration file.  
  
  ![](images/2020-02-12-15-02-29.png)

<a id="update-python-app-version"> </a>  

### 3.3 Update Python App version
Generally, if you need to update the Python App version, you only need to import the new version of the App on the Edge Computing > Python Edge Computing page.  

![](images/2020-03-19-16-14-45.png)  

After the update is completed, as shown below：  

![](images/2020-03-19-16-16-20.png)

<a id="enable-the-debug-mode"> </a>  

### 3.4 Enable the Debug Mode
To run and debug Python code on IG501, you need to enable IG501's debug mode.  Choose Edge Computing > Python Edge Computing, select Enable Debug Mode. After enabling, you can develop IG501 through VS Code. How to use VS Code for Python development of IG501, please refer to [Quick Start for MobiusPi Python Development](http://sdk.ig.inhandnetworks.com/en/latest/MobiusPi%20Python%20QuickStart-EN.html).  

![](images/2020-02-12-15-04-41.png)  

After the debugging mode is enabled, IG501 will start an SSH server to listen on port 222 of LAN (default IP address being 192.168.1.1). The user name and password of the SSH server are displayed on the previous web page. A random password is generated every time the debugging mode is enabled or the IG501 is restarted to ensure security.

<a id="device-manager"> </a>  

## 4. Device Manager
The Device Manager developed by InHand supports functions such as monitoring IG501 status, remote maintenance of equipment, remote batch delivery of IG501 configuration, and IG501 batch upgrade, helping users to conveniently and efficiently manage IG501 and field devices. In order to enable the Device Manager to remotely manage the IG501 and field devices, the IG501 needs to be connected to the cloud platform. The connection method is as follows:  
Choose System Management > Device Manager, tick Enable Device Manager and configure the corresponding server address and registered account, and click Submit after the configuration is complete.  
- Server address: the address of the Device Manager. The address of the Device Manager developed by InHand is as follows:  
  - Domestic version Device Manager：`c.inhandcloud.com`  
  - Overseas version Device Manager：`iot.inhandnetworks.com`  
  - Domestic version InConnect：`ics.inhandiot.com`  
  - Overseas version InConnect：`ics.inhandnetworks.com`  
- Registered account: the Device Manager account associated with the IG501 device (if you have not registered an account, you need to register an account first)  
- Advanced settings: Contains configurations such as heartbeat interval. Generally, you can use the default configuration.  

![](images/2020-03-19-16-26-25.png)   

After the IG501 is successfully connected to the Device Manager, the status is described as Connection Accepted.   

![](images/2020-03-19-16-27-08.png)  

## Appendix
### Factory reset
There are two ways to restore the IG501 to factory settings: hardware factory reset and software factory reset.  
- Hardware factory reset  
  - Step 1: After the device is powered on and the ERR light is off, press and hold the RESET key;  
  - Step 2: When the ERR light is always on, release the RESET key;  
  - Step 3: After the ERR light goes out, press and hold the RESET key again, and release the RESET key when the ERR light flashes; wait for the ERR light to go out, indicating that the factory reset was successful.   
   
- Software factory reset  
  
  Choose System Management > Configuration Management, click the reset button and select OK. IG501 will complete the factory reset operation by itself.  

  ![](images/2020-02-14-20-42-48.png)