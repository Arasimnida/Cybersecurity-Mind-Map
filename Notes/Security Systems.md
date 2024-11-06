There is 3 main **security systems**, [[Cryptography]], [[Steganography]] and [[Watermarking]].
![[digital-stegano-scheme.png]]

## The 'magic' triangle

Trade-off between capacity, security and robustness:
![[magic-triangle.png]]

## Steganography vs Watermarking

Both techniques **hide a message** *m* in some cover data *d*, to obtain *d’*, practically indistinguishable from *d*.

|                             Steganography                              |                           Watermarking                           |
| :--------------------------------------------------------------------: | :--------------------------------------------------------------: |
| An eavesdropper must not be able to **detect** the presence of m in d’ |       An eavesdropper cannot **remove** or replace m in d’       |
|                 Primarily for **1-to-1** communication                 |            Primarily for **1-to-many** communication             |
|                 Robustness **not typically an issue**                  |           Robustness of watermark is a **main issue**            |
|               Capacity desired for message is **large**                |                   Known watermark may be there                   |
|                          **Always invisible**                          |                 Can be **visible or invisible**                  |
|                 Typically **dependent on file format**                 | Watermark can be considered to be an **extended data attribute** |


#steganography #cryptography #watermarking #cybersecurity