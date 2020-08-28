---
title: RTMP
nav_order: 4
description: Vantibyte Documentation for the RTMP solution
---

Our RTMP service allows you to easily transfer video feeds across the globe for central production.

## Pre-requisites

To stream to our service, you need to have each of the following:

| Thing              | Description                                            |
| ------------------ | ------------------------------------------------------ |
| Streaming Software | You need something to stream from, probably OBS Studio |
| Ingest Server      | The server you stream to, we provide this for you      |
| Stream Application | The path you stream to, we provide this too            |
| Stream Name        | The name of the stream, which must be unique           |
| Stream Key         | A secret key allowing you to stream to this            |

{% include note.html type="note" content="In our current phase, all of the details above will be provided to you. Management of Stream Name/Keys will be part of Dash" %}

Invidually these don't mean much, but altogether these form the **Server** and **Stream Key** that you need for your broadcasting tool (like OBS), which will look like the following:

```text
Server: rtmp://{ingest}.rtmp.vantibyte.com/{application}/
Stream Key: {streamname}:{streamkey}
```

{% include note.html type="info" content="Don't worry about remembering this, we'll provide these to your exact requirements in the Dash" %}

## Stream Settings and Bitrate

We accept ingest in the same format as the popular livestream providers (Twitch, YouTube, etc) using H264 encoding. Similarly to them, streaming to us with particular resolution and bit rate settings is preferred.

We do not provide specifics on full stream configuration (such as b-frames, encoding profiles, or similar) for some reasons:

- The defaults in most streaming software are suitable
- The settings you've been using with other providers are suitable
- The options do not have a major effect on our service (but are very important when streaming for viewers!)
- Keeping these up-to-date with industry changes would be annoying

However we do recommend the key settings per the below:

| Resolution  | FPS | Bitrate (kbps) |
| ----------- | --- | -------------- |
| 1920 x 1080 | 60  | 6000           |
| 1920 x 1080 | 30  | 4500           |
| 1280 x 720  | 60  | 4500           |
| 1280 x 720  | 30  | 3000           |
