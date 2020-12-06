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
なお、これ以外のアルファベットを入力した場合、何も起きません。

________________________________

### 必要となるもの

・Raspberry Pi 4 Model B　  ×1  
・ブレッドボード　　　　　×1  
・LED　　　　　　　　　　 ×1  
・抵抗(220Ω)　　　　　　　×1  
・ジャンパー線(オス-オス)　×2  
・ジャンパー線(オス-メス)　×2  
・その他、Raspberry Piを動かすのに必要なもの
