# majdata-charts

maimai 創作譜面

## ダウンロード方法 / How to Download

以下のURLを書き換えるとダウンロードできます。

```
https://www.chikach.net/api/v2/dl-maidata?title=<directory name>
```

`<directory name>`の部分には、「freedom-dive」のようなディレクトリ名を入れてください。

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

ここに記載のディレイを音源の先頭に加えると、MajdataViewで再生した際にオフセットと一致するようになっています。(録画モード時のクロック音の関係上)

| タイトル                                                                                       | 音源URL                        | 音源ディレイ(ms) |
|:-------------------------------------------------------------------------------------------|------------------------------|------------|
| [トンデモワンダーズ](tondemo-wonders/maidata.txt)                                                   | https://youtu.be/dBQg24mx45Y | 2400*      |
| [FREEDOM DiVE](freedom-dive/maidata.txt)                                                   | https://youtu.be/vz7sJkJydQY | 692        |
| [Viyella's Tears](viyellas-tears/maidata.txt)                                              | https://youtu.be/Pm9oqTzsCqk | 2162       |
| [風花の招待](invitation-of-windblume/maidata.txt)                                               | https://youtu.be/MYqsfjhj3c4 | 2087       |
| [純白での瞑想](contemplation-in-snow/maidata.txt)                                                | https://youtu.be/BhDT66CcTco | -*         |
| [FLUFFY FLASH](fluffy-flash/maidata.txt)                                                   | https://youtu.be/-gl7sZFr9gs | 905        |
| [INTERNET YAMERO](internet-yamero/maidata.txt)                                             | https://youtu.be/Js_-gKm1RYI | -*         |
| [Recollect Lines](recollect-lines/maidata.txt)                                             | -                            | -          |
| [天空カフェテリア ～Re arranged～](tenkucafeteria-re-arranged/maidata.txt)                           | https://youtu.be/h4DpKHlO__c | 1180*      |
| [なかよし!〇!なかよし!](./nakayoshi-maru-nakayoshi/maidata.txt)                                     | https://youtu.be/ogj7RZNCOFw | 2551*      |
| [POTENTIAL](./potential/maidata.txt)                                                       | https://youtu.be/n8QFVPxm3zg | 1990       |
| [Galaxy Blaster](./galaxy-blaster/maidata.txt)                                             | https://youtu.be/t-VWXPD2jfI | 1887       |
| [アイドル](./idol/maidata.txt)                                                                 | https://youtu.be/ZRtdQ81jPUQ | 2492*      |
| [スターダストメドレー](./stardust-medley/maidata.txt)                                                | https://youtu.be/trfjV9iIeJk | 2774       |
| [Third Time UNLucky](./third-time-unlucky/maidata.txt)                                     | https://youtu.be/2hQyktmzl5A | 0          |
| [人生](./jinsei/maidata.txt)                                                                 | https://youtu.be/wpVa0cnEeIw | 1297       |
| [ときめきポポロン♪](./tokimeki-poporon/maidata.txt)                                                | https://youtu.be/49vjbjdZaOY | 2893       |
| [\[宴\] 天空カフェテリア](./tenkuucafeteria/maidata.txt)                                            | https://youtu.be/mP6PUA0e3oU | 1228       |
| [INTERNET YAMERO (Another cut)](./internet-yamero-another-cut/maidata.txt)                 | https://youtu.be/Js_-gKm1RYI | ?*         |

\* 独自にカット編集した音源を使用しています。カット編集は各自で行っていただきますようお願いします。
「?」となっているものは、計算したディレイが不明になってしまったものです。
