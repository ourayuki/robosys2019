# robosys2019 課題1
## 概要
### 使用部品

LED赤×１，LED黄×１,抵抗(330Ω)×２ RaspberryPi3B+ ×１
### 動作

2種類の点灯パターンから1つを選択し実行.
実行すると点灯は5回繰り返し終了.

- パターン1 : 交互に1秒ずつ点灯を5ループ
- パターン2 : 同時に1秒ずつ点灯を5ループ
## 使用方法
GPIOピン21と25にLEDと抵抗を接続
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
- echo 0 : パターン1
- echo l : パターン2
## デモ動画URL
https://www.youtube.com/watch?v=qcV_UHHnZg0&feature=youtu.be
