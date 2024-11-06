The Least Significant Bit (LSB) of a pixel is used to encode hidden information. The idea is to use 2 mains ideas:
1. **Digital image or sound files can be altered to a certain extent** without loosing their functionality.
2. **Humans are unable to distinguish minor changes** in image colour or sound quality.

![[lsb-example.png]]
## Analysis of LSB encoding

From a forensics point of view:
- **The good:** Simple to implement and good capacity
- **The bad**: Can be easy to extract message if attacker knows the message is there (vulnerable to [[Statistical Analysis]]) Here we are looking for noise to find proof of a LSB usage.
- **The ugly**: Integrity is extremely frail, it is easy for attacker to corrupt the message, vulnerable to unintentional corruption (image cropping, conversion to jpeg and back, etc).

## Variations in the LSB

You can see variation regarding the LSB algorithm depending of how many [[Bits]] are going to be impacted and which [[Pixels]] and in what order. The variation and possibility in the LSB can make it very hard to detect. This can have a lot of potential for any [[Cyber crime]]. We have to be aware that **more bits means higher capacity, but higher noise**. Emerges a side effect named [[Banding]].
#### Adding protection against passive attacks

- **Intuition**: *Obfuscate the location of the stego pixels* containing the embedded message based on the knowledge of a shared key between sender/receiver.
- **Shifting**: Indicated an offset != 0 of the first stego pixel to embed bit secrets (ex: p = k % 27)
- **Random walk**: use a function to spread the secret message over the cover
	- Can be implemented by a pseudo-random number generator seeded by a value r derived from k, e.g., r = SHA2(k)


#steganography #information-hiding #images #watermarking