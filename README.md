# Natural Language Satisfiability: Exploring the Problem Distribution and Evaluating Transformer-based Language Models

Efforts to apply transformer-based language models (TLMs) to the problem of reasoning in natural language have enjoyed ever-increasing success in recent years. The most fundamental task in this area to which nearly all others can be reduced is that of determining satisfiability. However, from a logical point of view, satisfiability problems vary along various dimensions, which may affect TLMs' ability to learn how to solve them. The problem instances of satisfiability in natural language can belong to different computational complexity classes depending on the language fragment in which they are expressed. Although prior research has explored the problem of natural language satisfiability, the above-mentioned point has not been discussed adequately. Hence, we investigate how problem instances from varying computational complexity classes and having different grammatical constructs impact TLMs' ability to learn rules of inference. Furthermore, to faithfully evaluate TLMs, we conduct an empirical study to explore the distribution of satisfiability problems.

### Data Constuction

We construct data by sampling from ``phase-change region`` (region around which the probability of satisfiability is around 0.5); refer to the visulisation of how probability of satisfiability vary with number of unary predicates and number of binary predicates below. 

```
data_construction.py   --fragment <FRAGMENT> \
    --max_a <maximum number of unary predicates> \
    --min_a <minimum number of unary predicates> \
    --max_b <maximum number of binary predicates> \
    --min_b <minimum number of binary predicates> \
    --sampling_file <link to the sampling file> \
    --max_ab <max prob(sat)> \
    --min_ab <max prob(sat)> \
    --time_out <time out for the sat solver> \
    --prob <probility for complex fragment compared to simple ones> \
    --num_datapoints 4000 \
    --output_file "data-construction/numerical_k_diff.csv" \
```