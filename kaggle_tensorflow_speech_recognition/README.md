
# 仮想環境作成
Anacondaのパスを通し、condaコマンドが利用可能か確認する。  
以下のコマンドで仮想環境を作成する。  
```shell
conda create -n {環境名} python=3.10
```
仮想環境を起動する  
```shell
conda activate {環境名}
```
ライブラリをインストール  
- `scripts/iTransformer.ipynb` を実行する場合
```shell
pip install -r require_itrans.txt --user
```
- `scripts/Prophet.ipynb` を実行する場合
```shell
pip install -r require_prophet.txt --user
```


# データの探索的分析

```
# (オプション) 仮想環境のインストール
pip install virtualenv
# 仮想環境の構築
virtualenv venv
# 仮想環境をアクティベート
. venv/bin/activate

# 必要なライブラリをインストール
pip install -r requirements.txt

# jupyter notebook をバックグラウンドで動かす
nohup jupyter notebook &

# Webブラウザで http://localhost:8000 に接続した後, 
# 01_EDA/EDA.ipynb ファイルを実行
```

# Baseline モデル

```
cd 02_Baseline

# Baselineモデルの実行
python prepare.py
python trainer.py
```

# 勝者のコード

```
cd ../03_Winners_Code

# 勝者のコードを再現
python train.py
python base_average.py
python semi_train.py
python finetune_train.py
python final_average.py
```
