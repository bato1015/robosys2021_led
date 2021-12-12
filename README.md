# Robotsystem2021_devicedriver
ロボットシステム学課題1提出用レポジトリです。
ロボットシステム学第7~8講で作成した<a href="https://github.com/ryuichiueda/robosys_device_drivers/blob/master/myled.c">デバイスドライバ</a>
に機能を追記し、作成しました。
***
## 機能
ヌメロンを作成しました。1~9の重複を含まない三桁がランダムに生成されます。入力された数字を<a href="http://pumpkin.cool-biz.net/Numer0n/futari_rule.html">ルール</a>に沿って判定し、EATは黄色、BITEは緑色が当たった回数分光ります。アイテムカードは実装していません。
***

## 動作環境
OS:ubuntu 20.04 sever
***

## 用意するもの
Raspberry Pi 4 ModelB

・ブレッドボード

・LED 黄　緑　各1個

・電子ブザー

・抵抗　330Ω 2個

・ジャンパー線 オス−メス 4本

・ジャンパー線 オス−オス 3本

***
## ピン配置
| 役割   | GPIO |
| ------ | ---- |
| EAT    | 19   |
| BIT    | 26   |
| ブザー | 25   |
| GND | 39   |
***

## 参考資料
<a href="https://mementoo.info/archives/746">【C言語/C++】配列をシャッフルしてランダムに入れ替える</a>

<a href="https://github.com/hiroki-0001/LED_device_driver/blob/master/led_control.c">コード上にsystem関数を入れる方法</a>
***
## 環境設定
```
git clone  git@github.com:bato1015/robosys2021_led.git
cd robosys2021_led/myled  
make 
./numeron.c
```
***
## 回路
### 回路写真
![iOS の画像](https://user-images.githubusercontent.com/70883743/145702406-2623b50e-9325-4354-bf59-5bf592327433.jpg)
### 回路図
Raspberry Pi 4の回路データがなかったため、Raspberry Pi 3で代用
![Untitled Sketch_回路図](https://user-images.githubusercontent.com/70883743/145714838-c7d1596f-1462-453d-913c-44175b84a1c5.png)



***
## ゲーム詳細
### 条件
・設定された数字と位置が同じであればEAT(黄色ランプ)
   
・ 設定された数字が入力と同じであればBITE(緑色ランプ)

・設定された数字が入力とすべて異なる場合にはブザー

### 例

設定された数字:234
```bash
入力:213
```
→1EAT 2BITE

## 遊び方色
1. 入力欄が出るので任意の数字をうち込む 。
2. 正解すると終了処理が開始される。
3. [hlp]と入力すると3桁目の数字が表示される。
4. [giv]と入力すると設定された3桁の数字が表示され、終了処理が開始される。
***
## 動画
<a href="https://www.youtube.com/watch?v=-Vimi_2r2gI">提出用ビデオ</a>
***
## ライセンス
<a href="https://github.com/bato1015/robosys2021_led/blob/main/LICENSE">GNU General Public License v3.0</a>

