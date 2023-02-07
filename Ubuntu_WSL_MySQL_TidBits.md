# LINUX
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
