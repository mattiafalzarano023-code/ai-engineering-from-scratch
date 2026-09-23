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
| 0 | Setup & Tooling | Do | 14 |
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

## Next session plan
- **Next lesson:** 0/10-terminal-and-shell — remaining to finish Phase 0: 10 → 11 → 12, then `/check-understanding 0`. Heads-up: lesson 10 ships `code/shell_aliases.sh`, one of the files with CRLF line endings, so apply the CRLF fix before sourcing it. Following the FULL numeric curriculum, not the site's curated path.
- Uncommitted local changes (not yet committed; `~/aifs` symlink means they're already live in WSL, matter only for the Kubuntu laptop / fork): `code/docker-compose.yml` (07, NVIDIA deploy block removed), `LEARNING.md` (lessons 03 & 04 logged). NOTE: `.env` was created at repo root but is git-ignored (never commit it).
- Also pending on WSL: apply the CRLF fix (`git config core.autocrlf input` + strip `\r` from `.sh`) so course scripts run. Docker Engine (native, in WSL) is already installed and working.

## Review queue
- 0/02-git-and-collaboration — correct save/backup sequence is `git add` → `git commit` → `git push` (staged first, then snapshot, then upload to remote). Quiz score 2/3.
- 0/06-python-environments — Quiz score 1/3 (2026-09-17). Review on 2026-09-23 scored 3/4: lockfile-vs-pyproject ✅ and CUDA mismatch ✅ now recovered, venv activation ✅ solid. STILL WEAK: pip inside a conda env — picked "uninstall conda and switch to pip" this time (previously "incompatible interpreter"). Correct model: conda keeps an inventory/solver of the env and pip doesn't write to it, so install everything possible with conda first, pip-only packages last, and avoid further `conda install` after that (or recreate the env).
