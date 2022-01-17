# General
{{info}}
Duplicator d12 230
Using CURA 4.12

# Info
{{warning}}
Build volume: 230 x 230 x 250 mm
Feeder system: Bowden
Nozzle size: 0.4 mm
Max. hot end temperature: 260 ℃
Max. heated bed temperature: 105 ℃
Print bed material: Removable Magnetic
Frame: Aluminum
Bed leveling: Manual
Connectivity: WiFi, micro-SD card
Print recovery: Yes
Filament sensor: Yes
Camera: No
Filament: 1.75

# Usage
```sh
cd ~/.local/share
rm -rf cura
git clone https://github.com/Atelier-Epita/cura
cd
mkdir Application
curl https://github.com/Ultimaker/Cura/releases/download/4.12.0/Ultimaker_Cura-4.12.0.AppImage
chmod +x Ultimaker_Cura-4.12.0.AppImage
```
Get a file from thingiverse in `.stl`
Start the Ultimaker_Cura application
Slice the file in Cura
Mount the usb

<details><summary>Example to mount (click me)</summary>
Get the device
```sh
sudo fdisk -l
```
Let's imagine the device is `/dev/sda1`
Mount it
```sh
sudo mount /dev/sda1 /mnt
```
Copy the file
```sh
sudo cp my/path/to/gcode/example.gcode /mnt
```
Unmount
```sh
sudo fusermount -u -z /mnt
```
</details>
Start the printer
Plug the micro-sd
Impression>example.gcode
**Done !**
