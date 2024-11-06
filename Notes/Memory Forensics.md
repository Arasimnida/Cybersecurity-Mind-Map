Using **memory** in a [[Digital forensics]] point of view.
## **Dump the physical [[Memory]] ([[Physical Memory (RAM)]]):

There a lot of potentially relevant data:
- **Information on [[Processes]]:** Running and terminated processes
- **Information on [[Network]]:** Open [[TCP]] / [[UDP]] [[Ports]], raw [[Sockets]] or active connections
- **Information on [[File systems]]:** Memory mapped files like executable image, shared libraries, modules/drives, text files.
- **Information in the [[Cache]]:** [[Web addresses]], typed [[Commands]], [[Password]], [[Clipboard]], SAM [[Database]], edited files
- [[Hidden data]], [[Encryption keys]] and many more

We then have to **analyse the [[Memory Image]]** which implies traverse relevant [[Data structures]], [[Signature-based carving]], find text [[Strings]], [[Virus scans]]

**If the system is alive** we have to perform a *specific type of forensics* called [[Live Forensics]].
## Interpreting [[Memory Addresses]]

Once a memory dump has been performed, it is necessary to **interpret the [[Data structures]]** in the raw memory sample. *This operation is [[Operating Systems]]-dependent.*

Several [[Forensics tools]] exist to help us in this task, especially [[Volatility]].

#### Interpretation example
In a forensics investigation we are looking for [[Digital evidence]]. After collecting the memory image we want to deference a [[Pointer]] to access a [[Data structures]] (*user_info*) that contains interesting data.

![[ex-forensics-memory-addresses.png]]
## Memory forensics methods comparison

|                 Methods                 |                                       +                                       |                                           -                                           |
| :-------------------------------------: | :---------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------: |
|    [[Tree - List traversal Method]]     |       Can stitch together more related records from kernel perspective        |                          Can miss unlinked, dead structures                           |
| [[Fingerprint - pattern search Method]] | Find unlinked, dead structures (warm reboot)<br>Can work with imperfect dumps | Less context without following<br>related structures / objects Susceptible to rubbish |

## Example of a Fileless Malware investigation

We’re analysing a Windows workstation, suspected to be infected by malware. We are going to **look for evidence of [[Malware]] residing in memory**.
#### Memory dump

The first step is to perform a **memory dump** of [[Physical Memory (RAM)]] inside the workstation (*need of admin privileges*) using [[FTK Imager]]. Then we analyse the memory dump using [[Volatility]].

Fileless malware are a particular type of malware who conducts their operations within the RAM. Traditional methods of [[Digital forensics]] searching in [[Persistent Storage]] would find it difficult with assessing this type of malware; making tools like Volatility all the more important.

#### Identifying malicious processes

Usually, look at **what processes were running** when the RAM dump was captured. *Looking at the running [[Processes]] of a device is always a great way to try and identify any [[Malware]]* that may be running on the device.

Using the tool Volatility we can list all running processes using *pslist* and *pstree* to makes it easier to spot suspicious process activity. For example, it can be used to see what process launched ‘cmd.exe’ or ‘powershell.exe’ and see if this looks like legitimate activity. It can also help detect malicious processes [[Masquerading]] as legitimate Windows processes.

#### Identifying malicious network connections

When a RAM dump is captured *any network connections at the time the capture was*
*taken will also be stored within the captured memory*. Using the tool Volatility and more especially **pslist**. It can shows the network connections associated with the RAM dump. Indeed, **any malicious network connections can be identified** such as the **source and destination [[Ports]], destination IP and the process** that the network activity relates to.

If we found something suspicious, we can review each IP using [[Symantec]] site review: 
- https://sitereview.symantec.com/
This **can confirms that this activity is related to a known malware [[Command and Control (C2) Server]]**. if the URL is flagged as a security risk, we found [[Indicators of compromise (IOCs)]]. Using Volatility we can extract the malicious process for further analysis using a feature called *procdump*. We can then try and extract additional information from the dumped process using *[[Strings CLI tool]]* for example to search for any additional [[Indicators of compromise (IOCs)]] such as [[IP addresses]], filenames, persistence locations...

## Acquisition of volatile memory

There is several trade offs when choosing the acquisition technique:
- **Time of installation:** prior to incident or post incident ?
- **Access to system:** local or remote ?
- **Access to main memory:** pure hardware vs software ?
- **Required privileges:** user vs administrator ?
- **Impact on system:** live vs post mortem ?

*Two main factors* can be used to help make a decision:
- ***Atomicity:*** how close to the present memory statue can the forensic memory snapshot be retrieved
- ***Availability:*** Whether the tools necessary to perform memory acquisition are available or not

An **ideal acquisition method** is characterised by both **a high atomicity and availability**. ***The decision matrix*** helps investigators in choosing a specific memory acquisition technique:
![[decision-matrix.png]]

#forensics #memory