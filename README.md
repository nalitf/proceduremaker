# schememaker

このマクロは試作品です。このマクロを使用したことによって生じた不利益に対して作成者は一切の責任を負いません。  
改変などは自由に行ってください。また、改善点などあれば是非教えてください。

このマクロの再配布は禁止します。  
なお、参考元サイトを末尾に付記しています。

2021.07.18 Sana

***

## 【使い方】

**A列**には以下の操作種別を入力してください
  
    begin  縦矢印の始点を決定  
    end    縦矢印の終点を決定

    以下のコマンドはbegin-endの中で使ってください  
        add         試薬や溶媒などを加える
        bar         横線の描画
        stir        攪拌する
        envbegin    実験環境の始点（窒素下, Gloveboxなど）
        envend      実験環境の終点
        ※envbegin-envendは必ず対で使ってください

    以下のコマンドはbegin -endの外で使ってください
        wu      ワークアップ操作
    
    以下のコマンドはどこでも使用可能です
        space   空行を作成

**begin**, **add**, **bar**, **stir**, **envbegin**, **envend**, **wu** は<u>**B列**に説明を記載</u>できます  
**space** は<u>**B列**に空白行数を指定</u>できます（小数可）。

**行間隔**の数字を変更することで文字の行間隔を調整できます。推奨値は14～16です。  
図はグループ化された図形オブジェクトとして出力されます。
出力された図はCopy/Pasteでパワポに貼り付けられます。フォントサイズなどもそちらで調整可能です。グループ解除して個別編集も可能です。  

シート上にある**GENERATE**セルをダブルクリックすると図を出力します。（<u>C4セルを指定して動作していますので、動かさないでください</u>）または、scehemeakerモジュールを**表示タブ>マクロ**から直接実行してください。  
また、シート上にある**CLEAR**セル（C5セル）をダブルクリックするとシート上のすべての図形を消去します。（出力した図ではなく、シート内のすべての図形オブジェクトを一括削除することに注意してください。）  

~~シート上では記載していませんが「**add**の横矢印の長さ」「**bar**の横線の長さ」「**add**や**bar**の横線の太さ」「**envbegin**-**envend**の縦線の太さ」「**wu**などのテキストの横位置」はVBAコードの冒頭で定数として指定しているので一括して調整可能です。必要に応じて変更してください。~~　動作未保障

***

## 【更新履歴】

2021.07.24
* 各描画要素を移動基準点（OrientX,Y）をもとに描画する方式に変更しました。  
* これに伴い複数の縦矢印を挿入できるようになりました。  
　※初版では特定のセルを基準点としていたため複数の矢印を挿入できませんでした  
* **space**, **bar**, **envbegin**/**envend**コマンドを追加しました。  
* 一部の不正な操作に対してエラーメッセージが出るようにしました。

2021.07.18
* 試作版を作成・公開しました｡
