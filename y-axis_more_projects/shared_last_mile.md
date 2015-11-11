# Shared Last Mile

You have a bunch of applications that are independently deployable and independently testable - to a point.

** How can you ensure that only a group that has been tested together goes to production? **

![Diagram](file:///Users/Thoughtworker/repos/PipelinePatterns/patterns/imgs/shared_last_mile.png)

Use the shared last mile pattern. This let's each of the applications have an independent portion of the pipeline, but brings them together at some point for final integration and cross-fuctional requirement testing, and ensures that the versions that goes to production are the group that have passed the final testing together.
