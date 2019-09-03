# NOTE: Pushover.net pushing is not yet available (despite described below)

# K8 Gnomish Queuing Device
![alt text](https://github.com/kitsun8/K8-Gnomish-Queuing-Device/blob/master/Screenshot/K8GDC.png)

# How to use?
1. Get your Pushbullet API key from https://www.pushbullet.com/#settings (create access token).

OR

1. Buy Pushover for your mobile device (4.99USD one time fee) and set up an application at https://pushover.net/apps/build

2. Place the access token to appsettings.json file inside "Compiled" Release folder (fill either Pushover or PushBullet, or both), then Select APImode (1 for PushBullet, 2 for Pushover).
3. Open the .exe from "Compiled" Release folder. 
4. Place the open application so that you can see the Queue status on the "window" of the application.
5. After this, press Start GQD. 

# What it does
WinForms application that takes a screenshot of a screenarea, passes the image to Tesseract OCR (Optical character recognition), and sends a Pushbullet message to the user of notable events, such as:
- Queue status less than 1000 (this message is sent once every 5 minutes when under 1000 players in queue)
- Queue status not found
- Different error messages
- You have been disconnected -message

In addition, it tracks the total time you have spent in queue (while activated from "Start GQD"), and keeps track of the original queue place you started in.

# PLEASE NOTE!
Your World of Warcraft must be running in either Maximized Windowed or Windowed mode, since this application has to be on top of the game.

Also, I take no responsibility of you using this tool. It is not an forbidden tool type as far as I know, since it does not interfere or modify anything, it merely observes text on a screenshot and sends a message if it matches a rule.

PushBullet API has a 500 API messages / month limit.

Pushover.net has a 7500 API messages / month limit / application, you can create more applications.


# Powered by
- Tesseract OCR 3.0.2 (https://www.nuget.org/packages/Tesseract/3.0.2)
- PushBulletSharp (https://www.nuget.org/packages/PushBulletSharp/)
- Pushover.NET (https://www.nuget.org/packages/PushoverNET/)
- WinForms, .NET Framework 4.7
