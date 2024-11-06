**Watermarking** is about establishing identity/ownership of digital content to prevent unauthorised use:
- Watermarks can be *perceptible* or *imperceptible*.
- They are *inseparable* from the works they are embedded in.
- They *remain embedded in the work* even during transformation.
##### Watermarking Examples:
- Machine ID codes in laser printers: Some printers print yellow tracking dots on their output

## Watermarking applications in digital World:

**Copyright protection:**
- Embed info about owner to prevent others from claiming copyright
- Require very high level of robustness

**Copy protection:**
- Embed watermark to disallow unauthorised copying of the cover
- For example, a compliant DVD player will not playback or data that carry a "copy never" watermark

**Content authentication:**
- Embed a watermark to detect modifications to the cover
- The watermark in this case has low robustness, "fragile"

The [[Least Significant Bit (LSB)]] is a watermark technique.

## Watermark attacking methods

1. **Removal Attacks:** Aim for complete removal of the watermark, ideally restore the original object (ex: lossy compression)
2. **Geometrical Attacks:** Don’t remove, but distort the watermark detector sync with the embedded info (ex: rotation)
3. **Cryptographic Attacks:** Aim at cracking the security methods of watermarking schemes (ex: brute force key search) using [[Cracking techniques]]
4. **Protocol Attacks:** Aim at attacking the algorithms of the watermarking application (ex: watermark inversion, copy attack)

#information-hiding #watermarking 