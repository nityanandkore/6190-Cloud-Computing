# Discussion 5

## How does the CAP Theorem play a role in designing for the cloud?

CAP Theorem states that any shared-data system can, at most, have two of following properties: consistency, availability and (tolerance to network) partitions.
 
Consistency: Every read receives the most recent write or an error
Availability: Every request receives a (non-error) response, without the guarantee that it contains the most recent write
Partition tolerance: The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes
 
With availability of modern cloud technology, there now is more flexibility for handling partitions and recovery. Therefore, with the new technology, designers can now aim to maximize combinations of consistency and availability that make sense for specific usage.


## What are the implications of Amdahl’s law for Machine Learning projects?

Amdahl's law is used to get an idea about where to optimize while considering parallelism. The theory of doing computational work in parallel has some fundamental laws that place limits on the benefits one can derive from parallelizing a computation.
Processor comes with some other resources like cache which can affect the performance. So, if we add more processor, cache memory also increases. Each processor will get less data size to process that can fit into processor's cache which will increase the Performance(Superlinear speedup). But Amdahl's Law considers processors as the only resource but does not consider cache memory.
Amdahl’s law expresses the law of diminishing returns. You can add an enhancement that speeds up an operation in processor. This serves as a guide to how much will improve performance of a model in machine learning and how to distribute resources to improve the performance of a model. This can also be used to compare two models to see which model performs better.

## Post a screenshot of a lab where you had difficulty with a concept or learned something.
*In progress*
