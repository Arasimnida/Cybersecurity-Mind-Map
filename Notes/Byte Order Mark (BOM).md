The **Byte Order Mark (BOM)** is a Unicode char that appears as a *magic number* at the start of a text stream telling it's encoding.

There is different value for [[UTF-8]], UTF-16, UTF-32. [[Microsoft]] software like Notepad add a BOM when saving data as UTF-8 and cannot interpret text without a BOM unless it is pure [[ASCII]].

![[BOM-example.png]]