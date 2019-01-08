## HLS(HTTP Live Streaming)

hls.js demo

#### Getting started

Install ffmpeg with full options on OSX

```sh
$ brew install ffmpeg $(brew options ffmpeg | grep -vE '\s' | grep -- '--with-' | tr '\n' ' ')
```

Create the HLS media (segments and manifests)

```sh
ffmpeg -i ./oceans.mkv -profile:v baseline -level 3.0 -start_number 0 -hls_time 10 -hls_list_size 0 -f hls index.m3u8
```

start local web server

```sh
php -S localhost:3000
```

open http://localhost:3000/demo2.html


