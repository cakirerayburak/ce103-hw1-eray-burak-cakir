@echo off
color a
> client_device_information.txt (
echo ----- Computer Name and User Name  -----
whoami 
echo -------------------------------------------------------

echo ----- Host Name -----
hostname 

echo --------------------------------------------------------
echo ----- IP and Network Adaptors -----
ipconfig/all

echo --------------------------------------------------------
echo ----- Available Memory Space -----
systeminfo | find "Available Physical Memory"

echo ---------------------------------------------------------
echo ----- Available Hard Disk Space -----
wmic logicaldisk get freespace,caption

echo ----------------------------------------------------------
echo ----- Working Directory -----
cd

echo ----------------------------------------------------------
echo ----- Running Applications and Services -----
tasklist

echo -----------------------------------------------------------
echo ----- Opened Ports -----
netstat -an |find /i "listening" 
)

