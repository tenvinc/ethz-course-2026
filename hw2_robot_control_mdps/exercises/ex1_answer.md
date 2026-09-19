# Answers to EX 1

1. If you increase the width of the Lemniscate (increasing a), what issue can happen with the robot performing IK?

When the width of the Lemniscate is too large, the robot may fail to track the trajectory properly since the desired target position might fall outside of the robot's working range.

2. What can happen if you change the dt parameter in IK?

A dt that is too large can cause divergence in the solution, while a dt that's too small might lead to excessive iterations needed and increase control latency.

3. We implemented a simple numerical IK solver. What are the advantages and disadvantages compared to an analytical IK solver?

The numerical IK solver implemented is an iterative algorithm. Advantage is that it's can be applied more generally to other dynamic model, without significant changes needed. An analytical IK solver would require an analytical solution to be possible in the first place, which may not apply to most models

4. What are the limits of our IK solver compared to state-of-the-art IK solvers?

Standard IK solvers uses hard clamping, near the joint limits or high speed curvature sections, it may result in unfeasible commands or commands that are damaging to the hardware. SOTA IK solvers addresses these considerations by applying various kinematic and dynamic constraints.