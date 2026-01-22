# Run Instructions Template

Replace all placeholders with the exact steps needed to build and run your submission in the grader's `grading_ws`. Keep commands copy-pastable (Avoid adding '$' or '>' prompts).

## Dependency Setup
```bash
# From grading_ws
rosdep install --from-paths src --ignore-src -r -y
```
- Extra setup (if any):

## Build
```bash
# From grading_ws
colcon build --packages-select your_pkg
source install/setup.bash
```
- Notes on build options or warnings to expect:

## Launch (recommended)
```bash
ros2 launch your_pkg your_launch.py
```
- Parameters file used (path and how to override):

## Individual Nodes (if graders need to run separately)
```bash
ros2 run your_pkg talker --ros-args --params-file path/to/params.yaml
ros2 run your_pkg relay
```
- Topics expected (i.e `drive`, `drive_relay`):
- Parameter defaults (i.e for `v` and `d`):

## Verification Steps
- `ros2 topic list` should show:
- `ros2 node list` should show:
- Any other checks or logs to expect:

## Troubleshooting
- Common issues and fixes (missing deps, permissions, sourcing, etc.):
