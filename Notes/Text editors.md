There is different type of text editors:

- [[Hexadecimal editor]]
- Editor based on [[Data encoding schemes]]

## How an editor determines the encoding of a text file ?

- **Uses a default encoding scheme**: May lead to poorly rendered document The user usually has to manually change it.
- **Uses heuristics:** Based on statistical analysis of byte values and patterns. If the bit 7 of all bytes is unset, we can assumed it might be [[ASCII]] ?. Project: [[hex heuristics]]
- Uses embedded information: [[Byte Order Mark (BOM)]]