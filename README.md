# TPFanControl for dual-fan ThinkPads (P1, X1 Extreme..)

Tested and working without issues on my ThinkPad P1 Gen 3 with Nvidia GPU.

## About

This is a fork of https://github.com/byrnes/TPFanControl.

Features / fixes:

- **On my machine, this completly fixes the issue that the fan on the right side was not always stopped**
- Speed of both fans (left and right) is now read from the embedded controller and displayed in RPM
- Sensor name for GPU and some presets are set correctly for modern machines
- Minor cosmetic changes

Some files were removed from the repository that should not be under version control. Other than that, no code reformatting or refactoring was done for the utmost transparency of changes to the original version of TPFanControl.

## Installation

Either install [tvicport](https://www.entechtaiwan.com/dev/port/index.shtm) manually or install the original version of TPFanControl found [here](https://sourceforge.net/projects/tp4xfancontrol/) and run the dual-fan version instead of the original version:

After you installed the original version of TPFanControl, replace the .exe (and possibly .ini) file with the corresponding files in the `fancontrol/Release` directory.

## Running at startup
To my knowledge, running at startup is currently not possible with Windows 10 because it lacks a certificate to prevent the Windows security warning. If you have working and easy to reproduce instructions how to create a self signed certificate: please let me know or create a pull request.
