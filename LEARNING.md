# My AI Engineering Path
<!-- Managed by the ai-engineering-from-scratch learning skills.
     Repo: https://github.com/rohitg00/ai-engineering-from-scratch -->

## Mission
Career change from **IT sysadmin** into AI engineering. Main goal: build real-world applications, above all **workflow automation and intelligent, autonomous decision-making systems** (AIOps-style: alert/ticket triage, runbook assistants, safe remediation with human approval and audit trails). Interested in theory too, but only the part that supports doing things well. **No deadline and no weekly-hours target: quality over speed.** Principle: do not reinvent the wheel. Build from scratch only where it creates the mental model; use the standard tool where it ships.

## Learner profile and teaching approach
- Background: philosophy degree, no university math; works as an IT sysadmin. Talk in English.
- Math and any abstract topic: intuition-first, one small step at a time, define every term, use logic/philosophy analogies (e.g. a dependent vector = a redundant premise). Ask a check question after each step.
- Always say which method to use for which job before using it (e.g. rows to compute `M @ point`, columns to understand or build a matrix). Use x/y wording, not e1/e2.
- Move on by mastery, not by the clock: a block is done when the learner can do its "can you do this" checks.
- Quizzes: `quiz.json` is missing or empty for Phases 2, 3, 6, 8, 9, 10, 12, 15, almost all of 7 and most of 11. For those lessons, write a short quiz from the lesson text and log the score as usual.
- The program below can be changed at any time on the learner's request. "Skip" in the Path table means deferred, not rejected.

## Placement
- Date: 2026-09-16
- Score: 5/10 (Math & Statistics: 0/2, Classical ML: 1/2, Deep Learning: 1/2, NLP & Transformers: 1/2, Applied AI: 2/2)
- Entry point: Phase 0: Setup & Tooling (learner override — placement suggested Phase 3, but learner chose to restart from scratch on 2026-09-16 despite the quiz result)
- Pace: no fixed schedule; mastery-based (learner wants things done well, no deadline)
- Order (superseded on 2026-10-01 by the Program section below; kept for history): FULL numeric curriculum (all 12 Phase 0 lessons in order), NOT the site's curated "Software Engineering Fundamentals" learning path. Confirmed 2026-09-17. The site's Learning Paths view had silently skipped 03/04/05/08/11, which caused out-of-order study (02→06→07); learner reads lessons via the CATALOG page (or `lesson.html?path=...` URLs), not Learning Paths.
- Backfill (completed 2026-09-22/23; skipped by the site path): 0/03-gpu-setup-and-cloud, 0/04-apis-and-keys, 0/05-jupyter-notebooks, 0/08-editor-setup.

## Path
| Phase | Name | Status | Est. hours |
|-------|------|--------|------------|
| 0 | Setup & Tooling | Done | 14 |
| 1 | Math Foundations | Do | 23 |
| 2 | ML Fundamentals | Do | 21 |
| 3 | Deep Learning Core | Do | 15 |
| 4 | Computer Vision | Skip | 27 |
| 5 | NLP — Foundations to Advanced | Do | 30 |
| 6 | Speech & Audio | Skip | 18 |
| 7 | Transformers Deep Dive | Do | 14 |
| 8 | Generative AI | Skip | 14 |
| 9 | Reinforcement Learning | Skip | 13 |
| 10 | LLMs from Scratch | Do | 26 |
| 11 | LLM Engineering | Do | 17 |
| 12 | Multimodal AI | Skip | 65 |
| 13 | Tools & Protocols | Do | 43 |
| 14 | Agent Engineering | Do | 55 |
| 15 | Autonomous Systems | Do | 20 |
| 16 | Multi-Agent & Swarms | Skip | 28 |
| 17 | Infrastructure & Production | Do | 32 |
| 18 | Ethics, Safety & Alignment | Do | 31 |
| 19 | Capstone Projects | Skip | 620 |

"Do" = only the selected lessons in the Program below, not the whole phase. "Skip" = deferred (Phase 19 is replaced by the Projects section plus a personal capstone).

## Program (adopted 2026-10-01; the learner can change it anytime)
**Rule:** follow this order, NOT numeric phase order. **Next lesson = the first item below that has no row in the Progress log.** Items in [brackets] are projects from `projects/` (use the `build-project` skill). Already done before the program: Phase 0 (all 12, phase quiz 8/8), 1/01, 1/02. Block order is A, B, C, D, E; D (theory) can be moved before C on request, since nothing in C depends on D.

**A. Launch set (understand training and evaluation)**
1/03 (finish lightly: eigenvector idea only, no characteristic-equation algebra) → 1/04 (first ~9 sections; skip Hessian, Taylor, integrals, Jacobian) → 1/05 → 1/06 → 1/09 → 2/01 → 2/02 → 2/03 → 2/09

**B. Build 1: LLM engineering**
10/01 → 1/14 → 11/01 → 11/02 → 11/03 → [Prompt Regression Tester] → 11/04 → 11/05 → 11/06 → 5/22 → 5/23 → 5/14 → [Document QA With Citations] → 11/09 → 1/15 → 11/10 → 5/27 → [Retrieval Evaluation Lab] → 11/11 → 11/12 → 11/13 → [CSV Question Workbench]. Add the real-build bridges (below) along the way.

**C. Build 2: agents, safe autonomy, production (the core for this learner)**
1. Tools and MCP: 13/01 → 13/02 → 13/05 → 13/06 → 13/07 → 13/09 → 13/10
2. Agents and workflows: 14/01 → [Tiny Coding Agent] → 14/06 → 14/12 → 14/02 → 14/05 → 14/07 → 14/13 → 14/29 → 14/17
3. Failure and security: 14/26 → 14/27 → 14/30 → 18/15 → 13/15 → 13/16
4. Safe autonomy: 15/10 → 15/13 → 15/14 → 15/15 → 15/16 → 15/12
5. Reliability and workflow discovery: 14/31–14/42 → 14/47–14/54
6. Ops ML (logs and metrics): 2/07 → 2/15 → 2/16
7. Projects: [Inbox Triage Desk] → [Incident Postmortem Writer] → [Agent Budget Planner] → [Tool Call Firewall] → [Sandbox Ladder] → [Durable Agent Jobs] → [MCP at Scale]
8. Production and responsibility: 17/01 → 17/13 → 17/19 → 17/20 → 17/21 → 17/23 → 17/25 → 17/26 → 17/27 → 18/20 → 18/24 → 18/26
9. Capstone: an ops copilot (see below)

**D. Theory deepening (how it works inside)**
1/12 → 1/13 → 3/01 → 3/02 → 3/03 (skim; it repeats 1/05) → 3/04 → 3/05 → 3/06 → 3/07 → 3/11 → 3/13 → 5/10 → 7/01 → 7/02 → 7/03 → 7/04 → 7/05 → 7/06 → 7/07 → 7/12 → 7/13 → 10/06 → 10/07 → 10/08 → 10/10

**E. Optional, by interest**
1/10 (PCA, UMAP), 2/04, 2/08, 2/13, 2/17, 1/07 (Bayes), 1/11 (SVD), Phase 9 (reinforcement learning), the alignment-research half of Phase 18, the Claude certification tracks (independent community curriculum), optional modules by project domain (documents/vision 12/22–12/24, fine-tuning 11/08 + 10/04, deep MCP 13/08–13/18).

**Deliberately skipped as duplicates or specialties:** 1/08 (re-taught in 3/06), 2/10 (overlaps 2/01 and 2/09), 3/10 and 3/12, 11/07 (mostly 5/14 again; read only query transformation and metadata filtering if needed), GPU-serving lessons in Phase 17, Phases 4, 6, 8, 12, 16 and 19.

**Real-build bridges (not in the repo; most lesson code is simulated):** a real SDK call with structured output and tool use (after 11/03); real embeddings plus Qdrant, which is already in the 0/07 compose file (after 11/04 and 11/06); a RAG eval set; a FastAPI app in Docker (after 11/13); tracing with Langfuse; a prompt-injection test suite; CI eval gates. Outside the repo, pick one workflow orchestrator (for example n8n or Temporal) at 14/13 and 14/29.

**Capstone:** an ops copilot. It ingests alerts or tickets, triages them, retrieves the right runbook, proposes a remediation, waits for human approval, executes through a tool-call firewall in a sandbox, and writes an audit log; then evaluate it with a test set. Autonomy ladder: read-only advice, then propose-then-approve, then bounded autonomy for low-risk actions with rollback, never for destructive ones.

**Mastery checks (examples):** explain and implement a train/val/test split and spot leakage; build a RAG pipeline and measure its retrieval quality; show a prompt change helped using a significance test; explain why an action needs human approval and how it can be rolled back.

## Progress log
| Date | Lesson | Quiz | Note |
|------|--------|------|------|
| 2026-09-16 | 0/01-dev-environment | 3/3 | Set up Python venv + PyTorch (CPU) in WSL2, not Windows-side; working from a repo clone at ~/aifs (symlinked/shortened path) to avoid /mnt/c slowdowns. |
| 2026-09-16 | 0/02-git-and-collaboration | 2/3 | Missed the git add/commit/push order (picked git clone/add/push instead). Also set up GitHub CLI device-flow auth in WSL and pushed personal fork for the first time. |
| 2026-09-17 | 0/06-python-environments | 1/3 | Taught interactively step-by-step. Strong on venv isolation & PATH concept once explained. Missed: (1) pip+conda mixing breaks conda's dependency tracking — picked "incompatible interpreter"; (2) CUDA mismatch cause — picked "forgot to import torch.cuda". Also confused reproducibility: thought pyproject.toml reproduces an identical env, but it's the lockfile (== pins) vs pyproject range (>=). Skipped lesson 03 (GPU) and 04/05 to do 06 out of order. Hit CRLF line-ending bug in env_setup.sh (autocrlf=true in WSL clone). |
| 2026-09-21 | 0/07-docker-for-ai | 3/3 | Perfect score. Built the image, hit `--gpus all` failure (machine is CPU-only, no NVIDIA GPU) and correctly diagnosed it; dropped the flag to run on CPU. Explored Jupyter running in the container (port mapping + volume mount clicked). Removed the `deploy.resources...nvidia` GPU block from code/docker-compose.yml so `docker compose up` runs on CPU. Understood compose service-name networking (ai-dev → qdrant). |
| 2026-09-22 | 0/03-gpu-setup-and-cloud | 3/3 | Perfect score (B/B/C: nvidia-smi, cuda.synchronize before timing, 12B params in 24GB fp16). Read on the site. Before this, hit "PyTorch not installed" running gpu_check.py — root cause was forgetting to `source .venv/bin/activate` (system python3.14 has no torch; venv python3.12 does). Confirmed CPU-only via gpu_check.py (torch 2.14.0+cu130, CUDA False). Also researched Colab pricing: free tier still exists; cheapest paid path is Pay-As-You-Go $9.99/100 CU, no subscription. |
| 2026-09-22 | 0/04-apis-and-keys | 3/3 | Perfect score (A/D/B: .env in .gitignore, Anthropic uses x-api-key header, rate limit = HTTP 429 retry). Read on site. Asked where keys live: created `~/aifs/.env` (root, git-ignored) with empty ANTHROPIC_API_KEY / OPENAI_API_KEY / HF_TOKEN placeholders for the learner to fill in. Note: the lesson's first_api_call.py reads os.environ directly (no load_dotenv), so `.env` must be sourced (`set -a; source .env; set +a`) before running. Curious/engaged — also asked for a deep walk-through of the CPU/GPU matmul benchmark. |
| 2026-09-23 | 0/05-jupyter-notebooks | 3/3 | Perfect score (B/C/D: %timeit vs %%time, out-of-order execution = hidden state, explore in notebooks / ship in scripts). Read on site. Asked whether JupyterLab needs a GUI on WSL (no, it's a web server opened from the Windows browser; `jupyter-lab` is already in the venv). Asked why `pip` is missing from .venv: venv was made with `uv venv`, which omits pip by design, so use `uv pip install ...`. |
| 2026-09-23 | 0/08-editor-setup | 3/3 | Perfect score (D/D/D: Remote SSH, notebook output scrolling, basic type checking). Uses the existing Windows VS Code + WSL extension (`code .` from ~/aifs). First installed extensions on the Windows side, then also on WSL side — no harm. Got stuck on step 3: the lesson says `code/.vscode/` but the folder is actually `code/vscode/` (no dot). Created workspace settings at `~/aifs/.vscode/settings.json` (git-ignored) from the lesson file, minus `git.confirmSync: false` so VS Code asks before sync/push. Verified rulers + Black format-on-save work. |
| 2026-09-23 | 0/09-data-management | 3/3 | Perfect score (C/C/A: Parquet columnar, streaming=True, DVC for reproducible cross-machine data). Found the lesson unclear, so taught step by step with runs. Installed `datasets huggingface_hub` via `uv pip` (harmless hardlink warning: uv cache on WSL fs vs venv on /mnt/c → set `UV_LINK_MODE=copy`). Correctly predicted the split sizes 17500/2500/5000 and spotted the lesson's 80/10/10 text vs 70/10/20 code mismatch. Off-by-one on the streaming `break` (said 4 titles, it's 5). Initially typed Python in bash — reminded: enter `python` (>>>) first. Measured IMDB train: CSV 32M / JSON 33M / Parquet 20M (in ~/prova-dati, outside the repo). Ran data_utils.py successfully. |
| 2026-09-24 | 0/10-terminal-and-shell | 2/3 | Missed SSH local port forwarding (picked the non-existent `ssh --forward-port`; correct is `ssh -L 8888:localhost:8888 user@host`). Got tmux vs nohup and `> log 2>&1`. Session switched to English. Found that 4 `.sh` files (incl. shell_aliases.sh, env_setup.sh) are committed with CRLF in the upstream repo itself, not a local config issue (`core.autocrlf=input` already set at repo level). Left the repo untouched and installed the aliases via `tr -d '\r' < .../shell_aliases.sh > ~/.ai_aliases.sh` + `source ~/.ai_aliases.sh` in ~/.bashrc. Needed the run-vs-source distinction explained. Merged 15 upstream commits (no conflicts) and pushed. |
| 2026-09-24 | 0/11-linux-for-ai | 3/3 | Perfect score (C/C/D: chmod +x, du \| sort -hr \| head, macOS `sed -i ''` vs GNU). Read on site. Pre-briefed on WSL quirks: chmod doesn't stick on /mnt/c (practice in ~), df -h shows / (WSL disk) and /mnt/c (Windows), `uv cache clean` instead of pip cache, systemctl works (docker service). |
| 2026-09-24 | 0/12-debugging-and-profiling | 3/3 | Perfect score (B/C/D: data leakage on 99% accuracy, data loading as the usual bottleneck, locate NaN with gradient checks + breakpoint()). Asked what NaN is — explained IEEE NaN/inf, propagation, NaN != NaN, and the causes of NaN loss. Pre-briefed: install line_profiler/memory_profiler/tensorboard with `uv pip`, run TensorBoard outside ~/aifs (`runs/` isn't git-ignored), GPU memory section skipped on CPU. Last lesson of Phase 0 → Phase 0 marked Done. |
| 2026-09-24 | 1/01-linear-algebra-intuition | 3/3 | Perfect score (B/A/A: v3 dependent, rank = independent columns, LoRA low-rank update). Read the first half on the site; asked what "similar" means for the dot product (explained a·b = \|a\|\|b\|cos θ, length bias, cosine similarity, normalized embeddings). Found linear independence onward fuzzy → taught step by step, intuition-first (philosophy degree, no uni math; analogy: dependent vector = redundant premise/axiom). Answered all 9 check questions correctly: linear combination, span (floor vs room), basis/dimension, rank, multicollinearity (m² vs ft²), projection [4,2] onto [2,0] = [4,0], Gram-Schmidt → standard basis. |
| 2026-09-25 | 1/02-vectors-matrices-operations | 2/2 | Perfect score (A/B: det 0 ⇒ singular, transpose swaps rows/cols). Quiz now has only 2 post questions after the upstream lesson repair. Taught step by step. Solid: shape rule, `*` vs `@` (computed both by hand, saw A@B ≠ B@A), det/inverse via dependent columns. Slips worth re-checking in the warm-up: (1) thought transpose *reverses* a vector ([1,2,3] → [3,2,1]) and multiplied pairs without summing — fixed with a second example; (2) explained a broadcasting failure with the matmul inner-dimension rule; (3) got stuck reading shapes at the dense layer until the dot product was re-framed as a shopping receipt (quantities · prices), and matrix @ vector as one receipt per shop/row. Then computed relu(W@x+b) = [3.5, 0] by hand. Suggested 3Blue1Brown's Essence of Linear Algebra. |
| 2026-10-01 | 1/03-matrix-transformations | 3/3 | Essentials-only finish (Program block A). Perfect score on the 3 post questions (C/C/D: matrix multiplication is not commutative, RNN eigenvalues > 1 explode, `[[2,1],[1,2]]` stretches ×3 along [1,1] and leaves [1,-1] unchanged). Part 1 earlier: matrix = where the x-arrow and y-arrow land (columns), scaling, rotation (sin/cos from the unit circle), shear, reflection, chaining. Eigenvector/eigenvalue `A @ v = λ v` with the divide-and-compare recipe; characteristic equation explained but deliberately not practiced; PCA explained. Check slips: in the `D = diag(2, 0.5)` exercise computed (8, 0.125) correctly, but then described `A = [[2,1],[1,2]]` as "explodes on the x axis", mixing up `D` (A in eigen-coordinates) with A, whose special directions are the diagonals (1,1) and (1,-1). Re-check in the 1/04 warm-up. |
| 2026-10-07 | 1/04-calculus-for-ml | 2/3 | First ~9 sections only (Hessian, Taylor, integrals, Jacobian skipped per the Program, so the Newton's-method quiz question was not asked). Taught step by step with numeric checks. Warm-up on 1/03 was shaky at first (said the 3 in λ=3 was "a line", and "A stretches up and down") but fixed after a re-teach: `(1,0)` tilts, `(1,-1)` is the λ=1 eigenvector. Covered: derivative = rate per tiny nudge (disk-fill analogy), numerical derivative with h=0.1 then 0.01 (2.1 → 2.01 → true slope 2), slope sign tells the downhill direction, gradient descent `x − lr × slope` (3 → 2.4 → 1.92), lr=1.0 bounces forever (thermostat analogy; above 1 explodes, link to NaN in 0/12), partial derivatives and gradient `[8,7]` for `x²+3xy+y²` at (1,2), numeric check 7.01, chain rule as multiplying the rates of each link (pipeline `u = 3x+1`, `y = u²`, `dy/dx = 42` at x=2, checked 42.09). Quiz: C/D correct (gradient is the vector of partials; update rule), missed the central difference (picked the one-sided forward difference, A). Slips: dividing by 0.1 as if by 10 (0.021 instead of 2.1), `2 − 0.7` written as 0.3. |
| 2026-10-07 | 1/05-chain-rule-and-autodiff | 3/3 | Essentials only (forward mode, dual numbers and the from-scratch `Value` class build skipped; offered as optional practice). Perfect score (A/A/B: computational graph, `+=` accumulation, gradient checking). Taught step by step with hand-computed graphs: forward pass of `y = relu(x1·x2 + b)`, backward pass multiplying local rates (open gate: grads 3, 2, 1; closed gate with `c = -2`: all zero, "dying ReLU"), `x·x` gives 3+3 = 6, `x·x + 5·x` at x=2 gives 4+5 = 9 (slip: gave 2 instead of 5 for the `5·x` path; the rate of a multiply node for one input is the OTHER input), reverse vs forward mode (1,000,000 passes vs 1 for a million weights, one loss; reason is the many-inputs/one-output shape, not "learning from errors"). Confirmed with a real PyTorch `.backward()` run in the venv: 9.0 and the same grads, zeros for the closed gate. Also clarified before the lesson: backprop computes the gradient, gradient descent uses it. The learner asked for one explanation in Italian (done once; session language stays English). Recommended videos: StatQuest gradient descent, 3Blue1Brown ch.2 (watched), Karpathy micrograd (optional). |

## Next session plan
- **Next = Program block A, item 4: 1/06 (probability and distributions).** 1/03, 1/04 and 1/05 are DONE. Start with a short warm-up: (1) central difference `(f(x+h) − f(x−h)) / (2h)` vs the one-sided recipe (missed in the 1/04 quiz); (2) in a multiply node, the rate for one input is the OTHER input (slip in 1/05: `5·x` path gave 2 instead of 5); (3) why reverse mode (many weights, one loss) and what a closed relu gate does to the gradient. Also re-check the eigen idea from 1/03: eigenvalue = stretch factor, eigenvector = direction that only gets stretched, `D` = diagonal matrix of eigenvalues. Optional extras if the learner wants them: the lesson's `Value` class build (1/05 Build It) and Karpathy's micrograd video.
- (Older note, superseded by the line above) In progress (2026-10-01): 1/03-matrix-transformations, Part 1 done, Part 2 + quiz still to do. Part 1 covered (all answered correctly after help): a matrix = where the x-arrow and y-arrow land (columns); scaling, rotation (sin/cos taught from the unit circle, radians gotcha), shear, reflection; chaining = first move goes closest to the point (`S @ R` = rotate first, then stretch). STILL TO DO: Part 2 eigenvalues/eigenvectors (`A @ v = λ v`, 2x2 characteristic equation, eigendecomposition), determinant as area scaling, then the 2 post-quiz questions. The learner also asked "What is PCA?" (explained intuitively; an unanswered check question was left: keeping 1 principal component = projecting each point onto one direction, losing the spread in the others). Resume with a short warm-up on 1/02 (`W @ x` shape: rows = outputs; transpose = tip sideways) and a recap of the x/y-arrow reading.
- Teaching notes for 1/03: the learner mixed rows and columns three times. Always label the method: ROWS to compute `M @ point` (dot product per row), COLUMNS to understand or build a matrix (left column = where the x-arrow goes, right column = where the y-arrow goes). Use x/y wording, not e1/e2. Recommended: 3Blue1Brown "Essence of Linear Algebra" ch. 3 (watched). Phase 0 is Done and passed its phase quiz 8/8 (2026-09-24). For Phase 1, default to teaching step by step, intuition-first (the learner asked for it on 1/01). Follow the Program section, not the numeric phase order and not the site's curated path.
- CRLF status: `core.autocrlf=input` is set in the repo's `.git/config`. Four `.sh` files are committed with CRLF upstream (env_setup.sh, shell_aliases.sh, agent-workbench install.sh, scripts/scaffold-lesson.sh) and always show as "modified" — that's noise, don't commit them. To run one: `tr -d '\r' < script.sh | bash`.
- `.env` (API key placeholders) and `.vscode/settings.json` exist at the repo root and are git-ignored — never commit them.

## Phase quizzes
| Date | Phase | Score | Note |
|------|-------|-------|------|
| 2026-09-24 | 0 · Setup & Tooling | 8/8 | Mastered. All three review-queue topics answered correctly (git add→commit→push, pip-only package last in a conda env, SSH `-L 9999:localhost:8888` with differing ports), so the queue was cleared. |

## Review queue
- (empty — cleared after the Phase 0 quiz on 2026-09-24)
