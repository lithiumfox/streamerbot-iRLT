# streamerbot-iRLT
iRacing Live Timing actions for Streamer.Bot!

![image](https://github.com/lithiumfox/streamerbot-iRLT/assets/4545555/8d1ebae5-ab91-4135-938d-7dbc18d5d914)



## What this is:
An obnoxious list of actions that can be used to remotely control iRacing Live Timing via multiple systems, such as StreamDeck buttons using the Streamer.Bot plugin, or via Twitch Redeems, and to make it easier to build actions without having to code anything.
All you need is a state, an object, and the execute action:

![image](https://github.com/lithiumfox/streamerbot-iRLT/assets/4545555/65cb34ef-e073-4266-8a72-11695c8f5ccc)


Quick Note: This is not the most optimized method in my opinion, and there may be some actions I have missed. Please let me know in the issues section. 
I also would like to make this a proper plugin in the future! If you have any information or would like to help, please let me know!

Also remember, you can only use one remote connection to your iRacingLiveTiming at a time! Sockets only allow one connection, meaning you can't use any other remote web app while using this!

## Prerequisites:
Streamer.Bot (https://streamerbot.github.io/client/)

iRacingLiveTiming (https://www.sdk-gaming.co.uk/)

## Download: 
https://github.com/lithiumfox/streamerbot-iRLT/releases/tag/release

# Setup:

## iRacingLiveTiming Preconfiguration (REQUIRED):

There are a couple of steps within iRacingLiveTiming that need to be done prior to setting up the actions. You will need 3 pieces of information.

- Server
- User
- Room Name

I would recommend writing them down in a notepad file as we get them.

### 1. Get your Server and Room Info
**Servers**
Europe: livetiming.sdk-gaming.co.uk/ws
US: livetiming2.sdk-gaming.co.uk/ws
![image](https://github.com/lithiumfox/streamerbot-iRLT/assets/4545555/cbfbe0c1-05cc-4f4c-88c4-83d603ca246b)

This will be your **server**.

**Room Name**

![image](https://github.com/lithiumfox/streamerbot-iRLT/assets/4545555/3fccef5e-bdd2-4dd3-b884-6014ee6efa96)

You will need to know what server you are located on so you can make the correct websocket connection.

This will be your **Room Name**.

### 2. Set up Variable access credentials

Under ***Variable Access Credentials**, set up the credentials here. The "User Name" should be something unique for yourself. The variable filter must be "Overlay".

![image](https://github.com/lithiumfox/streamerbot-iRLT/assets/4545555/95cf9ce6-bb31-4c9a-af69-9aff73b5f0da)

The User Name will be your **User**

## Streamer.Bot Setup and Installation:

### 1. Create a Websocket Client to connect to iRacingLiveTiming

Under **Servers/Clients** -> **Websocket Clients**, right click and Add. Use the **Server** that was selected earlier.
![image](https://github.com/lithiumfox/streamerbot-iRLT/assets/4545555/000d4077-d4ab-401c-acb3-a0615224ee70)

Note: You can set this to automatically connect if you want though I'd wait until after you are done!

### 2. Import Actions

Click the Import button at the top, copy the long string from streamerbot-iRLT.txt into the "Import String" box. 

After it's pasted, the window should look like this:
![image](https://github.com/lithiumfox/streamerbot-iRLT/assets/4545555/75c766d2-0ac4-427c-b12d-c87afb1b6d50)

### 3. Update (Settings) Room

There are 2 settings you will need to change. **User** and **room**

Select (Settings) Room and double click "set global "user" to "YourUserNameHere".

Update "YourUserNameHere" to **User** you created Earlier

![image](https://github.com/lithiumfox/streamerbot-iRLT/assets/4545555/9e7acddf-9f2d-4a96-8364-ee1246f1a765)

Repeat these steps for "room" with your **Room Name** value.

### 4. Add Trigger for (Settings) Room [if it's not there]

This is something I couldn't test, but you may need to add a trigger to this. This basically sets the values of the global variables once after your websocket connects. 

![image](https://github.com/lithiumfox/streamerbot-iRLT/assets/4545555/743f9da0-937a-487c-9a95-1cbbf6366802)

![image](https://github.com/lithiumfox/streamerbot-iRLT/assets/4545555/80ab8092-5ace-4830-8ce7-d45899029b37)


That's it! I may have examples of how to create actions in the future, but for now, you're setup to play around with this!
