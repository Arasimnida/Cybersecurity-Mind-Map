The *base64* tool on [[Linux]] can be use to encode or decode file.

#### User Manual:

- base64 -option [file]
	- -d to decode
	- -i when decoding, ignore non-alphabet characters
	- -w *n* to wrap encoded lines after *n* character

#### Example

```bash fold title:"Encode text to base 64"
echo -n 'scottlinux.com rocks' | base64
```

```bash fold title:"Decode base 64"
echo -n 'c2NvdHRsaW51eC5jb20gcm9ja3M=' | base64 -d
```

#linux  #hacking-tools #encoding