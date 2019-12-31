# robosys_2019
ledを点滅させるデバイスドライバ
# デモ
https://youtu.be/iwKFRmwze-4
# 説明
RaspberryPi3 Model B+のGPIO25(22番ピン)に接続したledを点滅させるデバイスドライバ
ONしたときは数回点滅する
使用機材は以下の通り
- RaspberryPi3 Model B+
  - Raspbian
- 150Ω抵抗
- 緑色LED
- ブレッドボード
- ジャンパー線
# インストール
$ git clone https://github.com/red-ksingyuunyuu/robosys_2019.git
# 使用方法
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
$ echo '1' > /dev/myled0 # LED_ON
$ echo '0' > /dev/myled0 # LED_OFF
