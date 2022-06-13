# History

[@T-Grave](https://github.com/T-Grave) started this community driven project in March 2021.

The [first approach](https://github.com/GoXLR-on-linux/goxlr-on-linux/) of getting the GoXLR (and GoXLR Mini) to work under Linux was a shell script to assign the channels to audio in and outputs.
[@T-Grave](https://github.com/T-Grave/) initially documented the channels and got the Project to roll.
[@Gregory-Hepicloud](https://github.com/Gregory-Hepicloud/) added Arch support.
[@lm41](https://github.com/lm41/) and [@VirtuelJunky](https://github.com/VirtuelJunkey/) have written the installation script, for easier installation.
From time to time the scripts were improved by [many people](https://github.com/GoXLR-on-Linux/goxlr-on-linux/graphs/contributors).

On November 11th 2021 was the ALSA-UCM method by [@Toniob](https://github.com/Toniob) introduced. It removed the need of the script, but worked only before kernel 5.11. To get it working a [kernel bug](https://bugzilla.kernel.org/show_bug.cgi?id=215079) was opened.

On November 23rd 2021 Linus Tech Tips made a [video](https://youtu.be/3E8IGy6I9Wo?t=250) where the project was mentioned which brought many new people to it.
The criticism from him, especially that it is difficult for non linux users to run the script,
was noticed and the work on the above kernel bug has therefore been resumed.

On Dezember 6th, 2021, mainly inspired by the LTT video, [@FrostyCoolSlug](https://github.com/FrostyCoolSlug) started reverse engineering the GoXLR.
Later on [@Dinnerbone](https://github.com/Dinnerbone) started helping [@FrostyCoolSlug](https://github.com/FrostyCoolSlug).
From there on the functionality of the GoXLR was recreated.

On January 3rd, 2022 [@Dinnerbone](https://github.com/Dinnerbone) and [@FrostyCoolSlug](https://github.com/FrostyCoolSlug) started to write a [rust application](https://github.com/GoXLR-on-Linux/GoXLR-Utility/) to initialize and configure the GoXLR.
_Note: A gui application is going to be created soon._

On May 30th, 2022 the kernel bug was patched by [@FrostyCoolSlug](https://github.com/FrostyCoolSlug). With the patch, the script is no longer needed, although there is about 500 ms latency under pulseaudio.
For pulseaudio, the old script is still recommended until the problem is fixed.
Alternatively, you can also switch to pipewire, since the latency problem does not exist here.
To apply the patch (kernel 5.15+) with dkms look [here](https://github.com/GoXLR-on-Linux/snd-usb-audio-goxlr/).
