#! /bin/bash

#echo "Enter The service name!"
#read sr_name

echo $1
sr_name=$1
sr_status=$(sudo systemctl is-active $sr_name)
sr_enabled=$(sudo systemctl is-enabled $sr_name)

if [[ "$sr_enabled" != "enabled"  &&  "$sr_enabled" != "disabled" ]]
	then
	clear
	echo  -e "\033[33;5m$sr_name service is not found. Please install the $sr_name service\033[0m" > /script_practice/logfile
	cat /script_practice/logfile
#	yum install -y $sr_name
	exit 0
fi

if [ "$sr_status" != "active" ]
	then
	clear
	echo  -e "\033[33;5m$sr_name service is insatlled. But not running. Please start the $sr_name service\033[0m" > /script_practice/logfile
	cat /script_practice/logfile
#	systemctl start $sr_name
	exit 0
fi
	clear
	echo  -e "\033[33;5m$sr_name service is already insatlled and running\033[0m" > /script_practice/logfile
	cat /script_practice/logfile
