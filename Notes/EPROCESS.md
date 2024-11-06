EPROCESS is a [[Windows]] [[Data structures]].

![[windows-data-struc.png]]

EPROCESS linked list has pointers to:
- "_ ETHREAD" structures
- [[Security identifier (SID)]] of starting user
- Start time, [[PID]] and other metadata in [[Process Environment Block (PEB)]]
- Process virtual memory pages

#windows