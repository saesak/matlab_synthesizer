# matlab_synthesizer
This is a synthesizer created in MATLAB during my ENGR105(Introduction to Scientific Computing) course at UPenn.

![Synthesizer Menu](/example_images/synthsizer_menu.PNG)

This is what the GUI of the synthesizer looks like. 

Short Description of the Project:
By pressing different keys, that particular note on the synthesizer keyboard will play. You can customize the type of waves and distortion ratios in order to make the synthesizer sound different. Each note as you play it will appear on the window, and if you play a recording, the notes will appear on the window as well. You can also make recordings, layer recordings on top of each other, and export the final product when you're finished recording. 


Long Description of the Project:
The buttons at the bottom with the notes written on them are the keyboard of this synthesizer. I have only included notes from C3 to B4. The notes placed over some of the other notes are the sharps/flats of the synthesizer keyboard. If you click them, for 1.5 seconds, the sound of the key will play. The notes are only playable through clicking on them. Most of the difficult part about writing the code for this part was because I had to understand the relationship between frequency and time, because I would have to account for the frequency of each note if each note was going to play for the same amount of time. For this part, I used the fact that the period of a wave and the frequency of the wave are inverses of each other to account for the time taken for each note to play. Another part I needed to account for is the sample rate. I eventually figured out that the sample rate is how many data points there are for a single second of sound, and using that fact, I adjusted how large of a matrix I would have to create to play that sound. 

In terms of distortion, I had to figure out what distortion in music did to a wave. I researched some while online to find out that distortions were the “hard clipping” in the image. I implemented this by using the distortion meter. Since the maximum amplitudes of my waves were 1, the degree of my distortion would be from 0 to 1. Since my notes are generated such that 1 and -1 are the respective limits of the amplitudes of the notes, if you turn the distortion up to 1 no sound will play.

![Sound Distortion](/example_images/sound_distortion.jpg)
(http://georgeantonios.com/2017/05/19/distortion/)

Above, there is a on off switch that says "Record" under it. This is the thing that decides whether the app is going to be recording sound or not. Of course, if the slider for the length of the recording is set to 0, nothing will be recorded. Turning the switch off will stop the recording. If you choose not to reset the recording or change the length of the recording after you finish recording, you can continue to record sound after turning the switch on again to layer your soundwaves. So you can record multiple layers of sound. Another important part of this button is that the way it visually shows you that it is off is if you press a key after the recording time has elapsed. Then it will visually change to off. But before that, it will look as if it is on. The recording will never record past the recording time, rest assured, though. Also, I made the recording so that when waves are recorded, they aren't recorded separately, but they are all added and superimpose upon each other. There's some interesting effects that can be observed from this and you can literally hear when some waves are infringing upon each other. I thought it was pretty interesting. 

