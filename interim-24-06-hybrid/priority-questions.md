# Questions about Priority Solutions

1. What is the scope of priority (eg: what does it apply to)?
2. What is the priority model (eg: HTTP/2 tree, urgency/incremental, send order)?
3. Who can send a priority signal (publisher, subscriber, both)?
   1. How are conflicting signals merged?
5. What is the granularity of the signal?
6. Can priorities change over time?
7. Are the signals extensible?

# Evaluation Criteria

Some possible criteria for evaluating a priority solution might be:

1. _Adequate Expressiveness_ - can the desired order of bits be achieved for all use cases?
2. _API Simplicity_ - will applications be able to use the priority system to achieve their goals?
3. _Fairness_ - can the system be gamed?
4. _Implementation Complexity_ - how hard is it to build correctly and maintain?
5. _Wire Efficiency_ - what is the overhead of the signal?
6. _Runtime Efficiency_ - is the algorithm efficient?
7. _Extensibility_ - can the signal be updated?
8. _Fit_ - how does the system interact with other protocol features like Forwarding Preferences, Max Cache Duration, Delivery Timeouts and drops?
