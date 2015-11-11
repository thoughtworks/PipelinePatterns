# Layered with Artifact Promotion

You have a very active pipeline that is producing a lot of artifacts. This is slowing down your artifact server, or even causing it to run out of disk space.

** How can you retain the important artifacts while archiving or deleting the others? **

![Diagram](http://thoughtworks.github.io/PipelinePatterns/imgs//layered_with_repo.png)

The layered pattern can easily be enhanced by adding a separate artifact repository for each layer. The stage that promotes from one layer to the next becomes responsible for pushing artifacts from one layer to the next.

This has several benefits:
* Artifact retention policies become easier, because you can set a different policy for each layer. You could keep bronze for 2 weeks, silver for 2 months, and gold for 2 years.
* The layered approach to artifact servers may be familiar to operations. Many projects and organizations traditionally have different repositories based on the level of testing of the artifact. Linux distributions are a good example.
* If stages in different layers happen in different data centers (as a result of stages becoming "more production like" as they flow through the layers) then this is a good opportunity to sync the changes from one data center to another. This gives more visibility to the sync process and times than using a proxy or a cron job to sync artifacts between artifact servers in different locations.
