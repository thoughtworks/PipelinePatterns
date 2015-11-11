# Joint Labeling

You have a pipeline that depends on multiple upstream pipelines or materials with different version labels.

** How do you produce a meaningful label reflecting multiple materials? **

![Diagram](/imgs/imgs/joint_labels.png)

You can use the joint labeling pattern. This makes a compound label by joining the versions with a separator like '-'.

This pattern is sometimes encountered when one version is for the application version and the other is for the infrastructure version. It stops being useful if you have more than two or three versions.
