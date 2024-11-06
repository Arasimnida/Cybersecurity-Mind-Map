**Unicode character set** and **encoding schemes** allow encoding
many more foreign language symbols and graphic characters. Unicode 4.0 supports over 96,000 characters, which requires 4-bytes per
character instead of the 1 byte that [[ASCII]] requires. **[[UTF-8]] is the most commonly used** and it's was designed to be ***fully backwards compatible*** with [[ASCII]].

## 3 ways of storing a Unicode character

1. UTF-32: uses a 4-bytes value for each character
2. UTF-16: most used character in 2-byte value, lesser-used 4-bytes
3. UTF-8: uses 1, 2, or 4 bytes (most frequently used in byte)

![[UTF-screen.png]]

### [[Endianness]] in Unicode encoding

Since UTF-16/32 use 2/4 bytes [[Integers]] endianness also applies to them.

#encoding #data-representation