# script.sh-invent
#!/bin/bash

#DESCRIPTION: Class assignment wk11 second question
#AUTHOR: Banks
#DATE: Dec/10/2021


operation=`hostnamectl |grep O |awk '{print $3}'`
version=`hostnamectl |grep O |awk '{print $4}'`

echo " your OS is ${operation} and the Version is ${version} "
sleep 3
 rpm --eval 'your memory size is:'
 sleep 3
 free -m | tail -2 | head -1 | awk '{print $1,$2}'
 sleep 3
  rpm --eval 'your harddrive size is:'
  sleep 3
  lsblk
  sleep 3
   rpm --eval 'your cpu is:'
   sleep 3
    lscpu |head -4 | tail -1 | awk '{print $2}'
    sleep 3
     rpm --eval 'your kernel version is:'
     sleep 3
     uname -r
     sleep 3
      rpm --eval 'your system bits is:'
      sleep 3
      getconf LONG_BIT
      sleep 3
       rpm --eval 'your hostname is:'
       sleep 3
       hostname
       sleep 3
        rpm --eval 'your ip address is:'
        sleep 3
        hostname -I | awk '{print $1}'
        sleep 3
         rpm --eval 'searching for all open ports:'
         sleep 3
         lsof -i -P -n | grep LISTEN |awk '{print $1,$8,$9,$10 }'
         sleep 3
          rpm --eval 'your dns is:'
          sleep 3
          grep "nameserver" /etc/resolv.conf
          rpm --eval 'your manufacturer is'
          dmidecode -t system |grep Man |awk '{print $2,$3}'          sleep 3

           rpm --eval 'your system is virtual or physical'
           sleep 3
            dmidecode | grep Fa |awk '{print $2,$3}'
            sleep 3
             rpm --eval 'your mac address is:'
             sleep 3
             ip a | grep ether |head -1 |awk '{print $2}
