<http://www.openrelief.org/home/labs/>

#Labs

#ラボ

There are many aspects of UAV (drone) technology that require further research and development, especially in the context of developing Open Source-based solutions suitable for use around the world.

UAV(無人飛行機)のテクノロジーには、まだまだ多くの面で更なる研究開発が必要とされています。世界中で使われるのに相応しいオープンソースベースのソリューションを開発しようとするならばなおのことです。

Our labs page covers some of the work that OpenRelief volunteers and other projects have done in key areas.

このラボのページでは、OpenReliefのボランティアと他のプロジェクトが重要な分野で取り組んでいることの中から一部を紹介します。


##Vision Technology

##映像技術

Drones provide an “eye-in-the-sky” but need to be combined with other technologies to provide complete solutions.  
 ドローン（ロボット飛行機）は、私たちに「空からの目」をもたらしますが、完全なソリューションを提供するためには、他の技術と組み合わせる必要があります。  
 For example, with image-processing software a drone can “recognise” roads, people and smoke.   
 例えば、画像処理ソフトの助けによって、ロボット飛行機が道路や人々、煙などを「認識」することができるのです。  
 OpenRelief worked on this technology and produced test code using the open source project called OpenCV.  
 OpenReliefはこの技術に取り組み、OpenCVと呼ばれるオープンソースプロジェクトの成果物を利用したテストコードを作成しました。

Here is an example of how we taught a computer to see:  
これは、私たちがコンピュータに対して見るということを教えている様子です:  
<http://youtu.be/y4ltvMniFL0>

Here is an example of how we taught it to recognise what it was seeing:  
このようにして、写ったものを認識させました：
<http://youtu.be/9gx7PizS4YU>

Here is an example of how it learned to understand what it was seeing:  
何が見えていたかを理解させたやり方です：  
<http://youtu.be/dvyUZciRbNQ>

Putting it all together, here is an overview of our code recognising roads, people and smoke:  
私たちのコードが道路や人、煙を認識しています：  
<http://youtu.be/vD5oTNAbC5I>

Naturally all of our code is freely available. You can find it on Gitorious.  
もちろん、私たちのコードのすべてを自由に利用できます。[Gitoriousのリポジトリ][Gitorious]にアクセスしてください。

[Gitorious]:https://gitorious.org/openrelief/opencv


##Command and Control

##ロボット飛行機のコントロール

An important part of managing drones is the “Command and Control” technology.  
ロボット飛行機を管理するために重要なのは「指令・制御」の技術です。  
 This is the hardware and software that you use to manage the missing planning before the drones take off and the extraction of information after they return.  
 具体的に言うと、ロボット飛行機が飛び立つ前の飛行計画の管理と、帰還後に情報を取り出すために使用するハードウェアとソフトウェアです。

The simplest version of this is the ‘Ground Control Station’ used to program an autopilot.  
この最も基本的なものは、自動操縦装置をプログラムするのに使用される"Ground Control Station"（地上管制局の意）です。  
 A great example is Mission Planner for the open source ArduPilot autopilot that we use.  
 私たちが使用しているオープンソースの自動操縦装置であるArduPilot用の [Mission Planner] がその好例です。

[Mission Planner]:http://code.google.com/p/ardupilot-mega/wiki/GroundStation

訳注：ここではmissionというのは、調査などの目的を持った1回の飛行を指しています。Mission Plannerというのはそういう意の名称です。
原文中では、飛行ルートや調査結果など、その飛行に関連する一連のもの全て含めて指し示す単位として、missionという語が多用されています。missonを作成するというのは管理ソフトで飛行ルートを設定する事を指していますし、droneにmissionをloadするというのは、この飛行ルートをロボット飛行機の自動操縦装置に設定することです。訳文中では適宜適切と思われるように言い替えていますが、ミッションと書くしか他に書きようが無いケースではそのように記述します。



 Mission Planner is very useful to put waypoints into the drones and to see precisely where they went in post-mission summaries.  
 Mission Planner は、ロボット飛行機にウェイポイント（飛行経路を指定するための通過地点情報）を設定し、また飛行後に実際にどこを飛行してきたのかを正確に見ることができ、とても便利です。

However, a disaster relief drone needs more software or features to integrate with disaster management technology.  
しかし災害救援のためのロボット飛行機には、災害時の情報管理技術と統合するため、より多くのソフトウェアや機能が必要となります。  
 A key example would be Sahana Eden, an Open Source Humanitarian Platform which can be used to provide solutions for Disaster Management, Development, and Environmental Management sectors, and which is used in response to disasters around the world.  
 その重要な例は、[Sahana Eden]でしょう。これは世界中の災害に対するために使用できるオープンソースの人道プラットフォームで、災害情報の管理、開発、さらに環境管理部門のためのソリューションを提供しています。

[Sahana Eden]:http://eden.sahanafoundation.org/

Importing and exporting information from a Ground Control Station into a disaster management platform is a problem that has yet to be addressed effectively in the open source drove eco-system.  
ロボット飛行機の地上管制局である Ground Control Station と災害時救援情報共有システムとの間で情報をインポート/エクスポートする事は、まだオープンソース界で効果的に対処されていません。  
 In the OpenRelief project we considered addressing this through the creation of a little bridging server that sits in the middle and talks with everything via RESTful interfaces.  
 OpenReliefプロジェクトでは、RESTfulインタフェースを通じて双方とのやりとりを中継する小規模のサーバーを立てる事で、これに対処する事を検討しました。  
 Below you can find our notes on how the Drone Manager could work, though please note that the test system has not been created yet.  
 私たちの検討した「ドローン・マネージャ」の機能についての覚え書きを以下に示します。ただし注意して欲しいのは、これはテストシステムすらまだ出来ていないものだということです。


##Introduction
##はじめに

Drone Manager is conceptualized as a little web server.  
「ドローン・マネージャ」は次のような機能を持った小規模のWebサーバーとして構想されています。  
 It can contact Mission Planner to load/unload data from drones.   
 それは、ロボット飛行機に飛行データを渡したり、逆に受け取ったりするための Mission Planner ソフトウェアと接続し、  
 It can send mission data to Sahana Eden.  
 それらのデータをSahana Edenに送ることができます。  
 Ideally Drone Manager will be very light, it will be very modular, and we can start from a small base of critical functions to gradually add more ability.  
「ドローン・マネージャ」は、とても軽量で、モジュール式で、そして最初は重要な機能だけの小さな土台から始めて、徐々により多くの機能を追加していくのが理想的です。

The most basic function is listed below under (1) in the use-cases section, and it basically just has Drone Manager calling Mission Planner, loading and unloading mission data from autopilots, and sending mission GPS waypoint data back to Sahana Eden.  
最も基本的な機能は、ユースケースの1番目の項に記載されており、 Mission Planner に対して、自動操縦装置にロードするための飛行ルートデータを送り、逆に飛行後のGPSデータをSahana Eden に送り返します。


##Drone Manager Use Cases
##ユースケース

The Drone Manager will have three use-cases, and they can be understood both in order of development priority and time to deployment.  
「ドローン・マネージャ」には3つのユースケースが想定されています。それらは開発の優先順位や実際に利用可能となる時期ごとの段階でもあります。

We expect the first generation of designs to be load mission, go and return without ground to air interaction.  
最初のバージョンでは、地上から飛行中のロボット飛行機を操作するのではなく、予め組み込んだ飛行ルートに基づいて飛行を行う事になるでしょう。  
 Moving ahead, the ability to stream some data will be useful, starting with the simple “where is the drone now” and moving towards “what is it seeing?”  
 さらに進んで、飛行中のロボット飛行機からデータをストリーミングできれば便利です。最初はシンプルに「今どこにロボット飛行機があるのか？」から始めて、続いて「何が見えているか?」を。  
 The later end of that is likely to rely on communication hubs we will prototype off Tegra2 boards, which can make use of multiple bands via software defined radio, as well as GSM and similar methods of obtaining data from the planes and deployed sensors.  
 最終目標となる三番目のユースケースに必要と思われる通信ハブは、Tegra2ベースのボードを使ってプロトタイプを作ろうとしています。これは、飛行機や配置されたセンサーからデータを取得するためのGSMやその他類似の方式と同様に、ソフトウェア無線を介して複数のバンドを利用することができます。

Putting that in context, here are the Drone Manager (our drone control server software) use-cases, and they can be understood both in order of development priority and time to deployment.  
「ドローン・マネージャ」（私たちのロボット飛行機制御用のサーバソフトウェア）のユースケースを以下に示します。

1. Direct laptop connection to drone autopilot via USB (one to one).  
ラップトップとロボット飛行機の自動操縦装置とをUSBで１対１接続する。  
 This is the starting situation, where one laptop will load a mission to one drone, the drone will fly away into a zone with no live communication, and will return to download telemetrics back to the laptop.  
 これが始めの状態であり、1台のラップトップが1台（づつ）のロボット飛行機に飛行ルートを設定し、ロボット飛行機はライブ通信無しに目的地まで飛行し、戻って来ると測定結果をラップトップにダウンロードする。  
 Vanilla Mission Planner can do this, and I would assume that Drone Manager would do the same simply by calling Mission Planner via RESTful API to load and download data.
 Vanilla Mission Planner ではこれが可能であり、同じ事を「ドローン・マネージャ」が、RESTful APIを通じて Mission Planner を操作することによって行わせる。

2. Direct laptop connections to multiple drone autopilots via USB (one to many), as above, where the drones fly and return to dump mission data.  
ラップトップと複数の飛行機の自動操縦装置をUSBで接続する。そして前項のケースと同じように自動的に航行しデータを出力する。  
This is the first type of fleet management we are likely to see in practice, and appear to involve Drone Manager calling Mission Planner via RESTful, Drone Manager having the expansion to support multiple drones via public key ID, and Drone Manager helping you visualize where the drones went and what they saw using its modules/plugins.  
 これは実際の災害現場で目にする事になるであろう飛行機団管理の初期のタイプであり、「ドローン・マネージャ」は、RESTful API経由で Mission Planner を呼び出し、公開鍵によって複数のロボット飛行機をサポートする拡張機能を持ち、モジュールやプラグインを使用してロボット飛行機がどこに行ったか、そして、それらが何を見たかを視覚化する。

3. Drone Manager is running at HQ and is able to talk with networked drones in the air.  
「ドローンマネージャ」は本部基地で稼働し、飛行中の複数のロボット飛行機と通信する事ができる。  
These are identified and secured using the public key ID system.  
公開鍵IDシステムを使用することで複数のロボット飛行機を識別し、安全に管理する。  
The drones can be loaded with missions over the network, they can send back data and can (regulations and hardening permitting) have their missions altered in the air.  
ロボット飛行機は、ネットワークを介して飛行指示を受け取る事やデータを送り返すことができる。（法規や安全性が許せば）飛行中に飛行ルートを変更することができる。  
This is the advanced use case, and it will involve a balancing of technology with regulations.  
これは高度なユースケースであり、法規と技術とのバランスを要するでしょう。  
It’s likely to be first deployed in a sort of (2a), where the drones get missions loaded physically, but provide live data back over the air to HQ and other interested parties over the network.  
最初の配備では(ケース2a)として、飛行ルートの指示は地上で受けるが、観測データは飛行しながら本部基地やその他の関係先にネットワーク越しに送るといった形になるだろう。


##Sahana Eden Integration
##Sahana Edenとの統合

The drones are quite complex.  
ロボット飛行機はかなり複雑です。  
They have GPS data, telemetrics and imaging, with some of the former being able to tag the latter.  
それはGPSデータを持ち、また遠隔測定や画像のデータを持ちます。GPSデータは測定データや画像をタグ付けするのにも使用されます。  
A substantial amount of the complex data from the drone is managed via software called Mission Planner.  
ロボット飛行機からの複雑なデータの大部分は Mission Planner と呼ばれるソフトウェアで管理されます。  
That basically allows you to tell the drone where to go, and it provides a blackbox of what the drone was up to.  
それは基本的にはロボット飛行機にどこへ行くべきかを伝えるために利用でき、またロボット飛行機の飛行記録を提供します。  
Conceptually, we then plan to build a little server called Drone Manager that acts as a bridge between the drone itself (autopilot/computer), the mission planner, the processing done at HQ (if any) and external systems that need the GIS data (i.e. Eden).  
構想としては、私たちが「ドローン·マネージャー」と呼んでいる小さなサーバーを構築することを計画しています。それは、ロボット飛行機(自動操縦装置/コンピュータ)自体と、Mission Planner（飛行管理ソフト）、（もしあれば）HQ（本部）で行われた処理、そしてGISデータを必要とする外的システム(すなわち、Sahana Eden)との間のブリッジとして機能します。

The important point is that Eden should never talk with a drone to ensure that (a) you guys don’t get a headache as we change and twist around lower level stuff and (b) we don’t get a headache trying to upstream things which don’t actually help your mission.  
重要なポイントは、 Sahana Eden とロボット飛行機に直接やりとりさせる事はないということです。
目的の実現のために必要である以上の事をやろうとして頭痛を起こすことはありません。  
It would be great if we could push data to Eden through a RESTful module called by the Drone Manager.  
 「ドローン·マネージャー」から呼び出されるためのRESTfulモジュールを通じて Sahana Eden にデータを送り込めればそれで十分です。  
The way George and I discussed this so far, the Drone Manager will just be a little server calling the Mission Planner via RESTful, so push/pull data via RESTful to Eden fits right in.  
ジョージと私がこれまで議論してきた「ドローン·マネージャー」が Mission Planner をRESTfulインターフェースを通じて操作するやり方は、Sahana Eden との統合へもぴったりです。

In summary, if we conceptually have the Drone Manager pushing and pulling data from Eden, that allows us to send our waypoints and data, and it allows export of “make this point a waypoint for a drone” notes in Eden.    
要約すると、構想通りに「ドローン·マネージャー」によって Sahana Eden からデータをプルあるいはプッシュできるなら、 飛行記録や観測データをSahanaに送ったり、Sahana Eden を使って「この地点にロボット飛行機を飛ばす」といった事を指定できるようになります。


##Conceptualizing Data Transfer
##データ転送のコンセプト

Understanding what the data going back and forth is an important point of working out the practical bridge between Drone Manager and Sahana Eden.  
「ドローン·マネージャー」と Sahana Eden との間の実用的な橋渡しを解決するための重要なポイントは、どんなデータを行き来させるかを理解する事です。

Some things are pretty clear.  
明確になっているのは次の事です。

- On a basic level, there will be missions, there will be drones, there will be locations, there will be times and there will be associated images and/or flags (“I saw smoke”).  
 基本的なレベルでは、ミッション（個々の飛行を指し示す単位）と、それに関連付けられたロボット飛行機（の識別）・位置情報・時間情報、そして画像情報とフラグ（例えば"煙を見た"等）があります。

- The Drone Manager should be able to deliver all that type of data to Eden so that relief workers know what went where, when, and why.  
救援活動に携わる人々が、何が・どこで・いつ・なぜ起きたのかを把握できるように、「ドローン・マネージャ」はそれら全て種類の情報を Sahana Eden に送らなければならないでしょう。  
I’m not sure if we need to send any more data than this, as Eden has all the general relief mission planning, task management and so on needed for relief worker in general.  
 一方、Sahana Eden が救援活動に携わる人々に通常必要とされる全ての救援活動計画やタスクを管理するのと同じように、私たちがさらに多くの種類のデータを送る必要があるかと言えば、それはどうでしょうか。  
We don’t want to duplicate or pull that data.  
私たちは、そういったデータをコピーしてきたりするつもりはありません。  
We just want to make sure relief workers know a drone mission was carried out, they can access the data from the mission, and they can identify the physical units involved in the mission.  
私たちは救援活動者に、ロボット飛行機が調査を行ってきた事を知らせ、その調査データにアクセスできるようにし、そして
それらのデータを実際に起きた事と関連付けて見極めることができるようにしたいのです。

- The export from Eden side is probably a lot thinner, consisting of the “make this point a waypoint for a drone” flag that the drone managers can load into the Mission Planner, and work out new missions with optimal waypoints/range, and perhaps a “refly mission” flag to request a simple waypoint reload on Mission Planner for reviewing previously seen land.  
Sahana Eden の側からエクスポートするべきデータはおそらくずっと少ないです。まずは最適な飛行ルートによる新しいミッション（飛行任務）を作成するための「ロボット飛行機に経由させる地点」の情報、そしておそらくそれに加えて既に調査されたエリアを再調査するための「やり直すミッション」の情報です。

- One area where we probably need to duplicate is the “who assigns the mission ID” feature.  
 ミッションに対する識別IDの割り当てに関しては、おそらく重複して行わなければなりません。  
Eden probably needs to be able to assign mission IDs for its normal workflow, but we probably also need to be able to create/import/export mission IDs in the Drone Manager, especially in contexts where people are not using Eden.   
 Sahana Eden でミッションを管理する際、その正常な作業フローのためにデータに識別IDを割り当てる必要があるでしょう。一方「ドローン・マネージャ」の方でも（ Sahana Eden を併用せずにこれを利用する場合などには）、独自に識別IDを割り当てる必要があります。  
This is where we have to be aware that while Eden is a primary target for interoperability, the OpenRelief solution needs to also function without it.  
  Sahana Eden が相互運用のための主要なターゲットであるとしても、同時にOpenReliefのソリューションは、それなしでも機能する必要があるのです。

- It therefore sounds like we need to have common table modules for data import/export on both sides to allow us to push/pull data from each other seamlessly.  
 それゆえ、シームレスに相互にデータをプッシュ/プルできるようにするため、（双方の識別IDを関連付ける）共通のテーブルモジュールを持っている必要があるでしょう。  
An OpenRelief API? ;)  


##Splitting Responsibilities
##役割分担

Drone Manager should be responsible for Mission IDs, talking with the drones and all interaction with the Mission Planner software.  
「ドローン・マネージャ」は、 Mission Planner ソフトウェアを介したロボット飛行機との全ての入出力・指示報告と、ミッションの識別ID管理を担うものとする。

Sahana Eden should be able to request “Add this point to a future mission” and “please (re) survey this area.”  
 Sahana Eden からは、飛行ルートの指定やエリアの再調査を要求できるようにする。

Overview of the Proposed Architecture  
提案されたアーキテクチャの概要

![](http://www.openrelief.org/home/wp-content/uploads/2013/06/EdenDroneManagerRestfulGrandPlan.png)




The major components are:  
主な構成要素は次のとおりです。

- The Mission planner is existing software as outlined above.
  Mission Planner は上記のように既存のソフトウェアです。

- The Drone Manager is new software that acts as a bridge between the Mission Planner and Sahana Eden.  
 「ドローン・マネージャ」は、 Mission Planner と Sahana Eden の間のブリッジとして機能する新しいソフトウェアです。

- Sahana Eden is the Disaster Management solution we are initially targeting. It has its own database of assets, people, etc.  
  Sahana Eden は、私たちが最初のターゲットとしている救援情報管理ソリューションです。それは資産や人などの独自のデータベースを持っています。

- The OpenRelief module in Sahana Eden consists of the plugin to Eden that is required to link to the Drone Manager to Eden.  
  Sahana Eden の OpenRelief モジュールは、「ドローン・マネージャ」との接続に必要なSahana Edenのプラグインです。


The Open Relief module has a number of responsibilities to perform:  
Open Reliefモジュールは、多くの役割を担います。

1. It should provide the data models used to store the GIS and mission data supplied by the Drone Manager. These models define the tables within the Eden Database.  
 「ドローン・マネージャ」によって供給されたGISおよびミッションのデータを格納するために使用されるデータモデルを提供する。これらのモデルは、 Sahana Eden のデータベース内のテーブルを定義する。

1. It should provide the controllers to allow access to the models to both humans – via an HTML interface, and to machines via a RESTful interface.  
 HTMLインターフェースを介して人間が、RESTfulインターフェースを介してコンピュータが、データモデルにアクセス可能なコントローラを提供する。

1. Any necessary views to display the information.
The Eden architecture will provide a substantial amount of the controller implementation, including the RESTful interface. This leaves the bulk of the work in defining the data models and the views.  
 情報を表示するに任意の必要なビュー。 Sahana Eden のアーキテクチャは、RESTfulインタフェースを含むコントローラを実装するためのかなりの部分を提供するでしょう。やるべき事の大半はデータモデルとビューを定義する作業です。


##Map Data Visualisation
##地図データの視覚化

The OpenRelief module will also need to define the layers e.g. smoke, so that data points can be displayed on a map.  
また、地図の上にデータポイント（例えば煙）を表示できるように、OpenReliefモジュールは、レイヤーなどを定義する必要があります。

Additionally, the we need to link “pins” on the map back to the original data, and possibly as “refly this location” option.  
さらに、地図に立てた"ピン"を、元のデータと関連付ける必要があります。例えば「この地域を再調査する」というようなオプションのためにです。


##Actual implementation of data transfer between Drone Manager and Sahana Eden
##ドローン・マネージャとSahana Edenとのデータ転送の実装

It is proposed that the implementation takes place in two stages:  
なお、実装は二段階で行われることが提案されている。

1. We export a CSV file containing the mission data from the Drone Manager into Eden.  
 ミッションデータを格納したCSVファイルをDrone Managerから Sahana Eden にエクスポートする。  
Eden in turn will export a CVS file containing a list of way points that need to be re-flown.  
 次に Sahana Eden から再飛行する必要がある飛行地点のリストを格納したCVSファイルをエクスポートする。
The Drone Manager should import this file.   
 Drone Managerは、このファイルをインポートする。

2. Once this has been proved to work and the model structures on both sides have settled, the full RESTful interface can be implemented on both the Eden side and the Drone Manager side.  
これらの機能が正常に働く事が実証され、さらに双方のデータモデル設計が固まった後、Sahana Eden とドローン・マネージャの双方で、完全なRESTfulインタフェースを実装することができる。

On the Eden side a RESTFul interface should be presented that supports CRUD operations on the mission’s GIS data.  
Sahana Edenの側では、ミッションのGISデータに対するCRUD操作をサポートするRESTFulインタフェースが必要です。  
Eden should return an Event ID for each mission event to the Drone Manager.  
Sahana Edenはドローン・マネージャに各ミッションイベントのイベントIDを渡さなければなりません。  
On the Drone Manager side a RESTful interface should be presented that allows Eden to create a list of way points that should be used in future missions, and request that a specific mission is re-flown.  
ドローン・マネージャ側では、ミッションの実施に必要な経路情報をEdenから作成できるようなRESTfulインターフェースが必要です。


##Reasoning
##論拠

If it is done this way then on the Eden side the table structures can be defined and redefined as needed.  
このようにする事で、Sahana Edenの側でテーブル構造を定義し、また必要に応じて再定義することができます。  
These tables will be reused via the RESTful interface that Eden presents to the Drone Manager.  
これらのテーブルは、Sahana Edenがドローン・マネージャに提供するRESTfulインタフェースを通じて再利用されるでしょう。  
The Drone manager uses this interface to push mission data into Eden via CRUD style interface.  
ドローンマネージャは、このインタフェースを用いCRUDスタイルの作法で、Sahana Edenにミッションの調査データをプッシュします。  
Using CSV files, initially, will also decouple the Eden OpenRelief module from the Drone Manager.  
初めのうちはCSVファイルを使用する事で、Sahana Edenの OpenRelief モジュールとドローン・マネージャを分離しておきます。  
Likewise on the Drone Manger side, if it initially imports way-point data via a CSV file, until a RESTFul interface is fully defined.  
 同様に、ドローン・マネージャの側でもRESTFulインタフェースが完全に定義されるまで、CSVファイルによってを航路地点情報をインポートします。

In both cases while the RESTFul interfaces are in a state of flux, dummy data can be served by serving static response files from the web server.  
どちらの場合も、（相手側の）RESTFulインタフェースが未完成の間は、Webサーバからstaticなファイルを送り返す事でダミーのデータを提供することができます。


##Defining a data transfer API
##データ転送APIの定義

We need to clarify what data we want to pass to Eden from the Drone Manager. One suggestion below:  
どんなデータをドローン・マネージャからSahana Edenに渡したいのかを明確にする必要があります。 以下に1つの提案を示します:

1. a) For a given sensor reading we need:  
 a) 必要とされる特定のセンサの観測データ:

	1. time (in UTC – you can take this from the GPS)  
	時間（UTCで - GPSから取得可能）

	1. position of “event” as lat, long (+ altitude?)  
	"事象"の発生位置（緯度、経度、+標高？）

	1. mission ID  
	ミッションID

	1. event id (note from Fran at Sahana: “UUID?”  
	事象ID（SahanaのFranからの提案 UUID?

	1. Type of event (smoke/fire/person/radiation/weather etc)  
	事象のタイプ(煙/火災/人/放射線/天候など)

	1. reference to further event data, if any (note from Fran at Sahana: “We’d do that the other way around normally – the further data would refer to the event by event_id (the further data is a ‘component’ of the main resource)”  
	もしあれば、追加のデータへの参照（追加データの方からメインデータを参照するのが本来じゃね？ By Fran@Sahana）

	1. drone ID (does Eden need this?)  
	ロボット飛行機のID（Edenに必要？）

1. b) For each event the data I think is different.  
事象の種類によって異なるデータ

	1. i) In the case of smoke/fire/people we need the image data  
	煙/火災/人の場合は、画像データ

	1. ii) Radiation needs the sensor value  
	放射線の場合は、センサーの値

	1. iii) Weather needs??? (as a suggestion: current Temp, max temp, min temp, wind direction, and speed?)  
	天候の場合は？（提案として：現在気温、最高気温、最低気温、風向、風速）


##User Interface Mockups
##ユーザーインターフェイスのモックアップ

A series of prototypes have been created to serve as a basis for discussion about the way users will interact with the Drone Manager.  
ユーザーがドローン・マネージャと対話する方法についての議論の叩き台として一連のプロトタイプを作成しました。
