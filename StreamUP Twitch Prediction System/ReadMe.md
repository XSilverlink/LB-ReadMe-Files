# StreamUP Twitch Prediction System by [Silverlink](https://twitch.tv/silverlink)
**An extension and deck for [Lioranboard](https://obsproject.com/forum/resources/lioranboard-stream-deck-animator.862/) that utilizes the new Twitch Prediction System API!**

![](https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/StreamUPTwitchPredictionSystem.png)
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

# Getting started after install
There should be a new deck available in Lioranboard called 'StreamUP - Predictions' open up this deck and you will be greeted by the deck :

![](https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/LioranBoard_Receiver_15IkbU6WVI.png)
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

![](https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/LioranBoard_Receiver_h7ErAZNGmd.png)

### Information section:
This just has some general info for you to read
### Edit section:
This section you can edit the values on the right where it says 'Var./Real/"String"*'
|  Value | Variable |  Type | Extra info |
|--|--|--|--|
| 1 | Prediction Title | String | Max 45 characters
| 2 | Answer 1 / Blue | String | Max 25 characters
| 3 | Answer 2 / Pink | String | Max 45 characters
| 4 | Timer | Number | Min: 1, Max: 1800

*Strings needs values to be put in between "quotes"  
Number you can put in without any "quotes"*
### Do not touch
I think this does not need any explaining right? 😉

# Starting a prediction through Lioranboard Stream Deck
This guide assumes that you know how to connect to Lioranboard through the Lioranboard Stream Deck app for android or PC. Once you're connected to the app it should look something like this:
![](https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/LioranBoard_Stream_Deck_We5ZSC950y.png)

Once you've set up your buttons you can press them on this screen. In this example we are going to click on 'Example Prediction 1' . Once the prediction has started the answer you've specified will be showing up on the Answers button as shown below:

![](https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/LioranBoard_Stream_Deck_zmoT2boEgZ.png)

Also on twitch the prediction should have started and if you look into your chat or channel point menu this should be showing somewhere:

![](https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/firefox_sq05UVAR7S.png)

You can now press one of the answer buttons to set that as the winning prediction, you can also lock the prediction so that no new votes can be put in or you can cancel the running prediction and give everyone their points back.

Once you've picked a winning side points will be distributed to the winners of that side!

As you can see when a prediction is running the button 'Retrieve prediction information' flashes every 2 seconds. This will be happening until the timer runs out or if you lock the prediction. Manually pressing this button while nothing is running or when a prediction is locked will not do anything. This button is meant for retrieving prediction information that is made through this extension.⁴ If you find that every 2 seconds is to quick you can edit the button and put in a higher number than 2000. We don't recommend to go lower than that though.

![](https://raw.githubusercontent.com/XSilverlink/LB-ReadMe-Files/main/StreamUP%20Twitch%20Prediction%20System/images/LioranBoard_Receiver_pP8Ite0cSE.png)

⁴ The reason why information has been pulling will be explained later on 
# Starting a prediction through the Transmitter
You can also start a prediction by clicking on the 'StreamUP Twitch Prediction System' tab in your tsl_transmitter and you can start a prediction there. 
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTY2NTE3MTgwLC0xMjUxNzc3MTI5LDE2Mz
cxOTQ4NywtMTgyMDAzMzcyLC0xMTQ4MDkyMjM1LDI0MjYyMDE5
NSwtOTE1NzAzMjQ3LC0xNjM4MTEwNDI4LC05MTU3MDMyNDcsLT
gwMDc5MTc5NSwtOTI0MjIwMzA4LC0xMzM2NTM2Mzg4LDIxMDAy
NTE5NzIsLTIyNzI2MTI1LDI2MzkwMTEwMiwtMTU1Njk2NjU1Ni
wxMDY0MTU4NzEwLC05OTI4NzQzNzMsNDQ0ODY3NDA3LC0xMTU1
OTQ4NzI3XX0=
-->