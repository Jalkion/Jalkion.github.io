EAC 1.0 Setup Guide


Download link: http://www.exactaudiocopy.de/en/index.php/resources/download/
Current version as of this guide: EAC 1.0 Beta 3.
This guide was made for EAC version 1.0 beta 3 and will not completely work with earlier versions (which are not recommended any longer). Versions 0.99 or earlier should use the EAC 0.99 guide. 

Anything with a green outline around it is a required setting. Anything orange is required but depends on your drive. Anything unmarked is optional. This is meant to be a no-frills guide with little extra info. The old EAC 0.99 guide is more comprehensive (but outdated as far as settings go since there are new features in EAC 1.0) - visit it if you run into problems, the background information is basically still correct.

#Step 1: Download and install EAC

Download the installer and fire it up.

![](https://web.archive.org/web/20140714023611im_/http://blowfish.be/eac/Caaok/Images/eac01.png)
Eventually you'll get to a screen like this. Make sure you install AccurateRip, CDRDAO, CTDB and freedb as a bare minimum. FLAC will be useful as well if you don't have it separately installed. GD3 is only useful if you want to pay for metadata results. I assume you don't. 
Note: The above screenshot is from Beta 3. The new Beta 3 adds the option to include the CueTools Database Plugin. It is recommended to install it but not required. Full details for installation of the plugin on older versions is located in the appendix at the end of this guide.

#Step 2: Start EAC

![](https://web.archive.org/web/20140714033449im_/http://blowfish.be/eac/Caaok/Images/eac02.png)
When you first start EAC, you'll see a screen like this one. Hit "Cancel". Next, put a popular CD into your drive, preferably not one that was recently released (a few months old at least). You'll see a window like the one below appear. If you have an older version of EAC or dBpoweramp installed, it's likely AccurateRip was already configured, and this may not appear. You may need to try multiple CDs to get this to show up.


![](https://web.archive.org/web/20140714084437im_/http://blowfish.be/eac/Caaok/Images/eac03.png)

Hit Configure. It may take a few minutes. Hit "Ok" afterward. This is a necessary step, make sure you try several CDs.

#Step 3: EAC Options

All of the options dialogs can be found from the EAC menu at the top of the screen.

![](https://web.archive.org/web/20140714031903im_/http://blowfish.be/eac/Caaok/Images/eac04.png)
Start with EAC Options. Any tabs not pictured are completely optional settings, or are irrelevant to ripping.


![](https://web.archive.org/web/20140714024410im_/http://blowfish.be/eac/Caaok/Images/eac07.png)
If your drive is capable of reading UPC/ISRC codes and CD-Text (you can only really figure this out by trial and error), you're welcome to keep the top two options checked. Otherwise, uncheck them.

Other than that, these settings are pretty much ideal. I wouldn't recommend using more than 1 compressor thread even if you have a multicore computer. It doesn't take very long compared to the track extraction anyway. Note that in tests run by punkmeup, disabling the queue of external compressors in the background fixed an issue where EAC was generating WAV files instead of FLAC, so I've made that a required option. It should have no bearing on the rip quality. If rip queueing works for you (it does for me), feel free to leave it enabled.

Note that m3u file creation is technically optional, however, some users use these files to manage their libraries. 

![](https://web.archive.org/web/20140714035652im_/http://blowfish.be/eac/Caaok/Images/eac05.png)
Make sure you set the green highlighted settings as shown. If you're using an older version of EAC, make sure "No use of null samples for CRC calculations is UNCHECKED. The rest is optional, choose as you will. Locking the drive tray during extraction isn't a bad idea though.

![](https://web.archive.org/web/20140714023148im_/http://blowfish.be/eac/Caaok/Images/eac06.png)
These settings are pretty much all optional and self explanatory. I'd recommend using Alternate CD play routines and disabling autostart though.

The "Show status dialog after extraction" option setting has been problematic for some users. This displays the log after the rip is done, and offers you the option to save the log file. If you follow this guide, EAC will do this automatically. Do NOT hit "Save Log". As such I've disabled the setting here. Only turn it on if you know what you're doing.


![](https://web.archive.org/web/20140714030229im_/http://blowfish.be/eac/Caaok/Images/eac08.png)
Friends don't let friends normalize their EAC rips. Don't ever do it. The rip will no longer be a true "exact copy" of the CD.


![](https://web.archive.org/web/20140714023544im_/http://blowfish.be/eac/Caaok/Images/eac09.png)
As shown in the screenshot above here is the proper way to name tracks.

Naming Convention : %tracknr2% - %title%

Check 'Use Various Artists Naming Scheme' and use : %tracknr2% - %artist% - %title%


The only difference acceptable here would be perhaps %tracknr2%. %title% if you prefer periods instead of dashes in the filenames. If you need track numbers to go into triple digits for some reason, use %tracknr3% instead.

Don't replace spaces by underscores. It looks ridiculous.

A note on directory naming schemes and cuesheets:: Don't use a directory structure in your EAC filename options, unless you want to go back and edit your CUE sheet later. When you add a directory to the naming scheme, it'll put that directory path into the files. When, at a later date when you may have moved the files, you want to burn the files in EAC using your cuesheet, you'll be unable to do so. If you do insist on using a directory structure here, you need to go back, edit the CUE sheet in a program such as notepad, and remove the folder name from each line.

For example, a cuesheet line should look like this:

FILE "01 Last Known Surroundings.wav" WAVE

Not like this: 

FILE "C:\EAC Rips\Explosions in the Sky - Take Care, Take Care, Take Care (2011) [FLAC]\01 Last Known Surroundings.wav" WAVE

If you insist on doing this, the scheme might look something like this:
%artist% - %albumtitle% (%year%) [FLAC]\%tracknr2% - %title%

Follow the listed items on the Filename tab if you prefer a different scheme.

#Step 4: Drive Options

![](https://web.archive.org/web/20140714034919im_/http://blowfish.be/eac/Caaok/Images/eac10.png)
Start by hitting "Detect Read Features...". This will actually take a few minutes. The only feature detection that actually matters is Accurate Stream. If your drive can use it, checkmark the setting (most modern drives have Accurate Stream). If it can't, don't.

Even if your drive doesn't cache audio, it will not harm the rip quality to leave that checked. The rips take a bit longer with that setting enabled, though. Go watch TV or something while you wait.

Do not use C2, even if EAC thinks you can. Most drives have terrible C2 error implementation.


![](https://web.archive.org/web/20140714032740im_/http://blowfish.be/eac/Caaok/Images/eac11.png)
Hit "Autodetect read command now". It shouldn't take long. Leave everything else unchecked unless you're having problems. You can checkmark "CD-Text Read capable drive" if you want to test whether your drive can do it. If it can, great, otherwise, uncheck it. It's unlikely you'll ever use that feature anyway.


![](https://web.archive.org/web/20140714025157im_/http://blowfish.be/eac/Caaok/Images/eac12.png)
If you did the AccurateRip configuration at the start of this guide, the top half here will be greyed out. If not, you'll need to find your read offset correction from this list. Don't use a combined read/write offset. AccurateRip is a very useful function for checking that your rips are OK, so you should go back and try to get it configured if this option isn't greyed out.

If you want to figure out whether your drive needs "Overread into Lead-in and Lead-Out" checked, you can check by temporarily unchecking "Use AccurateRip with this drive". Stick a CD in the drive and hit "Detect read sample offset correction...". If you're just doing this for the Overread, see below:

![](https://web.archive.org/web/20140714023814im_/http://blowfish.be/eac/Caaok/Images/obrvpi.png)
xuncat's EAC 0.99 guide says:

Check "Overread Lead-In and Lead-Out" only if the test result says that your drive can overread from both the Lead-In and Lead-Out, or if it says Lead-Out and your offset correction is positive ,or if it says Lead-In and your offset correction is negative. Otherwise disable (uncheck) it.

Remember to check "Use AccurateRip with this drive" again once you're finished.


![](https://web.archive.org/web/20140714022340im_/http://blowfish.be/eac/Caaok/Images/eac13.png)
Pretty much every drive should work with the settings shown. If yours stalls on detecting gaps or detects gaps that are obviously wrong (like 30 second gaps on a non-live album), try Detection method B or C. If A, B, and C all fail, you can switch "Secure" to "Accurate" and try again.

#Step 5: Metadata Options

![](https://web.archive.org/web/20140714024249im_/http://blowfish.be/eac/Caaok/Images/eac14.png)
Here's where you pick your metadata provider. If you did install GD3, it'll be in the list. You can only rip 10 discs before you have to pay for a subscription though. Otherwise, you have a choice between the MusicBrainz plugin (CTDB), freedb plugin and EAC's native freedb support. I'm not really sure what the big difference is, I'm guessing it's the cover+lyrics. Anyway, change those settings above if you wish.


![](https://web.archive.org/web/20140714025554im_/http://blowfish.be/eac/Caaok/Images/eac15.png)
If you use EAC's native freedb instead, the settings should look like this. Make sure you put an email at the top, it doesn't need to be real. Hit "Get active freedb server list". Then checkmark the last option.

#Step 6: Compression Options

![](https://web.archive.org/web/20141003171408im_/http://blowfish.be/eac/Caaok/Images/eac16.png)
Set up this tab exactly as shown. You'll have to browse to the path where you have flac.exe, if you installed it with EAC it's in C:\Program Files (x86)\Exact Audio Copy\FLAC\flac.exe. If you installed it separately it's wherever you installed it. The bit rate and high/low quality have no effect on the rip.

The commandline parameters have changed in this version, so this will look new to most of you. The commandline recommended for optimal completeness is this: 
-8 -V -T "ARTIST=%artist%" -T "TITLE=%title%" -T "ALBUM=%albumtitle%" -T "DATE=%year%" -T "TRACKNUMBER=%tracknr%" -T "GENRE=%genre%" -T "PERFORMER=%albuminterpret%" -T "COMPOSER=%composer%" %haslyrics%--tag-from-file=LYRICS="%lyricsfile%"%haslyrics% -T "ALBUMARTIST=%albumartist%" -T "DISCNUMBER=%cdnumber%" -T "TOTALDISCS=%totalcds%" -T "TOTALTRACKS=%numtracks%" -T "COMMENT=%comment%" %source% -o %dest%

It takes no extra effort on your part, just copy and paste that into the additional commandline options and you're done.

![](https://web.archive.org/web/20141003171408im_/http://blowfish.be/eac/Caaok/Images/eac17.png)
Leave everything unchecked except the last option. 

Congrats! EAC is now properly set up! You may wish to save your settings in a profile by hitting "New" at the bottom of the screen. However, unless you're changing your settings frequently there's no need, EAC will remember all of this on next launch regardless.

For ripping, view the ripping guide here: