# Lab Sample Submission Template

This repo shows the expected layout for Lab submissions. Files are placeholders only, and meant to guide you in structuring your own submission only, not as a starting codebase.

## Best practices
- Place your package inside a folder named after your repository (e.g., `your-repo/your_pkg`). This keeps the repository organized so README.md and SUBMISSION.md are at the root.
- Use clear, descriptive names for your package and nodes (e.g., `intro_pkg`, `talker`, `relay`).
- Keep `package.xml` clean with dependencies like `ackermann_msgs` declared.
- **Always** avoid committing `build/`, `install/`, or `log/` directories.

## Package contents (placeholders)
- `your_pkg/package.xml`, `CMakeLists.txt`, `setup.py`, `setup.cfg`: standard ROS2 package files.
- `your_pkg/src/` and `your_pkg/include/your_pkg/`: C++ node and header placeholders.
- `your_pkg/your_pkg/`: Python node placeholders.
- `your_pkg/launch/lab1_launch.py`: launch file placeholder.
- `your_pkg/params/params.yaml`: parameter placeholder.

## How graders will use your repositories to test your code
- Clone your repo into `grading_ws/src`, then from `grading_ws` run `rosdep install --from-paths src --ignore-src -r -y` followed by `colcon build --packages-select your_pkg`.
- Source the workspace (`source install/setup.bash`) and run either `ros2 launch your_pkg your_launch.py` or the individual nodes (`ros2 run your_pkg your_node`) once implemented.
- Graders will **NOT** attempt to fix any broken builds or missing dependencies, so ensure your package builds and runs correctly before submission and has all needed files (i.e includes your racelines) and dependencies declared.

## If you created the package elsewhere
- Copy the finished `your_pkg` folder into this repository root.
- Verify the folder now lives at `grading_ws/src/<your-repo>/your_pkg`, then commit and push.
- To test, clone your repo into a fresh workspace and build and run/launch from there to ensure no files are missing.

## Required student documentation (if needed)
- Include a dedicated run guide in this repo. Start from `RUN_INSTRUCTIONS_TEMPLATE.md`, rename it (e.g., `RUN_INSTRUCTIONS.md`), and replace all placeholders with your exact commands and parameters.
- Complete `SUBMISSION.md` with the checklist and any written answers requested by the assignment.

> [!NOTE]
> If your code follows the template's instructions exactly (i.e., node names, package names, node names, launch file names), you may choose to omit the run guide. However, you must still complete and include `SUBMISSION.md`.

