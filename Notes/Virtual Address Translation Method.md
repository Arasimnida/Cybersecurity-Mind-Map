1. We find a reference to a [[Virtual Memory Address]] (VA) within the [[Virtual Address Space]] of a process
2. **Found the [[PID]]** associated to this process. 
3. **Found the CR3** for this PID.
4. **Convert the [[Virtual Memory Address]] to binary** and decompose it into the relevant offsets (table, left).
5. **Calculate the PA of the [[Page Directory Entry (PDE)]]** by multiplying the **page directory index** by the **size of the entry** and then adding the **page directory base**. Here the entry size correspond to the size of the PA we just found because it will be the scale of this structure.
6. **Read the value** from [[Physical Memory (RAM)]] stored at the [[Page Directory Entry (PDE)]] address. *Check for the [[Endianness]]*. 
7. From bits 31:12 of the [[Page Directory Entry (PDE)]] **learn the PA for the base of the [[Page Tables]]**
8. Add the [[Offset]] to **calculate [[Page Table Entry (PTE)]]'s physical address**
9. Read the value of this address and select bits 31:12 to **find the physical address for the page**
10. **Compute the offset using the bits 11:0 from the virtual address** resulting in the physical address.

#methodology #memory