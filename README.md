# majdata-charts

maimai 創作譜面

## ダウンロード方法 / Download Tutorial

赤丸で囲った部分をクリックするとダウンロードできます。/ Click on the area circled in red to download.

![image](https://user-images.githubusercontent.com/43089218/224856484-8e6b814a-c6a9-49d1-aec0-37a2a1f8bef9.png)


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
| [FREEDOM DiVE↓](freedom-dive/maidata.txt) | https://www.youtube.com/watch?v=vz7sJkJydQY | 692 |
