# PhysicsNeMo local-project audit handoffs

These projects are known as local repositories but are not accessible through the connected GitHub installation in this audit session. No claim below says their current code or results were independently inspected here. Use these prompts locally and require Claude to establish evidence from the repository before accepting any numerical claim.

## Common rules

For every PhysicsNeMo project:
1. record git commit/status, PhysicsNeMo/PyTorch/CUDA versions, GPU, precision and seeds;
2. identify whether the code uses PhysicsNeMo primitives materially or merely wraps a generic PyTorch implementation;
3. derive the governing PDE/operator and boundary/initial conditions before discussing ML;
4. establish a trustworthy numerical/reference solution and train/validation/test split;
5. separate discretization/reference error from surrogate/PINN/operator-learning error;
6. test shape/normalization/nondimensionalization and boundary conventions;
7. report multiple seeds where training stochasticity matters;
8. compare against a simple relevant baseline;
9. do not treat a smoke/reduced run as a scientific benchmark;
10. preserve failed generalization/optimization as evidence rather than tuning after test inspection.

## physicsnemo-fno-darcy

**Claude prompt:** Audit this repository as an operator-learning study for Darcy flow. Read all code/configs/results first and state exactly what mapping the FNO learns, how permeability/forcing/boundaries are represented, and what numerical solver/dataset defines ground truth. Verify normalization and resolution conventions and check PDE residual/boundary error independently of field L2 error. Reproduce the reduced study, but label it reduced. Then run the planned 256x256/upstream-compatible baseline on CUDA only if the dataset/protocol matches. Compare multiple seeds and a simple non-operator baseline. Test resolution transfer only if grids/normalization make it meaningful. Record complete provenance. Do not push or rewrite history until results are reviewed.

## physicsnemo-pino-darcy

**Claude prompt:** Audit the PINO Darcy project by deriving the supervised and physics-informed losses from the stated elliptic PDE. Verify spatial derivatives/discretization, coefficient positivity, boundary treatment, normalization and loss scaling on analytical/manufactured fields before training. Compare FNO/PINO under identical data and architecture budgets where possible and include a no-physics ablation. Measure solution error, PDE residual and boundary error separately. Do not infer physical correctness from low training loss. Use multiple seeds and preserve failed regimes. Show tests/results before commits.

## physicsnemo-pinn-cavity

**Claude prompt:** Audit the lid-driven-cavity PINN as a steady incompressible Navier-Stokes problem. State Reynolds number, nondimensionalization, pressure gauge, wall/lid BCs and corner treatment. Verify autograd residuals on manufactured fields. Check that continuity, momentum, BC and pressure-reference losses are all enforced and scaled transparently. Compare centerline velocities/vortex structure against a trustworthy numerical benchmark at the same Reynolds number; do not rely only on residual loss. Investigate corner singularity effects. Record seed sensitivity and collocation convergence. Do not claim CFD accuracy without benchmark agreement.

## physicsnemo-ldc-pinns

**Claude prompt:** First determine whether this repository is scientifically distinct from physicsnemo-pinn-cavity or a second implementation of the same lid-driven-cavity experiment. If duplicate, do not present both as independent portfolio projects. Audit PDE, nondimensionalization, pressure gauge, boundary/corner handling, residual derivatives and benchmark comparisons exactly as for the cavity PINN. Identify what PhysicsNeMo-specific capability this repository demonstrates and whether that difference justifies retaining it separately.

## physicsnemo-meshgraphnet-vortex

**Claude prompt:** Audit this MeshGraphNet vortex project from the underlying PDE/time-stepping problem outward. Identify node/edge features, graph construction, target increment/state definition, normalization, rollout method and numerical ground truth. Verify one-step targets and conservation/physical diagnostics. Evaluate both one-step error and long-horizon rollout stability on trajectories not used for training. Check whether train/test meshes or initial conditions actually test generalization. Compare against persistence/simple numerical baselines. Do not call a stable-looking rollout physically accurate without quantitative diagnostics.

## physicsnemo-stokes-finetuning

**Claude prompt:** Audit the Stokes MeshGraphNet/fine-tuning project by first writing the exact Stokes problem, geometry/mesh, forcing and BCs. Verify numerical ground truth and graph feature construction. Establish the pretrained/source task and target task precisely; distinguish fine-tuning from training from scratch. Use identical target-data budgets for scratch vs pretrained comparisons and multiple seeds. Report velocity and pressure errors, divergence, boundary error and any force/integral quantities relevant to the problem. Check pressure gauge consistency. Do not claim transfer-learning benefit without a controlled scratch baseline.

## Portfolio decision after local audits

For each repository return one of: STRONG TO DISCUSS, DISCUSS WITH QUALIFICATION, DO NOT USE AS HEADLINE YET, or DUPLICATE/REMOVE FROM SELECTED PROJECTS. Include the exact evidence supporting the status and the one most important limitation to disclose in a PhD interview.
