---
layout: post
title: "Attention is all you need"
date: 2024-12-13
categories: [AI]
author: Vipul Kumar Singh, claud.ai
---

_These are notes and thoughts on the [Attention is All You Need](https://arxiv.org/abs/1706.03762) paper._

RNNs (Recurrent Neural Network) and LSTM (Long Short-Term Memory) were the state-of-the-art for sequence tasks like translation, but their sequential nature limits parallelization and efficiency. The praper proposes Transformer architecture, that replaces recurrence with attention mechanisms, enabling parallel processing and achieving superior translation quality with significantly less training time.

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

<h3>Concept of Attention</h3>

Before we dive into the Transformer architecture, let's first understand the concept of attention, with Start Wars and Harry Potter Analogy.

<b>Star Wars Analogy:</b> When lifting the X-wing from the swamp, Luke specifically focuses on the X-wing (high attention weight) while ignoring rocks and trees (low attention weights), even though all objects are within his Force reach.

![Star Wars Analogy]({{ site.url }}/assets/luke_force.png)

<b>Harry Potter Analogy:</b> When Harry casts his strongest Patronus, he doesn't give equal weight to all memories. Instead, he specifically focuses on powerful happy memories (high attention) while automatically filtering out memories of the Dursleys (low attention), even though all memories are technically available to him.

![Harry Potter Analogy]({{ site.url }}/assets/harry_patronus.png)

In both cases, attention works like a selective focus mechanism, automatically weighing what's important for the current task while still having access to everything.

<h3>Attention Mechanism in Transformer Architecture</h3>

The Attention mechanism is a fundamental innovation in the Transformer architecture that enables the model to focus on relevant parts of the input when producing output. However, when processing language, a single attention mechanism may be insufficient to capture the complexity of language. Just as humans understand language by simultaneously considering multiple aspects like grammar, context, and tone, the model needs to analyze the input from various perspectives. This is where Multi-Head Attention becomes crucial. 

<b>Multi-Head Attention</b> Multi-Head Attention works like a team of experts studying a problem from different angles. Instead of one person analyzing everything, you have eight specialists each focusing on different aspects - like how your brain simultaneously processes grammar, context, and tone in a sentence. One head might focus on grammar, another on context, while others look at word relationships. Their individual findings are then combined to create a complete understanding, making it powerful at catching various patterns and connections in the data.

<div class="mermaid">
graph TD
    I[Input] --> H1[Head 1<br>Focus on grammar] & H2[Head 2<br>Focus on context] & H3[Head 3<br>Focus on tense] & H4[Head 4<br>...]
    H1 & H2 & H3 & H4 --> C[Combine Results]
    C --> O[Final Output]
</div>

<h3>Encoder & Decoder</h3>

Encoder and Decoder are the two main components of the Transformer architecture. We can think of the encoder as a thorough reader creating a complete understanding, and the decoder as a careful writer using that understanding to generate output one piece at a time. Transformer architecture uses encoder-decoder model to process sequence data. 

- <b>The Encoder</b> takes input sequence (like an English sentence) and transforms it into a continuous representation (z) that, in some sense, captures the meaning.
- <b>The Decoder</b>  generates the output sequence (like a French translation) one element at time, using both the encoded representation and its own previously generated outputs

<div class="mermaid">
graph LR
    subgraph Encoder
        I1[x₁] & I2[x₂] & I3[x₃] --> E1[Encoder Block]
        E1 --> Z1[z₁] & Z2[z₂] & Z3[z₃]
    end
    
    Z1 & Z2 & Z3 --> D[Decoder Block]
    Y0[Start] --> D --> Y1[Current Output]
    Y1 -->|Feed Next Step| D

    classDef input fill:#F0F8FF,stroke:#333
    classDef encoder fill:#E6E6FA,stroke:#333
    classDef middle fill:#FFE4E1,stroke:#333
    classDef decoder fill:#E0FFFF,stroke:#333
    classDef output fill:#E0FFF0,stroke:#333

    class I1,I2,I3,Y0 input
    class E1 encoder
    class Z1,Z2,Z3 middle
    class D decoder
    class Y1 output
</div>

<h3>Putting it all together</h3>

_The image on the right is taken from the paper._

![Transformer Model]({{ site.url }}/assets/transformer_model.png){: style="float: right; width: 50%;"}

In the Transformer model, at its core, the encoder processes the entire input simultaneously, while the decoder generates output sequentially. The architecture's key innovation lies in its multi-head attention mechanism, where eight parallel attention processors analyze different aspects of the input concurrently - capturing elements like grammar, context, and word relationships.

**The Processing Pipeline:** Each input first receives positional encoding - a clever way to timestamp words since the model processes them simultaneously. The data then flows through multiple layers of processing, each containing two main components: attention mechanisms and feed-forward networks. The feed-forward networks consist of two linear transformations with a ReLU activation (a simple function that passes positive numbers unchanged while zeroing out negatives) in between, processing information from the attention layer.

The Transformer employs several techniques to maintain stable and effective training. Residual connections act as shortcuts, adding each layer's input to its output to prevent signal degradation in deep networks. Layer normalization stabilizes the learning process by standardizing values at each layer, similar to standardizing test scores. Finally, the softmax function converts the model's raw outputs into probabilities, enabling the model to make decisions about word selection in tasks like translation.

Through this combination of innovative components, the Transformer achieves high-quality sequence transformations more efficiently than its predecessors, setting new standards in natural language processing tasks.

