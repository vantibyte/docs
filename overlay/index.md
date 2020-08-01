---
title: Overlay
nav_order: 3
---

The overlay is primarily used for stream overlays by providing "remote" production teams the ability to make changes to specific elements being shown on broadcast.
This is achieved by providing teams an Interface (via Dash) to update the values to be shown on stream, and an API that is used by the broadcaster to show these on screen.

For each of the values set in the dash, they can be accessed via the API. In streaming software such as OBS, these should be used as a **Browser Source**, using the following URL format

```text
http://overlay.vbapi.tech/{url_key}/{API_Name}
```

Each of the API endpoints will return the type of data and values as listed in the tables below.

{% include note.html type="warn" content="Currently, *Video* types should be used in **Media Source** rather than Browser Source." %}

## Dash and API endpoints

| Dash Name           | API Name          | Dash Type | API Type | Description                                                  |
| ------------------- | ----------------- | --------- | -------- | ------------------------------------------------------------ |
| Team One Name       | teamonename       | Text      | Text     | The name of Team One                                         |
| Team Two Name       | teamtwoname       | Text      | Text     | The name of Team Two                                         |
| Team One Logo       | teamonelogo       | Select    | Image    | The logo of Team One                                         |
| Team Two Logo       | teamtwologo       | Select    | Image    | The logo of Team Two                                         |
| Team One Score      | teamonescore      | Option    | Text     | The score of Team One                                        |
| Team Two Score      | teamtwoscore      | Option    | Text     | The score of Team Two                                        |
| Caster One Name     | casteronename     | Text      | Text     | Name of Caster One                                           |
| Caster One Social   | casteronesocial   | Text      | Text     | Social of Caster One                                         |
| Caster Two Name     | castertwoname     | Text      | Text     | Name of Caster Two                                           |
| Caster Two Social   | castertwosocial   | Text      | Text     | Social of Caster Two                                         |
| Caster Three Name   | casterthreename   | Text      | Text     | Name of Caster Three                                         |
| Caster Three Social | casterthreesocial | Text      | Text     | Social of Caster Three                                       |
| Caster Four Name    | casterfourname    | Text      | Text     | Name of Caster Four                                          |
| Caster Four Social  | casterfoursocial  | Text      | Text     | Social of Caster Four                                        |
| Map Progress        | mapprogress       | Text      | Text     | Usually "Map x of x"                                         |
| Current Game Logo   | gamelogo          | Select    | Image    | Logo of the current game\*                                   |
| Text Input          | textinput         | Text      | Text     | A completely free text input, for whatever your team decides |
| Square Animation    | animationsquare   | Select    | Video    | An animation, usually square                                 |
| Long Animation      | animationlong     | Select    | Video    | An animation, usually longer                                 |
| Team One - player one Name   | playeroneteamonename   | Text | Text | The name of player one, team one   |
| Team One - player two Name   | playertwoteamonename   | Text | Text | The name of player two, team one   |
| Team One - player three Name | playerthreeteamonename | Text | Text | The name of player three, team one |
| Team One - player four Name  | playerfourteamonename  | Text | Text | The name of player four, team one  |
| Team One - player five Name  | playerfiveteamonename  | Text | Text | The name of player five, team one  |
| Team One - player six Name   | playersixteamonename   | Text | Text | The name of player six, team one   |
| Team Two - player one Name   | playeroneteamtwoname   | Text | Text | The name of player one, team two   |
| Team Two - player two Name   | playertwoteamtwoname   | Text | Text | The name of player two, team two   |
| Team Two - player three Name | playerthreeteamtwoname | Text | Text | The name of player three, team two |
| Team Two - player four Name  | playerfourteamtwoname  | Text | Text | The name of player four, team two  |
| Team Two - player five Name  | playerfiveteamtwoname  | Text | Text | The name of player five, team two  |
| Team Two - player six Name   | playersixteamtwoname   | Text | Text | The name of player six, team two   |

{% include note.html type="note" content="Game Logos are provided for your convinience. If you need a logo that is not currently available, let us know!" %}

## The various Types

| Where | Type   | Description                                      |
| ----- | ------ | ------------------------------------------------ |
| Both  | Text   | It's just a bunch of text                        |
| API   | Image  | An image formatted to show at it's standard size |
| API   | Video  | _We're still working on improving this one_      |
| Dash  | Select | Choose from a hosted asset                       |
| Dash  | Option | Choose a provided option                         |

For `text` types, styling can be applied in the browser source to either `html` or `body` elements.  
For `image` types, styling should be applied to the `img` element. By default, the image is simply returned at it's original size.

## Uploading assets

Assets to be used in the Select options can be uploaded via Dash.

{% include note.html type="note" content="Managing assets is currently not supported" %}
