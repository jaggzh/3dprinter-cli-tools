# 3dprinter-cli-tools
Command line tools for convenient working with 3d printer

# Installation

1. Clone this repo
1. Symlink the scripts in a directory in your path.
1. Edit `printer-device` so it echos your proper USB/serial device (eg. /dev/ttyACM0)

## Example:
```bash
cd ~/bin
ln -s ~/opt/lib/3dprinter-cli-tools/printer-device
ln -s ~/opt/lib/3dprinter-cli-tools/printer-voice-home
ln -s ~/opt/lib/3dprinter-cli-tools/serial-echo-into
ln -s ~/opt/lib/3dprinter-cli-tools/voice-recognize-commands
```
# Usage examples:

## Go home, manually:
```bash
echo 'G28 Z' | serial-echo-into
```
The above (serial-echo-into) uses the default device set in `printer-device`.

If you want, you can override it:
```bash
echo 'G28 Z' | serial-echo-into /dev/ttyUSB0
```

## Listen to microphone for "go home" command, and issue that to the printer:
```bash
printer-voice-home
```


