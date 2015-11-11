# Layered

You want to encourage testing to happen in parallel stages but you want the pipelines to remain easy to understand and refactor.

** How can you encourage simple parallel pipelines without tight coupling? **


![Diagram](/imgs/imgs/layered.png)

The layered pipeline pattern strongly encourages testing to happen in parallel, but discourages direct dependencies between test stages.

A simple version of this pattern was described in
[](http://link/to/cv/blog) as "Olympic Pipelines". It used precious metals - bronze, silver, and gold - as names for the layers so that anyone could easily understand the relationship between layers. The promotion from one layer to the next was made explicit, and pipeline order was defined by depending on the promotion into the layer where that pipeline was intended to run, rather than depending on each other.

This pattern makes it easy to refactor the pipeline order, because pipelines don't depend on each other. If you want to move a pipeline from one layer to a different one, you just change it to depend on the promotion to a different layer. If you want it to be required before the next promotion, then you just change the dependencies for the subsequent promotion.

Additionally, this pattern has strong cultural ties. Since it is easy to understand and talk about the progress of a release candidate through the layers you may find that everyone starts adopting the terminology and understanding the progression. Even the most non-technical stakeholders may begin asking "how long until this feature is 'silver'?" I
