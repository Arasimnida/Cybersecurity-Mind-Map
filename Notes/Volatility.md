Volatility is a **[[Memory]] analysis framework**.

**Volatility modules are written in [[Python]]:**
- Functionality can be extended by adding plugins
- Suitable for high degree forensic tasks
- Many OS supported

**Employs several approaches for discovery and reconstitution of memory data structures:**
- Data structure traversal ([[Tree - List traversal Method]])
- Object fingerprint / pattern searches ([[Fingerprint - pattern search Method]])


## Basic commands for identifying malicious processes

**Pslist**: 
1. **Lists running processes**
```bash fold title:"Lists running processes"
pyhton3 vol.py -f <filename> windows.pslist
```
List of outputs: 
- **[[PID]]** 
- **[[PPID]]**
- **ImageFileName:** name of the running process
- **[[Offset]]:** representing the location in memory the process is running.
- **CreateTime:** Time process started
- **ExitTime:** Time process ended

2. Shows the network connections associated with the [[Physical Memory (RAM)]] dump.
```bash fold title:"Shows the network connections associated with the RAM dump"
pyhton3 vol.py -f <filename> windows.netscan
```
List of outputs: 
- **[[Offset]]:** Location in memory
- **Proto:** [[Network protocol]] used by process
- **LocalAddr:** Source address of the network connection
- **LocalPort:** Source port of the network connection
- **ForeignAddr:** Destination address of the network connection
- **ForeignPort:** Destination port of the network connection
- **State:** State of the network connection
- **[[PID]]**
- **Owner:** Account associated with process
- **Created:** Time network connection has initiated

**Pstree:** helps to get an idea of what process spawned another process
```bash fold title:"Lists running processes"
pyhton3 vol.py -f <filename> windows.pstree
```
Ex: to see what process launched ‘cmd.exe’ or ‘powershell.exe’ and see if this looks like legitimate activity in a [[Digital forensics]] investigation.

**Procdump:** Extract the executable and all of the associated [[DLLs]].
```bash fold title:"Lists running processes"
pyhton3 vol.py -f <filename> -o <location out> windows.dumpfiles -pid <PID>
```


#hacking-tools #forensics #memory #python #network