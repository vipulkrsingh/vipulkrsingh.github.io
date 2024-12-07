---
layout: post
title: "Attention is all you need"
date: 2024-12-07
categories: [AI]
---

These are notes and thoughts on the [Attention is All You Need](https://arxiv.org/abs/1706.03762) paper.

RNNs and LSTMs have been state-of-the-art for sequence tasks like translation, but their sequential nature limits parallelization and efficiency. The Transformer architecture replaces recurrence with attention mechanisms, enabling parallel processing and achieving superior translation quality with significantly less training time.

<div class="mermaid">
graph TD

    subgraph "Transformer Model"
        D1[Input1] --> E1{Self-Attention}
        D2[Input2] --> E1
        D3[Input3] --> E1
        E1 --> F1[Output1]
        E1 --> F2[Output2]
        E1 --> F3[Output3]
        
        style E1 fill:#E0FFFF,stroke:#333
    end

    subgraph "RNN/LSTM Model"
        A1[Input1] --> B1[Hidden State h1]
        B1 --> C1[Output1]
        B1 --> B2[Hidden State h2]
        A2[Input2] --> B2
        B2 --> C2[Output2]
        B2 --> B3[Hidden State h3]
        A3[Input3] --> B3
        B3 --> C3[Output3]
        
        style B1 fill:#E6E6FA,stroke:#333
        style B2 fill:#E6E6FA,stroke:#333
        style B3 fill:#E6E6FA,stroke:#333
    end

    classDef input fill:#F0F8FF,stroke:#333
    class A1,A2,A3,D1,D2,D3 input
    classDef output fill:#E0FFF0,stroke:#333
    class C1,C2,C3,F1,F2,F3 output
</div>
