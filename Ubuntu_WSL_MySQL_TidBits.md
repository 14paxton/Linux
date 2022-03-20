WSL - Ubuntu for windows -
https://docs.microsoft.com/en-us/windows/wsl/reference

https://docs.microsoft.com/en-gb/windows/wsl/install-win10

Ubuntu for windows path

relative path

\\wsl$\Ubuntu\home\bpaxton

absolute path to root

C:\Users\bpaxton\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_79rhkp1fndgsc\LocalState\rootfs

shell exe, (can point ide to this to use ubuntu in terminal)

C:\Users\bpaxton\AppData\Local\Microsoft\WindowsApps\ubuntu.exe

use in JetBrains ides https://www.jetbrains.com/help/idea/how-to-use-wsl-development-environment-in-product.html

wsl.exe --distribution Ubuntu

CMD
Check time echo %date% %time% & tzutil /g

   “Central Standard Time”

Force delete

   RMDIR /S /Q

Change TimeZone

  check timezone   tzutil /g

  list timezones tzutil /l

  set timezone tzutil /s

Create symbolic link

o   mklink /D "E:\Path\newFolder" "F:\folderIwantToLinkFrom"

Get WIFI password

o   netsh wlan show profile ALLO1D67CF_5G key=clear

Power saver:
powercfg -duplicatescheme a1841308-3541-4fab-bc81-f71556f20b4a

Balanced:
powercfg -duplicatescheme 381b4222-f694-41f0-9685-ff5bb260df2e

High Performance:
powercfg -duplicatescheme 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c

Ultimate Performance (available since Windows 10 April 2018 Update):
powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61

 

-change timeout

            You can enter the below commands to do so, the equivalent of setting them to never:

powercfg /change standby-timeout-ac 0

powercfg /change standby-timeout-dc 0

powercfg /change monitor-timeout-ac 0

powercfg /change monitor-timeout-dc 0

powercfg /change hibernate-timeout-ac 0

powercfg /change hibernate-timeout-dc 0

AC and DC determine 'on battery' and 'plugged in', while 0 disables these options.

-getting to control panel display setting,

            Open win + r, enter       shell:::{ED834ED6-4B5A-4bfe-8F11-A626DCB6A921} -Microsoft.Personalization\pageWallpaper

 

LINUX
Find and kill instance by port

   netstat -ano | findstr :3000

   taskkill /PID 8880 /F

zip files

    sudo apt-get install zip

   zip -r {filename.zip} {foldername}

UBUNTU

Java

JPS - https://docs.oracle.com/en/java/javase/17/docs/specs/man/jps.html

running java processes = jps -lV

 find process by port

lsof -i:18090

MYSQL
mysql -u USERNAME -p

show databases;

SETTING TIMEZONES

o    Get timezone = SELECT @@global.time_zone, @@session.time_zone;

o    Get timestamp = SELECT CURRENT_TIMESTAMP();
o    Set timestamp utc = SET @@session.time_zone='+00:00';
§  You can set in my.cnf

o    [mysqld]

                                 **other variables**

                 default_time_zone='+00:00'

-GET PATHS

 

MySQL import
 

LOAD DATA LOCAL INFILE 'C:/Groovy/englishData.csv' INTO TABLE original_data

FIELDS TERMINATED BY ','

ENCLOSED BY '"'

LINES TERMINATED BY '\r\n'

IGNORE 1 LINES

 

 

 

SDKMAN- https://sdkman.io/usage
Install sdkman

   curl -s https://get.sdkman.io | bash

   source "$HOME/.sdkman/bin/sdkman-init.sh"

list candidates

   sdk list

list versions

   sdk list [program]

sdk use [program] [version number]

   will use for cmd shell only

sdk default [program][version number]

   will switch default
