#!/bin/bash

echo "--------------------Computer Name and User Name--------------------" >> client_device_information.txt
whoami >> client_device_information.txt
#This command returns information about the computer name and user name
echo "------------- Host Name --------------" >> client_device_information.txt
hostname >> client_device_information.txt
#This command information about the host name 
echo "------------- IP and Network Adapters ---------" >> client_device_information.txt
ifconfig >> client_device_information.txt
#This command provides IP information and network information
echo "------- Available Memory Space ----------" >> client_device_information.txt
cat /prog/meminfo | grep Free >> client_device_information.txt
#This command information about available memory space
echo "------------- Available Hard Disk Space ----------------" >> client_device_information.txt
df -h >> client_device_information.txt
#This command information about hard disk space
echo "-------- Current Working Directory ----------" >> client_device_information.txt
pwd >> client_device_information.txt
#This command gives information about which file it is running.
echo "------ Running Applications and Services --------" >> client_device_information.txt
ps aux >> client_device_information.txt
#This command provides information about running applications.
echo "-------- Get Current Opened Ports -------------" >> client_device_information.txt
netstat -an >> client_device_information.txt
#This command provides information about open ports
