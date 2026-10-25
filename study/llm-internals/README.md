# 小さなモデルを三つの角度から解剖する

小型モデル（Qwen2.5-0.5B / GPT-2）を主役に、一本の筋で学ぶ3冊のノートブックです。

| # | ノート | 幕 | 学ぶこと | 実行環境 |
|---|---|---|---|---|
| 1 | `01_quantization.ipynb` | 縮める | 量子化のサイズ・速度・perplexity トレードオフを実測 | GPU/CPU どちらも可 |
| 2 | `02_abliteration_paper.ipynb` | 方向を知る | 「拒否は1方向」論文(Arditi+2024)の読解（概念のみ・作図だけ） | 計算不要 |
| 3 | `03_interpretability.ipynb` | 中を覗く | Logit Lens / Activation Patching で事実想起を観察 | GPU/CPU どちらも可 |

## 物語
縮めて軽くし(1) → 中で意味がどう表されるかを知り(2) → 内部を直接読む顕微鏡を手に入れる(3)。

## 使い方
あなたのPCで実行してください（このクラウド環境は PyTorch と外部DLが無効なため実行不可）。

```bash
# ノート1
pip install torch transformers bitsandbytes accelerate datasets matplotlib pandas
# ノート3
pip install transformer_lens torch matplotlib
jupyter lab   # もしくは VS Code で開く
```

## 方針について
ノート2は abliteration を**概念として理解する読解ノート**で、安全対策を取り除くコードは含みません。
ノート3では、その論文と同じ解釈性の道具（内部状態を読む・差し替えて因果を見る）を、
**事実の想起という無害な題材**で自分の手で動かします。
