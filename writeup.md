# **Hiding Creatures**

## Indroduction
We are given a .jpeg file. the name of the file is "Ash.jpeg"
We can check if its actually a jpeg file or not ny using "file <file_name>" in our terminal

>"Ash.jpeg: JPEG image data, JFIF standard 1.01, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 578x327, components 3"

we can confirm that this is an actual jpeg file

we run "strings" on this file to check to see are any strings attached to this .jpeg file

>....
....
cv;\)
8)s%
ZU]#
'-c+
sn}&;
aBVz
%f8U
Z"g/i
Lv#''vh
I wanna be the very best, Like no one ever was....
password is the fast, may be the fastest...

ok we can confirm that this file has something hiding in it.

We know the name of the challenge is "Hiding Creatures"

so we might need to use the steg hide tool for this.

the .jpeg is of a cartoon which many may not recognise, as its the recent reboot of the popular series.

Ok by now, adding up all the clues we can confidently say that this is related to "Pokemon"

And the fastest pokemon as of now is Regieleki with a speed stat of 200

now if we try to extact the hidden file from the "Ash.jpg" file using the steghide tool and for the passphrase we use "Regieleki" we get
 
>$ steghide extract -sf Ash.jpeg
Enter passphrase: 
wrote extracted data to "flag.txt".

the flag.txt has some giberish which is base64 encoded. After we dcode that we get our flag!

>CTF{g0774_c47ch_'eM_411}