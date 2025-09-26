If the server wants to send a file to a client that the client does not support in it's original format, the server must first repackage it into a format the client does support. This process is called **transcoding.**

General Steps Taken:
1. Decode the original file
2. Apply filters/ change data
3. Encode into a new format

This is computationally expensive, and while is usually done by the CPU, **Hardware-accelerated transcoding** offloads transcoding to a GPU or iGPU. Without a lot of transcoding power, as expected, you get buffering, lag, and/or failure to play at all.

### The natural question is, why transcode at all? Why not just store all my data in a format readable by my client(s)?

While for video [[Containers and Codecs|codecs]], there are few standard options, getting the right combination of audio, video, and metadata codecs is difficult to do with significant success.

**Even if a TV supports a codec, it does not guarantee it can keep up with the bitrate.**