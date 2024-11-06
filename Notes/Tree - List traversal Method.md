The goal of the **tree - list traversal method** is to find index into lists/trees of interest & follow them through [[Pointer]] dereferencing to reconstruct the full [[Data structures]].

## [[Linux]]

Use the [[Volatility]] tool. Volatility’s "linux_pslist" plugin enumerates [[Processes]] by walking the active process list pointed to by the global *init_task* variable.

```bash fold title:"Use linux_pslist showing information about each process"
python3 vol.py --profile=LinuxDebian-3_2x64 -f debian.lime linux_pslist
```
## [[Windows]]

Windows has a similar [[Data structures]] using [[EPROCESS]].

#methodology #forensics #memory #data-storage




