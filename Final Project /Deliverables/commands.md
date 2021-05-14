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
   * Note this command will take some time to complete.
  ![servercreating](../FP%20images/servercreating%20.png) 

  * Note that the rev number is based off the latest edition of Minecraft used. If you are using a newer or older version of Minecraft, enter that versions number instead.
  
* Command 5 - **java -Xms512M -Xmx1008M -jar /home/pi/minecraft/spigot-1.16.5.jar nogui** - This command will Launch your server, this also may take some time as it has to unpack and setup the server
  * Before it launches, a message will appear in your terminal asking you to accept the eula.txt, you can either **nano eula.txt** or **vim eula.txt** to enter the text file and change from **eula=false** to **eula=true** 
  ![accepteula](../FP%20images/eulaagree.png)
  ![agreeeula](../FP%20images/eulatrue.png)

 
  
* Command 6 - enter **reboot** into the terminal to reboot your Raspberry Pi and when your desktop re-appears, launch the server again using **command 5**. Wait for it to finish launching and then your server should be ready.

## Connecting to your Minecraft Server 

* The first step is to launch Minecraft java edition on your laptop or desktop.

* Select Multiplayer > add server > then you can name your server whatever you want but the server address **must be your raspberry pis IP**

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

* Now you can enable auto start by entering this command **sudo systemctl start minecraftserver.service**, your server should now start up every time you start your RPi
