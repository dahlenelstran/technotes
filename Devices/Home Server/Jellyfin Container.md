Jellyfin accesses my folders of movies and makes them accessible easily to other devices on the home network. 

There are three ways the videos can be accessed by the client:
- **Direct Play (Best)** The file is already in a form the client can handle, so it can be handled as sent
- **Direct Stream (Middle)** All the file codecs are handled, but the container is not, so the server is responsible for repackaging the file codecs into a different container. Light on the CPU, referred to as a [[Remux]].
- **[[Transcoding]] (Worst)** The file must be decoded and encoded in real time, very computationally demanding

Something to note is **codecs and resolution are not one-to-one**. A 4K TV can still direct play a 1080p video, if the codec is supported. The TV is responsible for down- and upscaling content.

**Examples:**
- 4K MKV -> 4K TV **direct play**
- 1080p MP4 -> 4K TV **direct play**
- 4K MKV -> 4K TV without MKV **direct stream**
- 4K HEVC -> 4K TV without HEVC **transcoding**
- 1080p with DTS Audio -> 1080p TV without DTS **transcoding**
- 4K file with PGS subtitles -> 4K TV without support **transcoding**

Because direct stream is computationally cheap, it shouldn't factor into the parts list of the home sever. Thus the more I expect to [[Transcoding|transcode]], the beefier my [[Home Server|home server]] should be. Based on the supported container and codec formats of the [[Insignia F50 70inch]], I (hypothetically) expect to be able to direct play most content. 

### Internet speeds causing transcoding

If the speeds of the home network cannot allow for direct play of a 60fps 4K HDR movie, the server is responsible for transcoding.

However, if the [[Home Server|home server]] has a direct gigabit ethernet connection to the main [[TV LibreELEC Machine|client]], I don't have to worry about internet speeds at all when watching on the [[Insignia F50 70inch]]. I can still connect the 