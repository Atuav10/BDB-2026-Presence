### Completion Probability Feature Dictionary

| Category | Feature Name | Description |
| :--- | :--- | :--- |
| **Play Context** | `absolute_yardline_number` | The specific yard line (0-100) where the play is occurring. |
| | `distance_from_los` | The receiver's depth downfield relative to the Line of Scrimmage. |
| | `distance_from_sideline` | Minimum distance from the receiver to the nearest sideline. |
| | `time_in_air` | Seconds elapsed since the pass was released (for frame-by-frame tracking). |
| | `yards_to_go` | Distance required for a first down. |
| | `defenders_in_the_box` | Count of defenders in the "box" area (near the line of scrimmage) at the snap. |
| | `dropback_distance` | Distance the QB retreated behind the line of scrimmage. |
| **Receiver Info** | `receiver_x` / `receiver_y` | Absolute field coordinates of the receiver. |
| | `s` / `a` | Speed (yards/sec) and Acceleration (yards/sec²). |
| | `dir` / `o` | Direction (movement angle) and Orientation (body facing angle). |
| | `initial_receiver_x` / `y` | Receiver's starting coordinates at ball released. |
| | `lagged_receiver_x` / `y` | Receiver's position at the previous timestep ($t-1$). Used to capture immediate trajectory changes. |
| | `lagged2_receiver_x` / `y` | Receiver's position two timesteps ago ($t-2$). |
| **QB Info** | `qb_distance_from_target` | Euclidean distance between the QB and the target receiver at the current frame. |
| | `qb_distance_from_sideline` | QB's proximity to the sideline. |
| | `qb_release_x` / `y` | Fixed coordinates of the QB at the moment of pass release. |
| | `qb_release_s` / `a` | Speed and acceleration of the QB at the moment of release. |
| | `num_defenders_within_2_yards_qb`| Count of defenders immediately pressuring the QB. |
| | `num_players_within_5_yards_qb` | Pocket density (teammates + defenders) around the QB. |
| **Proximity Info** | `num_defenders_in_front` | Count of defenders positioned between the receiver and the passer. |
| | `num_defenders_behind` | Count of defenders positioned between the receiver and the endzone. |
| | `num_defenders_in_passing_lane` | Count of defenders intersecting the direct vector between QB and Receiver. |
| | `defenders_within_1_yard` | Count of defenders within 1 yard (immediate coverage). |
| | `defenders_within_3_yards` | Count of defenders within 3 yards (tight coverage). |
| | `defenders_within_5_yards` | Count of defenders within 5 yards (loose coverage). |
| **Defender Info** | `defender[1-5]_dist_to_receiver` | Euclidean distance from the $i$-th closest defender to the receiver. |
| *(Top 5 sorted by dist)* | `defender[1-5]_relative_depth` | **Vector Projection:** <br>(+) Defender is deeper than WR ("Over"). <br>(-) Defender is underneath ("Under"). |
| | `defender[1-5]_horizontal_leverage`| **Signed Cross Product:** <br>(+) Defender is to the LEFT of the flight path. <br>(-) Defender is to the RIGHT of the flight path. |
| | `defender[1-5]_dist_from_path` | **Absolute Cross Product:** The perpendicular distance from the defender to the ball's flight path. |
