# GoXLR on Linux

<p align="center">

[![Support Server](https://img.shields.io/discord/828348446775574548.svg?label=Discord&logo=Discord&colorB=7289da&style=flat)](https://discord.gg/Wbp3UxkX2j)

<img src="img/GoXLR-Linux.png" alt="Logo" height="200px" width="200px">
</p>

## About

[@T-Grave](https://github.com/T-Grave) started this community driven project in March 2021. 

The [first approach](https://github.com/GoXLR-on-linux/goxlr-on-linux/) of getting the GoXLR (and GoXLR Mini) to work under Linux was a shell script to assign the channels to audio in and outputs.
[@T-Grave](https://github.com/T-Grave) initially documented the channels and got the Project to roll.
From time to time the scripts were improved by [many people](https://github.com/GoXLR-on-Linux/goxlr-on-linux/graphs/contributors). 

On November 23rd 2021 Linus Tech Tips made a [video](https://youtu.be/3E8IGy6I9Wo?t=250) where the project was mentioned which brought many new people to it. 
The criticism from him, especially that it is difficult for non linux users to run the script, 
was noticed and the work on a plug and play way was started. 
For this a [kernel bug](https://bugzilla.kernel.org/show_bug.cgi?id=215079) was opened. 

On January 3rd, 2022 [@Dinnerbone](https://github.com/Dinnerbone) started reverse engineering the GoXLR. From there on the functionality of the GoXLR was recreated.
[@FrostyCoolSlug](https://github.com/FrostyCoolSlug) and [@Dinnerbone](https://github.com/Dinnerbone) wrote a [rust application](https://github.com/GoXLR-on-Linux/GoXLR-Utility/) to initialize and configure the GoXLR. 
_Note: A gui application is going to be created soon._

On May 30th, 2022 the kernel bug was patched by [@FrostyCoolSlug](https://github.com/FrostyCoolSlug). With the patch, the script is no longer needed, although there is about 500 ms latency under pulseaudio. 
For pulseaudio, the old script is still recommended until the problem is fixed. 
Alternatively, you can also switch to pipewire, since the latency problem does not exist here.
To apply the patch (kernel 5.15+) with dkms look [here](https://github.com/GoXLR-on-Linux/snd-usb-audio-goxlr/).

### Disclaimer
```
This project is not in any way affiliated with TC-Helicon. 
There is no official support for GoXLR (Mini) on Linux. 
This project, or any of its contributors cannot be held responsible 
for any issues you experience with your device, 
before or after using the scripts or documentation provided.
```
