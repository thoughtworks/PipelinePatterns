# Pipeline Counter Labeling

You want a simple way to generate a meaningful version label.

** How do you generate a simple, sequential version label? **

Use the pipeline, stage, and/or job counter to build a version number when you create an artifact. Make sure that you only create new version numbers when creating a build artifact: if your pipeline is consuming an already built artifact it is better re-use the existing label.
