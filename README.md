
# Athena_assesment

### 目標　
オイル温度予測モデルの構築

### カラム説明
- date：​記録日時

- HUFL：​High UseFul Load（高負荷時の有効負荷）

- HULL：​High UseLess Load（高負荷時の無効負荷）

- MUFL：​Medium UseFul Load（中負荷時の有効負荷）

- MULL：​Medium UseLess Load（中負荷時の無効負荷）

- LUFL：​Low UseFul Load（低負荷時の有効負荷）

- LULL：​Low UseLess Load（低負荷時の無効負荷）

- OT：​Oil Temperature（油温）

### データ分析手法
- pairplot,heatmapによる特徴量分析
- ２年分のデータを分割し１年分のデータずつプロットすることによるデータのトレンド性および季節性の有無の確認
### 回帰モデル
-SVM(時系列性を考慮しないモデル)
models2にグリッドサーチを行ったモデルの重みがbest_svr_model.pklという名前で保存されている。
-Autoformer(データの時系列性を考慮したモデル)
学習の中で一番精度がよかったモデルの重みをmodelsにbest_model.pthという名前で保存している。
またその際のoptimizer情報をmodelsのbest_optimizer.pthに保存している
