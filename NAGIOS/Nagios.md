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
**OS**- Ubuntu 20.04
**CPU**- 8 Core
**STORAGE**- 1 TB
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
### Command 3:-


