# robosys2019 課題1
## 概要
### 使用部品

LED赤×１，LED黄×１,抵抗(330Ω)×２

### 動作

2種類の点灯パターンから1つを選択し実行.
実行すると点灯は5回繰り返し終了.

パターン1 : 交互に1秒ずつ点灯
パターン2 : 同時に1秒ずつ点灯
## 使用方法
~~~
git clone https://github.com/ourayuki/robosys2019.git
cd robosys2019
sudo make
sudo insmod myled.ko
sudo chmod 666 /dev/myled0
sudo echo 0 > /dev/myled0
sudo echo 1 > /dev/myled0
sudo rmmod myled
~~~
### コマンド
- echo 0 : 交互に１秒ずつ点灯を5ループ
- echo l : 両方が同時に1秒ずつ点灯を５ループ
## デモ動画URL
https://www.youtube.com/watch?v=qcV_UHHnZg0&feature=youtu.be
