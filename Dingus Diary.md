# Dingus Diary

All right, I think I’ve cracked this as well as it can currently be cracked.

After playing with numerous different combinations, it’s clear that location is definitely the time killer, but I found that retrieving it with “Current Weather Conditions” is actually worlds faster. Also, while it takes the same time to retrieve it anywhere in the flow of the shortcut, where you place it does make a substantial _perceived_difference in speed, particularly when you’re using it with audio cues only and not looking at your phone. 

You’ll obviously need to allow a bunch of stuff the first time, but then it should be cooking for you.

Grab it and take it for a spin here:

[“Log This” Shortcut](https://www.icloud.com/shortcuts/d78dac49e2794f6b813566a67c3b79b6)

## File Naming

To easily set or change the name of your CSV log file, you simply give it a name in the import question, or you can change it at any time in the first text box in the shortcut flow.

## File Lookup/Creation

I wanted to build in file creation with named headers, but not do that every time, obviously, so the shortcut checks for the existence of a file with the name you chose. If it doesn’t exist yet, it creates it with all the header names, if it does, it does nothing.

## Information Gathering

There somehow isn’t any stopwatch functionality built in to shortcuts, but I wanted to measure its runtime to compare its speed, whether on Wi-Fi or not, from different devices, etc. So there’s a hacky approach of taking a “Current Date” stamp at the very beginning (only in seconds), then again right before it writes all the data to the file, and finding the difference.

It also retrieves the Wi-Fi network you’re connected to, if any, what device you’re running the shortcut from (HomePods just show as your iPhone, since they don’t run shortcuts natively, for some reason), your dictated text, and your location (thanks, Weather app!), and then write them all to the file name you chose.

## Performance

My favorite way to use the shortcut is via the one AirPod Pro I often have in an ear. I don’t need to interact with my phone at all, and I have Siri responses set to “Only with ‘Hey Siri’”, so when connected to Bluetooth, it gives me a reassuring “What’s the text?”, and then a confirming, “Done,” “That’s done,” or “OK,” when the shortcut is complete.

I do have “Raise to Speak” turned on on my Series 7 Apple Watch, but not “Hey Siri”. Everything’s a little slower from the watch, of course, but still usable if needed, and pressing the Digital Crown seems to consistently work a bit faster than Raise to Speak for me.

## Shortcut Naming

I’ve had a lot of success with “Log This”. It’s short, not often confused by Siri for something else, and sounds minimally crazy in the event that anyone around me hears me using it. I’ve tested these a bunch with Merlin’s “Real Quick”, and that seems to be pretty effective for all the same reasons.

Using “Voice Log” regularly made Siri think it sounded like I was trying to change its volume, and I had fewer, but similar name-space/pseudo-homophone pollution issues with things like “Bike Log” as well.

## Closing

When I first started playing with this, I was taking a lot of pride in the minimal number of actions I was using to accomplish things, but as I started adding in things like runtime calculation and ways to make things slightly clearer and more easily editable, they started to creep up. Thankfully, virtually everything but location happens almost instantly, and the overall runtime is at a pretty consistent 5-8 second range for me, including dictation time, so it still feels about as fast as you could possibly want!

I think I’ve made it fairly easy to modify the things one might want to change, but if anyone has any trouble or questions, holler! I’m @hamrick, just about everywhere.

Thanks for posing a rare opportunity for me to nerd out on something for a bit.