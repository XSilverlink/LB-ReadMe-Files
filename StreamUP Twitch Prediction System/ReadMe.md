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
 7. This button has some complex logic in it so that moderators and the streamer can make a prediction through Twitch chat. This feature was implemented so that mobile users can also create a prediction. This is not possible at the time of writing.²
 8. This button will make you go to the StreamUP website
 9. This button will make you go to this documentation
 10. This button will make you go to an awesome streamer called Silverlink and you should totally follow him 😉  

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
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjQyNjIwMTk1LC05MTU3MDMyNDcsLTE2Mz
gxMTA0MjgsLTkxNTcwMzI0NywtODAwNzkxNzk1LC05MjQyMjAz
MDgsLTEzMzY1MzYzODgsMjEwMDI1MTk3MiwtMjI3MjYxMjUsMj
YzOTAxMTAyLC0xNTU2OTY2NTU2LDEwNjQxNTg3MTAsLTk5Mjg3
NDM3Myw0NDQ4Njc0MDcsLTExNTU5NDg3MjcsLTEwNjM3Njc1MD
YsLTk0NTAwMDk0NF19
-->