# Devicedriver_for_led
2021年度ロボットシステム学の課題1で作成したデバイスドライバです。  
入力した数値に応じてLEDが点灯、消灯します。  
レースでみられるスタートシグナルを模した動作を行います。

# 動作環境
・ Computer : Raspberry Pi 4 Computer Model B  
・ OS : ubuntu 20.04 server  

# 使用した部品
・ Raspberry Pi 4 Computer Model B  
・ 赤色LED x 3  
・ 緑色LED x 1  
・ 抵抗220Ω x 4  
・ ブレッドボード　  
・ ジャンパ線(オス-メス) x 6  
・ ジャンパ戦(オス-オス) x 4

# 回路  
gpio pin 配置  
> 引用 
DATASHEET Raspberry Pi 4 Model B
![スクリーンショット (101)](https://user-images.githubusercontent.com/92065217/145947513-d1888780-0faf-410d-aac0-9f29a3e14071.png)  
  
回路の写真  
![回路の写真](https://user-images.githubusercontent.com/92065217/145945369-ef5bb0d3-c6ed-435c-aaad-389330ddf34d.jpg)
画像ではGND(14番ピン, 39番ピン)が２つ接続されていますが、これは私が使用したブレッドボードの仕様で、4枚のブレッドボードを１つに組み合わせたボードを使用しているため両端にGNDを接続しています。  
通常のブレッドボードを使用される場合はGNDを１つ接続すれば問題ありません。

# 使用方法
(インストール)  
以下コマンドを実行してください.  

  
  $ git clone https://github.com/Masanori-Suzu1024/Devicedriver_for_led.git  
  $ cd Devicedriver_for_led  
  $ make  
  $ sudo insmod myled.ko  
  $ sudo chmod 666 /dev/myled0  
  
(アンインストール)  
以下コマンドを実行してください。  
  
  $ sudo rmmod myled  
  $ make clean
    
### すべてのledを消灯させる  
  
  $ echo 0 > /dev/myled0
  
### led1を点灯させる   
  
  $ echo 1 > /dev/myled0
  
### led2を点灯させる 
  
  $ echo 2 > /dev/myled0
  
### led3を点灯させる 
  
  $ echo 3 > /dev/myled0
  
### led4を点灯させる 
  
  $ echo 4 > /dev/myled0
  
### スタートシグナルの動作を行う 
  
  $ echo 5 > /dev/myled0
  
# 動作の動画  
https://youtu.be/klIfrCBkLFM

# ライセンス  
GNU General Public License v2.0

