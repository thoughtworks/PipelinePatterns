# Release Channels

You have stakeholders, either other teams within the organization, or early adopters and beta users, that want to have access to release candidates before they reach production.

** How can you simply implement the distribution of release candidates to interested parties? **

![Diagram](http://thoughtworks.github.io/PipelinePatterns/imgs//layered_with_channels.png)

The layered pattern with artifact promotion can easily support release channels. A release channel let's someone subscribe based on their preference of frequent (but possibly unstable) releases, or infrequent but well-tested releases.

For example, the Chrome browser has a daily, beta, and stable release channel. Many Linux distributions have something similar.
