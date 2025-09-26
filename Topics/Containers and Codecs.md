Movies and TV files are stored in **containers** (.mkv, .mp4, etc) that hold video streams, audio streams, subtitles, and metadata. Each of these files is of a certain **codec** (H.264, HEVC, AAC, etc).
# Codecs
Codecs are used to transcode data of individual streams. 
**Video Codecs:** H.264 (AVC), H.265 (HEVC), VP9, AV1
**Audio Codecs:** AAC, AC3, DTS, FLAC, MP3, TrueHD

Some subtitle codecs are **image-based**, meaning they are burned into the image real time, forcing a full transcode of the video on the server-side
# Containers
Containers are simply wrappers for holding together codecs. Options are:
- MP4
- MKV
- AVI
- MOV
**Changing the container does not change the codec;** containers and codecs are not mutually exclusive.

### Why are there different codecs and containers? Are there advantages/ disadvantages to each?