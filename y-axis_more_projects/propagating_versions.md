# Propagating Versions

You have information radiators or other dashboards that show information from your pipelines. But the version labels that are shown aren't related and are meaningless at a glance.

** How do you make the version label of every pipeline meaningful, so users can easily big the gaps are between pipeline runs or versions being deployed to different environments? **

![Diagram](/imgs/imgs/propagating_labels.png)

Propagate the version label downstream. Once you have created a meaningful version number, pass that version downstream and use it as the label for all subsequent pipelines.

This is especially useful for people to look at pipelines related to environments to see if they are in sync. For example, if you have pipelines named DeployToQA and a DeployToPerf, you want them to show the same version label if they have deployed the same version of the application. The default for most tools is to show the number of times those pipelines have run. You may have done the same number of deployments to different environments, but the latest deployment wasn't the same version. Similarly, you could have deployed a different number of times, but the environments are now in sync. So a pipeline-specific counter usually does not make a good label on dashboards.

Also, if your version numbers are sequential than people will be able to compare related pipelines to get an idea of how many changes have happened between them.
