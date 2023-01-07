[![test](https://github.com/TakumiIshiguro/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/TakumiIshiguro/mypkg/actions/workflows/test.yml)

# mypkg

千葉工業大学未来ロボティクス学科のロボットシステム学の講義で作成したレポジトリである。  
このレポジトリではros2を用いて、talekerとlistenerという名前のノードが通信するのを確認することができる。



## 機能


### ノード

### 1. talker

* 機能

実行すると0.5秒おきにメッセージを送信する。メッセージは自然数で、１ずつ増えていく。

* 使い方

```
$ ros2 run mypkg talker
```

### 2. listener

* 機能

talkerからのメッセージを受けとり表示する。talkerが実行されてない場合は何も表示しない。

* 使い方

```
$ ros2 run mypkg listner
```

* 実行結果

```
端末1$ ros2 run mypkg talker
端末2$ ros2 run mypkg listener

[INFO] [1672985676.048424444] [listener]: Listen: 36
[INFO] [1672985676.537401934] [listener]: Listen: 37
[INFO] [1672985677.036784671] [listener]: Listen: 38
[INFO] [1672985677.536960527] [listener]: Listen: 39
```

### ローンチ

talkerとlistnerを同時に実行することができる。

* 使い方

```
$ ros2 launch mypkg talk_listen.launch.py
```

* 実行結果

```
[INFO] [launch]: All log files can be found below /home/takum/.ros/log/2023-01-06-15-31-02-339914-DESKTOP-1F0ITBS-695
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [696]
[INFO] [listener-2]: process started with pid [698]
[listener-2] [INFO] [1672986663.202251355] [listener]: Listen: 0
[listener-2] [INFO] [1672986663.693480379] [listener]: Listen: 1
[listener-2] [INFO] [1672986664.193363459] [listener]: Listen: 2
[listener-2] [INFO] [1672986664.693530459] [listener]: Listen: 3
```


## テスト環境

* Ubuntu 22.04.1 LTS
* ROS2 Humble



## インストール方法

ros2をダウンロードした環境で以下のコマンドを実行

```
$ git clone https://github.com/TakumiIshiguro/mypkg.git
```



## ライセンス

このソフトウェアパッケージは3条項BSDのライセンスの下、再頒布および使用が使用が許可されます。  
© 2022 Takumi Ishiguro
