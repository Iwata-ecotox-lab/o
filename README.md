# Ecotox_Lab_iwata
 in silico data & program

# PLIF%表
1. PLIFデータ整理用<br>
*注意　三回分のドッキングシミュレーションに対するマクロであるため回数が増えたり減ったりすると使用できません。<br>
ドッキングデータをSheet1から順にU_dockスコア、PLIF、PLIFのアミノ酸残基、の順番でペーストする。<br>
（Sheet3は1行悪用にペーストされるが問題ない）<br>
データを取得後、Sheet3のD2から下に相互作用した種類別に分けて表記していく。<br>
例：Thr287DAA　→　Thr287D、ThrA、Thr287AA<br>
Sheet4を作成したあと、1. PLIFデータ整理用のコードをマクロに読み込ませて「すべてを実行するマクロ()」を実行する。<br>

2. PLIFデータ%まとめ<br>
1.で生成したSheet4のデータを新しいエクセルのSheet1-3にすべて貼り付ける。<br>
また新しいエクセルファイルでSheet4-8を作成する。<br>
Sheet8に先ほど編集したPLIFのアミノ酸残基をそれぞれA,C,E列の2行目に張り付ける。<br>
その後H列の1行目に"mseq"を、2行目からすべてのPLIFのアミノ酸残基を順番に表記する。<br>
例<br>
![image](https://github.com/yanakaru2020/Ecotox_Lab_iwata/assets/135199782/a677c137-6aca-446a-a887-4fe77fe483d8)

この際にSheet4,5,6には先ほど作成したH列を1行目にペーストする。
貼り付け後、このファイル内のマクロを読み込ませて「すべてを実行するマクロ()」を実行する。<br>

その後、相互作用の個数をカウントする行列を作成する。<br>
例<br>
![image](https://github.com/user-attachments/assets/bbed8522-a5ac-46fc-a2ef-41c10c300bab)

次にパーセントの行列を作成する<br>
例<br>
![image](https://github.com/user-attachments/assets/c183f4c7-f03f-4575-a53c-1ab369401f5e)

それぞれの画面に対応する式を書き入力してオートフィルを行う。<br>
オートフィルを終えたら1行目にフィルターをかけて、Chem列でENDのみ表示することでPLIF%表が完成する。<br>

# U_dock平均
