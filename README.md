# Kanatran Baquap
A free repository of AI-generated transcripts and translations of vtuber streams.

## Before You Start!
We have made the entirety of Kanatran free, in the spirit of free and open source software. If you are integrating Kanatran's AI translations in your app or extension, please consider following these guidelines:

* When displaying Kanatran's translations or transcripts, you should credit them to `Kanatran Bot by LiveTL`.
* Clicking on `Kanatran Bot by LiveTL` should redirect to [our website](https://kanatran.github.io/) which explains how it works.
* When including Kanatran's translations or transcripts as a feature in any advertisement or promotional material, you should properly credit the AI translation and transcription component to the `Kanatran/LiveTL Developers` (or some variation of the same phrase, preferably with a link to [our website](https://kanatran.github.io/) as well).

Although the guidelines listed above are not strict requirements, **we would most definitely appreciate it if you could credit our work**. Thank you!

## Retrieving Data
You can download transcripts from any domain by dispatching a `GET` request to retrieve a caption file. If a transcript or translation does not exist, the URL will return a `404` response. 

Each of the endpoints listed below are updated at a frequency of at most once every 15 seconds. To conserve bandwidth, you should avoid excessive polling. Furthermore, you should configure your request module to disable caching for these endpoints.

### Most Recent Transcript/Translation
```
https://raw.githubusercontent.com/kanatran/baquap/{VIDEO_ID}/last_tl.json
```
```json
{
    "index": 0,
    "time": "00:00:00,000 --> 00:00:15,000",
    "transcript": "日本語",
    "translation": "English"
}
```

### Full Transcript
```
https://raw.githubusercontent.com/kanatran/baquap/{VIDEO_ID}/transcript.srt
```

### Full Translation Transcript
```
https://raw.githubusercontent.com/kanatran/baquap/{VIDEO_ID}/tl_transcript.srt
```

## Other Info
Kanatran was developed by [Kento Nishi](https://github.com/KentoNishi) and [Ronak Badhe](https://github.com/r2dev2).
