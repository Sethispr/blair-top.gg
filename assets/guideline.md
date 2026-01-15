# blair image guideline

just a quick guide on making images better, these steps also apply for all of blair's cards slightly. if your interested there are more options for upscaling etc at [this Discord channel](https://discord.com/channels/1431529966868369473/1431529968419995655/1440714312523055184)

---

### noise reduction with waifu2x

use these settings on [waifu2x.net](https://www.waifu2x.net) for improving the image quality slightly

- **style:** artwork/scans
- **noise reduction:** high
- **upscaling:** none
- **image format:** .png

> [!NOTE]
> using "none" for upscaling so it doesn't increase image size dimensions, also the artwork/scans style mode is more trained i believe since all manga scans uses this

---

### lossless compression with oxipng

once the image is denoised, use **oxipng** to reduce the file size without losing a single pixel of data.

> [!TIP]
> please dont use lossy compression sites they sacrifice quality, also other lossless png software or websites exist but isn't as great as oxipng

#### option a: command line (recommended)

use the native one if possible [oxipng](https://github.com/shssoichiro/oxipng) or [pyoxipng](https://github.com/nfrasser/pyoxipng).

```bash
# simple example command
oxipng -o 6 image.png

```

#### option b: websites

if your in mobile or prefer websites, use [free.tinypng.site](https://free.tinypng.site) with these steps:

1. upload your waifu2x .png file
2. click the **blue edit button**
3. select **oxipng mode**
4. set the **compression level** to the maximum (level 3) not on 2, do not select interlace as well

---

| step            | tool    | objective          | settings              |
| --------------- | ------- | ------------------ | --------------------- |
| **denoising**   | waifu2x | remove artifacts   | noise reduction: high |
| **compression** | oxipng  | minimize file size | level 3 (max)         |
