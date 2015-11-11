# Aggregate Labeling

You have several related projects/applications that all have their own meaningful version numbers.

** How can you fan these in and still keep propagating a meaningful version on pipeline & environment labels? **

![Diagram](http://thoughtworks.github.io/PipelinePatterns/imgs//aggregate_labels.png)

Aggregate versioning is an alternative to joint labeling. It takes multiple versions and creates a new version to represent the group. Often this is combined with an aggregate manifest or artifact to represent the group.

This pattern can create a readible version label that corresponds to versions of many different components, but unlike the joint pattern you will need to look up the component version in the aggregate manifest or the upstream dependencies rather than being able to figure it out by glancing at the label.
