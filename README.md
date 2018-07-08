# timeaudio
raspberry pi half and hour play corresponding time voice file

# script code

```bash
#!/bin/bash

filePath=/home/pi/timeaudio
#time=`date | awk -F \  {'print $4'} | awk -F : {'print $1'}`
time=`date +%H%M`
audioFile="$filePath/$time.mp3"
echo $audioFile
player=/usr/bin/mplayer

$player $audioFile
#$player >> /tmp/1.log
#echo $audioFile >> /tmp/1.log
```
