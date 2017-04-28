
# 2webp

**Just a simplifying wrapper around [Google's cwebp command](https://developers.google.com/speed/webp/docs/cwebp)**


## Requirements
This script requires the [cwebp encoding tool](https://developers.google.com/speed/webp/docs/cwebp). For information about webp, see Google's article [“A new image format for the Web”](https://developers.google.com/speed/webp/) and their [webp encoding guide](https://developers.google.com/speed/webp/docs/cwebp)



## Usage

Pass an input file and optionally a quality parameter:

```bash
$ 2webp <image>
$ 2webp <image> [quality]
```

### Example

```bash
$ 2webp photo.jpg
$ 2webp photo.jpg 75
```

## What happens inside?

2webp calls `cwebp` with these parameters:

- `-quiet`
- `-alpha_cleanup on`
- `-q 85` or, the quality factor passed, respectively


## Installation

Clone the repo somewhere. Do not forget to add the **bin-2webp** directory to your local **$PATH** variable.

```bash
$ git clone https://github.com/GermaniaKG/bin-2webp.git bin-2webp
```





