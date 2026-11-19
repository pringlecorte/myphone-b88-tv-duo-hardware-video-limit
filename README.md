# myphone-b88-tv-duo-hardware-video-limit
idk why just read this thing man


DO NOT BELIEVE THAT THE MYPHONE B88 TV DUO CAN ONLY HANDLE 320 X 240 RES. IT CAN GO WAYYYY HIGHER. ITS A SLEEPER BUILD I SWEAR I TESTED THIS.

actual spec (16:9 ratio)s:
- max dimensions: 398 x 224
- max framerate (possibly more): 60 fps
- SWEET SPOT for dimensions: 384 x 216 (instead of it being pixelated, its more on the blurry but blending side)
- containder: .mp4
- codec: mpeg-4 part 2
- pixel format: yuv420p
- video bitrate: 1300 kbps (possibly more)
- audio codec: aac
- audio sample rate: 44.1 kHz 
- audio bitrate: 320 kbps
- channels: stereo (recommended mono to avoid the hollow middles)

(not related to video)
- biggest sd card it can support (possibly more): 128gb microsd cx I (yes it read my entire storage)
- fomrat: fat32

pro-tip: u can convert flac files into wav to have a sleeper music player


THESE ARE POSSIBLY JUST THE BEGINNING
I GENUINELY SWEAR THESE WORK

ffmpeg script i use:
```bash
ffmpeg -i input.mp4 \
  -vf "hqdn3d=1.5:1.5:3:3,scale=384:-2:flags=spline+accurate_rnd+full_chroma_int,eq=contrast=1.06:saturation=1.12:brightness=0.02" \
  -c:v mpeg4 -vtag mp4v -pix_fmt yuv420p -r 60 -b:v 1300k \
  -c:a aac -ac 2 -ar 44100 -b:a 320k \
  output.mp4
```
