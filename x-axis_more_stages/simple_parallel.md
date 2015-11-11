# Simple Parallel

You had a simple pipeline but many stages are starting to be added for to support many different types of testing activities.

**How do you keep the time to production short?**


![Diagram](http://thoughtworks.github.io/PipelinePatterns/imgs//parallel.png)

Run stages in parallel when possible. If two or more activities are orthogonal, like scanning for security vulnerabilities, testing performance, and running a suite of functional regression tests, you should be able to perform those activities simultaneously.

This is a good way to speed up a pipeline with many stages, but the pipeline may become very complex. You are also creating explicit dependencies between test stages, so reordering them later may become difficult. You may want to considered the layered pattern, a similar but more organized alternative.

