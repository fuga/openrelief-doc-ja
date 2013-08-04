#Radiation Detector
#放射線検出器

![](http://www.openrelief.org/home/wp-content/uploads/2013/06/7255313404_e99bbd8842_o.jpg)
A Treacle Tin Radiation Detector  
シロップ缶の放射線検出器

##Overview
##概要

![](http://www.openrelief.org/home/wp-content/uploads/2013/06/Circuit-300x272.jpg)  
Radiation Detector Circuit  
放射線検出回路

This is a prototype of an ionisation chamber-based radiation detector for OpenRelief. It is designed around a Nanode but could easily make use of another Arduino-compatible board with Ethernet. The steps involved in its operation are as follows:  
これはOpenReliefの電離箱式の放射線検出器のプロトタイプです。これは、Nanodeボードを中心に設計されていますが、それとは別のイーサネット付きArduino互換ボードを利用することも簡単にできます。その動作に必要な手順は次のとおりです。

- Briefly pull the JFET source low to discharge the chamber wire  
JFET（ジャンクションFETトランジスタ）のソース側をアースして、電離箱内の銅線を放電する。
- Take a voltage reading  
電圧を測定する
- Pause  
一時停止
- Take a second voltage reading  
２回目の電圧測定を行う
- Calculate the voltage drift  
電圧差を計算する

##Design Files / Code
##設計ファイル/コード

You can download the design files and the code here:  
ここから設計ファイルとコードをダウンロードすることができます：  
<http://solderpad.com/openrelief/radiation-detector>


##Learn More
##詳しくはこちら

There are two posts detailing the development of the OpenRelief radiation detector on DesignSpark.  
OpenRelief 放射線検出器の開発についての詳しい説明が DesignSpark に投稿されています。

The first is entitled ‘A Treacle Tin Radiation Detector‘ and covers the initial build process. In it Andrew explains that while “the Geiger counter has become synonymous with radiation detection [...] there are many ways to achieve this other than using a Geiger-Muller (GM) tube. The ionisation chamber works on similar principles to the GM tube, but is an incredibly simple design that can be constructed from an old tin can and which does not require the use of high voltages and an inert gas and halogen fill.  
”最初の投稿は「[シロップ缶の放射線検出器][a-treacle-tin-radiation-detector]」と題され、初期のビルドプロセスについて記載されています。その中でアンドリューは次のように述べています。「ガイガーカウンターは放射線検出の代名詞となっていますが[中略]ガイガー·ミュラー（GM）管を使用する以外にも多くの方法があります。電離箱は、GM管と同様の原理で動作しますが、古い缶を利用して作る事もできる非常にシンプルなデザインで、高電圧や不活性ガスやハロゲンの充填などを必要としません。」

[a-treacle-tin-radiation-detector]:http://www.designspark.com/blog/a-treacle-tin-radiation-detector

The second is entitled ‘An Ionisation Chamber Shield for OpenRelief‘ and details the construction of an inverter to replace the bank of batteries previously used for bias power supply. Andrew explains that “to recap, the bias voltage is applied across the ionisation chamber electrodes, between which tiny currents flow when ionising radiation enters the chamber. Using four PP3 batteries in series provided a bias of 36v, which is possibly suboptimal in addition to not being terribly convenient.”  
２つめは「[OpenRelief 電離箱シールド][an-ionisation-chamber-shield-for-openrelief]」というタイトルで、バイアス電源用に以前に使われていた電池群を置き換えるためのインバータの構成について詳しく書かれています。アンドリュー曰く、「電離箱の電極の間にバイアス電圧を加えると、電離箱の中に放射線が入った時に微かな電流が流れます。4個のPP3バッテリーを直列で使用する事で36Vのバイアス電圧を供給できます。これはおそらく最適ではないでしょうし、非常に扱いやすいという訳でもありません。」

[an-ionisation-chamber-shield-for-openrelief]:http://www.designspark.com/blog/an-ionisation-chamber-shield-for-openrelief


##License
##ライセンス

The radiation detector is licensed it under the Solderpad Hardware License, version 0.51.  
この放射線検出器は、[Solderpadハードウェアライセンス、バージョン0.51][license]によってライセンスされています。

[license]:http://solderpad.org/licenses/SHL-0.51/


##The People Behind The Radiation Detector
##放射線検出器の開発主導者

![アンドリュー・バック](http://www.openrelief.org/home/wp-content/uploads/2013/06/5a763ed1bba0e43bb8f4cb7ec0d5027c.png)

###Andrew Back
###アンドリュー・バック

Andrew is an artist, electronics hacker and open source advocate. He acted as BT’s Open Source Strategist, establishing company-wide open source policy and process and representing them at a number of bodies including The Linux Foundation and ATIS. Andrew co-founded the Electron Club in 2006 — one of the UK’s first hackerspaces, and founded and runs OSHUG, a monthly open source hardware meet-up in and around London, UK.  
アンドリューはアーティストであり、ハッカー、そしてオープンソースの提唱者でもある。彼はBTのオープン·ソース·ストラテジストを務め、全社的なオープンソースのポリシーとプロセスを確立し、それらをLinux FoundationとATISを含む多くの形で体現した。アンドリューは2006年に電子クラブを共同設立した。これはイギリス最初のhackerspacesの一つであり、ロンドンとその周辺で毎月オープンソースのハードウェアmeet-upを開催するOSHUGを設立・運営しています。


##Development Gallery
##開発ギャラリー

Released under CC BY-NC-SA 2.0 by Andrew Back  
全ての画像は、アンドリュー·バックによってCC BY-NC-SA 2.0の下で公開されています。

![](http://www.openrelief.org/home/wp-content/uploads/2013/06/7255308008_f2f7d4cb9c_o-150x150.jpg)  
Ionisation chamber end view.  
電離箱の端面図

![](http://www.openrelief.org/home/wp-content/uploads/2013/06/7255301718_c0b43fda2c_o-150x150.jpg)  
36v battery pack that provides the bias voltage for the chamber.  
電離箱の電極

![](http://www.openrelief.org/home/wp-content/uploads/2013/06/7255305694_1dd1599410_o-150x150.jpg)  
Ionisation chamber side view  
電離箱の側面図

![](http://www.openrelief.org/home/wp-content/uploads/2013/06/7255310096_c9b487593d_o-150x150.jpg)  
36v battery pack that provides the bias voltage for the chamber.  
電離箱にバイアス電圧を供給する36Vバッテリーパック

![](http://www.openrelief.org/home/wp-content/uploads/2013/06/7255313404_e99bbd8842_o-150x150.jpg)  
A Treacle Tin Radiation Detector  
シロップ缶の放射線検出器

![](http://www.openrelief.org/home/wp-content/uploads/2013/06/Assembled-150x150.jpg)  
Phase 2: an inverter to replace the batteries providing a reference charge.  
フェーズ2：電池に代わり基準電荷を提供するインバータ

![](http://www.openrelief.org/home/wp-content/uploads/2013/06/Connected-150x150.jpg)  
The bias voltage is applied across the ionisation chamber electrodes  
電離箱の電極間にバイアス電圧を加えます

![](http://www.openrelief.org/home/wp-content/uploads/2013/06/Testing-150x150.jpg)  
The updated detector in all its glory  
これが新しくなった検出器です!

