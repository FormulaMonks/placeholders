# Placeholders
A collection of tools to generate placeholder media

## Dependencies
ImageMagick, ffmpeg and jq
### macOs
```
brew install imagemagick
brew install ffmpeg
brew install jq
```
## Usage
Ensure the script files are executable
### Generate a sigle placeholder
`./gen <COLOR> <WIDTH>x<HEIGHT> <DURATION_IN_SECONDS>`
#### Example
`./gen red 1920x1080 5`

Named color options are the ones supported by ImageMagick. Hexcodes and `rgb(r, g, b)` can also be used. Please refer to their documentation for more detailed information.

### Generate all named color options
`./gen_all <WIDTH>x<HEIGHT> <DURATION_IN_SECONDS>`
#### Example
`./gen_all 1920x1080 5`

- All generated videos will go under a `videos` folder and all generated images will go under an `images` folder both in the root of the project.
- Videos and images files will have names in the format `color_WIDTHxHEIGHT.mp4` and `color_WIDTHxHEIGHT.png` respectively.
- Videos and images are cached so in order to generate a video again delete videos with the same name

