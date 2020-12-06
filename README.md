# myled
ロボットシステム学の課題で作成したデバイスドライバです

________________________________

### 内容について

これは、ロボットシステム学の講義で作成したデバイスドライバを一部改変したものです。
echoでアルファベット1文字を入力すると、LEDの点滅の長さで欧文モールス符号を表現し、あらかじめ決められた単語をローマ字または英語で作り出すようにしました。  
今回はs,m,cの3つを用意しており、それぞれ入力すると次のようになります。  
s　⇒　s, a, n, n, m, i, t, s, u　＝　sannmitsu (三密)  
m　⇒　m, e, r, r, y, c, h, r, i, s, t, m, a, s　＝　merrychristmas (メリークリスマス)  
c　⇒　c, o, r, o, n, a, b, u, t, o, r, i　＝　coronabutori (コロナ太り)  
なお、これ以外のアルファベットや数字等を入力した場合、何も起きません。

________________________________

### 必要となるもの

・Raspberry Pi 4 Model B　　×1  
・ブレッドボード　　　　　×1  
・LED　　　　　　　　　　 ×1  
・抵抗(220Ω)　　　　　　　×1  
・ジャンパー線(オス-オス)　×2  
・ジャンパー線(オス-メス)　×2  
・その他、Raspberry Piを動かすのに必要なもの

________________________________

### 実行の前準備

実行の前に以下の作業をお願いします。  
```
$ git clone https://github.com/yukisekido/myled.git  
$ cd myled   
$ make　　　   
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
```  

________________________________

### 実行方法

実行する方法は全部で3通りあります。  

##### 1.'s'を入力する  
```
$ echo s > /dev/myled0
```
デバイスドライバに's'を入力すると、LEDが"sannmitsu"のモールス信号を送ります。  

##### 2.'c'を入力する  
```
$ echo c > /dev/myled0
```
デバイスドライバに'c'を入力すると、LEDが"coronabutori"のモールス信号を送ります。  

##### 3.'m'を入力する  
```
$ echo m > /dev/myled0
```
デバイスドライバに'm'を入力すると、LEDが"merrychristmas"のモールス信号を送ります。  

________________________________

### 動画

こちらから動画に移動できます。  

________________________________

### 参考リンク
モールス符号に関してはこちらを参考にしました。  

________________________________

### ライセンス
GNU General Public License v3.0
