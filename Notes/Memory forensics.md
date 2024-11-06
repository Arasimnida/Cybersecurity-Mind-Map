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





#forensics #memory