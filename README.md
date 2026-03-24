# Will It 'Buzz?

This tool will compare the browser's native complex-shaping against HarfBuzz and identify differences.

Load up:
- A word list
- A font to test
- Click "Process"

And the tool will compare each word, producing a list of differences.

# Live Page

https://mattmatic.github.io/will-it-buzz/

# How it works

- The font is dynamically loaded into the css space
- HarfBuzzJS is used to shape and obtain the paths for each glyph

For each word:
- The word is filled to canvas in red.
- The word is stroked to canvas in black with a 1.5 wide line (this avoids aliasing issues in the overlap)
- The HarfBuzz shaping is pathed to the canvas in blue.
- The canvas bitmap is read, and a threshold of red pixels are detected as a failure

# Downloads
The failed list of words can be downloaded as a UTF8 text file.

Additionally, the rendering of Browser (red) vs HarfBuzz (blue) can be saved as a ZIP file.
The image renderings are in the `png\` folder, with the image index matching the line number
of the `data\fail.txt` file.

The PNG folder is limited to the first 4000 images.
