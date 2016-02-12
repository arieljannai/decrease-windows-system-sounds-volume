# Windows 10 sounds decrease volume
Decrease the volume of the sounds in windows 10.<BR>
They're strong, annoying and are never in harmony with other sounds or music.
<BR>

I didn't want to disable them completely and couldn't find a built-in way to adjust only their volume without harming other things.

## What to do
### Install and configure [audacity](http://www.audacityteam.org/) to batch manipulate all the audio files.
* Install
  * Install from their [download page](http://www.audacityteam.org/download/)
  * Install with choco: [`cinst -y audacity`](https://chocolatey.org/packages/audacity)
* Configure
  * copy [decrease-volume.txt](decrease-volume.txt) to the installation folder under the `Chains` directory - `C:\Users\%USERNAME%\AppData\Roaming\Audacity\Chains\decrease-volume.txt`

### Backup
Copy and backup the folder `C:\Windows\Media` to `C:\Windows\Media.bak` or something like that. Make it that way that the original folder is the backup - `bak`, and the one you copy will be the actual `Media`. That way the `Media` folder still has the same permissions and we don't ruin it

### Do it!
* Open audacity
* File -> Apply Chain -> select `decrease-volume` -> Apply to Files :s
* Select all the files in `Media` folder
* When the process finishes, all the files will be in a new folder named `cleaned`
* Copy all the files to `Media` and replace them (don't worry, remember we have the original as a backup in `Media.bak`!)
* Now it's quieter, enjoy :sunglasses:

## Customization
You can chose in how much to decrease the volume by changing the level (dB) in [decrease-volume.txt](decrease-volume.txt)

### Rollback
Just go back to your original `Media` folder!
