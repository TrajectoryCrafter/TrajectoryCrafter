## Important configuration for [inference.py](../inference.py):

### 1. General configs
| Configuration     | Default Value   | Explanation                                              |
|:----------------- |:--------------- |:-------------------------------------------------------- |
| `--video_path`    | `None`            | Input video file path                                    |
| `--out_dir`       | `./experiments/`| Output directory                                         |
| `--device`        | `cuda:0`        | The device to use (e.g., CPU or GPU)                     |
| `--exp_name`      | `None`           | Experiment name, defaults to video file name             |
| `--seed`          | `43`            | Random seed for reproducibility                          |
| `--video_length`  | `49`            | Length of the video frames (number of frames)            |
| `--fps`           | `10`            | fps for saved video                  |
| `--stride`        | `1`             | Sampling stride for input video (frame interval)         |
| `--server_name`   | `None`            | Server IP address  for gradio                           |
### 2. Point cloud render configs

| Configuration     | Default Value   |   Explanation                                              |
|:----------------- |:--------------- |:-------------------------------------------------------- |
| `--radius_scale`  | `1.0`           | Scale factor for the spherical radius                    |
| `--camera`        | `traj`          | Camera pose type, either 'traj' or 'target'                   |
| `--mode`          | `gradual`       | Mode of operation, 'gradual', 'bullet', or 'direct'      |
| `--mask`          | `False`         | Clean the point cloud data if true                       |
| `--target_pose`   | `None`            | Required for 'target' camera pose type, specifies a relative camera pose sequece (theta, phi, r, x, y). +theta (theta<50) rotates camera upward, +phi (phi<50) rotates camera to right, +r (r<0.6) moves camera forward, +x (x<4) pans the camera to right, +y (y<4) pans the camera upward  |
| `--traj_txt`      | `None`           | Required for 'traj' camera pose type, a txt file specifying a complex camera trajectory ([examples](../test/trajs/loop1.txt)). The fist line is the theta sequence, the second line the phi sequence, and the last line the r sequence |
| `--near`          | `0.0001`        | Near clipping plane distance                             |
| `--far`           | `10000.0`       | Far clipping plane distance                              |
| `--anchor_idx`    | `0`             | One GT frame for anchor frame                            |


