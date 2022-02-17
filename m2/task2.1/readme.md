# 
## TASK 2.1
### PART 1. HYPERVISORS
1.What are the most popular hypervisors for infrastructure virtualization?

**_Answer: Oracle VM Virtualbox and VMWare_**

2.Briefly describe the main differences of the most popular hypervisors

**_Answer: Oracle VM Virtualbox is free, VMWare is commertial software with official support and some additional instruments correct work of which garantied by owner_**

### PART 2. WORK WITH VIRTUALBOX
1.First run VirtualBox and Virtual Machine (VM).

1.1 Get acquainted with the structure of the user manual VirtualBox [1](see list of references in the end of the document)

1.2From the official VirtualBox site [2] download the latest stable version of VirtualBox according to the host operating system (OS) installed on the student's workplace. For Windows, the file may be called, for example, VirtualBox-6.1.10-138449-Win.exe. Install VirtualBox.

1.3Download the latest stable version of Ubuntu Desktop or Ubuntu Server from the official site [3].

1.4Create VM1 and install Ubuntu using the instructions [1, chapter 1.8]. Set machine name as "host machine name"_"student last name"

[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task2.1/images/1_4.JPG)]

1.5Get acquainted with the possibilities of VM1 control -start, stop, reboot, save state, use Host key and keyboard shortcuts, mouse capture, etc. [1, ch.1.9].

[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task2.1/images/1_5.JPG)]

1.6Clone an existing VM1 by creating a VM2 [1, ch.1.14].

[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task2.1/images/1_6.JPG)]

1.7Create a group of two VM: VM1, VM2 and learn the functions related to groups [1, ch.1.10].

[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task2.1/images/1_7.JPG)]

1.8For VM1, changing its state, take several different snapshots, forming a branched tree of snapshots[1, ch.1.11].

[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task2.1/images/1_8.JPG)]

1.9Export VM1. Save the *.ova file to disk. Import VM from *.ova file[1, ch.1.15

[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task2.1/images/1_9.JPG)]

[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task2.1/images/1_91.JPG)]

2.Configuration of virtual machines
2.1 Explore VM configuration options (general settings, system settings, display, storage, audio, network, etc.).

[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task2.1/images/2_1.JPG)]

2.2 Configure the USB to connect the USB ports of the host machine to the VM[1, ch.3.11].

[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task2.1/images/2_2.JPG)]

2.3 Configure a shared folder to exchange data between the virtual machine and the host [1, ch.4.3].

[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task2.1/images/2_3.JPG)]

2.4 Configure  different  network  modes  for  VM1,  VM2.  Check  the  connection between VM1, VM2, Host, Internet for different network modes. You can use the pingcommand to do this. Make a table of possible connections.

[![N|Solid](https://github.com/OleksandrK1/DevOps_online_Kyiv_2022Q1Q2/raw/main/m2/task2.1/images/2_4.JPG)]

3.Work with CLI through VBoxManage.3.1 Run the cmd.exe command line.3.2 Examine  the  purpose  and  execute  the  basic  commands  of  VBoxManage list, showvminfo, createvm, startvm, modifyvm, clonevm, snapshot, controlvm[1, ch.8].



`**_to be continued soon, I hope..._**`

