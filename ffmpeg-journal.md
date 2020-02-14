# My `ffmpeg` journal.
---
## The mission
* Show real examples of using ffmpeg over downloading/installing random programs out there to achieve same or less types of results.
* To take notes.

---
## My most frequent command entries and the scenarios they've been used

### Batch-convert files that match a file extension / format

#### Secondary objectives:
* Save them in a subfolder.
* Overwrite without asking.

```bash
for i in *.mkv;
  do name=`echo "$i" | cut -d'.' -f1`
  echo "$name"
  ffmpeg -i "$i" "converted/${name}.mp4" -y
done
```

#### Small details:
* The `-y` overrides overwriting prompts.

#### Reason:
* My phone can't play 1080p videos properly, so I downscale it to 720p.
* Most mobile video player apps don't support mkv (or either both the file/player aren't optimized enough).

#### Cons:
* Reduces quality, since it needs to be re-encoded for the scaling to apply.

#### Sources: 
> https://stackoverflow.com/questions/5784661/how-do-you-convert-an-entire-directory-with-ffmpeg
> https://stackoverflow.com/questions/39788972/ffmpeg-override-output-file-if-exists
  
##
