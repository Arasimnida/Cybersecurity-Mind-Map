## Substitution methods

**By exploiting the [[Structured data type]]**, we can hide **the secret into unused portions** of the carrier file. This can be used with [[JPEG or JPG]] file for example.
- C:\> Copy [image 1] /b + [secret file] /b [output image]
We can also **abuse the recognition of [[End-of-File (EOF)]]**. When our editor open an image on a photo editor, it ignores anything coming after the EOF tag. But when we open it in Notepad, we can see our message.
The [[EXIF]] image format is standard **used by digital camera manufacturers to store information** in the image file, such as, the make and model of a camera, the time of picture, etc.
Using the comment section of different format can be use, for example with [[GIF]] and [[ZIP]].

**By exploiting the space domain**, we can modify the secret and the cover by encoding at the level of the image [[Pixels]]. It can work with a grey scale or other media including audio and video.
A common digital steganography technique: [[Least Significant Bit (LSB)]]
## Transform method techniques

Embed secret info in a transform space of a signal (ex: frequency domain)
## Distortion techniques

Store information by signal distortion and measure the deviation from the original cover in the decoding step
## Cover generation methods

Encode information by creating a cover object (e.g., fractal generation)


#steganography #data-storage #information-hiding 