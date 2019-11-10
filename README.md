# 首藤研総合演習2019 (グラフ分野)
首藤研の2019年度研究プロジェクト第2ラウンドのページです．**グラフサンプリング**という分野を扱います．

# 場所・時間・日程
* 場所: 首藤研 学生室 (西8号館 W棟 8階 810号室)
* 時間: 15:05 ~ 16:35
* 日程:
	* 11/12 導入 (グラフサンプリングの概要, slack加入, 輪講担当決め)，環境構築 (Python, NetworkX)
	* 11/19 輪講第1回 (中嶋)
		* 1, 2章: イントロダクション, 関連研究
	* 11/26 輪講第2回 ()
		* 3章のⅢ.C以外: 事前知識やサンプリング手法の概要．
	* 12/3  輪講第3回 ()
		* 4章: Facebookのグラフデータのサンプリング．
	* 12/10 輪講第4回 ()
		* 5章のA, C: Adding convergence diagnostics and parallel crawls.以外: サンプリング手法の比較．
	* 12/17 質問，レポート作成の目処を立てる．

# 目的
* 研究のプロセス (既存の知識・方法を理解・実装する → 改善案・新しい知見を見出す → 論文を書いて世に公表する)の一部を体験する．

# 目標
1. グラフサンプリングの論文を読んで既存の知識・方法を理解・実装する．
	* 読む論文
		* メイン: Walking in Facebook: A Case Study of Unbiased Sampling of OSNs [Gjoka et al., 2010]
			* 輪講形式で論文を読みます．
		* サブ: Practical Recommendations on Crawling Online Social Networks [Gjoka et al., 2011]
			* 上の論文の詳細版です．参考資料として使ってください．
	* 研究の背景，研究目的，問題点とそれに対するアプローチ・解決策，研究方法，特色を理解する．
	* Python (NetworkX)で既存の手法を実装・検証する．

1. 既存論文に対する改善案・新しい知見を考える．
	* 研究目的の達成に近づけるために何が必要か？を考える．
		* 例
			* 従来の手法の精度を向上するために〜〜の点を改善しよう．
			* 従来の手法の応用範囲を広げるために〜〜のように拡張しよう．
			* 従来の研究で無視されていた新しい問題を定義し，研究の可能性を広げよう．
			* 他の分野の方法を応用して，全く新しい手法を提案しよう．
	* 「こうすればより良くなるのではないか？」という仮説を立てて検証する過程が醍醐味です．
	* 良い結果が出なくても構いません．まずは，考えて仮説を立ててみましょう．

# 輪講
* 自分が担当する範囲の内容を，他の人が理解できるようにスライドを使って説明する．
* 次以降の担当者のために，わかりやすいスライドを作る．そのためには自分が深く理解することが必須．
* 聞いている人は質問する．

# 課題レポート
* Texで書いてPDFで提出してください．サンプルを置いておきます．

* 以下の2つの内容を含めてください．
	1. 与えられたデータセットにおける，BFS，RW，MHRW, RWRWの4つの手法による次数分布推定の結果と考察．
		* 各手法の推定精度の実験結果
		* 各手法の推定精度の特徴の違いと考察
	1. ソーシャルネットワークの次数分布をより高精度に推定するための改善案・新しい知見．

* レポートは首藤先生に採点していただきます．わかりやすいレポートを心がけましょう．
	* レポートを書くときは，以下の点を心がけるといいかもしれません．
		* 目的，問題点とそれに対するアプローチ，特色を明確にする．
		* 事前知識 (グラフや各種統計量の定義, アクセスモデル，サンプリング手法の概要...)は，早い段階で1つの章にまとめて書く．
		* 実験で使ったデータセット，実験回数，サンプル数，誤差指標の定義...を明記する．
		* 改行・余白を上手に使う．
	* 先生に最終提出する前に，一度添削します．よって，以下の日程でそれぞれ提出してください．
		* 12/17: 第1稿を提出する．この時点である程度構成や文章は完成させてください．
		* 12/31 (予定): 添削結果を反映させて，最終版を提出する．

# 練習課題
* 輪講で得た知識をもとに，以下の順で練習課題を解いていくとスムーズに課題レポートに取り組めると思います．

	* **レベル0**
		* ファイル名を入力としてグラフGを返す関数を作る．
		* グラフGを入力としてGを表示する関数を作る．

	* **レベル1**
		* 正の整数nを入力として，ノード数nの完全グラフを返す関数を作る．
		* グラフGとノードvを入力として，vのクラスタ係数を返す関数を作る．
		* グラフGを入力として，Gの平均次数を返す関数を作る．

	* **レベル2**
		* グラフGを入力として，Gの次数分布を返す関数を作る．
		* グラフGを入力として，Gの次数分布の対数グラフを表示する関数を作る．
		* グラフGを入力として，Gの平均クラスタ係数を返す関数を作る．

	* **レベル3**
		* グラフGとサンプル数rを入力として，BFSによる長さrのサンプリングノード列を返す関数を作る．
		* グラフGとサンプル数rを入力として，RWによる長さrのサンプリングノード列を返す関数を作る．
		* グラフGとサンプル数rを入力として，MHRWによる長さrのサンプリングノード列を返す関数を作る．
			* 初期ノードはランダムに選択するでよい．
		* 2つの分布AとBを入力として，分布の誤差NRMSEを返す関数を作る．

	* **レベル4**
		* グラフGとサンプル数rを入力として，BFSによるGの次数分布の推定分布をプロットし，誤差NRMSEを返す関数を作る．
		* グラフGとサンプル数rを入力として，RWによるGの次数分布の推定分布をプロットし，誤差NRMSEを返す関数を作る．
		* グラフGとサンプル数rを入力として，MHRWによるGの次数分布の推定分布をプロットし，誤差NRMSEを返す関数を作る．
		* グラフGとサンプル数rを入力として，RWRWによるGの次数分布の推定分布をプロットし，誤差NRMSEを返す関数を作る．

	* **レベル5**
		* グラフGとサンプル数列{r1, r2, ...}を入力として，各サンプル数に対するBFSによるGの次数分布の推定分布の誤差NRMSEを返す関数を作る．
		* グラフGとサンプル数列{r1, r2, ...}を入力として，各サンプル数に対するRWによるGの次数分布の推定分布の誤差NRMSEを返す関数を作る．
		* グラフGとサンプル数列{r1, r2, ...}を入力として，各サンプル数に対するMHRWによるGの次数分布の推定分布の誤差NRMSEを返す関数を作る．
		* グラフGとサンプル数列{r1, r2, ...}を入力として，各サンプル数に対するRWRWによるGの次数分布の推定分布の誤差NRMSEを返す関数を作る．
			* サンプル数列は，グラフのノード数をnとして，{0.01n, 0.02n, 0.03n, 0.04n, 0.05n} (つまりサンプル率1 ~ 5%)でよいです．

	* **レベル6**
		* グラフGとサンプル数列{r1, r2, ...}，実験回数mを入力として，各サンプル数に対するBFSによるGの次数分布の推定分布の誤差NRMSEのm回の平均値を返す関数を作る．
		* グラフGとサンプル数列{r1, r2, ...}，実験回数mを入力として，各サンプル数に対するRWによるGの次数分布の推定分布の誤差NRMSEのm回の平均値を返す関数を作る．
		* グラフGとサンプル数列{r1, r2, ...}，実験回数mを入力として，各サンプル数に対するMHRWによるGの次数分布の推定分布の誤差NRMSEのm回の平均値を返す関数を作る．
		* グラフGとサンプル数列{r1, r2, ...}，実験回数mを入力として，各サンプル数に対するRWRWによるGの次数分布の推定分布の誤差NRMSEのm回の平均値を返す関数を作る．

	* **レベル7**
		* ソーシャルネットワークの次数分布推定における精度向上などに向けて，改善案や新しい知見を考える．

# その他
* 質問などあれば，slackへ．

