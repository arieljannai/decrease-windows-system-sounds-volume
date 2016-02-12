# Windows 10 sounds decrease volume
Decrease the volume of the sounds in windows 10.<BR>
They're strong, annoying and are never in harmony with other sounds or music.
<BR>

I didn't want to disable them completely and couldn't find a built-in way to adjust only their volume without harming other things.

## Examples:
You can here the original or the lowered one to see the difference:
 1. [Origianl](https://clyp.it/yuccfowh) or [Lower](https://clyp.it/gifemwj2)
 2. [Origianl](https://clyp.it/kuabr1du) or [Lower](https://clyp.it/blgkxcrj)

## What to do
### Download a ready archive
Download an [archive (~6mb)](http://www.filedropper.com/media_6) with my `Media` folder which is already decreased (and then jump to the backup section)


OR


### Install and configure [audacity](http://www.audacityteam.org/) to batch manipulate all the audio files.
* Install
  * Install from their [download page](http://www.audacityteam.org/download/)
  * Install with choco: [`cinst -y audacity`](https://chocolatey.org/packages/audacity)
* Configure
  * copy [decrease-volume.txt](decrease-volume.txt) to the installation folder under the `Chains` directory - `C:\Users\%USERNAME%\AppData\Roaming\Audacity\Chains\decrease-volume.txt`

### Backup
Copy and backup the folder `C:\Windows\Media` to `C:\Windows\Media.bak` or something like that. Do it in a way that the original folder is the backup - `bak`, and the one you copy will be the actual `Media`. That way the `Media.bak` folder will keep the permissions and we won't ruin it

### Do it!
* Open audacity
* File -> Apply Chain -> select `decrease-volume` -> Apply to Files :s
* Select all the files in `Media` folder
* When the process finishes, all the files will be in a new folder named `cleaned`
* Copy all the files to `Media` and replace them (don't worry, remember we have the original as a backup in `Media.bak`!)
* Now it's quieter, enjoy :sunglasses:

## Customization
You can chose in how much to decrease the volume by changing the level (dB) in [decrease-volume.txt](decrease-volume.txt)

### Restore
Just go back to your original `Media` folder!
