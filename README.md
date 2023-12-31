## レポジトリについて
![test](https://github.com/suudoohmahiro/ros2/actions/workflows/test.yml/badge.svg)
* ロボットシステム学のros2の練習レポジトリ

## ダウンロード方法
* ターミナルで以下を実行
```
$ git clone https://github.com/suudoohmahiro/ros2
```

## 概要
* talkerというノードでパブリッシュしてlistenerというノードでサブスクライブしている.
* メッセージの型は16ビット符号つき整数 
#### talker.py
* countupというトピックを通じてメッセージを送信する
#### listener.py 
* countupというトピックを通じてメッセージを受け取る
#### talk_listen.launch.py
* 上記2つのノードを一度に立ち上げることが出来る

## 実行方法
### talker.py & listener.py
1. ターミナル上で以下を実行
```
$ ros2 run mypkg talker
```
2. 他のターミナルを立ち上げる
3. ターミナルで以下を実行
```
$ ros2 run mypkg listener
```
4. ``` Ctrl + c ``` で終了

***
### talk_listen.launch.py
1. ターミナルで以下を実行
```
$ ros2 launch mypkg talk_listen.launch.py
```
2. ``` Ctrl + c ```で終了


## 実行結果
### talker.py & listener.py
* 以下のように出力される
```
1. ターミナル上で以下を実行
[INFO] [1703996405.851544662] [listener]: Listen: 11
[INFO] [1703996406.343763013] [listener]: Listen: 12
[INFO] [1703996406.844056282] [listener]: Listen: 13
[INFO] [1703996407.343960938] [listener]: Listen: 14
[INFO] [1703996407.843923728] [listener]: Listen: 15
[INFO] [1703996408.343911225] [listener]: Listen: 16
[INFO] [1703996408.843936536] [listener]: Listen: 17
[INFO] [1703996409.343826739] [listener]: Listen: 18
[INFO] [1703996409.844303510] [listener]: Listen: 19
[INFO] [1703996410.344059873] [listener]: Listen: 20
[INFO] [1703996410.842737783] [listener]: Listen: 21
[INFO] [1703996411.343298745] [listener]: Listen: 22
[INFO] [1703996411.842442363] [listener]: Listen: 23
[INFO] [1703996412.343708412] [listener]: Listen: 24
[INFO] [1703996412.843639754] [listener]: Listen: 25
```
***
### talk_listen.launch.py
* 以下のように出力される
```
[listener-2] [INFO] [1703997617.804226043] [listener]: Listen: 0
[listener-2] [INFO] [1703997618.296265194] [listener]: Listen: 1
[listener-2] [INFO] [1703997618.795788629] [listener]: Listen: 2
[listener-2] [INFO] [1703997619.296747493] [listener]: Listen: 3
[listener-2] [INFO] [1703997619.796728751] [listener]: Listen: 4
[listener-2] [INFO] [1703997620.296696896] [listener]: Listen: 5
[listener-2] [INFO] [1703997620.796857864] [listener]: Listen: 6
[listener-2] [INFO] [1703997621.295603097] [listener]: Listen: 7
[listener-2] [INFO] [1703997621.795624590] [listener]: Listen: 8
[listener-2] [INFO] [1703997622.296458339] [listener]: Listen: 9
[listener-2] [INFO] [1703997622.796840197] [listener]: Listen: 10
```

## テスト環境
* Ubuntu 22.04 LTS
* ROS2 Humble

## Author
* Mahiro Sudoh
* Chiba Institute of Technology
* E-mail s22c1073xq@s.chibakoudai.jp

## LICENSE・著作権
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．

* このソフトウェアパッケージに関するコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
	* [https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)

© 2023 Mahiro Sudoh
