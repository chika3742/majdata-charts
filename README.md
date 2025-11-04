# majdata-charts

maimai 創作譜面

## ダウンロード方法 / How to Download

以下のURLを書き換えるとダウンロードできます。

```
https://www.chikach.net/api/v2/dl-maidata?title=<directory name>
```

`<directory name>`の部分には、譜面ファイルが保存されているフォルダー名（例: `freedom-dive`）を入れてください。

詳しくは[Wiki](https://github.com/chika3742/majdata-charts/wiki/%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89%E6%96%B9%E6%B3%95)をご参照ください。

## AstroDXへのインポート方法

詳しくは[Wiki](https://github.com/chika3742/majdata-charts/wiki/AstroDXへのインポート方法)をご参照ください。

## 利用条件 / Terms of Use

- 本リポジトリにはMITライセンスを付与しております。自分好みに改変したり、AstroDX等でのプレイ動画を投稿したり、ご自由にお使いください。
- ただし、MajdataViewとAstroDXは実装が大きく異なり、一方で動作する譜面データが他方では動作しない場合があります。もしAstroDXで動作しない譜面があれば、Issueを立てるか修正PRを送って頂けるとありがたいです。
- 楽曲の配布は、著作権的問題が明らかなため行っておりません。ご自身でYouTube等から楽曲を入手した上でご利用ください。また、一部、楽曲の一部分をカットした上で作成した譜面があります。そのような譜面の楽曲についても、ご自身でカット編集を行っていただきますようよろしくお願いします。

## ffmpegコマンドライン

音源・背景動画の作成にいつも利用しているコマンドラインです。

### 音源の作成

※`.\original.mp4`、`<delay>`、`track.mp3`はそれぞれ、元動画パス、ディレイ値、出力音源パスに置き換えてください。

```
ffmpeg -i .\original.mp4 -ar 44100 -af adelay=<delay>ms:all=1 track.mp3
```

### 背景動画の作成

※`.\original.mp4`、`<delay>`、`bg.mp4`はそれぞれ、元動画パス、ディレイ値、出力背景動画パスに置き換えてください。

```
ffmpeg -i .\original.mp4 -c:v h264 -an -filter_complex "[0]tpad=start_duration=<delay>ms:start_mode=add:color=black" bg.mp4
```

## 音源詳細

ここに記載のディレイを音源の先頭に加えると、MajdataViewで再生した際にオフセットと一致するようになっています。(録画モード時のクロック音の関係上)

| タイトル                                                                                       | 音源URL                            | 音源ディレイ(ms) |
|:-------------------------------------------------------------------------------------------|----------------------------------|------------|
| [トンデモワンダーズ](tondemo-wonders/maidata.txt)                                                   | https://youtu.be/dBQg24mx45Y     | 2400*      |
| [FREEDOM DiVE](freedom-dive/maidata.txt)                                                   | https://youtu.be/vz7sJkJydQY     | 692        |
| [Viyella's Tears](viyellas-tears/maidata.txt)                                              | https://youtu.be/Pm9oqTzsCqk     | 2162       |
| [風花の招待](invitation-of-windblume/maidata.txt)                                               | https://youtu.be/MYqsfjhj3c4     | 2087       |
| [純白での瞑想](contemplation-in-snow/maidata.txt)                                                | https://youtu.be/BhDT66CcTco     | -*         |
| [FLUFFY FLASH](fluffy-flash/maidata.txt)                                                   | https://youtu.be/-gl7sZFr9gs     | 905        |
| [INTERNET YAMERO](internet-yamero/maidata.txt)                                             | https://youtu.be/Js_-gKm1RYI     | -*         |
| [Recollect Lines](recollect-lines/maidata.txt)                                             | -                                | -          |
| [天空カフェテリア ～Re arranged～](tenkucafeteria-re-arranged/maidata.txt)                           | https://youtu.be/h4DpKHlO__c     | 1180*      |
| [なかよし!〇!なかよし!](./nakayoshi-maru-nakayoshi/maidata.txt)                                     | https://youtu.be/ogj7RZNCOFw     | 2551*      |
| [POTENTIAL](./potential/maidata.txt)                                                       | https://youtu.be/n8QFVPxm3zg     | 1990       |
| [Galaxy Blaster](./galaxy-blaster/maidata.txt)                                             | https://youtu.be/t-VWXPD2jfI     | 1887       |
| [アイドル](./idol/maidata.txt)                                                                 | https://youtu.be/ZRtdQ81jPUQ     | 2492*      |
| [スターダストメドレー](./stardust-medley/maidata.txt)                                                | https://youtu.be/trfjV9iIeJk     | 1362       |
| [Third Time UNLucky](./third-time-unlucky/maidata.txt)                                     | https://youtu.be/2hQyktmzl5A     | 0          |
| [人生](./jinsei/maidata.txt)                                                                 | https://youtu.be/wpVa0cnEeIw     | 1297       |
| [ときめきポポロン♪](./tokimeki-poporon/maidata.txt)                                                | https://youtu.be/49vjbjdZaOY     | 2893       |
| [\[宴\] 天空カフェテリア](./tenkuucafeteria/maidata.txt)                                            | https://youtu.be/mP6PUA0e3oU     | 1228       |
| [INTERNET YAMERO (Another cut)](./internet-yamero-another-cut/maidata.txt)                 | https://youtu.be/Js_-gKm1RYI     | ?*         |
| [カフェインファイター](./caffeine-fighter/maidata.txt)                                               | https://youtu.be/AnhVis5JcFQ     | ?*         |
| [ULTRA SYNERGY MATRIX](./ultra-synergy-matrix/maidata.txt)                                 | https://youtu.be/MwXdvTf64Is     | 1500       |
| [New York Back Raise](./new-york-back-raise/maidata.txt)                                   | https://youtu.be/sCxdDPO4zB0     | ?          |
| [よいまちカンターレ](./yoimachi-cantare/maidata.txt)                                                | https://youtu.be/vTDSUOlLhwg     | 764*       |
| [μ3](./mu-3/maidata.txt)                                                                   | https://youtu.be/cG3MradaVF0     | ?          |
| [ばんきちゃんは力を開放したくて仕方がない](./banki-chan-ha-chikara-wo-kaihou-sitakute-sikataganai/maidata.txt) | https://youtu.be/qoIy7DkOhdQ     | 722*       |
| [宵加減テトラゴン](./yoikagen-tetragon/maidata.txt)                                                | https://youtu.be/oL2gDDjkCb4     | ?*         |
| [ネ土会ェ貝南犬☆カゞんIよ″るノDA!!｡](./shakai-kouken-ganbaru-noda/maidata.txt)                          | https://youtu.be/Or5lCqWyYE8     | ?*         |
| [Abstruse Dilemma](./abstruse-dilemma/maidata.txt)                                         | https://youtu.be/nnpyIv4wGeQ     | 1352       |
| [snooze](./snooze/maidata.txt)                                                             | https://youtu.be/_gWn38pnmqI     | 1180*      |
| [アンコール](./encore/maidata.txt)                                                              | https://youtu.be/vcGbefQBvJ4     | ?*         |
| [ももいろの鍵](./the-peachy-key/maidata.txt)                                                     | https://youtu.be/sAUdWpemfGw     | -15* **    |
| [セカイがカフェになっちゃった!](./the-world-became-a-cafe/maidata.txt)                                   | https://youtu.be/XNpX6adQVmY     | 176*       |
| [勇者](./yuusha/maidata.txt)                                                                 | https://youtu.be/OIBODIPC_8Y     | 1628*      |
| [Stellar:Dream](./stellar-dream/maidata.txt)                                               | https://youtu.be/dt3p2HtLzDA     | 1720       |
| [チェスマッチカフェチェックオレ](./chess-match-cafe-check-au-lait/maidata.txt)                            | https://youtu.be/OPIso_I33a4     | 1664*      |
| [ライアーダンサー](./lier-dancer/maidata.txt)                                                      | https://youtu.be/UHbmkxv-874     | ?*         |
| [人マニア](./human-mania/maidata.txt)                                                          | https://youtu.be/HTxwOxFt5d4     | -830**     |
| [ne! ne! ne!](./ne-ne-ne/maidata.txt)                                                      | https://youtu.be/ohGzCZ5G3sk     | 2724       |
| [And Revive The Melody](./and-revive-the-melody/maidata.txt)                               | https://youtu.be/YPSJ-wnxnRI     | -50**      |
| [GAME：CHANGER](./game-changer/maidata.txt)                                                 | https://youtu.be/hPKs7vL-Xf4     | 1591       |
| [\[疑\] Mistempered Malignance](./mistempered-malignance-utage/maidata.txt)                 | - (公式音源なし)                       | ?          |
| [レイドバックジャーニー](./laid-back-journey/maidata.txt)                                             | https://youtu.be/eMgHOf0rpBQ     | 1387       |
| [オーバーライド](./override/maidata.txt)                                                          | https://youtu.be/LLjfal8jCYI     | 826        |
| [IF:U](./if-u/maidata.txt)                                                                 | https://youtu.be/Z1GjdDcwtyc     | 0          |
| [青春のアーカイブ](./archive-of-youth/maidata.txt)                                                 | https://youtu.be/Q4sWF6z9TuE     | 1274       |
| [Glorious Crown (tpz over-Over-OVERCUTE REMIX)](./glorious-crown-tpzrmx/maidata.txt)       | https://youtu.be/HJglGbM0hds     | ?          |
| [Möbius](./möbius/maidata.txt)                                                             | https://youtu.be/2fsZdfixj60     | ?          |
| [しとしとと](./sitositoto/maidata.txt)                                                          | https://youtu.be/QL7Drg1NPQc     | ?          |
| [メズマライザー](./mesmerizer/maidata.txt)                                                        | https://youtu.be/19y8YTbvri8     | -53**      |
| [シリウスの輝きのように](./as-the-shine-of-sirius/maidata.txt)                                        | https://youtu.be/LMFLssXrPX4     | -1501**    |                                                                                           |                              |            |
| [ファタール](./fatal/maidata.txt)                                                               | https://youtu.be/8tQiWHXSGN0     | 2737*      |
| [Baqeela](./baqeela/maidata.txt)                                                           | https://youtu.be/ggllDGhEuxQ *** | 1446       |
| [1番輝く星](./the-brightest-star/maidata.txt)                                                  | https://youtu.be/WMdXTiLrT2g     | 1428       |
| [MarbleBlue.](./marbleblue/maidata.txt)                                                    | https://youtu.be/Qb1vJnLrA3I     | ?          |
| [\[弧\]OMAKENO Stroke](./omakeno-stroke/maidata.txt)                                        | https://youtu.be/4xnZHzcJ-j4 *** | ?          |
| [I Wanna](./i-wanna/maidata.txt)                                                           | https://youtu.be/e_N_24PrPTU     | 340*       |
| [Synthesis.](./synthesis/maidata.txt)                                                      | https://youtu.be/dOP7G5J755s     | -*         |
| [ラブリージャッジメント](./lovely-judgement/maidata.txt)                                              | https://youtu.be/dfVsdGV4ePc     | 1207       |
| [テレパシ](./telepathy/maidata.txt)                                                            | https://youtu.be/AVIo9K-DrcY     | 1581       |
| [DIE IN](./die-in/maidata.txt)                                                             | https://youtu.be/FF-tQalIIUM     | 2353       |
| [Fighting My Way](./fighting-my-way/maidata.txt)                                           | ゲーム内音源                           | -          |
| [メクルメ](./mekurume/maidata.txt)                                                             | https://youtu.be/DLkNQgh4Ons     | 2970       |
| [ツキノカメ](./moon-turtle/maidata.txt)                                                         | ゲーム内音源                           | -          |
| [夢紡ぎのワンダラー](./夢紡ぎのワンダラー/maidata.txt)                                                       | https://youtu.be/sZVeGywmCu0     | 1156       |
| [Booo!](./booo/maidata.txt)                                                                | https://youtu.be/PcoWIZVaBNc     | 1082       |
| [スーパー類](./super-rui/maidata.txt)                                                           | https://youtu.be/owAteX-4kcw     | 1200       |
| [自己肯定感爆上げ↑↑しゅきしゅきソング](./self-affirmation-explosion-love-love-song/maidata.txt)             | https://youtu.be/WCDLyXJgbIo     | 923        |
| [プラシイボ♥バトラー](./placebo-battler/maidata.txt)                                                | https://youtu.be/f1x4WIP-9qg     | 858        |
| [Haunted Dance](./haunted-dance/maidata.txt)                                               | https://youtu.be/iwvi6gHm73k *** | ?          |

\* 独自にカット編集した音源を使用しています。カット編集は各自で行っていただきますようお願いします。

\*\* ディレイ値がマイナスとなっているものについては、その分だけ音源の先頭をカットする必要があります(FFmpegでは`-ss`オプションを用いてカットできます)。

\*\*\* 非公式音源です。

※「?」となっているものは、計算したディレイが不明になってしまったものです。大方音源を作成してから長期間放置していたものです。
