# publish_pose_from_tf

A simple ROS node to publish geometry_msgs/PoseStamped from listened tf.

The node lookups transform between base_frame and pose_frame for current time 
and publishes pose_frame's pose relative to base_frame if the transform available.

## Usage

```
rosrun publish_pose_from_tf publish_pose_from_tf _base_frame:=map _pose_frame:=base_link
```

## Published topic

* `~pose` (geometry_msgs/PoseStamped)

  pose_frame's pose relative to base_frame.

  Timestamp is same to the transform lookuped.

## Parameters

* `~base_frame` (string)

  Used as output pose's reference coordinate

* `~pose_frame` (string)

  This frame's pose relative to base_frame will be published as geometry_msgs/PoseStamped

* `~timeout` (double, default: 1.0)

  Timeout(sec) for lookup transform between base_frame and pose_frame
