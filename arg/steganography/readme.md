# steganography
Information can be hidden in such a way that it is only visible to those who
know how to find it.

One of the oldest methods is writing on paper using a substance that is
invisible upon aplication, but that becomes visible when exposed to a certain
chemical, heat, or UV light.

## Whitespace
Many programming languages ignore "whitespace" characters) spaces, tabs,
new lines) but there is one that was created to only use these characters. As a
result, a `whitespace` program can be embedded within any text file.

[whitespace on wikipedia][]

## image data manipulation
A high resolution digital image contains a significant amount of data. Some of
this data space can be used to embed other data within a file, reducing the
fidelity of the image by a small, usually imperceptible, amount. If only the
manipulated image is available and it cannot be compared to the original, it
can be very dificult to even know that there is anything to look for.

### lsb usage
In a 24-bit depth image (8 red, 8 green, 8 blue), the least significant bit of
each channel has very little impact on the overall image quality. The image
data can be modified to set the last bit of each channel to a specific value,
embedding data within the image.  
This can even be done with other images, but at a significantly reduced image
quality.

[lsb code][]

[whitespace on wikipedia]: <https://en.wikipedia.org/wiki/Whitespace_(programming_language)>

[lsb code]: <https://github.com/qtechdev/qlsb>
