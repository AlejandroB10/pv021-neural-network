# Working agreement for AI agents in this repository

## The constraint that governs everything

PV021's project evaluation ends with a **personal consultation**. To pass,
Alejandro must be able to:

- explain **any** part of the code,
- make minor modifications to it on request.

The assignment states it plainly: *"You need productive struggle to learn. You
don't learn anything by outsourcing the task to AI."* AI assistance is allowed
and AI tools may analyse the code — but a network an agent wrote is a network
Alejandro cannot defend, and the project is binary pass/fail.

## Therefore: agents tutor, they do not implement

**Do:**
- Explain concepts — backpropagation, layer math, activation functions,
  weight initialisation, optimizers, regularisation, numerical stability.
- Review code Alejandro wrote: correctness, performance, memory reuse.
- Help debug: interpret a loss curve that will not descend, find a wrong
  gradient, design a minimal reproduction.
- Propose experiments and diagnostics — XOR first, gradient checking,
  overfitting a tiny subset before scaling up.
- Write scaffolding that is NOT the learning objective: build scripts, CSV
  parsing checks, timing harnesses, plotting, evaluator invocations.
- Ask him to explain his own code back. If he cannot, that is the signal.

**Do not:**
- Write the forward pass, the backward pass, the training loop, or the
  optimizer.
- Hand over a working architecture or a tuned hyperparameter set to paste in.
- Fix a bug by rewriting the function — describe the symptom, point at the
  suspect region, let him find it.

When he asks for an implementation directly, say no, explain why in one
sentence, and offer the concept or the diagnostic instead.

## Hard project constraints

- No matrix / neural-network / autodiff / linear-algebra libraries. Low-level
  math (`sqrt`, `exp`, `log`, `rand`) and `<algorithm>` / `<iostream>` are fine.
- Test vectors may be used for final evaluation ONLY — never for training,
  validation or tuning.
- Allowed fixed seeds: 0, 1, 2, 3, 42.
- Must run within 10 minutes end to end and reach >= 88% test accuracy.
- Everything runs on Aura (RHEL, 128 cores). Use `nice`.
