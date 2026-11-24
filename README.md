<h1 align="center">
Conflict-Guided Relational Commonsense Routing and Heterogeneous Graph Reasoning for Multimodal Emotion Recognition in Conversations
</h1>

<p align="center">
Jia Liu, Shiqi Wu, Yongze Li, Manyi Han, Lina Wei, and Dapeng Chen*<br>
Nanjing University of Information Science and Technology
</p>

---

<h2 align="center">ABSTRACT</h2>
Multimodal emotion recognition in conversations integrates text, audio, and visual information according to dialogue context and speaker interactions to infer the emotion expressed by each utterance. However, emotional cues from different modalities may disagree, while implicit intentions and psychological reactions cannot be inferred from surface semantics alone. A key challenge is to use cross-modal disagreement to guide the selection of external commonsense and to incorporate the selected commonsense into contextual dialogue reasoning. To this end, we propose a conflict-guided framework for relation-level commonsense routing and heterogeneous graph reasoning (CGR-HGR). The framework retains pairwise differences among the three modalities through a three-dimensional conflict vector, dynamically assigns commonsense-relation weights jointly with utterance semantics, and forms knowledge-enhanced representations through reliability modulation and gated residual connections. Selected relation knowledge and utterances constitute a heterogeneous graph, in which conflict conditions further regulate edge weights and message propagation, enabling commonsense to support emotion inference in dialogue context. On IEMOCAP and MELD, the mean accuracies over five runs are 75.11% and 67.58%, and the mean weighted F1 scores are 75.25% and 66.63%, respectively. Compared with the five-run mean of SDT, weighted F1 improves by 1.64 and 1.31 percentage points, respectively.

---

# Conflict-guided Heterogeneous Knowledge Graph for Multimodal ERC

This repository contains the source code of our paper, using the following datasets:

- [IEMOCAP](https://drive.google.com/file/d/1y4xLSKicRHZCd7dsG5y75TFecvHHyY3Q/view?usp=drive_link) — Download the preprocessed dataset and put it into `data/`.
- [MELD](https://drive.google.com/file/d/1H8NAwW_ogxsFOQvCuesxiVqBqa8X19J-/view?usp=drive_link) — Download the preprocessed dataset and put it into `data/`.

## 1. Install requirements

```bash
pip install -r requirements.txt
```

## 2. Prepare datasets

Download the preprocessed datasets and put them into `data/`.

## Train

We provide training commands aligned with the paper settings.

```bash
# IEMOCAP

python -u train.py --Dataset IEMOCAP --use-knowledge --use-graph 

# MELD
python -u train.py --Dataset MELD --use-knowledge --use-graph 
```
