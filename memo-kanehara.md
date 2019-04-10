# Mon
## Tutorial #3: Formal Verification for an Internet of Secured Things
Frama-CというC言語のソースコード中の脆弱性を自動検出するツールの紹介．
e.g.) ゼロ割・初期化されていないなどの場合警告を出してくれる．
どこまで条件分岐やイテレーションの状態を同時に考慮するかを決定するparameterがあり，
計算コストと検知精度ののトレードオフがある．

Weakly Precondition (WP) plugin の紹介
- コメント形式でC言語の関数などに対して満たしてほしい条件を記述できるFrama-Cのプラグイン．
- 入力・出力される値の条件など．

# Tue
## DM-1: Data Mining
### AN ANOMALY DETECTION TECHNIQUE FOR BUSINESS PROCESSES BASED ON EXTENDED DYNAMIC BAYESIAN NETWORKS
[WIP]
Business Process:
注文システムを例に上げると， Aさんが注文→Bさんが注文の処理を行う→Cさんが商品の調達を行うなどの一つ一つの処理のこと．

人工データとBPI Challengeデータセットで実験


### DIRICHLET PROCESS MIXTURE MODELS MADE SCALABLE AND EFFECTIVE BY MEANS OF MASSIVE DISTRIBUTION
ディリクレ過程混合モデル (DPM) はクラスタ数を仮定しないモデルで，
逐次的にクラスタを割り当てる柔軟な手法であるが，計算コストが高いためデータ数が増えると難しい．

そこで，Sparkによる分散並列処理で計算できるように
通常のDPMに重みパラメータを追加し，DPMを拡張した．
スケーラビリティを計測したところ，通常はデータ数に対して指数オーダで計算時間が増加するが，
提案手法は線形オーダに済んだ．

人工データによる実験では問題のない精度でクラスタ割当が行えたことを示した．
評価指標としてAdjusted Rand Indexを用いている．

### PAIRWISE NORMALIZATION IN SIMRANK VARIANTS: PROBLEM, SOLUTION, AND EVALUATION
SimRankはグラフ構造におけるノード間の類似度を求める手法だが，
オリジナルのSimRankにより算出されたスコアにはPairwise Normalization Problemがあるため改善が必要．
これを解決するための手法はすでにいくつか提案されているが，これらを一般化した形にまとめた．

### GRAPH-BASED SELECTIVE OUTLIER ENSEMBLES
[WIP]
外れ値検知

## DM-2: Data Mining
### EXPLAINING BLACK BOX MODELS BY MEANS OF LOCAL RULES
[WIP]
目的: 機械学習モデルの解釈性を上げること

LACE: K最近傍法によってローカルルールを適用する
他に有名なブラックボックスモデルのためのLIMEと比較した．


## SONAMA-2: Social Network and Media Analysis
### KIDSGUARD: FINE GRAINED APPROACH FOR CHILD UNSAFE VIDEO REPRESENTATION AND DETECTION
子供に見せられない，アダルトコンテンツの判定．
既存手法では動画全体に対して判別する手法が提案されているが，こちらは粒度がより細かく，特定のシーンに対して危険なコンテンツがあればそのシーンにフラグをつける．

画像識別の学習済みモデルであるVGG-16を使用して動画の特徴抽出を行い，
その結果を入力とするLSTMベースのオートエンコーダーで前後関係を考慮した特徴抽出を
更に行い判別するモデルを提案．
その他比較手法よりも最も精度が高かった．

