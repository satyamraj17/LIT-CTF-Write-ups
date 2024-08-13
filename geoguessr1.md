Description:

`Where is this? Flag format: Use three decimal points of precision and round. The last digit of the first coordinate
is ODD, and the last digit of the second coordinate is EVEN. Example: LITCTF{80.439,-23.498} (no spaces)`

<img src="https://github.com/user-attachments/assets/a5a136a7-62b8-4ae6-be40-f2019899088b" width="500" height="500">

This is an OSINT problem. With images, we can use images.google.com to find the image location.

Using the site, we know that this is the image of Daxi Bridge, which is in the Taoyuan City, Taiwan

We then used Google Maps to find the coordinates.

The coordinates: (24.8850230994896, 121.28347765279547)

But we have to round it up as stated in the question.

So the final answer is: `LITCTF{24.885,121.284}`
