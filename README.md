# MacOS Finder Quick Actions Automator
🎰 MacOS Finder Quick Actions Automator


#### Where it lives: 

```bash

/Users/andrewlevin/Library/Services

```

- [FFPEG convert any audio to .m4a with bitrate ](#ffpeg-convert-any-audio-to-m4a-with-bitrate)
- [etc]()

### FFPEG convert any audio to .m4a with bitrate 

ffmpeg-m4a-bitrate48k.workflow

[quick-actions/ffmpeg-m4a-bitrate48k.workflow.zip](quick-actions/ffmpeg-m4a-bitrate48k.workflow.zip)

[quick-actions/ffmpeg-m4a-bitrate96k.workflow.zip](quick-actions/ffmpeg-m4a-bitrate96k.workflow.zip)


Code: 

```bash

#!/bin/bash

# Check if an argument is provided
if [ $# -eq 0 ]; then
    echo "Usage: $0 filename"
    exit 1
fi

bitrate="48k"

finput="$1"

# Remove the extension
fname="${finput%.*}"

/opt/homebrew/bin/ffmpeg -i "$finput" -c:a aac -b:a "$bitrate" "$fname".m4a

```

