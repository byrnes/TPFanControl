# TPFanControl for dual-fan ThinkPads (P1, X1 Extreme..)

Confirmed to be working on:
- ThinkPad P1 Gen 3 with Nvidia GPU
- ThinkPad X1 Extreme Gen 3 (@dharmatech)
- ThinkPad P15 Gen 2 (@stavoxnetworks)

Please open an issue to have me add your model to the confirmed list. Thank you!

## About

This is a fork of https://github.com/byrnes/TPFanControl.

Features / fixes:

- **On my machine, this completly fixes the issue that the fan on the right side was not always stopped**
- Speed of both fans (left and right) is now read from the embedded controller and displayed in RPM
- Sensor name for GPU and some presets are set correctly for modern machines
- Minor cosmetic changes

Some files were removed from the repository that should not be under version control. Other than that, no code reformatting or refactoring was done for the utmost transparency of changes to the original version of TPFanControl.

## Future development
It is possible but not yet implemented to control both fans separatly. This way you could have only the CPU fan running as long a the Nvidia is not used. Possible benefit would be to reduce fan noise on each level by 50% while using the Intel GPU.

## Installation

Either install [tvicport](https://www.entechtaiwan.com/dev/port/index.shtm) manually or install the original version of TPFanControl found [here](https://sourceforge.net/projects/tp4xfancontrol/) and run the dual-fan version instead of the original version:

After you installed the original version of TPFanControl, replace the TPFanControl.exe (and possibly TPFanControl.ini) with the files from the release package or the corresponding files in the `fancontrol/Release` directory.

## Running at startup
To my knowledge, running at startup is currently not possible with Windows 10 because it lacks a certificate to prevent the Windows security warning.

You can however achieve the same result with Windows Task Scheduler:
- Create a new task, give it a descriptive name and select "Run with highest privileges"
- In tab "Triggers" create a new trigeger and select "Begin task": "At log on"
- In tab "Actions", create a new action and select "Start a program" and the path to TPFanControl.exe
- Enjoy :)
