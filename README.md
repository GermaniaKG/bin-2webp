
# 2webp

**Just a simplifying wrapper around [Google's cwebp command](https://developers.google.com/speed/webp/docs/cwebp)**

## Usage

Pass an input file and optionally a quality parameter:

```bash
$ 2webp <image>
$ 2webp <image> [quality]
```

##### Example

```bash
$ 2webp photo.jpg
$ 2webp photo.jpg 75
```

## What happens inside

2webp calls `cwebp` with these parameters:

- `-quiet`
- `-alpha_cleanup on`
- `-q 85`


## About webp
See Google's article [“A new image format for the Web”](https://developers.google.com/speed/webp/) and their [webp encoding guide](https://developers.google.com/speed/webp/docs/cwebp)

