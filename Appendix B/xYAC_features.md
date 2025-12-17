### xYAC Feature Dictionary

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
| **Proximity Info** | `num_defenders_in_front` | Count of defenders positioned between the receiver and the passer. |
| | `num_defenders_behind` | Count of defenders positioned between the receiver and the endzone. |
| | `defenders_within_1_yard` | Count of defenders within 1 yard (immediate coverage). |
| | `defenders_within_3_yards` | Count of defenders within 3 yards (tight coverage). |
| | `defenders_within_5_yards` | Count of defenders within 5 yards (loose coverage). |
| **Defender Info** | `defender[1-5]_dist_to_receiver` | Euclidean distance from the $i$-th closest defender to the receiver. |
| *(Top 5 sorted by dist)* | `defender[1-5]_relative_depth` | **Vector Projection:** <br>(+) Defender is deeper than WR ("Over"). <br>(-) Defender is underneath ("Under"). |
| | `defender[1-5]_horizontal_leverage`| **Signed Cross Product:** <br>(+) Defender is to the LEFT of the flight path. <br>(-) Defender is to the RIGHT of the flight path. |
| **YACOE Info** | `defenders_ahead` | Weighted count of defenders specifically blocking the path to the endzone. |
| | `sideline_danger` | A penalty metric increasing as the receiver gets closer to the sideline (limits YAC potential). |
| | `orientation_penalty` | Metric quantifying if the receiver is facing away from the endzone (requires turning before running). |
| | `receiver_dist_to_goal` | Euclidean distance from the receiver to the goal line. |
| | `downfield_velocity` | The component of the receiver's speed vector directed specifically toward the endzone. |
| | `defender_isolation_gap` | The distance to the nearest defender relative to other defenders (isolation metric). |
| | `cone_open_space` | Percentage/Area of an imaginary cone projected downfield from the receiver that is free of defenders. |
