<http://www.openrelief.org/home/open-source-airframe/>

#Open Source Airframe
#オープンソースの飛行機体

>訳者注記:
OpenRelief のロボット飛行機は、既存のコンポーネントの組み合わせで作られており、その多くが設計の公開されたオープンハードウェアやオープンソース・ソフトウェアです。  
一方、機体については独自に設計・開発が行われ、その成果は同様にオープンライセンスで公開されています。  
ここでは、この機体の設計について説明します。


##Specifications

##仕様

- Length 1.4 meters

- 長さ 1.4メートル

- Wing span 1.8 meters

- 翼幅 1.8メートル

- Chord 30cm

- 翼弦長（翼の前後方向の長さ）30cm

- Uses counter-rotating motors (redundancy, speed, balance, no torque)

- ２重反転式モーター使用（冗長性、スピード、バランス、反動トルク無し）

 訳注：同じ軸に互いに逆方向に回転する２つのプロペラが付いています。  
![](http://www.openrelief.org/home/wp-content/uploads/2013/05/20130430_095201-300x225.jpg)

- Uses remote servos (wing flaperons, the tail surface) for more storage and ease of repair

- より多くのストレージと修理の容易さのためにリモートサーボ（フラッペロン、尾翼面）を使用

 訳注：フラッペロンとは、フラップ（翼の後方を下げて揚力を高める）と、補助翼（機体の左右の傾き・ロールを制御するため、翼の後縁に左右対称に取り付けられている操縦翼面）を、１つにしたもの。下画像の尾翼後縁を参照
![](http://www.openrelief.org/home/wp-content/uploads/2013/05/20130430_100921-225x300.jpg)

- Empty weight 5.5kg
- 無荷載時重量5.5キログラム

- Thrust is 12kgs
- 推力 12キログラム

- Max load 12kg (lift at 100mph/160kph is approx 12kg)
- 最大荷重12キログラム（時速100マイル=160kmでの揚力は約12キロ）

- Endurance is between 1 to 4 hours with existing specifications
- 航続時間 1〜4時間（既存の仕様の場合）

- Wings can be repositioned to change CoG for large payloads
- 重い荷物を積載した際に重心を調整するため、翼の位置を変えることができる

- Stringers located on the fuselage to carry the wing, landing gear and other modules
- 翼、着陸装置、その他のモジュールを固定するため、胴体には縦げた材が設置されている

- These channels also hold internal items like the motor via bulkhead rings, for quick changes
- これらの形鋼材はまた、（変更しやすいように環状隔壁を介して）モーター等の内部の部品を支えている

 訳注：Stringersあるいはchannelsと表現されているのは下画像の長い鋼材の事のようです。bulkhead ringsは胴体の筒の事だと思われます。  
![](http://www.openrelief.org/home/wp-content/uploads/2013/05/20130430_095613-300x225.jpg)

- Fuselage can carry liquids (same diameter as 2L bottle of cola)
- 胴体は（コーラの2Lボトルと同じ直径の）液体を運ぶことができる

- Can be launched by rail and use parachute recovery
- レールから射出する事ができ、パラシュートで回収できる

- Can be fitted with front wheels for conventional landing in rough fields
- 荒地に着陸するために前輪を取り付けることができる

- CAD files are from Solidworks
- CADファイルは、SolidWorksで作成されている

> 訳注: ファイルはソリッドワークス社の無償CADツールで開くことができます。
<http://www.solidworks.co.jp/sw/products/free-cad-software-downloads.htm>  
 上記はWin Vista以降のみ対応です。XPの人はRhinoceros評価版等が使えます。
 <http://www.rhino3d.co.jp/product/Rhino50/download.html> 

##Design Files

##設計ファイル

You can download the CAD schematics and the bill of materials here:

CAD図面と部品表をここからダウンロードすることができます：

<http://www.openrelief.org/documents/CTOL-UAV-current.zip>


##The People Behind The Airframe

##プロジェクトを支える人々

Edward Strickland

Edward Strickland, a gentleman with a degree in aeronautical engineering, experience with Open Source Auto Pilots and 7 years experience with QinetiQ and UK MoD, has lead the development of the OpenRelief airframe.

エドワード·ストリックランドは、航空工学の学位を持つ紳士で、オープンソースの自動航行技術に通じ、キネティック社と英国国防省で7年の経験を持ち、OpenReliefでの機体の開発をリードしています。

The OpenRelief airframe is an expansion of Eddie's research regarding commercial Vertical Take Off and Landing (VTOL) drones.

OpenReliefの機体は、商用の垂直離着陸（VTOL）無人機についてのエディの研究を発展させたものです。

 You can review an interesting overview of his VTOL focus on YouTube.

[ユーチューブ][YouTube]で彼のVTOLに関する興味深いまとめを見ることができます。

[YouTube]:http://www.youtube.com/watch?feature=player_embedded&v=YATWJQmPoMA

 You can visit Eddie's profile on DIYDNROES to learn more about his day-to-day work on drones and open technology.

DIYDRONES上の[エディのプロフィールページ][DIYDNROES]を訪問すれば、無人機とオープンテクノロジーに関する彼の日々の活動についてもっと知ることができるでしょう。

[DIYDNROES]:http://diydrones.com/profile/EdwardStrickland

##The Organisations Behind The People

##人々を支える組織

Working with the OpenRelief disaster relief project, students from Oldham College on the BTEC Level 3 Mechanical engineering course have been contributing to the development of airframe parts for the Open Source Unmanned Aerial Vehicle.

オールダム·カレッジ（英マンチェスター州）の機械工学コース（BTECレベル3）の学生達は、OpenRelief 災害救助プロジェクトに参加して、オープンソース無人飛行機用の機体部品の開発に貢献してきました。


Students have been working;

学生が取り組んできたのは、

- On a new design of wing which has internal load space for payloads.
- 内部に荷物を積む事ができる新しい設計の翼。

- Stronger landing gear to suit a longer airframe.
- 長くなった機体に合わせたより頑丈な着陸装置。

- A unique installation of the avionic and power units within the wing.
- 航空電子システムや電力ユニットを翼に納めるユニークなやりかた

- Stronger modular tail and control system.
- より強い組立式尾翼と制御システム。


It is expected that the airframe will be shipped from Oldham College to an experienced UAV user for initial flights in the UK,

イギリスでの最初の飛行のため、機体がオールダム·カレッジから経験豊富なUAVユーザーに送り出されるでしょう。

 leading to further rigorous testing in the Australian outback with a final destination of Japan for humanitarian flight testing over the Tsunami affected disaster areas.

これは、オーストラリアの奥地での更に厳しいテストを経て、日本の津波被災地での飛行テストに繋がるでしょう。


#History

#ここまでの軌跡

The first version of the OpenRelief CTOL-UAV airframe was released on the 6th of July 2012.

OpenRelief プロジェクトのCTOL-UAV（従来型離着陸方式の自動操縦飛行機）の最初のバージョンは2012年7月6日にリリースされました。

You can read the original release announcement here

オリジナルのリリースアナウンスは[ここ][release announcement]で読めます。

[release announcement]:http://openrelief.org/pipermail/developer_openrelief.org/2012-July/000504.html

 and download the version 1.0 CAD files / bill of material here.

また、バージョン1.0のCADファイル/部品表を[ここ][CAD1.0]からダウンロードできます。

[CAD1.0]:http://www.openrelief.org/documents/CTOL-UAV-1.0.0.zip

 It is based on a Conventional Take Off and Landing (CTOL) airframe developed for VTOL testing purposes.

これは、VTOL（垂直離着陸型飛行機）のテストのために開発された従来型離着陸（CTOL）機体に基づいています。

The 2.0 airframe was released at LinuxCon Japan on the 31st of May 2013.

バージョン2.0の機体は2013年5月31日にLinuxCon Japanでリリースされました。

 It features the following refinements:

これは、次の改良を備えています：

- An updated tail section to simplify and strengthen the airframe
- 機体を簡素化し、強化するために改良された尾翼部

- An updated front fuselage to strengthen the airframe
- 機体を強化するために改良された前部胴体

- An updated rear fuselage to strengthen the airframe
- 機体を強化するために改良された後部胴体


##License

##ライセンス

The airframe is licensed it under the TAPR Open Hardware License 1.0.

この機体は[TAPRオープンハードウェアライセンス1.0][TAPR]の下でライセンスされています。

[TAPR]: http://www.tapr.org/OHL


##Notes
##注釈

Please note that the propellors are located at the front of the plane, which allows for a simple build and flight quickly, but does introduce the potential issue of damage on landing.

この機体ではプロペラが機体正面の先端部にあり、そのためシンプルな構造と高速飛行が可能になっていますが、着陸の際に壊れやすいという問題点もあります。  

 There are various ways around this like deploying a parachute, flying into a net or rods which stop the propellor at 3pm position.

この問題に対しては様々な対処方法があります。例えばパラシュートを付けたり、網に飛び込ませたり、あるいは午後3時の位置でプロペラを止めるためのロッド（What is rod?）。

 However, the default airframe is intended to simplify the build process and does not include these features.

しかし標準の機体では、製造工程を簡素化するためにこれらの機能は含まれていません。

It is also worth bearing in mind that small scale aerodynamics produce large drag components at low speed that continually limit range.

また、継続的に範囲を制限する低速では小規模な空気力学が大きな抗力をもたらす事を念頭に置いておくことも大切です。

 Be conservative about endurance in your local environment.

あなたの環境での飛行距離・時間については控えめにしてください。

You should also be aware that testing shows even 2 to 3 flights can take a real toil on the system at this scale.

これまでのテスト結果から見て、僅か２,３回の飛行でもこのスケールのシステムには大きな負荷となる事に留意してください。

 This means that the lifetime of an airframe may be limited, especially if it is not checked and maintained frequently.

つまり機体の耐用期間は長くはないでしょう。もし頻繁に検査やメンテナンスを行わなければなおさらです。
