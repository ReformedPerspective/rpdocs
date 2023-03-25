# Manna: Daily Scripture Meditations Podcast

## Introduction

The Manna Podcast (Manna: Daily Scripture Meditations) is a daily podcast published via a shell script with a systemd timer and is based on The Voice of the Church's weekly radio broadcasts, which were originally published on Sermon Audio.

The VOTC website and Sermon Audio presence have been taken down, and Reformed Perspective has been given permission to re-broadcast and re-use that content.

## Sermon Audio Data Processing

All of the Sermon Audio data is stored in our PCloud drive. It was ripped, along with all the associated meta-data (sermondata.xml [PowerShell CLIXML format]) from Sermon Audio using a PowerShell script.

The audio has been processed using a short introduction recorded by Maria? and a public domain recording of the 1st movement of Mozart's Clarinet Concerto in A to bracket the meditation with an intro. and outro.

```PowerShell
$ffmpegFilter = "[1]areverse[rev];[rev]silenceremove=start_periods=1:start_silence=0.2:start_threshold=-35dB[revtrim];[revtrim]areverse[trim];[trim]speechnorm[norm];[0][norm]acrossfade=d=12.000:curve1=nofade:curve2=nofade[intro];[intro][2]acrossfade=d=15.000:curve1=nofade:curve2=nofade"
ffmpeg -i PodcastIntro.mp3 -i "${beforeFile}" -i PodcastOutro.mp3 -filter_complex "$ffmpegFilter" "${afterFile}"
```

and tagged and a cover image added using the Python '[eyeD3](https://eyed3.readthedocs.io/en/latest/)' script.

```PowerShell
[string]$artist = $item.speaker
[string]$album = 'Manna Podcast'
[string]$title = $item.title
if($item.subtitle -ne '') {$title = "${title}: $($item.subtitle)"}
[string]$track = $item.rownum
[string]$total = 900
[string]$genre = 'Speech'
[datetime]$date = $item.date
[string]$relYear = $date.Year.ToString()
[string]$relDate = $date.ToString('yyyy-MM-dd')
[string]$publisher = 'Reformed Perspective'
[string]$cover = "./manna-cover.jpg"

eyeD3 --artist "${artist}" --album "${album}" --title "${title}" --track $track --track-total $total --genre "${genre}" --release-year $relYear --release-date "${relDate}" --publisher "${publisher}" --remove-all-images --add-image "${cover}:FRONT_COVER" "${afterFile}"
```

## Podbean Hosting

The Manna Podcast is published via Podbean using Podbean's REST API. There is a custom domain as well, so the Podbean page is at [https://www.mannapodcast.ca](https://www.mannapodcast.ca).
