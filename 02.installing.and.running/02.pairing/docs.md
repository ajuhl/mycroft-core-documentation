---
title: 'Mycroft Home Device and Account Manager'
taxonomy:
    category:
        - docs
---
Mycroft AI, Inc. - the company behind Mycroft maintains the Home device and account management system. Developers can sign up at https://home.mycroft.ai

Mycroft software by default uses speech-to-text services on Home, so any request such as "Hey Mycroft, what is the weather?" is handled there.  In order to use this service, you need to pair your device with your account.  Mycroft will speak a 6-digit code, which you enter into the pairing page on the [Home site](https://home.mycroft.ai).

### Getting the pairing code
First, you need to get the pairing code from Mycroft. If this doesn't happen automatically, say `Mycroft, register my device`. Listen for what he says or, if you are running Mycroft in a terminal, you can look at the terminal running the voice process. You should be able to see what code he says, as shown in the lower right corner of the image above.

### Pairing with Home
 - Go to https://home.mycroft.ai and log in using your preferred mechanism.  You can use Facebook, Google or Github to authenticate or log in directly using your email address.

 - Visit the 'Devices' page by clicking on the link in the upper-middle portion of the page.
 
 - Click on the `+ Add Device` button
 
 - Enter the pairing code you received above from Mycroft.  Then fill in the other fields and select `OK, Let's Pair`
 
 - That's it!  Mycroft is ready to be used.

The unit will use our API keys for services, such as the STT (Speech-to-Text) API. It also uses allows you to use our API keys for weather, Wolfram-Alpha, and various other skills.

## Customizing your interaction

You can customize Mycroft to work the way you want to work by visiting the Settings page on Home.  You can chose preferred units (metric or imperial), time format, etc.

## Under the hood

Pairing information generated by registering is stored in:

`~/.mycroft/identity/identity2.json` <b><-- DO NOT SHARE THIS WITH OTHERS!</b>

It can be useful to know the location of the identity file when troubleshooting device pairing issues.

### API Key services

- [STT API, Google STT](http://www.chromium.org/developers/how-tos/api-keys)
- [Weather Skill API, OpenWeatherMap](http://openweathermap.org/api)
- [Wolfram-Alpha Skill](http://products.wolframalpha.com/api/)

These are the keys currently built-in to Skills from Mycroft