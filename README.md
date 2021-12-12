# Devicedriver_for_led
2021年度ロボットシステム学の課題1で作成したデバイスドライバです。  
入力した数値に応じてLEDが点灯、消灯します。

# 動作環境
・ Raspberry Pi 4 Computer Model B  
・ OS:ubuntu 20.04 server  

# 使用した部品
・ Raspberry Pi 4 Computer Model B  
・ LED x 3  
・ 抵抗200Ω x 3  
・ ブレッドボード  
・ ジャンパ線(オス-メス) x 4  
・ ジャンパ戦(オス-オス) x 3

# 回路


# 使用方法
(インストール)  
以下コマンドを実行してください.  

  
  $ git clone   
  $ cd Devicedriver_for_led  
  $ make  
  $ sudo insmod myled.ko  
  $ sudo chmod 666 /dev/myled0  
  
(アンインストール)  
以下コマンドを実行してください。  
  
  $ sudo rmmod myled  
  $ make clean
    

# 

#
