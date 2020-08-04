# InGateway501 Command Line Instructions

  - [Command Line Instructions](#command-line-instructions)
    - [1. Help Command](#help-command)
      - [1.1 ?](#firstone)
    - [2. View Switching Commands](#view-switching-commands)
      - [2.1 enable](#enable)
      - [2.2 disable](#disable)
      - [2.3 exit](#exit)
    - [3. System Status Display Commands](#view-system-status-commands)
      - [3.1 show version](#show-version)
      - [3.2 show system](#show-system)
      - [3.3 show clock](#show-clock)
      - [3.4 show log](#show-log)
      - [3.5 show users](#show-users)
      - [3.6 show startup-config](#show-startup-config)
    - [4. Network Status Display Commands](#view-network-status-command)
      - [4.1 show interface](#show-interface)
      - [4.2 show ip route](#show-ip-route)
      - [4.3 show arp](#show-arp)
    - [5. Network Test Commands](#network-test-commands)
      - [5.1 ping](#ping)
      - [5.2 telnet](#telnet)
      - [5.3 traceroute](#traceroute)
    - [6. Configuration Commands](#configuration-commands)
      - [6.1 configure terminal](#configure-terminal)
      - [6.2 hostname](#hostname)
      - [6.3 clock timezone](#clock-timezone)
      - [6.4 clock set](#clock-set)
      - [6.5 sntp-client](#sntp-client)
    - [7. System Management Commands](#system-management-commands)
      - [7.1 reboot](#reboot)
      - [7.2 enable password](#enable-password)
      - [7.3 username](#username)

<a id="command-line-instructions"> </a>

## Command Line Instructions

<a id="help-command"> </a>

### 1. Help Command

You can enter **help** or a question mark (**?**) on the console to obtain help information about commands. When typing in a command, you can enter **?** anytime to obtain help information about the current command or parameters of the command. If the character string you have entered matches a unique command or parameter, the command or parameter will be displayed automatically after you enter **?**.

<a id="firstone"> </a>

#### 1.1 ?

**Command**: [\<cmd>] ?  

**Function**: provides help information about a command.   

**View**: all views  

**Parameters**: <cmd>, which specifies a command name  

**Example**:

- Enter: `?`   
  
  The list of available commands is displayed.
- Enter: `show ?`   
  
  All parameters of the **show** command and descriptions of these parameters are displayed.

<a id="view-switching-commands"> </a>

### 2. View Switching Commands

<a id="enable"> </a>

#### 2.1 enable

**Command**: enable 15 [\<password>]  

**Function**: switches to the view of the privileged user level.   

**View**: ordinary user view  

**Parameters**:

- 15: specifies the user privilege level. Currently, the value can only be 15 (super user).
- password: specifies the password of the specified privilege level. If you do not enter the password, the system displays a password input prompt.

**Example**:

- In the ordinary user view, enter: `enable 15 123456`  
  
  The super user view is displayed. The password used in this example is **123456**.

<a id="disable"> </a>

#### 2.2 disable

**Command**: disable  

**Function**: exits from the view of the privileged user level.   

**View**: super user view, configuration view  

**Parameters**: none  

**Example**:

- In the super user view, enter: `disable`  
  
  The ordinary user view is displayed.

<a id="exit"> </a>

#### 2.3 exit

**Command**: exit  

**Function**: exits from the current view and returns to the previous view. (If the current view is the ordinary user view, you will exit from the console after running this command.)   

**View**: all views  

**Parameters**: none  

**Example**:

- In the configuration view, enter: `exit`  
  
  The super user view is displayed.
- In the ordinary user view, enter: `exit`  
  
  You exit from the console.

<a id="view-system-status-commands"> </a>

### 3. System Status Display Commands

<a id="show-version"> </a>

#### 3.1 show version

**Command**: show version  

**Function**: displays the version information of the IG902, such as the product model and software version.   

**View**: all views  

**Parameters**: none  

**Example**:

- Enter:  show version  
  
  The following information is displayed:   

  Model: indicates the model of the IG902.  

  Serial number: indicates the serial number of the IG902.  
  
  Firmware version: indicates the firmware version running on the IG902.  
  
  Bootloader version: indicates the Bootloader version running on the IG902.

<a id="show-system"> </a>

#### 3.2 show system

**Command**: show system  

**Function**: displays the system information of the IG902.   

**View**: all views  

**Parameters**: none  

**Example**:

- Enter: `show system`  
  
  Information similar to the following is displayed:  
  
  `09:26:45 up 5 days, 14:33, 1 users, load average: 0.00, 0.01, 0.04`

<a id="show-clock"> </a>

#### 3.3 show clock

**Command**: show clock  

**Function**: displays the system time of the IG902.   

**View**: all views  

**Parameters**: none  

**Example**:

- Enter: `show clock`  
  
  Information similar to the following is displayed:  
  
  `Wed Apr 15 09:33:48 UTC 2020`

<a id="show-log"> </a>

#### 3.4 show log

**Command**: show log [lines \<n>]  

**Function**: displays system logs of the IG902. By default, the latest 100 logs are displayed.   

**View**: all views  

**Parameters**: lines <n>, which limits the number of logs displayed. When n is a positive integer, the command displays the latest n logs. When n is a negative integer, the command displays the earliest n logs. When n is 0, the command displays all logs.   

**Example**:

- Enter: `show log`  
  
  The latest 100 logs are displayed.
- Enter: `show log lines 10`  
  
  The latest 10 logs are displayed.

<a id="show-users"> </a>

#### 3.5 show users

**Command**: show users  

**Function**: displays the list of users on the IG902.   

**View**: all views  

**Parameters**: none  

**Example**:

- Enter: `show users`  
  
  Information similar to the following is displayed:  

  <table>
  <tr>
  <td>USER</td>
  <td>TTY</td>
  <td>IDLE</td>
  <td>TIME</td>
  <td>HOST</td>
  </tr>
  <tr>
  <td>adm</td>
  <td>pts/0</td>
  <td>00:00</td>
  <td>Apr 15 09:26:41</td>
  <td>192.168.1.15</td>
  </tr>
  </table>


<a id="show-startup-config"> </a>

#### 3.6 show startup-config

**Command**: show startup-config  

**Function**: displays the startup configuration of the IG902.   

**View**: super user view, configuration view  

**Parameters**: none  

**Example**:

- Enter: `show startup-config`  
  
  The startup configuration of the system is displayed.

<a id="view-network-status-command"> </a>

### 4. Network Status Display Commands

<a id="show-interface"> </a>

#### 4.1 show interface

**Command**: show interface  

**Function**: displays the status of interfaces on the IG902.   

**View**: all views  

**Parameters**: none  

**Example**:

- Enter: `show interface`  
  
  The status of all interfaces is displayed.

<a id="show-ip-route"> </a>

#### 4.2 show ip route

**Command**: show ip route  

**Function**: displays the routing table of the IG902.   

**View**: all views  

**Parameters**: none  

**Example**:

- Enter: `show ip route`  
  
  The routing table of the system is displayed.

<a id="show-arp"> </a>

#### 4.3 show arp

**Command**: show arp  

**Function**: displays the ARP table of the IG902.   

**View**: all views  

**Parameters**: none  

**Example**:

- Enter: `show arp`  
  
  The ARP table of the system is displayed.

<a id="network-test-commands"> </a>

### 5. Network Test Commands

The IG902 provides multiple network test tools, such as ping, telnet, and traceroute.

<a id="ping"> </a>

#### 5.1 ping

**Command**: ping \<hostname> [count \<n>] [size \<n>] [source \<ip>]  

**Function**: performs an ICMP probe to a specified host.   

**View**: all views  

**Parameters**:

- hostname: specifies the IP address or domain name of the host to be tested.
- count \<n>: specifies the number of probes.
- size \<n>: specifies the size (bytes) of each probe datagram.
- source \<ip>: specifies the source IP address of probe datagrams.

**Example**: Enter: `ping www.baidu.com count 5 size 32`  

A ping test is initiated to www.baidu.com, and the test result is displayed.

<a id="telnet"> </a>

#### 5.2 telnet

**Command**: telnet \<hostname> [\<port>] [source \<ip>]  

**Function**: accesses a specified host through Telnet.   

**View**: all views  

**Parameters**:

- hostname: specifies the IP address or domain name of the host that you want to log in.
- port: specifies the port number of the Telnet service.
- source \<ip>: specifies the IP address used for Telnet login.

**Example**:

- Enter: `telnet 192.168.1.1`  
  
  You log in to the host at 192.168.1.1 through Telnet.

<a id="traceroute"> </a>

#### 5.3 traceroute

**Command**: traceroute \<hostname> [maxhops \<n>] [timeout \<n>]  

**Function**: traces the route to a specified host.   

**View**: all views  

**Parameters**:

- hostname: specifies the IP address or domain name of the host to be tested.
- maxhops \<n>: specifies the maximum number of hops allowed.
- timeout \<n>: specifies the timeout period on each hop.

**Example**:

- Enter: `traceroute www.baidu.com`  
  
  A traceroute test is initiated to www.baidu.com, and the test result is displayed.

<a id="configuration-commands"> </a>

### 6. Configuration Commands

You can run the `configure terminal` command in the super user view to switch to the configuration view, and run configuration commands in this view to manage the IG902. Some configuration commands support both the **no** and **default** forms. The **no** form cancels the setting of a parameter, and the **default** form restores the default setting of a parameter.

<a id="configure-terminal"> </a>

#### 6.1 configure terminal

**Command**: configure terminal  

**Function**: switches to the configuration view so that you can enter 
configuration commands on your terminal.   

**View**: super user view  

**Parameters**: none  

**Example**:

- In the super user view, enter: `configure terminal`  
  
  The configuration view is displayed.

<a id="hostname"> </a>

#### 6.2 hostname

**Command**:

- hostname [\<hostname>]
- default hostname

**Function**: sets a host name for the IG902.   

**View**: configuration view  

**Parameters**: \<hostname>, which specifies a new host name  

**Example**:

- In the configuration view, enter: `hostname MyRouter`  
  
  The host name of the IG902 is set to MyRouter.
- In the configuration view, enter: `default hostname`  
  
  The host name of the IG902 is restored to the factory setting.

<a id="clock-timezone"> </a>

#### 6.3 clock timezone

**Command**:

- clock timezone \<timezone>-\<n>
- default clock timezone  

**Function**: sets the time zone for the IG902.   

**View**: configuration view  

**Parameters**:
- \<timezone>: specifies a time zone name consisting of three uppercase English letters.
- \<n>: specifies the deviation of the time zone against the UTC, in the range of -12 to +12.  

**Example**:
- In the configuration view, enter: `clock timezone UTC-8`  
  
  The time zone of the IG902 is set to UTC+08:00, which is applicable to the Chinese mainland, Hong Kong, Western Australia, Singapore, Taiwan, and Russia.
- In the configuration view, enter: `default clock timezone`  
  
  The time zone of the IG902 is restored to the factory setting.

<a id="clock-set"> </a>

#### 6.4 clock set

**Command**: clock set \<YEAR/MONTH/DAY>-\<HH:MM:SS>  

**Function**: sets the date and time for the IG902.   

**View**: configuration view  

**Parameters**:

- \<YEAR/MONTH/DAY>: specifies a date, in the format of year-month-day.
- \<HH:MM:SS>: specifies a time, in the format of hours-minutes-seconds.

**Example**:

- In the configuration view, enter: `clock set 2009.10.5-10:01:02`  
  
  The time of the IG902 is set to 10:01:02 AM on October 5, 2009.

<a id="sntp-client"> </a>

#### 6.5 sntp-client

**Command**:

- sntp-client update-interval \<n>
- sntp-client source interface \<interface> \<slot/port>
- sntp-client server \<hostname> [\<port>] \<n>

**Function**: configures the IG902 as a Simple Network Time Protocol (SNTP) client.   

**View**: configuration view  

**Parameters**:

- update-interval \<n>: specifies the time synchronization interval. The valid value range is 60-2592000.
- \<interface> \<slot/port>: specifies the source interface of SNTP packets. Valid values are interfaces on the IG902, such as `cellular1`.
- \<Hostname>: specifies the IP address or domain name of the SNTP server.
- [\<port>] \<n>: specifies the port number of the SNTP server.

**Example**:

- In the configuration view, enter: `sntp-client update-interval 7200`  
  
  The time synchronization interval of the SNTP client is set to 7200 seconds.
- In the configuration view, enter: `sntp-client source interface cellular 1`  
  
  The source interface of the SNTP client is set to cellular1.
- In the configuration view, enter: `sntp-client server 0.pool.ntp.org port 123`  
  
  The SNTP client is configured to synchronize time from the server with the address of 0.pool.ntp.org and port of 123.

<a id="system-management-commands"> </a>

### 7. System Management Commands

<a id="reboot"> </a>

#### 7.1 reboot

**Command**: reboot  

**Function**: reboots the system.   

**View**: super user view, configuration view  

**Parameters**: none  

**Example**:

- In the super user view, enter: `reboot`  
  
  The system restarts.

<a id="enable-password"> </a>

#### 7.2 enable password

**Command**: enable password [\<password>]  

**Function**: changes the password of the super user.   

**View**: configuration view  

**Parameters**: \<password>, which specifies the new password of the super user  

**Example**:

- In the configuration view, enter: `enable password`  
  
  The password of the super user is changed.

<a id="username"> </a>

#### 7.3 username

**Command**:

- username \<name> [password [\<password>]]
- no username \<name>

**Function**: sets a user name and its password.   

**View**: configuration view  

**Parameters**:

- \<name>: specifies a user name.
- \<password>: specifies the password of the user.

**Example**:

- In the configuration view, enter: `username abc password 1234567`  
  
  An ordinary user **abc** is created, and its password is set to **1234567**. Or the password of ordinary user **abc** is changed to **1234567**.
- In the configuration view, enter: `no username abc`  
  
  The ordinary user **abc** is deleted.