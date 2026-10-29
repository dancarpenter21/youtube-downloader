# Youtube Download Script

Helper script to download Youtube videos. Requires Docker
and uses a standard Docker container.

```
./youtube-dl <link>
```

The container names the saved file.

For age-restricted videos, export YouTube cookies in Netscape format from an
account that can watch the video, following the
[yt-dlp instructions](https://github.com/yt-dlp/yt-dlp/wiki/Extractors#exporting-youtube-cookies).
Then run:

```sh
./youtube-dl --cookies /path/to/cookies.txt 'https://www.youtube.com/watch?v=36X1UnUFhIg'
```

You can also set `YTDLP_COOKIES=/path/to/cookies.txt`. The script gives the
container a temporary copy and removes it when finished. Keep the original
cookies file outside this repository; it contains login credentials.
