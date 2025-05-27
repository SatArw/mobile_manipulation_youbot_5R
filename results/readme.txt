FeedForward controller with velocity inputs

Kp =[[1, 0, 0, 0, 0, 0],
    [0, 1, 0, 0, 0, 0],
    [0, 0, 1, 0, 0, 0],
    [0, 0, 0, 1, 0, 0],
    [0, 0, 0, 0, 1, 0],
    [0, 0, 0, 0, 0, 1]]

Ki =[[1, 0, 0, 0, 0, 0],
    [0, 1, 0, 0, 0, 0],
    [0, 0, 1, 0, 0, 0],
    [0, 0, 0, 0, 0, 0],
    [0, 0, 0, 0, 0, 0],
    [0, 0, 0, 0, 0, 0]]

----------------------------------------------------------------------------------
reference_initial_configuration = [0, 0, 0 , 0, -0.7, -1.7, 0.5, 0, 0, 0, 0, 0]
actual_initial_configuration = [0.2, 0.05, 0.05 , 0, -0.17, -1.57, 0.45, 0, 0, 0, 0, 0, 0]

----------------------------------------------------------------------------------
joint_speed_limit = 6 rad/s
wheel_speed_limit = 1 m/s

----------------------------------------------------------------------------------
Time duration for each segment in seconds - CartesianTrajectories used for all segments
[30, 10, 10, 50, 10, 10, 10, 10]

----------------------------------------------------------------------------------
Standoff configuration relative to cube

[[cos(phi_standoff), 0, sin(phi_standoff), 0],
[0, 1, 0, 0],
[-sin(phi_standoff), 0, cos(phi_standoff), 0.06],
[0, 0, 0, 1]]

----------------------------------------------------------------------------------
Grasp configuration relative to cube

[[cos(phi_standoff), 0, sin(phi_standoff), 0],
[0, 1, 0, 0],
[-sin(phi_standoff), 0, cos(phi_standoff), 0],
[0, 0, 0, 1]]

where phi_standoff = 90 degrees

----------------------------------------------------------------------------------
No joint limits implemented.  