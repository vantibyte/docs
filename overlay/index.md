---
title: Overlay
nav_order: 3
---

## Overlay

The overlay is primarily used for stream overlays by providing "remote" production teams the ability to make changes to specific elements being shown on broadcast.
This is achieved by providing teams a Web UI (via Dash) to update the values to be shown on stream, and an API that is used by the broadcaster to show these on screen.

For each of the values set in the dash, they can be accessed via the API. In streaming software such as OBS, these should be used as a **Browser Source**, using the following URL format

```text
http://overlay.vbapi.tech/{url_key}/{API_Name}
```

Each of the API endpoints will return the type of data and values as listed in the tables below.

## Dash and API endpoints

|Dash Name|API Name|Type|Description|
|---|---|---|---|
|Team One Name|teamonename|Text|The name of Team One|
|Team Two Name|teamtwoname|Text|The name of Team Two|

## The various Types

|Type|Description|
|---|---|
|Text|It's just a bunch of text|
|Image|An image formatted to show at it's standard size|
|Video|*We're still working on improving this one*|

For `text` types, styling can be applied in the browser source to either `html` or `body` elements.  
For `image` types, styling should be applied to the `img` element. By default, the image is simply returned at it's original size.
