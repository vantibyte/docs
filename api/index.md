---
title: API Reference
nav_order: 99
---

If you're looking for details on how to use the API for a particular service, please check that service's page on the menu. The information presented below should be treated as reference only, and not part of any usage instructions.

Responses from the API should be self-explanatory in all cases, let us know if not so we can get them updated!

## General

| HTTP Code | Response              | Details                                                   |
| --------- | --------------------- | --------------------------------------------------------- |
| 500       | Internal Server Error | You're supplying us bad data, or something has gone wrong |
| 404       | Not Found             | You've used an incorrect route                            |

{% include note.html type="note" content="If your details are correct and either of these persist, please get in touch." %}

## Overlay

| HTTP Code | Response                                    | Details                                                  |
| --------- | ------------------------------------------- | -------------------------------------------------------- |
| 200       | _blank_                                     | You haven't set a value for this, or it's actually blank |
| 404       | Key/Item pair does not exist, or is not set | You've never set a value for this                        |
