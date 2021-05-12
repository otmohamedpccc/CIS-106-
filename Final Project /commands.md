# Commands used 

## Best practice 
* sudo apt-get update - This command will acquire any update that was added to the OS
* sudo apt-get upgrade - This will upgrade any old software.
* reboot

## updating memory split
* You want to tell Raspberry Pi OS how it should use its available memory. (My RPI400 does not need to have its memory manually split but for older versions of RPi, like the Rpi 3 you do. In this case I did the same for the sake of universal application of this setup)

  * First, enter **sudo raspi-config** - This will prompt the RPi Software Configuration Tool, From There got to: 
  * **Performance Options** > **Memory Split** > **Set to 16** - this will give your GPU a constant 16mb. 

## Allow SSH connections (optional) 
This will allow you to connect remotely  to your Raspberry Pi and the Minecraft Server.
* In the **Tool Bar** Navigate to **Preferences** > **Raspberry Pi Configuration** > Select the **Interfaces** Tab > Look for **SSH** and select **Enable** then press **Ok**
* Afterwards you want to reboot your Raspberry Pi by either entering the reboot command in the terminal or by navigating to reboot on your desktop so the settings youve changed take immediate affect.

## Installing Java
Since the version of Minecraft we are using is the java edition, you want to make sure your Raspberry Pi has Java Installed. 
* To install the default Java Package (JDK) enter 
  * **sudo apt-install default-jdk** - this will download the default java package

## Create a Spigot Server
* Spigot is a modified Minecraft server that includes useful performance optimizations, we are going to use a builders tool that is provided by spigot called BuildTools.jar

* First you need to build the Minecraft server file
  
 
* Command 1 **mkdir /home/pi/minecraft** - this will create the minecraft directory in your home directory. 
    * Note that my user is still called pi, if you have changed the name of the user, replace 'pi' in the command with your name.

* Command 2 **cd /home/pi/minecraft** - will change your current directory to the minecraft directory where we will be holding everything involving the minecraft server.

* Command 3 **wget https://hub.spigotmc.org/jenkins/job/BuildTools/lastSuccessfulBuild/artifact/target/BuildTools.jar** - This will download the building tool called BuildTools.jar.

* Command 4 **java -Xmx1024M -jar BuildTools.jar --rev 1.16.5** This command will create the java archive (.jar) file for your minecraft server. This command may take time and will notify you in the terminal when complete 
  * Note that the rev number is based off the latest edition of Minecraft used. If you are using a newer or older version of Minecraft, enter that versions number instead.
  
* Command 5 **java -Xms512M -Xmx1008M -jar /home/pi/minecraft/spigot-1.16.5.jar nogui** - This command will launch your server. 
  * Before it launches, a message will appear in your terminal asking you to accept the eula.txt, you can either **nano eula.txt** or **vim eula.txt** to enter the text file and change from **eula=false** to **eula=true** 
  
* Command 6 enter **reboot** into the terminal to reboot your Raspberry Pi and when you desktop re appears. luanch the server again using command 5. Wait for it to finish launching and then your server should be ready.

## Connecting to your Minecraft Server 

* The first step is to launch Minecraft java edition on your laptop or desktop.

* Select Multiplayer > add server > then you can name your server whatever you want but the server address **must be your raspberry pis IP**

* In order to connect to the server on your RPi you need to know the IP address of the device.
* Enter the command **sudo hostname -I** - This will display your IP address on the terminal.

* You should now be connected and able to play on your minecraft server

## Boot your server Automatically 


