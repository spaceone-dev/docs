---
title: "Telegram Protocol"
linkTitle: "Telegram Telegram Protocol"
weight: 1
date: 2021-08-12
description: >
    Telegram Protocol Service
---

# Create Telegram Bot Alert Channel

## Overview

We can also add **`Telegram`** to our list of `Notification` channels. There are few prerequisites to use Telegram Bot on SpaceONE notification service, and the following will guide you to your **SpaceONE** notification journey.
<br>

## Prerequisites
- Install the Telegram app on your phone or PC.
You will need a **BOT API TOKEN** and **CHAT ID**.

### How to get BOT API Token
Open `Telegram`, and create a new Bot by searching for `@BotFather` and then typing `/start` , `/token`, and `/newbot` by turns. Your interaction with BotFather will be similar as following: 
<br>
![telegram_get_http_tlken.png](/docs/content/en/docs/using_spaceone_console/user_guide/notification/notification_img/telegram_get_http_tlken.png)
<br>
Do not forget that the username must end in bot and must be unique. 
You will get given a HTTP API token which is your BOT API Token to be used in SpaceONE. It will be in the form **`XXXXXXXXX: YYYYYYYYYYYYYYYYYYYYYYYYYYYYY`**.



### How to get Chat ID
You then need the **Chat ID**. To get this, following will help you to get the Chat ID.
1. Create a group and then add the new bot to it.
<br>
![telegram_add_bot.jpeg](/docs/using_spaceone_console/user_guide/notification/notification_img/telegram_add_bot.jpeg) 

2. send a message to the group, so that the group has at least 1 message.

3. Go to your browser, visit the url [https://api.telegram.org/botXXX:YYY/getUpdates](https://api.telegram.org/botXXX:YYY/getUpdates) (replace the XXX:YYY with the **BOT API token** you just got from Telegram)

4. In the JSON Response, you should see a node with a message that has the type=group, This node will also have an ID. Copy this into CHAT ID field in SpaceONE. The CHAT ID will most likely be a negative number in the form of -#########.
#### Precautions
The chat id is likely to be a negative number, so make sure you copy the negative symbol as well when setting the chat id in the script.
```
Eg, If chat id = -123456789, occasionally quickly copying and pasting you may forget the - character and copy just 123456789
```


## Add Telegram Channel to your Project / User in SpaceONE 
Go to `SpaceONE Console` > `Project` which you want to get alerts through `Telegram`. 
<br>
![telegram_spaceone_console.png](/docs/using_spaceone_console/user_guide/notification/notification_img/telegram_spaceone_consol.png) <br>
<br>
Set information above.
![telegram_spaceone_console.png](/docs/using_spaceone_console/user_guide/notification/notification_img/telegram_add_info.png) 

Save and Test, now you are ready for SpaceONE Journey with Telegram notification channel.

`Happy SpaceONE-ing with Telegram notification!`

## Troubleshooting <br>
If the `getUpdates` url doesn't return a node containing a group with an id, then
- Remove your bot from the group,
- and then re add your bot the the group,
- then send a message to the group again,
- then try the getUpdates url again.


Visit [Telegram API Bot](https://core.telegram.org/bots#3-how-do-i-create-a-bot) for an additional understading of Telegram API Bot services. 