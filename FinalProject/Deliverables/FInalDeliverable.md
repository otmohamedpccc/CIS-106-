# Creating a Private Minecraft Server on Raspberry Pi

<!-- TOC -->autoauto- [Creating a Private Minecraft Server on Raspberry Pi](#creating-a-private-minecraft-server-on-raspberry-pi)auto    - [Project Description](#project-description)auto    - [Requirements and Hardware used for this build](#requirements-and-hardware-used-for-this-build)auto    - [Software used](#software-used)auto    - [Hardware used to build a minecraft server](#hardware-used-to-build-a-minecraft-server)auto    - [Important information on software being used](#important-information-on-software-being-used)auto    - [What is Minecraft](#what-is-minecraft)auto- [Commands used to build the Server](#commands-used-to-build-the-server)auto    - [Best practices](#best-practices)auto    - [Updating Memory Split](#updating-memory-split)auto    - [Allow SSH connections (optional)](#allow-ssh-connections-optional)auto    - [Installing Java](#installing-java)auto    - [Create a Spigot Server](#create-a-spigot-server)auto    - [Connecting to your Minecraft Server](#connecting-to-your-minecraft-server)auto    - [Boot your server Automatically (optional)](#boot-your-server-automatically-optional)auto    - [Issues Encountered](#issues-encountered)auto    - [Works Cited](#works-cited)autoauto<!-- /TOC -->

## Project Description
* For my project I have decided to build a private Minecraft sever using a 3rd party server software which is also supported by minecraft, so dont worry! Everything you do here is completely safe and legal!

## Requirements and Hardware used for this build
* Raspberry pi 400(RPi-400)
  * roadcom BCM2711 quad-core Cortex-A72 (ARM v8) 64-bit SoC @ 1.8GHz
  * 4GB LPDDR4-3200
  * Dual-band (2.4GHz and 5.0GHz) IEEE 802.11b/g/n/ac wireless LAN
  * MicroSD card slot for operating system and data storage

* Asus 27 inch monitor
* micro HDMI to standard HDMI - this is used to connect your RPi to a monitor that supports HDMI
* rpi optical mouse - so you can navigate RPi's GUI


* lenovo laptop - *I used a laptop running minecraft for this build, a desktop will work the same*
  * Ryzen 5 
  * 16gb ram 
  * 256gb storage 

* Make sure your laptop and/or desktop is able to run minecraft.

*Minimum requirements:* 
  * CPU: Intel Core i3-3210 3.2 GHz / AMD A8-7600 APU 3.1 GHz or equivalent.

  * RAM: 4GB.
  
  * GPU (Integrated): Intel HD Graphics 4000 (Ivy Bridge) or AMD Radeon R5 series (Kaveri line) with OpenGL 4.4*
  
  * GPU (Discrete): Nvidia GeForce 400 Series or AMD Radeon HD 7000 series with OpenGL 4.4.

## Software used 
* Minecraft (Java Edition)
* BuildTools.jar
* Raspberry Pi OS (FKA:Raspbian)
* Windows 10 (what my laptop is running) 

## Hardware used to build a minecraft server
* Raspberry pi 400
    * roadcom BCM2711 quad-core Cortex-A72 (ARM v8) 64-bit SoC @ 1.8GHz
    * 4GB LPDDR4-3200
    * Dual-band (2.4GHz and 5.0GHz) IEEE 802.11b/g/n/ac wireless LAN
    * MicroSD card slot for operating system and data storage

* Asus 27 inch monitor
* micro HDMI to standard HDMI
* rpi optical mouse


* lenovo laptop 
  * Ryzen 5 
  * 16gb ram 
  * 256gb storage 


## Important information on software being used
* Spigotmc.org
* Youtube : MakeTechEasier: How to turn your Raspberry Pi into a Minecraft Server
* Minecraft.net

* What is SpigotMC.org? - SpigotMC.org is home to the community behind the biggest Minecraft server software projects and provides a place for everyone involved with minecraft servers to connect with each other whether theyre seeking help and support or sharing and showcasing their work. SpigotMC.org provides a webforum, chatroom, and wiki for providing support aswell as project hosting for content creators. Spigot hopes to have new users join the growing community of 300,000 members

* What is Spigot?- is a modified Minecraft server based on CraftBukkit which provides additional performance optimizations, configuration options and features, whilst still remaining compatible with all existing plugins and consistent with Vanilla Minecraft game mechanics.There are over 150 improvements present in only in Spigot, including BungeeCord support; configuration of many internal server values such as crop growth rates, hunger, entity tracking, map seeds; enhanced watchdog and timings profiling to catch plugin issues; further configuration to heavy elements such as entity activation and hoppers; rewritten chunk loading, unloading and saving; and some useful API additions for developers.

* CraftBukkit- a modified version of the Vanilla Minecraft Server which allows it to run Bukkit plugins. The main goal of this project is to produce a server as close to Vanilla as possible, barring the addition of plugin support. That being said CraftBukkit still retains some useful configurability and optimizations such as asynchronous chunk loading, and also fixes for some critical Vanilla bugs or exploits.

* Bukkit - Bukkit is the API that developers can use to make server plugins

* API - Application Plugin Interface which allows applications to talk to each other

* BuildTools.jar - is the solution to building Bukkit, CratBukkit, Spigot, Spigot-API

## What is Minecraft
* Minecraft is a single/multiplayer sandbox that challenges players to survive, build, and, defeat mobs(enemies) using the natural resources around the minecraft world. Each time a new world is created, a new seed is generated, meaning every Minecraft world is totally unique.

* There are multiple versions of Minecraft, like java edition for computers, mobile edition for phones and mobile devices, and bedrock edition which is seen on consoles. For this build we are using the java edition as it enables us to create the private server we want.

# Commands used to build the Server

## Best practices
* It is always best practice to enure your system is up to date whenever logging in.

* Enter the following commands:

  * sudo apt-get update - This command will acquire any update that was added to the OS
  * sudo apt-get upgrade - This will upgrade any old software.
  * reboot - your RPi will reboot 

## Updating Memory Split
* You want to tell Raspberry Pi OS how it should use its available memory. (My RPI400 does not need to have its memory manually split but for older versions of RPi, like the Rpi 3 you do. In this case I did the same for the sake of universal application of this setup)

  * First, enter **sudo raspi-config** - This will prompt the RPi Software Configuration Tool, From There got to: 
  * **Performance Options** > **Memory Split** > **Set to 16** - this will give your GPU a constant 16mb to work with.
  * The configuration tool will ask if youd like to reboot in which case you will so select *yes*
![perfoptions](../FP%20images/performance%20options.png)
![memorysplit](../FP%20images/memorysplit%2016mb.png)

## Allow SSH connections (optional) 
This will allow you to connect remotely to your Raspberry Pi and the Minecraft Server.
* In the **Tool Bar** Navigate to **Preferences** > **Raspberry Pi Configuration** > Select the **Interfaces** Tab > Look for **SSH** and select **Enable** then press **Ok**

* Afterwards you want to reboot your Raspberry Pi by either entering the reboot command in the terminal or by navigating to reboot on your desktop so the settings you've changed take immediate affect.

## Installing Java
Since the version of Minecraft we are using is the java edition, you want to make sure your Raspberry Pi has Java Installed. 

* To install the default Java Package (JDK) enter 
  * **sudo apt-install default-jdk** - this will download the default java package
[installingjava](../FP%20images/installing%20java.png)

## Create a Spigot Server
* Spigot is a modified Minecraft server that includes useful performance optimizations, we are going to use a builders tool that is provided by spigot called BuildTools.jar

* First you need to build the Minecraft server file
  
 
* Command 1 - **mkdir /home/pi/minecraft** - this will create the minecraft directory in your home directory. 
  
    * Note that my user is still called *pi*, if you have changed the name of the user, replace *pi* in the command with your  username.

* Command 2 - **cd /home/pi/minecraft** - will change your current directory to the minecraft directory where we will be holding everything involving the minecraft server.

* Command 3 - *wget https://hub.spigotmc.org/jenkins/job/BuildTools/lastSuccessfulBuild/artifact/target/BuildTools.jar* - This will download the building tool called BuildTools.jar.
![BuildTools.jar](../FP%20images/spigotbuildtools.png)

* Command 4 - **java -Xmx1024M -jar BuildTools.jar --rev 1.16.5** This command will create the java archive (.jar) file for your minecraft server. This command may take time and will notify you in the terminal when complete 
  * Note that the rev number is based off the latest edition of Minecraft used. If you are using a newer or older version of Minecraft, enter that versions number instead.
  * Note this command will take some time to complete.
  ![servercreating](../FP%20images/servercreating%20.png) 


  
* Command 5 - **java -Xms512M -Xmx1008M -jar /home/pi/minecraft/spigot-1.16.5.jar nogui** - This command will Launch your server, this also may take some time as it has to unpack and setup the server
  * Before it launches, a message will appear in your terminal asking you to accept the eula.txt, you can either **nano eula.txt** or **vim eula.txt** to enter the text file and change from **eula=false** to **eula=true** 
  ![accepteula](../FP%20images/eulaagree.png)
  ![agreeeula](../FP%20images/eulatrue.png)

 
  
* Command 6 - enter **reboot** into the terminal to reboot your Raspberry Pi and when your desktop re-appears, launch the server again using **command 5**. Wait for it to finish launching and then your server should be ready.

## Connecting to your Minecraft Server 

* The first step is to launch Minecraft java edition on your laptop or desktop.

* Select Multiplayer > add server > then you can name your server whatever you want but the server address **must be your Raspberry Pis IP**

* In order to connect to the server on your RPi you need to know the IP address of the device.

* Enter the command **sudo hostname -I** - This will display your IP address on the terminal.

* Enter your RPi Ip into *server address* 
![minecraftsever](../FP%20images/minecraftserver.PNG)

* You should now be connected and able to play on your minecraft server
![upandrunning](../FP%20images/minecraftserverupandrunning.PNG) 

## Boot your server Automatically (optional)

* If you decide that you do not want to set up your server for automatic boots, you will have to re enter **command 5** everytime you start your RPi.
* To start your server at boot you need to create a new service for the Minecraft server

* In your terminal enter this command - **sudo nano /lib/systemd/system/minecraftserver.service**

* In the nano file you just created, enter the following information.
![autostartcontent](../FP%20images/autostartcontents.png) 
* this is the information and commands your RPi will use to automatically start the server. Save the contents.

* Now you can enable auto start by entering this command **sudo systemctl start minecraftserver.service**, your server should now start up every time you start your RPi.

## Issues Encountered 
* There were no issues encountered when building this server.

## Works Cited 
* Spigotmc.org/wiki/index
* Youtube : MakeTechEasier: How to turn your Raspberry Pi into a Minecraft Server
* Minecraft.net



