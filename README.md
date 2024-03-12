# まち歩きマップメーカー

## 目的・用途
印刷向けのまち歩き地図、案内地図、地図柄のグッズ制作などに使えるOpenStreetMap。  
でも、高機能だけど複雑なソフトウェアやプログラミングの知識は持っている人は少ない。  
  
そんな「パソコンでちょっとした文書は作れる程度」の方たちでも、もっと自由に地図を  
使って欲しいと思って、この「まち歩きマップメーカー」を開発しています。  
  
まち歩きマップメーカーを使うと、PNG/SVGという一般的な画像で地図のダウンロードが  
出来ます。あとは、プレゼンソフトでポップやアイコンを追加するだけで、お店や施設の  
案内地図や、まち歩きのイベントなどで配る地図を作ることが出来ます。  

## マニュアル
* [まち歩きマップメーカーのススメ](https://medium.com/@K_Sakanoshita/ea38ce4fd10)

2018/06/17
* メモしてなかったので、記憶が曖昧
* 建物、森、公園を書き出し出来るように変更
* 名前を「OSM Access Map」から「まち歩きマップメーカー」へ変更

2018/08/25
* PNG/SVGダウンロード時にCopyrightを追記するように(tom-kondaさんに感謝！)
* 信号のサイズを若干小さくする
* 「program by K.Sakanoshita」を削除

2019/01/03
* インターフェイスの見直し（画面を広く、画面遷移を分かりやすく）
* マップデータのダウンロード速度を改善（並列処理化）
* ダウンロード可能なファイルサイズを増加（古いブラウザだと重い）
* 恐らくInternetExploer11だと正常に動作しなくなったと思われます

2019/02/21 
* カフェのアイコンを表示・削除する機能を追加

2019/06/08
* レストラン、ファストフード、消火器、消火栓、避難所アイコンを表示する機能を追加
* 追加したアイコンに店舗名を表示するよう仕様変更（非表示やアイコン変更は今後）
* 追加したアイコンをドラッグアンドドロップで任意の場所へ移動する機能を追加
* 地図のデザインを見直し（色パレット追加、初期値の色を変更、線の太さなど）
* ユーザーインターフェースの見直し（表示/非表示のチェックボックスを統合など）

2019/08/09
* 更新情報を更新するのを忘れてました
* 地図スタイルを見直しました（少しGoogle Maps風？）
* カフェ以外にも消火器/避難所アイコンを追加出来ます
* その他にも、色々あるけど忘れました（笑）

2020/01/05
* 指定した年月日のデータをもとに描画する機能を追加
* 図書館、壁、ロープ、フェンス、擁壁を表示する機能を追加
* turf.jsの導入によるgeojsonのsimplifyを実施

2020/01/09
* ベンチを表示する機能を追加

2020/02/10
* 色選択を改善（クリックしやすく、選択状態を可視化）
* 選択出来る色数を増やしつつ、不要な色は削減
* 上記の機能強化に合わせて、標準地図の表現を見直す

2020/05/31
* 背景地図を openstreetmap.org から Maptiler へ変更
* 住所検索機能を追加(geoloniaの宮内氏に感謝！)
* 上記に合わせて画面レイアウトを一部変更（内部も見直し予定）
* ホスト先を netfort から GitHub へ変更

2020/07/08
* インターフェイス刷新
* * POIの選択機能（カテゴリ選択、キーワード検索）
* * 編集モード追加、メニュー追加、利用規約の表示機能
* 地図のレンダリング品質と機能を強化
* * カラーパレット追加、背景色選択、線の太さ選択
* * 海の描画、建物・道路などの個別表示・非表示選択
* * 並木や橋の描画、アイコンの刷新・サイズ変更
* * ズームレベル12に対応（ズームレベル毎に取得データを変更）
* データ更新
* * 大阪市オープンデータポータルサイトのCSV(避難所情報)を更新
* 「指定した年月日のデータを元に描画する機能」を一旦削除
* * かなり範囲を絞らないとサーバー側から応答が帰らないため
* 「turf.jsの導入によるgeojsonのsimplifyを実施」を削除
* * 大量のgeojsonを扱うことが目的で導入するも効果が低いため

2020/10/10
* 画面上部にあるメニューの背景画像を見直し
* OverPass APIのクエリを最適化し、サーバーの負担を軽減
* POIの選択機能を強化（宗教施設、遊具、樹木など）
* POIの選択機能の強化に合わせて対応するアイコンを追加
* POIのアイコン選択機能を追加
* POIのアイコン表示サイズを画面上でも反映
* A4サイズ（縦・横）のサイズでダウンロードする機能を追加
* カラーパレットの色数を追加（白に近い淡い色を中心）
* 内部構造の見直し（簡単にPOIを扱えるように改良）

2020/11/23
* 標準表示する地図をOpenStreetMap（モノクロ加工）へ戻す
* * 以下の地図を選択できるように設定
* * OpenStreetMap Mono
* * OpenStreetMap Standard
* * OpenStreetMap Maptiler
* * 国土地理地図 オルソ
* * 国土地理地図 淡色 
* 生垣を「壁・擁壁」から「森・田畑」で表示するよう変更
* スマートフォンへの暫定対応
* * 住所検索をメニューへ移動
* * ズームレベルの表示位置を変更
* * やり直しボタンの表示位置を変更

2021/04/24
* 「階段」を表示・カスタマイズする機能を追加
* アイコン表示の内容を追加・改良
* * 「樹木」と「動物」を一つにまとめる
* * 「防災関連」を「防災・防犯・移動」へ変更
* * 「防災・防犯・移動」に「街灯」「貯水槽」「社会福祉施設」を追加
* * 「ちょっとしたポイント」に「遊具」を統合
* * 「ちょっとしたポイント」に階段と段数を追加
* アイコンのデザインを追加・変更
* * 自動販売機、樹木、階段、貯水槽、汎用ポイント（オレンジ）

2021/05/09
* OpenStreetMapの標準地図で使われているMapnik Iconの取り込み開始
* * [Mapnik Icon svg](https://wiki.openstreetmap.org/w/index.php?title=Category:Mapnik_Icon_svg)
* * [Amenity icons](https://wiki.openstreetmap.org/wiki/Category:Amenity_icons)
* Digital北海道研究会が公開している地図記号を取り込み
* * [地図記号集の提供](https://dghok.com/gisx/662.html)
* 以下のアイコンを表示する機能を追加
* * コミュニティセンター(公民館)、図書館、宗教施設、幼稚園、保育園、学校(小中高)、大学・短大
* * 病院(大規模・中規模)、診療所・医院、動物病院、警察署、駐車場、駐輪場(バイク・自転車)
* * 博物館、美術館、行政機関、BBQ、ピクニック場、裁判所、消防署、郵便局、刑務所、避難小屋
* * 銭湯・シャワー、トイレ、水飲み場、給水所、リサイクル施設、ゴミ箱、火葬場、ネットカフェ
* * 証明写真ボックス、街角文庫、劇場、エレベーター、遺跡、モール、赤ちゃん用品、ブティック
* * 衣服店、化粧品店、大人のおもちゃ、薬局、美容院、マッサージ店、靴屋、クリーニング店
* * 眼鏡店、時計店、古着・リサイクル店、質屋、ホームセンター、散髪屋、医療用品店、花屋
* * 園芸・植木屋、金物屋、家具屋、内容用品店、パソコンショップ、家電販売店
* Poi表示機能の改善
* * 宗教の宗派や小中高の種類など、他のタグと組み合わせでアイコンが変わるタグへの対応
* * Poi取得メニューの見直し(店舗と施設を分離。ただし、shopとamenityへの分離なので不十分)
* * Poi表示時の白背景に透過度を追加(印刷時の透過は実施済み)
* * Poi選択時のカテゴリが増えたためソートさせてから表示させる
* * キオスクなど、いくつかのアイコンをMapnikなどのアイコンへ変更

2021/09/12
* Firefox でsvgファイルをダウンロードすると拡張子がpngになる不具合を修正

2022/09/28
* Community Mapmakerで開発したコードを一部取り込み(共有化を少しだけ進める)
* OverPass APIを提供しているサーバーを変更し、エラー時の切り替え機能も追加
* OverPass API呼び出し時のタイムアウト値を調整し、より広範囲のマップに対応
* * 上記の調整により、ズームレベル15→11が実用レベルで使えるようになる
* 海を誤判定する不具合(陸地が海になってしまうなど)を大幅に減少
* カラーパレットを変更(ブラウザ標準)し、任意の色指定が可能になる
* WikipediaのQRコード作成時、記事中の画像も表示するように変更
* アイコンを大量追加。利用するアイコンをMaki/Temakiベースへ変更
* * 古いアイコンもPOIをクリックして「アイコン変更」から選択可能

2022/12/14
* 地図に表示するアイコンの位置ズレを修正
* 地図に表示するアイコンと文字の最大サイズ指定を大きく(24pt→102pt)
* 地図に表示するアイコンの枠を丸から四角(角なし)へ変更
* 地図に表示するアイコンを追加するメニューを見直し
* * 各種店舗 → 各種店舗/施設、各種施設を削除(両者を一つのメニューへ統合)

2023/02/24
* フェンスが描画されない不具合を修正
* 生垣と並木を描画するように（森・田畑扱い）

2023/03/20
* サイトデザインの見直し(ヘッダ部分のリサイズ含む)
* 地物表示の種類・表現を見直し(歴史・文化・アートなど)
* 「マンホール」を表示(防災・防犯・移動メニューから)
* いくつかのアイコンは枠なしで表示するように変更
* 大きめの道路にはセンターラインを表示するように改善
* 道路種別に「生活道路」を追加(敷地内道路などを表示)
* ズームレベル18以上で建物に少し影が付くように変更

2023/03/24
* 建設中のレールも表示するように変更
* railway=rail以外のレールが表示されないバグを修正
* Leafletを1.9.3へ更新
* ズームレベル18以上で建物に影が付かないよう戻す

2023/07/27
* MapTilerを一旦タイル一覧から外す(API使用量削減)
* カラーパレット機能を追加（カラー、モノクロ機能）
* 内部処理を一部だけリファクタリング（先は長い）

2023/08/12
* ポップアップが表示されないバグを修正
* 一部のメソッド、ファイルを整理整頓（先は長い）

2023/12/30
* 内部処理を少し見直し(不要なコード/データ削除など)
* 大阪市オープンデータを更新
  https://www.city.osaka.lg.jp/contents/wdu290/opendata/#cat-all_data-00000001
  17_防災関連施設ポイントデータ（災害時避難所・一時避難場所）
  21_防災関連施設ポイントデータ（津波避難ビル）
  ※2020/02/09時点
* アイコンサイズの見直し、フォント表示位置の微調整

2024/03/09
* Wikipedia説明文を書き出す時に表示が崩れるのを修正
* Overpass APIにOSMJPのテストサーバを指定

2024/03/13
* Wikipedia説明文を書き出す時に表示が崩れるのが完全に治ってなかったのを修正
