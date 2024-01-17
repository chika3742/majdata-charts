# majdata-charts

maimai 創作譜面

## ダウンロード方法 / How to Download

以下のURLを書き換えるとダウンロードできます。

```
https://www.chikach.net/api/v2/dl-maidata?title=<directory name>
```

`<directory name>`の部分には、「freedom-dive」のようなディレクトリ名を入れてください。

## 利用条件 / Terms of Use

- 本リポジトリにはMITライセンスを付与しております。本リポジトリをフォークした上で自分好みに改変したり、AstroDX等でのプレイ動画を投稿したり、ご自由にお使いください。
- ただし、MajdataViewとAstroDXは実装が大きく異なり、一方で動作する譜面データが他方では動作しない場合があります。そのような場合の保障は致しかねます。
- 楽曲の配布は、著作権的に問題があるため行っておりません。ご自身でYouTube等から楽曲を入手した上でご利用ください。また、一部、楽曲の一部分をカットした上で作成した譜面があります。そのような譜面を再生する際の楽曲についても、ご自身でカット編集を行っていただきますようよろしくお願いします。
- 元の譜面を大きく改変しない限りは、譜面の改善PRを送って頂いても構いません。（だからといって何という訳ではありませんが）

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
| [スターダストメドレー](./stardust-medley/maidata.txt)                                                | https://youtu.be/trfjV9iIeJk | 1362       |
| [Third Time UNLucky](./third-time-unlucky/maidata.txt)                                     | https://youtu.be/2hQyktmzl5A | 0          |
| [人生](./jinsei/maidata.txt)                                                                 | https://youtu.be/wpVa0cnEeIw | 1297       |
| [ときめきポポロン♪](./tokimeki-poporon/maidata.txt)                                                | https://youtu.be/49vjbjdZaOY | 2893       |
| [\[宴\] 天空カフェテリア](./tenkuucafeteria/maidata.txt)                                            | https://youtu.be/mP6PUA0e3oU | 1228       |
| [INTERNET YAMERO (Another cut)](./internet-yamero-another-cut/maidata.txt)                 | https://youtu.be/Js_-gKm1RYI | ?*         |
| [カフェインファイター](./caffeine-fighter/maidata.txt)                                               | https://youtu.be/AnhVis5JcFQ | ?*         |
| [ULTRA SYNERGY MATRIX](./ultra-synergy-matrix/maidata.txt)                                 | https://youtu.be/MwXdvTf64Is | 1500       |
| [New York Back Raise](./new-york-back-raise/maidata.txt)                                   | https://youtu.be/sCxdDPO4zB0 | ?          |
| [よいまちカンターレ](./yoimachi-cantare/maidata.txt)                                                | https://youtu.be/vTDSUOlLhwg | 764*       |
| [μ3](./mu-3/maidata.txt)                                                                   | https://youtu.be/cG3MradaVF0 | ?          |
| [ばんきちゃんは力を開放したくて仕方がない](./banki-chan-ha-chikara-wo-kaihou-sitakute-sikataganai/maidata.txt) | https://youtu.be/qoIy7DkOhdQ | 722*       |
| [宵加減テトラゴン](./yoikagen-tetragon/maidata.txt)                                                | https://youtu.be/oL2gDDjkCb4 | ?*         |
| [ネ土会ェ貝南犬☆カゞんIよ″るノDA!!｡](./shakai-kouken-ganbaru-noda/maidata.txt)                          | https://youtu.be/Or5lCqWyYE8 | ?*         |
| [Abstruse Dilemma](./abstruse-dilemma/maidata.txt)                                         | https://youtu.be/nnpyIv4wGeQ | 1352       |
| [snooze](./snooze/maidata.txt)                                                             | https://youtu.be/_gWn38pnmqI | 1180*      |
| [アンコール](./encore/maidata.txt)                                                              | https://youtu.be/vcGbefQBvJ4 | ?*         |
| [ももいろの鍵](./the-peachy-key/maidata.txt)                                                     | https://youtu.be/sAUdWpemfGw | -15* **    |
| [セカイがカフェになっちゃった!](./the-world-became-a-cafe/maidata.txt)                                   | https://youtu.be/XNpX6adQVmY | 176*       |
| [勇者](./yuusha/maidata.txt)                                                                 | https://youtu.be/OIBODIPC_8Y | 1628*      |
| [Stellar:Dream](./stellar-dream/maidata.txt)                                               | https://youtu.be/dt3p2HtLzDA | 1720       |
| [チェスマッチカフェチェックオレ](./chess-match-cafe-check-au-lait/maidata.txt)                            | https://youtu.be/OPIso_I33a4 | 1664*      |

\* 独自にカット編集した音源を使用しています。カット編集は各自で行っていただきますようお願いします。

\*\* ディレイ値がマイナスとなっているものについては、その分だけ音源の先頭をカットする必要があります。

※「?」となっているものは、計算したディレイが不明になってしまったものです。
