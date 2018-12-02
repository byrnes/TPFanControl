# TPFanControl

This is a Fork of https://github.com/ThinkPad-Forum/TPFanControl/tree/master/fancontrol. I've updated it to work with two fan devices, such as the P51. This has only been tested on my P51, but it should work on the P50, P70, P71, P52, P72, P1, and X1 Extreme as well, as well as any other dual-fan Thinkpads that are released. A working debug build is included in fancontrol/Debug, but it will need to be run each boot, or added to run at startup. The default fan profile that is included is a silent one, with the fans only coming on at 60c. This can be changed by editing tpfancontrol.ini in the fancontrol/Debug. Many other options can be changed in the config file as well. I used Visual Studio 2017 Community to build, earlier/later versions may work as well but are not tested.

## Requirements

To avoid errors, either install [tvicport](https://www.entechtaiwan.com/dev/port/index.shtm) manually or install the original version of TPFanControl found [here](https://sourceforge.net/projects/tp4xfancontrol/), and run the dual-fan version instead of the original version.

## Running at startup

The easiest way to run TPFC at startup is:

- Right-click on fancontrol.exe and select copy
- Press Windows-r or search for run in the start menu
- Type `shell:startup` in the run box
- Right click in the window that opens and select paste shortcut

Note: this won’t start TPFC until you reboot.