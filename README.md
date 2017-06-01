# Podcast Encoder

Podcast Encoder is a simple application to make it easier to transcode audio or video files into MP3s and specifically for podcasts.

To use this app, drag an audio or video file onto the icon. You will get a notification as the app starts encoding the file and when it finishes. The output file will be saved in the same directory as the input file.

To change the encoding settings, double click on the app icon. The encoding options are:

- Bitrate (32kbps, 64kbps, or 128kbps): Higher bitrates offer better quality sound but increase the file size. Small file sizes are especially important for people listening through their phones.
- Stereo vs. Mono: For voices and speech, mono is recommended because of the smaller file sizes. For music, stereo sound will give a more full, realistic sound.
- Normalized vs. Unnormalized Volume: Different recordings can be at different volume levels. Even in a single recording, someone may move closer or farther from the mic causing volume changes. Normalizing the volume sets the volume at a consistant level for every recording and even during the course of a single recording.

## Under the Hood
Podcast Encoder is an Applescript app that uses ffmpeg to encode the MP3s. ffmpeg can read nearly any audio or video file and turn it into an MP3. This app uses the "dynaudnorm" feature of ffmpeg to normalize the audio. This normalization varies slowly over the course of the recording so you should not have problems with rising hiss levels during quiet moments.