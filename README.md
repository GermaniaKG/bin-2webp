
# Germania KG · towebp

**Just a simplifying wrapper around [Google's cwebp command](https://developers.google.com/speed/webp/docs/cwebp)**


## Requirements
This bash script requires the [cwebp encoding tool](https://developers.google.com/speed/webp/docs/cwebp). For information about webp, see Google's article [“A new image format for the Web”](https://developers.google.com/speed/webp/) and their [webp encoding guide](https://developers.google.com/speed/webp/docs/cwebp)

## Installation

**Homebrew/OSX:** towebp is available via Germania's [homebrew-images](https://github.com/GermaniaKG/homebrew-images) tap.

```bash
$ brew install germaniakg/images/towebp
```

**Linux:** Clone the repo somewhere. Do not forget to add the **towebp** directory to your local **$PATH** variable.

```bash
$ git clone https://github.com/GermaniaKG/towebp.git towebp
```

## Usage

Pass an input file and optionally a quality parameter. If the input already has a *webp* companion, it will be silently ignored. Turn on `--verbous` mode to see what's going on.

```bash
$ towebp <images>
$ towebp *.jpg
$ towebp --quality 60 <images>
```

### Options

Option | Description
:------|:---------------
`-f` `--force`       | Overwrite existing webp files
`-q` `--quality`     | Quality factor, default 85
`-v` `--verbous`     | Turn on verbous mode.



### Examples

```bash
$ towebp photo.jpg
$ towebp -q 60 photo.jpg file2.jpg
```

## What happens inside?

towebp calls `cwebp` with these parameters:

- `-quiet`
- `-alpha_cleanup on`
- `-q 85` or, the quality factor passed, respectively








