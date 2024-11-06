## Translation from virtual memory address to physical memory address

**CR3 contains the [[Physical Memory Address]]** of the initial structure used for address translation. The CR3 register is updated during context switches when a new task is scheduled.

![[ia-32-translation.png]]

**Translation step by step:**

1. **Compute the [[Page Directory Entry (PDE)]]:** Combine bits 21:12 from the CR3 register with bits 31:22 from the [[Virtual Memory Address]]
2. **Compute the [[Page Table Entry (PTE)]]:** Locate the PTE by combining bits 31:12 of the PDE with bits 21:12 of the virtual address 
3. **Compute the [[Physical Memory Address]]:** Locate the physical address by combining bits 31:12 of the PTE with bits 11:0 of the virtual address 

![[pagearchi.png]]
Detailed translation: [[Virtual Address Translation Method]]

#architecture #computer-system