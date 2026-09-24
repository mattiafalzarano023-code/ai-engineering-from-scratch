# My AI Engineering Path
<!-- Managed by the ai-engineering-from-scratch learning skills.
     Repo: https://github.com/rohitg00/ai-engineering-from-scratch -->

## Mission
Learning AI engineering as part of a career change. Not sure yet exactly what to build by the end — open to finding that out along the way.

## Placement
- Date: 2026-09-16
- Score: 5/10 (Math & Statistics: 0/2, Classical ML: 1/2, Deep Learning: 1/2, NLP & Transformers: 1/2, Applied AI: 2/2)
- Entry point: Phase 0: Setup & Tooling (learner override — placement suggested Phase 3, but learner chose to restart from scratch on 2026-09-16 despite the quiz result)
- Pace: ~5 hours/week
- Order: FULL numeric curriculum (all 12 Phase 0 lessons in order), NOT the site's curated "Software Engineering Fundamentals" learning path. Confirmed 2026-09-17. The site's Learning Paths view had silently skipped 03/04/05/08/11, which caused out-of-order study (02→06→07); learner reads lessons via the CATALOG page (or `lesson.html?path=...` URLs), not Learning Paths.
- Backfill needed (skipped by the site path, must still be done): 0/03-gpu-setup-and-cloud, 0/04-apis-and-keys, 0/05-jupyter-notebooks, 0/08-editor-setup.

## Path
| Phase | Name | Status | Est. hours |
|-------|------|--------|------------|
| 0 | Setup & Tooling | Done | 14 |
| 1 | Math Foundations | Do | 23 |
| 2 | ML Fundamentals | Do | 21 |
| 3 | Deep Learning Core | Do | 15 |
| 4 | Computer Vision | Do | 27 |
| 5 | NLP — Foundations to Advanced | Do | 30 |
| 6 | Speech & Audio | Do | 18 |
| 7 | Transformers Deep Dive | Do | 14 |
| 8 | Generative AI | Do | 14 |
| 9 | Reinforcement Learning | Do | 13 |
| 10 | LLMs from Scratch | Do | 26 |
| 11 | LLM Engineering | Do | 17 |
| 12 | Multimodal AI | Do | 65 |
| 13 | Tools & Protocols | Do | 43 |
| 14 | Agent Engineering | Do | 55 |
| 15 | Autonomous Systems | Do | 20 |
| 16 | Multi-Agent & Swarms | Do | 28 |
| 17 | Infrastructure & Production | Do | 32 |
| 18 | Ethics, Safety & Alignment | Do | 31 |
| 19 | Capstone Projects | Do | 620 |

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

## Next session plan
- **Next lesson:** 1/02-vectors-matrices-operations. Phase 0 is Done and passed its phase quiz 8/8 (2026-09-24). For Phase 1, default to teaching step by step, intuition-first (the learner asked for it on 1/01). Following the FULL numeric curriculum, not the site's curated path.
- CRLF status: `core.autocrlf=input` is set in the repo's `.git/config`. Four `.sh` files are committed with CRLF upstream (env_setup.sh, shell_aliases.sh, agent-workbench install.sh, scripts/scaffold-lesson.sh) and always show as "modified" — that's noise, don't commit them. To run one: `tr -d '\r' < script.sh | bash`.
- `.env` (API key placeholders) and `.vscode/settings.json` exist at the repo root and are git-ignored — never commit them.

## Phase quizzes
| Date | Phase | Score | Note |
|------|-------|-------|------|
| 2026-09-24 | 0 · Setup & Tooling | 8/8 | Mastered. All three review-queue topics answered correctly (git add→commit→push, pip-only package last in a conda env, SSH `-L 9999:localhost:8888` with differing ports), so the queue was cleared. |

## Review queue
- (empty — cleared after the Phase 0 quiz on 2026-09-24)
