


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