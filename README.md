# LinuxDayOne
#First Day Commands &amp; Assignments

#BIOS -> MBR -> Kernel Loading ->  System script

#Run levels

#/etc/init startup Scripts
#Create customstartup.sh file (file exists in same repository ,copy that) and Run Below steps
#Please do the required changes in customstartup.sh . i.e /home/parallels shpuld be replaced by your path name.

   sudo vim customstartup.sh
   sudo chmod 777 customstartup.sh 
   sudo cp customstartup.sh /etc/init.d/customstartup.sh 
   cd /etc/rc3.d/
   sudo ln -s ../init.d/customstartup.sh /etc/rc3.d/S10customstart
   ls -ltr /etc/rc3.d/


#Now reboot the system and you will find the file created 

#for shutdown specific script

   sudo vim customshutdown.sh
   sudo chmod 777 customshutdown.sh 
   sudo cp customstartup.sh /etc/init.d/customshutdown 
   cd /etc/rc3.d/
   sudo ln -s ../init.d/customshutdown S10customshutdown
   ls -ltr /etc/rc3.d/



