# nozomu-printer

This script prints to a printer using the serial port of a Raspberry Pi, and plays a sound when printing.

## Set up

1. Download the files from GitHub by clicking on the green "Code" button, and "Download ZIP"
2. Extract the ZIP, and copy `start-printing` and `printer.config` to the home folder on your Pi*

(*) The home folder can be accessed by running `cd ~`. On a default Pi install, it will probably be in `/home/pi`.

## Configuration

Open the `printer.config` file in a text editor. The file contains options, in the format `option name: option value`.

Change the `text-path` and `sound-path` options to point at your files.
You can use `~` to refer to the home folder, e.g. `~/mysounds/sound.wav`.

Change the baud rate to match the rate of your printer.

## Usage

Simply open your Terminal, go to your home folder (`cd ~`) and run `./start-printing`.

## Things to remember

* The text file should be a plain `.txt`
* The printer will print one line of the text file at a time. So format it so that each paragraph is entirely on one line.
* Make sure the sound file is a valid WAV file. You can export it as WAV for example in Audacity (File > Export > Export as WAV).
