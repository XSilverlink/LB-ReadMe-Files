# StreamUP Twitch Prediction System by [Silverlink](https://twitch.tv/silverlink)
**An extension and deck for [Lioranboard](https://obsproject.com/forum/resources/lioranboard-stream-deck-animator.862/) that utilizes the new Twitch Prediction System API!**

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/StreamUPTwitchPredictionSystem.png"></p>

*You need to know how to install extensions in Lioranboard, you can follow [this](https://christinna9031.github.io/LBDocumentation/setup.html#extensions) guide created by the amazing [Christinna](https://github.com/christinna9031)!*

ℹ This extension comes with an with an **REQUIRED** deck. If you remove this deck automatic updating will **NOT** work.  Almost every button has an unique ID which should also **NOT** changed. It comes with 2 Example predictions which you can change however you want, you can even create more buttons on other decks.

**💭 If you have any questions, problems or feedback feel free to join us on the StreamUP discord:**
https://discord.gg/RnDKRaVCEu

# Features  

### Through Lioranboard, Transmitter and (Mobile) Chat:
- Create a prediction 
- Lock a prediction¹
- Cancel a prediction¹
- Pick a winning side¹
- Start, Stop, Cancel, Lock and pick a side through commands

¹ Currently its only possible to do these things if its launched through the extension.

# First things first!
Lioranboard does not have the capability yet to generate a token with predictions yet. Until this is resolved you need to generate a new code manually. Here are the steps about what to do:

 1. Click on 'Link your Twitch'
 2. Tick everything on you want to enable
 3. Click on 'Copy URL'
 4. paste the URL in notepad or some equivalent
 5. Add this to the end of the URL:  +channel:manage:predictions
 6. Copy the whole URL
 7. Paste it in your default / favorite browser
 8. And click the purple Authorize button

# Getting started after install
There should be a new deck available in Lioranboard called 'StreamUP - Predictions' open up this deck and you will be greeted by the deck :

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/LioranBoard_Receiver_15IkbU6WVI.png"></p>

We shall now go over the numbers what they do and mean:

 1. These are example prediction buttons. You can freely open and edit this button. You can make as many copies of these buttons as you want so you can easily make premade default predictions for yourself. Inside the button is a small instruction available about what you can change. But it will also be covered in this documentation later on also.
 2. This is a blank button. Just to fill up some space. You can resize or delete this button and make some space for more prediction buttons if you want.
 3. These buttons are for picking a winning side. The extension will autofill the answers into this button and will show it on the Lioranboard stream deck application.²
 4. This button will retrieve the latest prediction information as how many channel points have been used and how many people have chosen a side. ² ³
 5. This button will lock an open predication before the timer is finished.²
 6. This button will cancel any open or locked prediction. Viewers will get their points back.²
 7. This button has some complex logic in it so that moderators and the streamer can make a prediction through Twitch chat. This feature was implemented so that mobile users can also create a prediction.²
    - You can't use the native '/prediction' on mobile as of writing this.
 9. This button will make you go to the StreamUP website
 10. This button will make you go to this documentation
 11. This button will make you go to an awesome streamer called Silverlink and you should totally follow him 😉  

² **Please do not edit these buttons.  They are fully automated.**  
³ **This button only retrieves information when a prediction is created through this extension!**

# Setting up / editing the example prediction
This is where a big part of the magic happens. This button can be copied as many times as you want so that can create unlimited presets for your predictions.

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/LioranBoard_Receiver_h7ErAZNGmd.png"></p>

### Information section:
This just has some general info for you to read
### Edit section:
This section you can edit the values on the right where it says 'Var./Real/"String"*'
|  Value | Variable |  Type | Extra info |
|--|--|--|--|
| 1 | Prediction Title | String | Max 45 characters
| 2 | Answer 1 / Blue | String | Max 25 characters
| 3 | Answer 2 / Pink | String | Max 45 characters
| 4 | Timer | Real | Min: 1, Max: 1800

*Strings needs values to be put in between "quotes"  
Number you can put in without any "quotes"*
### Do not touch
I think this does not need any explaining right? 😉

# Starting a prediction through Lioranboard Stream Deck
This guide assumes that you know how to connect to Lioranboard through the Lioranboard Stream Deck app for android or PC. Once you're connected to the app it should look something like this:

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/LioranBoard_Stream_Deck_We5ZSC950y.png"></p>

Once you've set up your buttons you can press them on this screen. In this example we are going to click on 'Example Prediction 1' . Once the prediction has started the answer you've specified will be showing up on the Answers button as shown below:

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/LioranBoard_Stream_Deck_zmoT2boEgZ.png"></p>

Also on twitch the prediction should have started and if you look into your chat or channel point menu this should be showing somewhere:

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/firefox_sq05UVAR7S.png"></p>

You can now press one of the answer buttons to set that as the winning prediction, you can also lock the prediction so that no new votes can be put in or you can cancel the running prediction and give everyone their points back.

Once you've picked a winning side points will be distributed to the winners of that side!

As you can see when a prediction is running the button 'Retrieve prediction information' flashes every 2 seconds. This will be happening until the timer runs out or if you lock the prediction. Manually pressing this button while nothing is running or when a prediction is locked will not do anything. This button is meant for retrieving prediction information that is made through this extension.⁴ If you find that every 2 seconds is to quick you can edit the button and put in a higher number than 2000. We don't recommend to go lower than that though.

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/LioranBoard_Receiver_pP8Ite0cSE.png"></p>

⁴ The reason why information has been pulling will be explained later on 
# Starting a prediction through the Transmitter
You can also start a prediction by clicking on the 'StreamUP Twitch Prediction System' tab in your tsl_transmitter and you can start a prediction there. 

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/chrome_e3LC4U85zf.png"></p>

First you need to press the button 'Get / Refresh OAuth Credentials from Lioranboard' so it will retrieve your credentials from Lioranboard. If you don't press that button, creating a prediction will not work. After that you can fill in the fields in the 'Create Prediction' area as you would in Lioranboard.  When the fields are filled you just press the button 'Start New Prediction' and voila the prediction should be started. This syncs up with Lioranboard itself so the decks will also be updated.

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/chrome_rrPyRt86Uya.png"></p>

When a prediction is started you'll see some information popup. These are are being live retrieved through lioranboard (That is what the flashing 'Retrieve prediction information' button does 😉) You can see live how many people have cast a prediction and how many channel points they have spend. This information is also pushed to Lioranboard (More information about this later in this document). Here you can, just as in the Lioranboard stream deck application, select a winner, lock and / or cancel a prediction.

# Starting a prediction through Twitch chat
With this you can also start predictions through twitch as a mod or streamer. Currently Twitch does not support '/prediction' on mobile so we made it possible through our own system. You just start by typing !prediction. If you or a mod start the prediction only the one who started the prediction can finish the prediction.

Here is a complete example how it works:

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/firefox_bpBEnwPl88.png"></p>

*The texts are customizable in the 'Mod Prediction Trigger' (How to edit and what to edit is available in this document)*

These are the available chat commands for moderators and streamers:

|  Chat Command| Information  |
|--|--|
| !prediction | This will start a prediction |
| !prediction stop | This will stop the current setup of a prediction
| !prediction-winblue | Pick Team Blue as the winner |
| !prediction-winpink | Pick Team Pink as the winner|
| !prediction-lock| Locks the current running prediction |
| !prediction-cancel| Cancels prediction and refunds channel points|

I don't think it needs any more explanation but if you have any questions, remarks or feedback please let us know on the StreamUP Discord.

# Editing the 'Mod Prediction Trigger'
You can edit this button to personalize the messages. If you find the messages good enough you skip this area.

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/LioranBoard_Receiver_SR8fDJB1zp.png"></p>

Everything is specified already in the deck but here is a little bit extra. My advise to you is to copy and paste the variables into a text file for easier editing. All these values are strings so they need to be in "quotes".

|  Bullet | Variable |  Type | Info | Default message
|--|--|--|--|--|
| 1 | predictionChatStep0 | String | First message that appears. | "Prediction setup started for /$SUPr:triggerUser$/. Please enter a title for the new prediction! Start typing !prediction and than the title of the prediction or type !prediction stop to stop anytime in the setup"
| 2 | predictionChatStep0Error | String | When at the first step and someone makes a boo boo | "I think you forgot a step. Please start the prediction by just typing !prediction"
| 3 | predictionChatStep1 | String | Title specified, waiting for 1st answer |"Title specified! Now please enter the first answer! Start typing !prediction and than the answer"
| 4 | predictionChatStep2 | String | 1st answer specified waiting for 2nd answer | "Answer 1 specified! Now please enter the second answer! Start typing !prediction and than the answer"
| 5 | predictionChatStep3 | String | 2nd answer specified waiting for timer number | "Answer 2 specified! Now enter how long in seconds the prediction should be running. Start typing !prediction and than a number between 1 and 1800 to start a prediction"
| 6 | predictionChatStep4a | String | Summary | "Prediction Settings: Title: /$SUPr:predictionTitle$/ || Answer 1: /$SUPr:blueTitle$/ || Answer 2: /$SUPr:pinkTitle$/"
| 7 | predictionChatStep4B | String | Question if the user wants to continue | "@/$SUPr:triggerUser$/ Do you want to start the prediction? Type !prediction YES to continue. Type !prediction and anything else to stop"
| 8 | predictionChatStep5Yes | String | Message when Yes | "Starting Prediction!"
| 9 | predictionChatStep5No | String | Message when Anything else | "Stopping prediction. You can start a new prediction by typing !prediction"
| 10 | predictionChatStop | String | Message when triggered by !prediction stop | predictionChatStep5No

*Strings needs values to be put in between "quotes"*

Don't edit anything else in this button or otherwise it may brake and you may need to reinstall the deck.

# Receiving Variables in Lioranboard
This is where the magic happens! Lioranboard receives every 2 seconds (or per what you've set in the 'Retrieve prediction information' button) information from the Twitch API. This means you can live update your sources in OBS through Lioranboard. You can show live numbers on stream. Make a moving bar for the countdown and other great stuff. [Andilippi](https://twitch.tv/Andilippi) has made a great example of what you can do with it. Here is a screenshot of it:

<p align="center"><img src="https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/firefox_yaMO23C7er.png"></p>

The extension sends out the following variables:

### Prediction Information
| Variable | Type | Information
|--|--|--|
| SUPr:predictionID | String | ID of prediction given by Twitch
| SUPr:predictionTitle | String | Title you specified for the prediction
| SUPr:predictionWindow | Real | Seconds you specified for the prediction
| SUPr:predictionStatus | String | Status of the prediction. (OPEN, LOCKED, RESOLVED or CANCELED)
| SUPr:isPredictionRunning | Real | Internal Variable to check if the prediction is running

### Blue Answer Information
| Variable | Type | Information
|--|--|--|
| SUPr:blueID | String | ID of Answer 1 / Blue given by Twitch
| SUPr:blueTitle | String | Answer you specified for Answer 1 / Blue
| SUPr:blueTotalCP | Real | Total amount of channel points spent for Answer 1 / Blue
| SUPr:blueTotalCPRounded | String | Total amount of channel points for Answer 1 / Blue⁵
| SUPr:blueTotalUsers | Real | Total amount of people who voted for Answer 1 / Blue
| SUPr:blueTotalUsersRounded | String | Total amount of people who voted for Answer 1 / Blue⁵

### Pink Answer Information
| Variable | Type | Information
|--|--|--|
| SUPr:pinkID | String | ID of Answer 2 / Pink given by Twitch
| SUPr:pinkTitle | String | Answer you specified for Answer 2 / Pink
| SUPr:pinkTotalCP | Real | Total amount of channel points spent for Answer 2 / Pink
| SUPr:pinkTotalCPRounded | String | Total amount of channel points for Answer 2 / Pink⁵
| SUPr:pinkTotalUsers | Real | Total amount of people who voted for Answer 2 / Pink
| SUPr:pinkTotalUsersRounded | String | Total amount of people who voted for Answer 2 / Pink⁵

### Totals Information
| Variable | Type | Information
|--|--|--|
| SUPr:totalPredictingCP | Real | Total amount spend on this prediction
| SUPr:totalPredictingCPRounded | String | Total amount spend on this prediction⁵
| SUPr:totalPredictingUsers | Real | Total amount of people who voted in this prediction
| SUPr:totalPredictingUsersRounded | String | Total amount of people who voted in this prediction⁵

*⁵ Values rounded to a String value. Ex: 42069 will be rounded to 42k*

You can use these variables in Lioranboard how ever you want. Show them in OBS via a text source, make advanced calculations with the numbers and many more stuff and things.

# Extension Triggers
When certain events happen in the extension the extension will send out some Extension Triggers. You can use these however you want.

| Extension Trigger | Info
|--|--|
| SUPrInitialize | Send out when you start a predictin through the transmitter, chat command or stream deck app
| SUPrWinBlue | Send out when you've selected blue as a winner through the transmitter, chat command or stream deck app
SUPrWinPink | Send out when you've selected pink as a winner through the transmitter, chat command or stream deck app
SUPrCancel | Send out when you cancel a prediction through the transmitter, chat command or stream deck app
SUPrLock| Send out when you lock a prediction through the transmitter, chat command or stream deck app

# Send to Extension
You can manually create buttons if you like in other decks or just create a template deck with just only starting predictions. 

*We strongly advise only to create 'StreamUP - Set Prediction' buttons and do not create any other buttons because they are handled in the default deck that comes with this extension.*

*You can **move** the 'Answer 1' and 'Answer 2' buttons to another deck but the button ID needs to be 'SUPr:A1' for the Answer 1 button and 'SUPr:A2' for the Answer 2 button if you want them to be updated like in the default deck. If you just want to pick a winner button without any updates on the button you can use 'StreamUP - End Prediction' and configure that correctly.*

### StreamUP - Set Prediction
| Parameter | Default value | Type | Information
|--|--|--|--|
| channel_id | /$channel_id$/ | String | This field is filled in automatically
| oauth_token | /$oauth_token$/ | String | This field is filled in automatically
| Prediction Title |  | String | Title of the prediction
| Answer 1 |  | String | Answer 1 / Blue
| Answer 2 |  | String | Answer 2 / Pink
| Prediction Window |  | Real | How long the prediction should stay open

### StreamUP - Get Prediction
| Parameter | Default value | Recommended value |  Type | Information
|--|--|--|--|--|
| channel_id | /$channel_id$/ | /$channel_id$/ | String | This field is filled in automatically
| oauth_token | /$oauth_token$/ | /$oauth_token$/ | String | This field is filled in automatically
| Prediction ID | | /$SUPr:predictionID$/ | String | ID of the running prediction

### StreamUP - End Prediction
| Parameter | Default value | Recommended value |  Type | Information
|--|--|--|--|--|
| channel_id | /$channel_id$/ | /$channel_id$/ | String | This field is filled in automatically
| oauth_token | /$oauth_token$/ | /$oauth_token$/ | String | This field is filled in automatically
| Prediction ID | | /$SUPr:predictionID$/ | String | ID of the running prediction
| Winning Outcome ID | | Empty, /$SUPr:blueID$/ or /$SUPr:pinkID$/| String | Can be left empty if you set Prediction Status to CANCELED or LOCKED. ID is required when setting to Resolved
| Prediction Status | Resolved |  | Selection box | Set the status of the prediction.
| Clear Variables | true |  | Selection box | IClear the variables
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTYwODg5NDM4MCwtNTMwODQ1MzY1LC0xMz
I5OTE2ODU4LDc1NDI1MzU3MCwzMTcxMTMzNjEsLTY3NDc1MDYx
Myw0NTE5MjU3MTIsLTE5NDcxMzQ2NjUsMTQ5Njg5NDc2MSwyMT
EwMTIxNzcxLDEyODMwMjY5NDcsLTE5NDcxMzQ2NjUsNTExNDc0
MzI1LDExNTA5MTcyMiwtMTAyNDg3MjA3MiwxOTQwMTA4NjUxLD
gzNzEzNTY2Miw1NDg4NzU2NzAsLTU1MDk2MTg0MCwtMTQ1MDE3
MzYyMl19
-->