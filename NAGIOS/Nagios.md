<u><h1 style="text-align:center">Nagios </h1></u>
Nagios is an open source continuous monitoring tool which monitors network, applications and servers. It gives the complete status of your IT infrastructure and its performance.

In case of any failure, Nagios alerts about the issues, so that the technical team can perform recovery process immediately.

Otherwise, application or server may be down.

<u><h1 style="text-align:center">Advantages of Nagios </h1></u>
- Detect all types of network or server issue.
- It helps you to find the root cause of the problem which allow you to get permanent solution to the problem.
- Reduce downtime.
- Active monitoring of entire infrastructure.
- Allow you to monitor & troubleshoot server performanance issues.
- Automatically fix problem.
  
 <u><h1 style="text-align:center">How does it works </h1></u>
- Mention all details in configuration file.
- Daemon read those details what data to be collected.
- Daemon use **NRPE** (Nagios Remote Plugin Executor) plugin to collect data from nodes & store in its own database.
- Finally, shows in dashboard.
  
<u><h1 style="text-align:center">Installation of Nagios in Ubuntu 20.04 </h1></u>

 <u><h2 >Environment details </h2></u>
**OS**- Ubuntu 20.04</br>
**CPU**- 8 Core</br>
**STORAGE**- 1 TB</br>

<u><h2 >Tool used </h2></u>

- podman version (3.4.2)
- Nagios version (4.4.8)
  
<u><h3 >Here are some steps for installing nagios in container: </h3></u>

### Command 1:-
This command is used for installation of podman.
```
apt install -y podman
```
### Command 2:-
This command will query the default container registry (usually Docker Hub) and return a list of container images with "nagios" in their name or description.
```
podman search nagios
```
![Alt text](image-fotor-20230909690.png)


### Command 3:-
This comand is used to pull the nagios container image from docker hub to your local system using podman.
```
podman pull docker.io/jasonrivers/nagios  
```
![Alt text](<Screenshot from 2023-09-04 20-07-24-fotor-2023090962043.png>)

### Command 4:- 
This command will start the Nagios container with the specified options. You can access the Nagios web interface by opening a web browser and navigating to http://localhost:8095/nagios. 

```
 podman run -d --name nagios -p 8095:80 --cap-add=NET_RAW -e NAGIOSADMIN_USER=reetu -e NAGIOSADMIN_PASSWORD=nagios docker.io/jasonrivers/nagios
 ```
 ![Alt text](run-fotor-2023090963145-fotor-2023090911117.png)

 ### Command 5 :-
Check running container details by this command.
 ```
podman ps
```
![Alt text](<podman ps-fotor-20230909105549.png>)

### Command 6:-
This command is used for going into the container and execute commands.
```
podman exec -it nagios bash
```

![Alt text](<Screenshot from 2023-09-09 11-03-36-fotor-202309091163.png>)

### Command 7:-
This command is used for  go into the directory.

```
cd /opt/nagios/etc
```

![Alt text](<Screenshot from 2023-09-09 11-08-52-fotor-20230909111153.png>)

### Command 8:-
```
ls
```
![Alt text](<Screenshot from 2023-09-09 11-13-39-fotor-20230909113319.png>)


### Command 9:-
This command is used  for editing in file.

```
vim cgi.cfg
```
Go to the cgi.cfg file and add your username.</br>
![Alt text](<Screenshot from 2023-09-09 11-53-29-fotor-20230909115510-fotor-2023090912821.png>)

### Final output

 Type **localhost:8095** on web page and then you can see preview on web interface.</br>

![Alt text](<Screenshot from 2023-09-08 11-34-20.png>) 

**checking services**
 we have to go on left side and click on the service option.</br>
 This is the dashboard of all services.</br>





 

![Alt text](<Screenshot from 2023-09-08 23-30-45.png>)
