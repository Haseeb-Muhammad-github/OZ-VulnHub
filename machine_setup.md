Before setting up the machine , let us understand some differences in different network types that machines connect/interact with each other

IN CONTEXT OF VIRTUALIZATION PLATFORMS

NAT:   Network Address Translation

Purpose of NAT is to translate your Public IP into Private IP , so  by doing the transaltion it means performing DHCP  among the devoces  it is connected to.

On virtualization platforms like VMware , it performs DHCP by using Network Address Port Translation , i.e assigning IP to each virtual machine  dynamically.

-> In NAT mode VMs are hidden from the physical local network. IT means your wifi router and other devices connected to it cannot discover your machine 
  
  But your VM and your OS can ping each other usingg  PING commmand

-> In Bridge mode : the VM has direct access to the physicalnetwork , i.e the IP  is assigned by the netowrk your device is connected to. So the name Bridge is obvious that , your Virtual platform makes a bridge over your host OS and makes it's own way to ge to the outer netowrk.
     
     Your machine is exposed to teh outer world.

     
1) Download the machine from here: https://www.vulnhub.com/entry/oz-1,317/


2) And dowenload a kali virtual machine for vmware  from kali website 

3) Extract both VMs  

4) OPEN the VMware (player or workstation) and click on "open a virtual machiine"
   Vmware will set up both machine by itself , just make sure to do NAT in both VMs settngs

5) Start both machines . 

6) Go to Kali terminal and use the tool ifconfig and  NMAP
     
     ifconfig will give you the IP of your kali machine
       ![alt text](../images/IFCONFIG.png)

     now use Nmap and use this command 

      nmap 192.168.32.0/24 

        use your machine's ip subnet to scan it using NMAP and it would look like this 
          ![alt text](../images/NMAP SUBNET SCAN.png)

     
7)  Now you are all set and just use this ip of the machine with everything that you wanna do with it 
