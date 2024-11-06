**Masquerading** is a technique used by [[Malware]] to hide them self. For example masquerading occurs, by naming the running malware process after legitimate Windows [[Processes]].

## Example of masquerading for Windows

For instance, **‘taskhostw’ always runs from ‘%systemroot%\system32\taskhostw.exe’** and its parent process is always ‘svchost.exe’, if you spot ‘taskhostw’ running from other location or different parent, it looks fishy.

#malware 