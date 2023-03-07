# majdata-charts

maimai 創作譜面

## ffmpegコマンドライン

### 音源の作成

```
ffmpeg -i .\original.mp4 -ar 44100 -af adelay=<delay>ms:all=1 track.mp3
```

### 背景動画の作成

```
ffmpeg -i .\original.mp4 -vcodec hevc_nvenc -b_ref_mode 0 -an -filter_complex "[0]tpad=start_duration=<delay>ms:start_mode=add:color=black" bg.mp4
```

## 音源詳細

ここに記載のディレイを音源の先頭に加えると、MajdataViewで再生した際にオフセットと会うようになっています。(録画モード時のクロック音の関係上)

| タイトル | 音源URL | 音源ディレイ(ms) |
| --- | --- | --- |
| [トンデモワンダーズ](tondemo-wonders/maidata.txt) | https://www.youtube.com/watch?v=dBQg24mx45Y | 2400 |
