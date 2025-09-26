A **remux** is the act of changing the container of a set of streams, but not the individual codecs themselves. This is computationally cheaper than [[Transcoding|transcoding]], or changing the codecs, and is therefore preferred whenever possible. 

**A remux is lossless because it doesn't re-encode!**
### How to Remux
Recommended tools: FFmpeg