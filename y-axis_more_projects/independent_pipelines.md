# Independent Pipelines

You want to do continuous delivery with many unrelated or loosely related applications.

** How can you put them all in production? **

![Diagram](http://thoughtworks.github.io/PipelinePatterns/imgs//independent_pipelines.png)

You can give each one a separate pipeline for deploying to production. If your CD tool has support for defining environments, you could create a production environment associated with the production deploy from each pipeline, so you'll have a simple way to see the versions and production deployment history of all of the applications.
