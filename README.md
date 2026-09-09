# Awesome OSS Directory

A large, categorized directory of open-source tools and projects — roughly 4,000 entries across four parts: a 60-domain categorized directory, notable builders and foundation ecosystems, a hand-curated "interesting architecture" collection of ~1,066 repos, and quick-reference lists of what major companies and foundations build in the open.

This isn't meant to be exhaustive or a popularity contest. It's a working reference: when you need "a self-hosted X," "an OSS alternative for Y," or "who builds Z in the open," start here instead of re-Googling it every time.

**Scope:** Infrastructure, backend/frontend frameworks, databases, security, mobile, ML/AI, dev tooling, per-language library picks (Go, Python, Rust, JS/TS), and company/foundation OSS ecosystems. Product-shaped SaaS tooling (project management, CRM, commerce platforms) lives in the companion [awesome-saas-tools](https://github.com/sudo-su-coffee/awesome-saas-tools). AI/ML-specific delivery tooling (agents, RAG, MLOps, model serving) has its own deeper treatment in [awesome-ml-tools](https://github.com/sudo-su-coffee/awesome-ml-tools).

> Stars and license info are approximate as of when each section was compiled — always verify current license terms before production or commercial use. Entries with no confidently-known link are marked `—`, or in Part 3's flagged section, kept as name-only rather than risk a wrong or guessed URL.

## Contents

- **Part 1** — Categorized OSS Directory (60 domains, ~3,000 tools)
- **Part 2** — Notable Builders, Ecosystems & Foundation Projects
- **Part 3** — Unique & Notable Repos (~1,066 hand-picked, by architecture/idea)
- **Part 4** — Corporate OSS Orgs & Foundation Directories

---

## Table of Contents (Part 1)
1. [Operating Systems & Distros](#1-operating-systems--distros)
2. [Shell & Terminal](#2-shell--terminal)
3. [Editors & IDEs](#3-editors--ides)
4. [Version Control & Git Tools](#4-version-control--git-tools)
5. [Languages & Runtimes](#5-languages--runtimes)
6. [Package Managers & Build Tools](#6-package-managers--build-tools)
7. [Containers & Virtualization](#7-containers--virtualization)
8. [Kubernetes & Orchestration](#8-kubernetes--orchestration)
9. [Infrastructure as Code](#9-infrastructure-as-code)
10. [CI/CD & GitOps](#10-cicd--gitops)
11. [Monitoring & Observability](#11-monitoring--observability)
12. [Logging](#12-logging)
13. [Databases - Relational](#13-databases---relational)
14. [Databases - NoSQL](#14-databases---nosql)
15. [Databases - Time Series](#15-databases---time-series)
16. [Databases - Graph](#16-databases---graph)
17. [Databases - Vector](#17-databases---vector)
18. [Databases - Search](#18-databases---search)
19. [Message Queues & Streaming](#19-message-queues--streaming)
20. [Caching & In-Memory](#20-caching--in-memory)
21. [Networking & Proxy](#21-networking--proxy)
22. [Service Mesh & API Gateway](#22-service-mesh--api-gateway)
23. [Security & Secrets](#23-security--secrets)
24. [Authentication & Identity](#24-authentication--identity)
25. [Web Frameworks - Backend](#25-web-frameworks---backend)
26. [Web Frameworks - Frontend](#26-web-frameworks---frontend)
27. [CMS & Headless CMS](#27-cms--headless-cms)
28. [E-Commerce](#28-e-commerce)
29. [Mobile Development](#29-mobile-development)
30. [Desktop Development](#30-desktop-development)
31. [Data Engineering & Pipelines](#31-data-engineering--pipelines)
32. [Data Visualization & BI](#32-data-visualization--bi)
33. [Machine Learning Frameworks](#33-machine-learning-frameworks)
34. [Deep Learning & Neural Networks](#34-deep-learning--neural-networks)
35. [MLOps & Model Serving](#35-mlops--model-serving)
36. [LLM & Generative AI](#36-llm--generative-ai)
37. [NLP & Text Processing](#37-nlp--text-processing)
38. [Computer Vision](#38-computer-vision)
39. [Audio & Speech](#39-audio--speech)
40. [CLI Tools & Utilities](#40-cli-tools--utilities)
41. [File & Storage](#41-file--storage)
42. [Backup & Disaster Recovery](#42-backup--disaster-recovery)
43. [Notification & Alerting](#43-notification--alerting)
44. [Email & Messaging](#44-email--messaging)
45. [Video & Media](#45-video--media)
46. [Documentation & Knowledge Base](#46-documentation--knowledge-base)
47. [Project Management & Collaboration](#47-project-management--collaboration)
48. [Finance & Payments](#48-finance--payments)
49. [Analytics & Product Tracking](#49-analytics--product-tracking)
50. [Testing & QA](#50-testing--qa)
51. [Go Libraries](#51-go-libraries)
52. [Python Libraries](#52-python-libraries)
53. [Rust Libraries](#53-rust-libraries)
54. [JavaScript/TypeScript Libraries](#54-javascripttypescript-libraries)
55. [DevEx & Developer Portals](#55-devex--developer-portals)
56. [Zerodha FOSS Stack](#56-zerodha-foss-stack)

---

## 1. Operating Systems & Distros

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Linux Kernel | C | 175k+ | The core OS kernel powering everything from servers to phones | GPL-2.0 | https://github.com/torvalds/linux |
| Ubuntu | C/Shell | — | Most popular Linux distro for servers & desktops | Various | — |
| Debian | C/Shell | — | The universal operating system, foundation for many distros | Various | — |
| Fedora | C/Shell | — | Red Hat-sponsored distro with cutting-edge packages | Various | — |
| Arch Linux | C/Shell | — | Rolling release, minimalist, build-it-yourself distro | Various | — |
| NixOS | Nix | 8k+ | Declarative, reproducible Linux OS using Nix package manager | MIT | https://github.com/NixOS/nixpkgs |
| Alpine Linux | C/Shell | 3k+ | Minimal security-oriented Linux for containers | Various | — |
| CentOS Stream | C/Shell | — | Community-supported upstream of RHEL | GPL-2.0 | — |
| Rocky Linux | C/Shell | 5k+ | Community enterprise OS, RHEL-compatible | Various | https://github.com/rocky-linux/rocky |
| AlmaLinux | C/Shell | 2k+ | RHEL binary-compatible community distro | Various | — |
| openSUSE | C/Shell | — | Flexible enterprise Linux distro by SUSE | Various | — |
| Void Linux | C/Shell | 4k+ | Independent rolling release with runit init | Various | — |
| Gentoo | C/Shell | 2k+ | Source-based meta-distro with Portage | GPL-2.0 | https://github.com/gentoo/gentoo |
| Slackware | C/Shell | — | Oldest surviving Linux distro | Various | — |
| Kali Linux | Shell | 5k+ | Penetration testing focused distro | GPL-2.0 | — |
| Parrot OS | Shell | 1k+ | Security and privacy focused Linux | GPL-3.0 | — |
| Tails OS | Shell | 2k+ | Privacy-focused live OS routed through Tor | GPL-3.0 | https://gitlab.tails.boum.org/tails/tails |
| Qubes OS | C/Python | 9k+ | Security-focused OS using Xen-based VMs | GPL-2.0 | https://github.com/QubesOS/qubes-issues |
| FreeBSD | C | 8k+ | Stable UNIX-like OS for servers | BSD | https://github.com/freebsd/freebsd-src |
| OpenBSD | C | 2k+ | Security-focused BSD with strong code audit | ISC | https://github.com/openbsd/src |
| NetBSD | C | 1k+ | Portable UNIX OS running on 57 platforms | BSD | https://github.com/NetBSD/src |
| illumos | C | 3k+ | Open-source UNIX (Solaris fork) | CDDL | https://github.com/illumos/illumos-gate |
| Haiku | C++ | 8k+ | RTOS designed for personal computing (BeOS-inspired) | MIT | https://github.com/google-deepmind/dm-haiku |
| ReactOS | C | 14k+ | Open-source Windows-compatible OS | GPL-2.0 | https://github.com/reactos/reactos |
| SerenityOS | C++ | 30k+ | UNIX-like OS built from scratch with custom everything | BSD-2 | https://github.com/SerenityOS/serenity |
| Redox OS | Rust | 16k+ | Rust-written microkernel UNIX-like OS | MIT | https://github.com/redox-os/redox |
| MenuetOS | ASM | — | Real-time OS written entirely in assembly | GPL | — |
| Minix3 | C | 4k+ | Microkernel-based UNIX for embedded/education | BSD-3 | — |
| Plan9 | C | 2k+ | Bell Labs' successor to UNIX | MIT/Lucent | — |
| HelenOS | C | 1k+ | Research OS with microkernel architecture | BSD-3 | https://github.com/HelenOS/helenos |

---

## 2. Shell & Terminal

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Bash | C | — | GNU Bourne Again Shell — default on Linux | GPL-3.0 | — |
| Zsh | C | — | Extended Bourne shell with scripting features | MIT-like | — |
| Fish | C++ | 26k+ | Friendly Interactive Shell with rich autocompletion | GPL-2.0 | https://github.com/fish-shell/fish-shell |
| Nushell | Rust | 33k+ | Modern shell with structured data pipelines | MIT | https://github.com/nushell/nushell |
| Elvish | Go | 5k+ | Expressive shell with powerful pipeline syntax | BSD-2 | https://github.com/elves/elvish |
| Xonsh | Python | 8k+ | Python-powered shell with full Python interop | BSD-2 | https://github.com/xonsh/xonsh |
| Oil Shell (Oils) | C++/Python | 3k+ | New Unix shell aiming to replace Bash/POSIX | Apache-2.0 | https://github.com/oils-for-unix/oils |
| Dash | C | — | POSIX-compliant minimal shell used in Debian | BSD | — |
| Tcsh | C | 1k+ | Enhanced C shell with history/completion | BSD-3 | — |
| Oh My Zsh | Shell | 173k+ | Framework for managing Zsh configuration | MIT | https://github.com/ohmyzsh/ohmyzsh |
| Oh My Fish | Fish | 10k+ | Fish shell framework inspired by Oh My Zsh | MIT | https://github.com/oh-my-fish/oh-my-fish |
| Oh My Bash | Bash | 4k+ | Community framework for Bash configuration | MIT | https://github.com/ohmybash/oh-my-bash |
| Prezto | Zsh | 14k+ | Zsh configuration framework | MIT | https://github.com/sorin-ionescu/prezto |
| Starship | Rust | 46k+ | Cross-shell minimal prompt (works with any shell) | ISC | https://github.com/starship/starship |
| Powerlevel10k | Zsh | 47k+ | Fast Zsh theme with configuration wizard | MIT | https://github.com/romkatv/powerlevel10k |
| Pure | Zsh | 13k+ | Pretty, minimal Zsh prompt | MIT | https://github.com/sindresorhus/pure |
| tmux | C | 34k+ | Terminal multiplexer — split panes, sessions | ISC | https://github.com/tmux/tmux |
| screen | C | — | Classic terminal multiplexer by GNU | GPL-3.0 | — |
| Zellij | Rust | 22k+ | Rust terminal workspace with layout engine | MIT | https://github.com/zellij-org/zellij |
| WezTerm | Rust | 17k+ | GPU-accelerated terminal with Lua config | MIT | https://github.com/wez/wezterm |
| Alacritty | Rust | 57k+ | Fast cross-platform GPU terminal emulator | Apache-2.0 | https://github.com/alacritty/alacritty |
| Kitty | C/Python | 24k+ | GPU terminal with image protocol support | GPL-3.0 | https://github.com/kovidgoyal/kitty |
| Hyper | TypeScript | 43k+ | Electron-based terminal built on web tech | MIT | https://github.com/vercel/hyper |
| iTerm2 | Objective-C | 15k+ | macOS terminal with split panes, profiles | GPL-2.0 | https://github.com/gnachman/iTerm2 |
| Tilix | D | 5k+ | Tiling terminal emulator for GNOME | MPL-2.0 | https://github.com/gnunn1/tilix |
| Konsole | C++ | — | KDE terminal emulator | GPL-2.0 | — |
| GNOME Terminal | C | — | Default GNOME terminal | GPL-3.0 | — |
| Windows Terminal | C++ | 96k+ | Open source terminal for Windows | MIT | https://github.com/microsoft/terminal |
| fzf | Go | 65k+ | Command-line fuzzy finder | MIT | https://github.com/junegunn/fzf |
| ripgrep | Rust | 49k+ | Ultra-fast `grep` alternative (rg) | MIT/Unlicense | https://github.com/BurntSushi/ripgrep |
| fd | Rust | 34k+ | Faster simpler `find` alternative | MIT | https://github.com/sharkdp/fd |
| bat | Rust | 50k+ | `cat` clone with syntax highlighting and git diff | MIT | https://github.com/sharkdp/bat |
| exa / eza | Rust | 23k+ | Modern `ls` replacement with colors and icons | MIT | https://github.com/eza-community/eza |
| lsd | Rust | 13k+ | `ls` replacement with icons and colors | Apache-2.0 | https://github.com/lsd-rs/lsd |
| delta | Rust | 23k+ | Syntax-highlighting pager for `git diff` | MIT | https://github.com/dandavison/delta |
| htop | C | 7k+ | Interactive process viewer, `top` replacement | GPL-2.0 | https://github.com/htop-dev/htop |
| btop | C++ | 21k+ | Resource monitor with beautiful UI | Apache-2.0 | https://github.com/aristocratos/btop |
| glances | Python | 26k+ | Cross-platform system monitor | LGPL-3.0 | https://github.com/nicolargo/glances |
| procs | Rust | 5k+ | Modern `ps` replacement in Rust | MIT | https://github.com/dalance/procs |
| bottom (btm) | Rust | 10k+ | System monitor similar to htop/gotop | MIT | https://github.com/ClementTsang/bottom |
| dust | Rust | 9k+ | `du` alternative showing disk usage clearly | Apache-2.0 | https://github.com/bootandy/dust |
| duf | Go | 13k+ | Disk usage / free utility with nice output | MIT | https://github.com/muesli/duf |
| tokei | Rust | 11k+ | Count lines of code in a project | MIT | https://github.com/XAMPPRocky/tokei |
| hyperfine | Rust | 21k+ | Command-line benchmarking tool | MIT/Apache-2.0 | https://github.com/sharkdp/hyperfine |
| tealdeer (tldr) | Rust | 5k+ | Fast `tldr` client for simplified man pages | MIT | https://github.com/tealdeer-rs/tealdeer |
| zoxide | Rust | 24k+ | Smarter `cd` command that learns your habits | MIT | https://github.com/ajeetdsouza/zoxide |
| autojump | Python | 16k+ | `cd` that learns; jump to frecently used dirs | GPL-3.0 | https://github.com/wting/autojump |
| thefuck | Python | 88k+ | Corrects previous console command | MIT | https://github.com/nvbn/thefuck |
| atuin | Rust | 20k+ | Encrypted shell history synced across machines | MIT | https://github.com/atuinsh/atuin |
| mcfly | Rust | 7k+ | Fly through shell history intelligently | MIT | https://github.com/cantino/mcfly |
| direnv | Go | 12k+ | Load/unload env vars based on directory | MIT | https://github.com/direnv/direnv |
| mosh | C++ | 13k+ | Mobile shell supporting roaming/intermittent connections | GPL-3.0 | https://github.com/mobile-shell/mosh |
| asciinema | Python | 14k+ | Record and share terminal sessions | Apache-2.0 | https://github.com/asciinema/asciinema |
| ttyd | C | 8k+ | Share terminal over the web via browser | MIT | https://github.com/tsl0922/ttyd |
| tmate | C | 5k+ | Instant terminal sharing over SSH | BSD-2 | https://github.com/tmate-io/tmate |
| pv | C | — | Pipe viewer — monitor data through pipeline | Artistic | — |
| peco | Go | 7k+ | Simplistic interactive filtering tool | MIT | https://github.com/peco/peco |
| percol | Python | 3k+ | Interactive grep-like selection | MIT | https://github.com/mooz/percol |
| glow | Go | 16k+ | Render markdown in the terminal | MIT | https://github.com/charmbracelet/glow |
| rich | Python | 49k+ | Rich text and beautiful formatting in Python terminal | MIT | https://github.com/Textualize/rich |
| lolcat | Ruby | 6k+ | Rainbow coloring for terminal output | WTFPL | https://github.com/busyloop/lolcat |

---

## 3. Editors & IDEs

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Neovim | C/Lua | 83k+ | Hyperextensible Vim-based editor | Apache-2.0 | https://github.com/neovim/neovim |
| Vim | C | 36k+ | The classic modal text editor | Vim License | https://github.com/vim/vim |
| Helix | Rust | 33k+ | Post-modern modal text editor | MPL-2.0 | https://github.com/helix-editor/helix |
| Emacs | C/Lisp | 4k+ | Extensible, self-documenting real-time editor | GPL-3.0 | https://github.com/emacs-mirror/emacs |
| VS Code | TypeScript | 163k+ | Microsoft's open-source extensible code editor | MIT | https://github.com/microsoft/vscode |
| VSCodium | TypeScript | 25k+ | VS Code without Microsoft telemetry/branding | MIT | https://github.com/VSCodium/vscodium |
| Kate | C++ | — | KDE advanced text editor | LGPL-2.0 | — |
| Gedit | C | — | GNOME lightweight text editor | GPL-2.0 | — |
| Mousepad | C | — | Xfce's simple text editor | GPL-2.0 | — |
| Lapce | Rust | 35k+ | Lightning-fast plugin-supported code editor | Apache-2.0 | https://github.com/lapce/lapce |
| Zed | Rust | 51k+ | High-performance multiplayer code editor | AGPL-3.0 | https://github.com/zed-industries/zed |
| Lite XL | C/Lua | 5k+ | Lightweight code editor written in C and Lua | MIT | https://github.com/lite-xl/lite-xl |
| micro | Go | 25k+ | Modern terminal text editor with syntax highlight | MIT | https://github.com/zyedidia/micro |
| nano | C | — | Beginner-friendly terminal editor | GPL-3.0 | — |
| Joe | C | — | Unix text editor (WordStar-compatible) | GPL-1.0 | — |
| ne | C | — | Nice editor — powerful but simple | GPL-3.0 | — |
| IntelliJ IDEA CE | Java/Kotlin | 17k+ | Community edition of JetBrains IDE | Apache-2.0 | https://github.com/JetBrains/intellij-community |
| Eclipse IDE | Java | 2k+ | Veteran Java/plugin-based IDE | EPL-2.0 | https://github.com/eclipse-platform |
| NetBeans | Java | 3k+ | Apache NetBeans IDE | Apache-2.0 | https://github.com/apache/netbeans |
| Theia | TypeScript | 20k+ | Cloud & desktop IDE framework (Eclipse) | EPL-2.0 | https://github.com/eclipse-theia/theia |
| Gitpod | TypeScript | 13k+ | Cloud dev environment built on Theia/VS Code | AGPL-3.0 | https://github.com/gitpod-io/gitpod |
| Coder | Go | 9k+ | Self-hosted remote dev environments | AGPL-3.0 | https://github.com/coder/coder |
| code-server | TypeScript | 68k+ | VS Code in the browser | MIT | https://github.com/coder/code-server |
| Jupyter | Python | 12k+ | Interactive computing notebooks | BSD-3 | https://github.com/jupyter/notebook |
| JupyterLab | TypeScript | 14k+ | Next-gen UI for Jupyter notebooks | BSD-3 | https://github.com/jupyterlab/jupyterlab |
| nteract | TypeScript | 6k+ | Interactive computing suite (notebooks) | BSD-3 | https://github.com/nteract/nteract |
| Pluto.jl | Julia | 5k+ | Reactive notebooks for Julia | MIT | https://github.com/fonsp/Pluto.jl |
| RStudio | C++/R | 4k+ | IDE for R statistical computing | AGPL-3.0 | https://github.com/rstudio/rstudio |
| Spyder | Python | 8k+ | Scientific Python IDE | MIT | https://github.com/spyder-ide/spyder |
| PyCharm CE | Java/Python | 1k+ | JetBrains Python IDE community edition | Apache-2.0 | — |
| IDLE | Python | — | Python's bundled lightweight IDE | PSF | — |
| Atom | CoffeeScript | 60k+ | GitHub's extensible text editor (archived) | MIT | https://github.com/atom/atom |
| Pulsar | CoffeeScript | 2k+ | Community-led Atom fork | MIT | https://github.com/pulsar-edit/pulsar |
| Notepad++ | C++ | 22k+ | Windows source code editor | GPL-2.0 | https://github.com/notepad-plus-plus/notepad-plus-plus |
| Sublime Text | — | — | Fast code editor (closed core, open plugins) | Proprietary | — |
| oni2 | ReasonML | 8k+ | Native modal editor powered by Neovim | MIT | https://github.com/onivim/oni2 |
| Kakoune | C++ | 10k+ | Modal code editor with multiple selections | Unlicense | https://github.com/mawww/kakoune |

---

## 4. Version Control & Git Tools

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Git | C | 52k+ | Distributed version control system | GPL-2.0 | https://github.com/git/git |
| Gitea | Go | 45k+ | Self-hosted Git service — lightweight Forgejo/GitHub alt | MIT | https://github.com/go-gitea/gitea |
| Forgejo | Go | 3k+ | Gitea hard fork, community-driven | MIT | https://codeberg.org/forgejo/forgejo |
| Gogs | Go | 44k+ | Simple self-hosted Git service | MIT | https://github.com/gogs/gogs |
| GitLab CE | Ruby/Go | 23k+ | Full DevOps platform with CI/CD and registry | MIT | https://gitlab.com/gitlab-org/gitlab |
| Sourcehut | Python | 1k+ | Minimalist open-source software forge | AGPL-3.0 | https://sr.ht/~sircmpwn/sourcehut/ |
| Phabricator | PHP | 12k+ | Code review & project management | Apache-2.0 | https://github.com/phacility/phabricator |
| Gerrit | Java | 1k+ | Web-based code review tool for Git | Apache-2.0 | https://gerrit.googlesource.com/gerrit |
| Allura | Python | — | Apache software forge | Apache-2.0 | — |
| Kallithea | Python | — | Python-based repo management tool | GPL-3.0 | https://github.com/kallithea-scm/kallithea |
| Rhodecode CE | Python | 1k+ | Enterprise source code management | AGPL-3.0 | https://github.com/rhodecode/rhodecode |
| Fossil | C | — | Distributed VCS + wiki + ticket tracker | BSD-2 | https://www.fossil-scm.org/ |
| Mercurial | Python | — | Distributed VCS — alternative to Git | GPL-2.0 | https://www.mercurial-scm.org/ |
| Darcs | Haskell | — | Patch-based distributed VCS | GPL-2.0 | https://github.com/darcs/darcs |
| Jujutsu (jj) | Rust | 9k+ | Git-compatible next-gen VCS by Google | Apache-2.0 | https://github.com/jj-vcs/jj |
| Pijul | Rust | 3k+ | Mathematically sound patch-based VCS | GPL-2.0 | https://nest.pijul.com/pijul/pijul |
| lazygit | Go | 51k+ | Terminal UI for Git commands | MIT | https://github.com/jesseduffield/lazygit |
| gitui | Rust | 18k+ | Blazing fast terminal UI for Git | MIT | https://github.com/gitui-org/gitui |
| tig | C | 12k+ | Text-mode interface for Git | GPL-2.0 | https://github.com/jonas/tig |
| gh | Go | 37k+ | GitHub's official CLI | MIT | https://github.com/cli/cli |
| glab | Go | 4k+ | GitLab's official CLI | MIT | https://gitlab.com/gitlab-org/cli |
| git-extras | Shell | 17k+ | Extra Git commands and utilities | MIT | https://github.com/tj/git-extras |
| git-flow | Shell | 26k+ | Git branching model extension | BSD-2 | https://github.com/nvie/gitflow |
| gitoxide | Rust | 9k+ | Pure Rust Git implementation | MIT/Apache-2.0 | https://github.com/GitoxideLabs/gitoxide |
| grv | Go | 11k+ | Git Repository Viewer TUI | MIT | — |
| gitstatus | C++ | 4k+ | Fast alternative to `git status` for prompts | MIT | https://github.com/romkatv/gitstatus |
| git-cliff | Rust | 9k+ | Changelog generator from Git history | MIT/Apache-2.0 | https://github.com/orhun/git-cliff |
| cocogitto | Rust | 1k+ | Conventional commits toolbox | MIT | https://github.com/cocogitto/cocogitto |
| commitlint | JavaScript | 15k+ | Lint commit messages | MIT | https://github.com/conventional-changelog/commitlint |
| commitizen | Python | 10k+ | Commit message formatting tool | MIT | https://github.com/commitizen-tools/commitizen |
| pre-commit | Python | 13k+ | Framework for managing git pre-commit hooks | MIT | https://github.com/pre-commit/pre-commit |
| husky | JavaScript | 31k+ | Git hooks manager for Node projects | MIT | https://github.com/typicode/husky |
| lefthook | Go | 5k+ | Fast Git hooks manager | MIT | https://github.com/evilmartians/lefthook |
| gitleaks | Go | 18k+ | Detect secrets in Git repos | MIT | https://github.com/gitleaks/gitleaks |
| trufflehog | Go | 17k+ | Find leaked credentials in Git history | AGPL-3.0 | https://github.com/trufflesecurity/trufflehog |
| detect-secrets | Python | 3k+ | Framework for detecting secrets in code | Apache-2.0 | https://github.com/Yelp/detect-secrets |
| BFG Repo Cleaner | Scala | 11k+ | Remove sensitive data from Git history | GPL-3.0 | https://github.com/rtyley/bfg-repo-cleaner |
| git-filter-repo | Python | 8k+ | Quickly rewrite Git history | MIT | https://github.com/newren/git-filter-repo |
| gitlint | Python | 1k+ | Git commit message linter | MIT | https://github.com/jorisroovers/gitlint |
| git-bug | Go | 8k+ | Distributed bug tracker embedded in Git | GPL-3.0 | https://github.com/git-bug/git-bug |
| git-absorb | Rust | 3k+ | Auto `git commit --fixup` | BSD-3 | https://github.com/tummychow/git-absorb |
| git-machete | Python/Java | 1k+ | Git branch organization & rebase aid | MIT | https://github.com/VirtusLab/git-machete |

---

## 5. Languages & Runtimes

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| CPython | C | 63k+ | Reference implementation of Python | PSF | https://github.com/python/cpython |
| PyPy | Python/RPython | 2k+ | JIT-compiled fast Python implementation | MIT | https://github.com/pypy/pypy |
| GraalPy | Java | 2k+ | Python on GraalVM (JIT + polyglot) | UPL-1.0 | — |
| MicroPython | C | 19k+ | Python for microcontrollers | MIT | https://github.com/micropython/micropython |
| CircuitPython | C | 4k+ | Adafruit's MicroPython fork | MIT | https://github.com/adafruit/circuitpython |
| Ruby MRI | C | 22k+ | Reference Ruby implementation (CRuby) | BSD/GPL/Ruby | https://github.com/ruby/ruby |
| JRuby | Java | 4k+ | Ruby on JVM | EPL/GPL/LGPL | https://github.com/jruby/jruby |
| TruffleRuby | Java | 3k+ | Ruby on GraalVM | EPL-2.0 | https://github.com/oracle/truffleruby |
| Node.js | C++ | 107k+ | JavaScript runtime on V8 | MIT | https://github.com/nodejs/node |
| Deno | Rust | 96k+ | Secure JavaScript/TypeScript runtime | MIT | https://github.com/denoland/deno |
| Bun | Zig | 74k+ | All-in-one JS runtime (fast) | MIT | https://github.com/oven-sh/bun |
| V8 | C++ | 23k+ | Google's JavaScript engine | BSD-3 | https://github.com/v8/v8 |
| SpiderMonkey | C++ | — | Mozilla's JavaScript engine | MPL-2.0 | — |
| QuickJS | C | 8k+ | Tiny embeddable JS engine by Fabrice Bellard | MIT | https://github.com/quickjs-ng/quickjs |
| Hermes | C++ | 9k+ | JavaScript engine for React Native | MIT | https://github.com/facebook/hermes |
| OpenJDK | Java/C | 4k+ | Open Java Development Kit | GPL-2.0 | https://github.com/openjdk/jdk |
| GraalVM | Java | 20k+ | Polyglot JVM with native image compilation | UPL-1.0 | https://github.com/oracle/graal |
| Kotlin | Kotlin | 48k+ | JVM language by JetBrains (Android official) | Apache-2.0 | https://github.com/JetBrains/kotlin |
| Scala | Scala | 14k+ | JVM language combining OOP + FP | Apache-2.0 | https://github.com/scala/scala |
| Clojure | Java | 10k+ | Functional Lisp on JVM | EPL-1.0 | https://github.com/clojure/clojure |
| Groovy | Java | 5k+ | Dynamic JVM scripting language | Apache-2.0 | https://github.com/apache/groovy |
| Go (golang) | Go/C | 124k+ | Google's fast compiled systems language | BSD-3 | https://github.com/golang/go |
| Rust | Rust | 98k+ | Memory-safe systems language without GC | MIT/Apache-2.0 | https://github.com/rust-lang/rust |
| Zig | Zig | 37k+ | Systems language with manual memory + comptime | MIT | https://github.com/ziglang/zig |
| Nim | Nim | 16k+ | Efficient, expressive, elegant language | MIT | https://github.com/nim-lang/Nim |
| Crystal | Crystal | 19k+ | Statically typed Ruby-like language | Apache-2.0 | https://github.com/crystal-lang/crystal |
| D Language | D | 2k+ | Systems/applications language by Andrei et al. | BSL-1.0 | https://github.com/dlang/dmd |
| Haskell (GHC) | Haskell | 3k+ | Purely functional typed language | BSD-3 | https://gitlab.haskell.org/ghc/ghc |
| OCaml | OCaml | 5k+ | Functional language with native compiler | LGPL-2.1 | https://github.com/ocaml/ocaml |
| Erlang/OTP | Erlang | 12k+ | Concurrent fault-tolerant language | Apache-2.0 | https://github.com/erlang/otp |
| Elixir | Elixir | 24k+ | Functional language on BEAM VM | Apache-2.0 | https://github.com/elixir-lang/elixir |
| F# | F# | 4k+ | Functional language on .NET | MIT | https://github.com/dotnet/fsharp |
| Gleam | Rust | 17k+ | Type-safe language on Erlang BEAM | Apache-2.0 | https://github.com/gleam-lang/gleam |
| Lua | C | 8k+ | Lightweight embeddable scripting language | MIT | https://github.com/lua/lua |
| LuaJIT | C | 3k+ | Just-in-time compiled Lua | MIT | https://github.com/LuaJIT/LuaJIT |
| Raku (Perl 6) | Raku | 3k+ | Successor to Perl with rich type system | Artistic-2.0 | https://github.com/rakudo/rakudo |
| Perl | C | 2k+ | Text manipulation powerhouse | Artistic-1.0 | — |
| Julia | C/Julia | 44k+ | High-performance language for scientific computing | MIT | https://github.com/JuliaLang/julia |
| R | C/R | 4k+ | Statistical computing language | GPL-2.0 | — |
| LLVM | C++ | 28k+ | Compiler infrastructure/toolchain | Apache-2.0 | https://github.com/llvm/llvm-project |
| GCC | C | 5k+ | GNU Compiler Collection (C/C++/Fortran...) | GPL-3.0 | https://gcc.gnu.org/git.html |
| Clang | C++ | — | LLVM-based C/C++ compiler | Apache-2.0 | — |
| Swift | C++ | 67k+ | Apple's open-source language | Apache-2.0 | https://github.com/swiftlang/swift |
| Dart | C++ | 10k+ | Client-optimized language by Google | BSD-3 | https://github.com/dart-lang/sdk |
| Pony | C | 4k+ | Actor-model language with capabilities | BSD-2 | https://github.com/ponylang/ponyc |
| Racket | Racket | 5k+ | Language-oriented programming platform | MIT | https://github.com/racket/racket |
| Janet | C | 3k+ | Lightweight Lisp/scripting language | MIT | https://github.com/janet-lang/janet |
| Fennel | Lua | 2k+ | Lisp that compiles to Lua | MIT | https://github.com/bakpakin/Fennel |
| Hy | Python | 5k+ | Lisp that compiles to Python | MIT | https://github.com/hylang/hy |
| Carp | Haskell | 5k+ | Statically typed Lisp for real-time apps | Apache-2.0 | https://github.com/carp-lang/Carp |
| V language | V | 35k+ | Simple, fast, safe compiled language | MIT | https://github.com/vlang/v |
| Odin | Odin | 7k+ | Systems language for high-performance apps | BSD-3 | https://github.com/odin-lang/Odin |
| Ada (GNAT) | Ada | 3k+ | GNAT Ada compiler, part of GCC | GPL-3.0 | — |
| Forth | C | 2k+ | Stack-based language used in embedded | Various | — |
| Prolog (SWI) | C | 2k+ | Logic programming language | BSD-2 | — |
| WebAssembly (WASM) | — | — | Binary instruction format for stack-based VM | Apache-2.0 | https://github.com/WebAssembly |
| AssemblyScript | TypeScript | 17k+ | TypeScript-like language compiling to WASM | Apache-2.0 | https://github.com/AssemblyScript/assemblyscript |
| TinyGo | Go | 15k+ | Go compiler for embedded/WASM targets | BSD-3 | https://github.com/tinygo-org/tinygo |

---

## 6. Package Managers & Build Tools

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Nix | C++ | 12k+ | Purely functional package manager | LGPL-2.1 | https://github.com/NixOS/nix |
| Guix | Scheme | — | GNU transactional package manager | GPL-3.0 | — |
| Homebrew | Ruby | 41k+ | macOS/Linux package manager | BSD-2 | https://github.com/Homebrew/brew |
| Linuxbrew | Ruby | — | Homebrew for Linux | BSD-2 | — |
| APT | C++ | — | Debian/Ubuntu advanced package tool | GPL-2.0 | — |
| pacman | C | — | Arch Linux package manager | GPL-2.0 | — |
| dnf/yum | Python | 1k+ | Fedora/RHEL package manager | GPL-2.0 | — |
| zypper | C++ | 1k+ | openSUSE package manager | GPL-2.0 | — |
| portage | Python | 1k+ | Gentoo source-based package manager | GPL-2.0 | — |
| pip | Python | 9k+ | Python package installer | MIT | https://github.com/pypa/pip |
| uv | Rust | 40k+ | Extremely fast Python package manager | MIT/Apache-2.0 | https://github.com/astral-sh/uv |
| Poetry | Python | 32k+ | Python dependency management & packaging | MIT | https://github.com/python-poetry/poetry |
| Pipenv | Python | 25k+ | Python dev workflow — combines pip+venv | MIT | https://github.com/pypa/pipenv |
| conda | Python | 6k+ | Package & env manager for data science | BSD-3 | https://github.com/conda/conda |
| mamba | C++ | 7k+ | Fast conda package manager reimplementation | BSD-3 | https://github.com/mamba-org/mamba |
| pdm | Python | 8k+ | Modern Python package manager with PEP 582 | MIT | https://github.com/pdm-project/pdm |
| Hatch | Python | 6k+ | Python project manager | MIT | https://github.com/pypa/hatch |
| cargo | Rust | 13k+ | Rust's official package manager + build tool | MIT/Apache-2.0 | https://github.com/rust-lang/cargo |
| npm | JavaScript | 8k+ | Node.js package manager | Artistic-2.0 | https://github.com/npm/cli |
| yarn | JavaScript | 41k+ | Fast Node package manager by Facebook | BSD-2 | https://github.com/yarnpkg/yarn |
| pnpm | JavaScript | 29k+ | Disk-efficient package manager for Node | MIT | https://github.com/pnpm/pnpm |
| bun install | Zig | 74k+ | Ultra-fast JS/TS package installer | MIT | — |
| Gradle | Kotlin/Java | 17k+ | Build automation for JVM projects | Apache-2.0 | https://github.com/gradle/gradle |
| Maven | Java | 4k+ | Build + project management for Java | Apache-2.0 | https://github.com/apache/maven |
| Bazel | Java | 23k+ | Fast polyglot build system by Google | Apache-2.0 | https://github.com/bazelbuild/bazel |
| Buck2 | Rust | 3k+ | Meta's fast polyglot build system | Apache-2.0 | https://github.com/facebook/buck2 |
| Pants | Python | 4k+ | Scalable build tool for monorepos | Apache-2.0 | https://github.com/pantsbuild/pants |
| Please | Go | 5k+ | High-performance cross-language build system | Apache-2.0 | https://github.com/please-build/please |
| Make (GNU Make) | C | — | Classic build automation tool | GPL-3.0 | — |
| CMake | C++ | 6k+ | Cross-platform build system generator | BSD-3 | https://gitlab.kitware.com/cmake/cmake |
| Meson | Python | 5k+ | Fast build system for large projects | Apache-2.0 | https://github.com/mesonbuild/meson |
| Ninja | C++ | 10k+ | Small, fast build system | Apache-2.0 | https://github.com/ninja-build/ninja |
| SCons | Python | 2k+ | Software construction tool | MIT | https://github.com/SCons/scons |
| Rake | Ruby | 2k+ | Ruby build tool like Make | MIT | https://github.com/ruby/rake |
| Task | Go | 11k+ | Task runner / build tool (Makefile alt.) | MIT | https://github.com/go-task/task |
| Just | Rust | 22k+ | `just` a command runner (Makefile alt.) | CC0 | https://github.com/casey/just |
| Earthly | Go | 11k+ | Repeatable build automation in Dockerfile-like syntax | MPL-2.0 | https://github.com/earthly/earthly |
| Dagger | Go | 12k+ | Portable dev pipelines as code | Apache-2.0 | https://github.com/dagger/dagger |
| asdf | Bash | 22k+ | Multi-language runtime version manager | MIT | https://github.com/asdf-vm/asdf |
| mise | Rust | 11k+ | `asdf` rewrite in Rust — faster | MIT | https://github.com/jdx/mise |
| nvm | Bash | 79k+ | Node version manager | MIT | https://github.com/nvm-sh/nvm |
| pyenv | Shell | 40k+ | Python version management | MIT | https://github.com/pyenv/pyenv |
| rbenv | Ruby | 16k+ | Ruby version manager | MIT | https://github.com/rbenv/rbenv |
| sdkman | Bash | 6k+ | SDK manager for JVM tools | Apache-2.0 | https://github.com/sdkman/sdkman-cli |
| volta | Rust | 10k+ | Hassle-free JavaScript tool manager | BSD-2 | https://github.com/volta-cli/volta |
| proto | Rust | 1k+ | Toolchain & runtime manager by Moonrepo | MIT | https://github.com/moonrepo/proto |

---

## 7. Containers & Virtualization

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Docker Engine (Moby) | Go | 28k+ | Open-source container runtime (Moby project) | Apache-2.0 | https://github.com/moby/moby |
| containerd | Go | 17k+ | Industry-standard container runtime | Apache-2.0 | https://github.com/containerd/containerd |
| CRI-O | Go | 5k+ | Lightweight container runtime for Kubernetes | Apache-2.0 | https://github.com/cri-o/cri-o |
| Podman | Go | 24k+ | Daemonless OCI container manager | Apache-2.0 | https://github.com/containers/podman |
| Buildah | Go | 7k+ | Build OCI images without Docker daemon | Apache-2.0 | https://github.com/containers/buildah |
| Skopeo | Go | 7k+ | OCI image operations tool | Apache-2.0 | https://github.com/containers/skopeo |
| Kaniko | Go | 15k+ | Build Docker images in Kubernetes | Apache-2.0 | https://github.com/GoogleContainerTools/kaniko |
| BuildKit | Go | 8k+ | Next-gen Docker build toolkit | Apache-2.0 | https://github.com/moby/buildkit |
| Nerdctl | Go | 8k+ | Docker-compatible CLI for containerd | Apache-2.0 | https://github.com/containerd/nerdctl |
| Lima | Go | 17k+ | Linux VMs on macOS (like WSL2 for Mac) | Apache-2.0 | https://github.com/lima-vm/lima |
| Finch | Go | 3k+ | AWS CLI for building containers on macOS | Apache-2.0 | https://github.com/runfinch/finch |
| Colima | Go | 20k+ | Container runtimes on macOS with Docker/containerd | MIT | https://github.com/abiosoft/colima |
| runc | Go | 11k+ | CLI tool for spawning OCI containers | Apache-2.0 | https://github.com/opencontainers/runc |
| crun | C | 2k+ | Fast OCI runtime written in C | GPL-2.0 | https://github.com/containers/crun |
| gVisor | Go | 16k+ | User-space kernel sandboxing containers | Apache-2.0 | https://github.com/google/gvisor |
| kata-containers | Go | 5k+ | Lightweight VMs for container workloads | Apache-2.0 | https://github.com/kata-containers/kata-containers |
| Firecracker | Rust | 26k+ | Lightweight VMs for serverless (AWS Lambda) | Apache-2.0 | https://github.com/firecracker-microvm/firecracker |
| QEMU | C | 9k+ | Multi-architecture processor emulator | GPL-2.0 | https://gitlab.com/qemu-project/qemu |
| KVM | C | — | Linux kernel virtual machine | GPL-2.0 | — |
| VirtualBox | C++ | — | Cross-platform x86 virtualizer by Oracle | GPL-2.0 | https://www.virtualbox.org/browser |
| libvirt | C | 1k+ | Virtualization API for Linux | LGPL-2.1 | https://gitlab.com/libvirt/libvirt |
| Vagrant | Ruby | 26k+ | Dev environment manager using VMs | BSL-1.1 | https://github.com/hashicorp/vagrant |
| Multipass | C++ | 8k+ | Ubuntu VM launcher for any OS | GPL-3.0 | https://github.com/canonical/multipass |
| Incus | Go | 2k+ | Linux container and VM manager (LXC fork) | Apache-2.0 | https://github.com/lxc/incus |
| LXC | C | 4k+ | Linux containers using namespaces+cgroups | LGPL-2.1 | https://github.com/lxc/lxc |
| LXD | Go | 4k+ | Container and VM manager built on LXC | Apache-2.0 | https://github.com/canonical/lxd |
| systemd-nspawn | C | — | Container-like isolation using systemd | LGPL-2.1 | — |
| Singularity | Go | 3k+ | Container system for HPC clusters | BSD-3 | https://github.com/sylabs/singularity |
| Apptainer | Go | 2k+ | Singularity fork for HPC | BSD-3 | https://github.com/apptainer/apptainer |
| Distrobox | Shell | 10k+ | Use any Linux distro inside terminal | GPL-3.0 | https://github.com/89luca89/distrobox |
| toolbox | Go | 2k+ | GNOME Boxes companion for dev containers | Apache-2.0 | https://github.com/containers/toolbox |
| Rancher Desktop | TypeScript | 5k+ | Open-source desktop for containers and K8s | Apache-2.0 | https://github.com/rancher-sandbox/rancher-desktop |
| OrbStack | — | — | Fast Docker on macOS (free tier) | Proprietary/free | — |
| Dive | Go | 44k+ | Explore Docker image layers | MIT | https://github.com/wagoodman/dive |
| hadolint | Haskell | 10k+ | Dockerfile linter | GPL-3.0 | https://github.com/hadolint/hadolint |
| dockle | Go | 4k+ | Container image linter for security | Apache-2.0 | https://github.com/goodwithtech/dockle |
| Trivy | Go | 24k+ | Vulnerability scanner for containers | Apache-2.0 | https://github.com/aquasecurity/trivy |
| Grype | Go | 8k+ | Vulnerability scanner for images/filesystems | Apache-2.0 | https://github.com/anchore/grype |
| Syft | Go | 6k+ | SBOM generator for containers | Apache-2.0 | https://github.com/anchore/syft |
| Docker Compose | Python/Go | 33k+ | Multi-container Docker app definition | Apache-2.0 | https://github.com/docker/compose |
| Kompose | Go | 9k+ | Convert Docker Compose files to K8s | Apache-2.0 | https://github.com/kubernetes/kompose |
| lazydocker | Go | 38k+ | Terminal UI for Docker and Compose | MIT | https://github.com/jesseduffield/lazydocker |
| ctop | Go | 15k+ | Top-like metrics for containers | MIT | https://github.com/bcicen/ctop |
| Portainer CE | Go | 30k+ | Container management UI | Zlib | https://github.com/portainer/portainer |
| Cockpit | C | 10k+ | Linux web-based server management UI | LGPL-2.1 | https://github.com/cockpit-project/cockpit |
| Watchtower | Go | 19k+ | Auto-update running Docker containers | Apache-2.0 | https://github.com/containrrr/watchtower |
| Diun | Go | 4k+ | Docker image update notifier | MIT | https://github.com/crazy-max/diun |
| cAdvisor | Go | 16k+ | Container resource usage analysis | Apache-2.0 | https://github.com/google/cadvisor |

---

## 8. Kubernetes & Orchestration

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Kubernetes | Go | 111k+ | Production-grade container orchestration | Apache-2.0 | https://github.com/kubernetes/kubernetes |
| k3s | Go | 28k+ | Lightweight Kubernetes for edge/IoT | Apache-2.0 | https://github.com/k3s-io/k3s |
| k0s | Go | 9k+ | Zero-friction Kubernetes distribution | Apache-2.0 | https://github.com/k0sproject/k0s |
| minikube | Go | 29k+ | Run local Kubernetes cluster | Apache-2.0 | https://github.com/kubernetes/minikube |
| kind | Go | 13k+ | Kubernetes in Docker — for testing | Apache-2.0 | https://github.com/kubernetes-sigs/kind |
| k3d | Go | 5k+ | Run k3s in Docker | MIT | https://github.com/k3d-io/k3d |
| microk8s | Go | 8k+ | Low-ops Kubernetes snap by Canonical | Apache-2.0 | https://github.com/canonical/microk8s |
| Talos Linux | Go | 7k+ | Immutable OS for Kubernetes | MPL-2.0 | https://github.com/siderolabs/talos |
| Kubeadm | Go | — | Official K8s cluster bootstrapping tool | Apache-2.0 | — |
| kubespray | Python | 16k+ | Deploy K8s with Ansible | Apache-2.0 | https://github.com/kubernetes-sigs/kubespray |
| Rancher | Go | 23k+ | K8s cluster management platform | Apache-2.0 | https://github.com/rancher/rancher |
| OpenShift OKD | Go | 7k+ | Kubernetes distro with developer features | Apache-2.0 | https://github.com/okd-project/okd |
| Helm | Go | 27k+ | Package manager for Kubernetes | Apache-2.0 | https://github.com/helm/helm |
| Helmfile | Go | 4k+ | Declarative Helm releases management | MIT | https://github.com/helmfile/helmfile |
| Kustomize | Go | 11k+ | Kubernetes config customization | Apache-2.0 | https://github.com/kubernetes-sigs/kustomize |
| Kapp | Go | 2k+ | Kubernetes deployment tool by VMware | Apache-2.0 | https://github.com/vmware-tanzu/carvel-kapp |
| Skaffold | Go | 15k+ | Local Kubernetes development workflow | Apache-2.0 | https://github.com/GoogleContainerTools/skaffold |
| Tilt | Go | 8k+ | Dev environment for microservices on K8s | Apache-2.0 | https://github.com/tilt-dev/tilt |
| Garden | TypeScript | 4k+ | Dev environments and CI for K8s apps | MPL-2.0 | https://github.com/garden-io/garden |
| Draft | Go | 3k+ | Simplified Kubernetes app development | MIT | — |
| Flux | Go | 16k+ | GitOps toolkit for Kubernetes (CNCF) | Apache-2.0 | https://github.com/fluxcd/flux2 |
| Argo CD | Go | 18k+ | Declarative GitOps CD for Kubernetes | Apache-2.0 | https://github.com/argoproj/argo-cd |
| Argo Workflows | Go | 15k+ | Kubernetes-native workflow engine | Apache-2.0 | https://github.com/argoproj/argo-workflows |
| Argo Events | Go | 3k+ | Event-driven automation for Kubernetes | Apache-2.0 | https://github.com/argoproj/argo-events |
| Argo Rollouts | Go | 3k+ | Advanced deployment strategies for K8s | Apache-2.0 | https://github.com/argoproj/argo-rollouts |
| Keptn | Go | 2k+ | K8s-native lifecycle orchestration | Apache-2.0 | https://github.com/keptn/keptn |
| Tekton | Go | 8k+ | Cloud-native CI/CD K8s framework | Apache-2.0 | https://github.com/tektoncd/pipeline |
| KEDA | Go | 9k+ | K8s-based event-driven autoscaling | Apache-2.0 | https://github.com/kedacore/keda |
| Vertical Pod Autoscaler | Go | 5k+ | Vertical resource autoscaling for K8s | Apache-2.0 | https://github.com/kubernetes/autoscaler |
| Cluster Autoscaler | Go | 8k+ | Automatically scale K8s cluster nodes | Apache-2.0 | https://github.com/kubernetes/autoscaler |
| Karpenter | Go | 7k+ | Node provisioner for Kubernetes (AWS) | Apache-2.0 | https://github.com/aws/karpenter-provider-aws |
| Knative | Go | 5k+ | K8s-native serverless framework | Apache-2.0 | https://github.com/knative/serving |
| OpenFaaS | Go | 25k+ | Serverless functions on Kubernetes | MIT | https://github.com/openfaas/faas |
| Fission | Go | 8k+ | Fast serverless functions for Kubernetes | Apache-2.0 | https://github.com/fission/fission |
| kubeless | Go | 7k+ | Kubernetes-native serverless framework | Apache-2.0 | https://github.com/vmware-archive/kubeless |
| OpenFunction | Go | 1k+ | CNCF cloud-native FaaS platform | Apache-2.0 | — |
| Istio | Go | 36k+ | Service mesh with traffic management | Apache-2.0 | https://github.com/istio/istio |
| Linkerd | Rust/Go | 10k+ | Ultra-light service mesh (CNCF) | Apache-2.0 | https://github.com/linkerd/linkerd2 |
| Cilium | Go | 20k+ | eBPF-based networking, security, observability | Apache-2.0 | https://github.com/cilium/cilium |
| Calico | Go | 6k+ | Network policy and security for K8s | Apache-2.0 | https://github.com/projectcalico/calico |
| Flannel | Go | 8k+ | Simple K8s network overlay | Apache-2.0 | https://github.com/flannel-io/flannel |
| Weave Net | Go | 6k+ | Network virtual overlay for containers | Apache-2.0 | https://github.com/weaveworks/weave |
| MetalLB | Go | 7k+ | Bare-metal load balancer for Kubernetes | Apache-2.0 | https://github.com/metallb/metallb |
| cert-manager | Go | 12k+ | Automatic TLS certs management in K8s | Apache-2.0 | https://github.com/cert-manager/cert-manager |
| external-dns | Go | 7k+ | Sync K8s services to DNS providers | Apache-2.0 | https://github.com/kubernetes-sigs/external-dns |
| Velero | Go | 8k+ | Kubernetes backup and migration | Apache-2.0 | https://github.com/vmware-tanzu/velero |
| Longhorn | Go | 6k+ | Cloud-native distributed storage for K8s | Apache-2.0 | https://github.com/longhorn/longhorn |
| Rook | Go | 12k+ | Cloud-native storage operator for Kubernetes | Apache-2.0 | https://github.com/rook/rook |
| OpenEBS | Go | 9k+ | Kubernetes-native container-attached storage | Apache-2.0 | https://github.com/openebs/openebs |
| Crossplane | Go | 10k+ | Cloud-native control plane for infra provisioning | Apache-2.0 | https://github.com/crossplane/crossplane |
| kubebuilder | Go | 7k+ | SDK for building K8s APIs using CRDs | Apache-2.0 | https://github.com/kubernetes-sigs/kubebuilder |
| Operator SDK | Go | 7k+ | Framework for K8s operators | Apache-2.0 | https://github.com/operator-framework/operator-sdk |
| kopf | Python | 2k+ | Python framework for K8s operators | MIT | https://github.com/nolar/kopf |
| kubectl | Go | — | Official Kubernetes CLI | Apache-2.0 | — |
| kubectx | Go | 16k+ | Switch between K8s contexts quickly | Apache-2.0 | https://github.com/ahmetb/kubectx |
| k9s | Go | 27k+ | Terminal UI for K8s cluster management | Apache-2.0 | https://github.com/derailed/k9s |
| Lens | TypeScript | 22k+ | Kubernetes IDE (open core) | MIT | https://github.com/lensapp/lens |
| Octant | Go | 6k+ | Kubernetes cluster visualizer by VMware | Apache-2.0 | https://github.com/vmware-archive/octant |
| Kubescape | Go | 10k+ | K8s security posture scanner | Apache-2.0 | https://github.com/kubescape/kubescape |
| kube-bench | Go | 7k+ | K8s CIS benchmark checker | Apache-2.0 | https://github.com/aquasecurity/kube-bench |
| Falco | C++ | 7k+ | Runtime security for K8s (CNCF) | Apache-2.0 | https://github.com/falcosecurity/falco |
| OPA/Gatekeeper | Go | 9k+ | Policy engine for Kubernetes | Apache-2.0 | https://github.com/open-policy-agent/gatekeeper |
| Kyverno | Go | 6k+ | K8s-native policy engine | Apache-2.0 | https://github.com/kyverno/kyverno |
| Polaris | Go | 3k+ | K8s best practices validation | Apache-2.0 | https://github.com/FairwindsOps/polaris |
| Popeye | Go | 5k+ | K8s cluster sanitizer | Apache-2.0 | https://github.com/derailed/popeye |
| kube-linter | Go | 2k+ | Static linting for K8s YAML | Apache-2.0 | https://github.com/stackrox/kube-linter |
| Nomad | Go | 15k+ | Flexible workload orchestrator (non-K8s) | BSL-1.1 | https://github.com/hashicorp/nomad |
| Consul | Go | 28k+ | Service mesh and service discovery | BSL-1.1 | https://github.com/hashicorp/consul |

---

## 9. Infrastructure as Code

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Terraform | Go | 43k+ | Infrastructure as Code by HashiCorp (BSL) | BSL-1.1 | https://github.com/hashicorp/terraform |
| OpenTofu | Go | 23k+ | Open-source Terraform fork (truly OSS) | MPL-2.0 | https://github.com/opentofu/opentofu |
| Pulumi | Go/TypeScript | 22k+ | IaC using real programming languages | Apache-2.0 | https://github.com/pulumi/pulumi |
| Ansible | Python | 63k+ | Agentless IT automation | GPL-3.0 | https://github.com/ansible/ansible |
| Chef | Ruby | 7k+ | Infrastructure automation platform | Apache-2.0 | https://github.com/chef/chef |
| Puppet | Ruby | 7k+ | Configuration management | Apache-2.0 | https://github.com/puppetlabs/puppet |
| SaltStack | Python | 14k+ | Event-driven IT automation | Apache-2.0 | https://github.com/saltstack/salt |
| CFEngine | C | 1k+ | Lightweight configuration management | GPL-3.0 | https://github.com/cfengine/core |
| Nix/NixOS | Nix | 12k+ | Declarative system configuration | LGPL-2.1 | https://github.com/NixOS/nixpkgs |
| cloud-init | Python | 3k+ | Linux cloud instance initialization | Apache-2.0 | https://github.com/canonical/cloud-init |
| cloud-nuke | Go | 2k+ | Nuke all cloud resources in AWS account | MIT | https://github.com/gruntwork-io/cloud-nuke |
| Atlantis | Go | 8k+ | Terraform pull request automation | Apache-2.0 | https://github.com/runatlantis/atlantis |
| Terragrunt | Go | 8k+ | Thin wrapper for Terraform | MIT | https://github.com/gruntwork-io/terragrunt |
| Terramate | Go | 3k+ | IaC orchestration and code generation | MPL-2.0 | https://github.com/terramate-io/terramate |
| Spacelift | — | — | IaC management platform (open core) | Proprietary | — |
| Packer | Go | 15k+ | Machine image builder (HashiCorp) | BSL-1.1 | https://github.com/hashicorp/packer |
| Vagrant | Ruby | 26k+ | Dev environment provisioner | BSL-1.1 | https://github.com/hashicorp/vagrant |
| CDK (AWS) | TypeScript | 11k+ | AWS Cloud Dev Kit — K8s-like for AWS | Apache-2.0 | https://github.com/aws/aws-cdk |
| CDK8s | TypeScript | 4k+ | K8s manifests using general-purpose languages | Apache-2.0 | https://github.com/cdk8s-team/cdk8s |
| Nitric | Go | 1k+ | Cloud-agnostic infrastructure framework | Apache-2.0 | https://github.com/nitrictech/nitric |
| Wing | TypeScript | 5k+ | Cloud-oriented programming language | Apache-2.0 | https://github.com/winglang/wing |
| Score | Go | 1k+ | Developer-centric workload spec | Apache-2.0 | https://github.com/score-spec/spec |
| CloudQuery | Go | 6k+ | Cloud asset inventory using SQL | MPL-2.0 | https://github.com/cloudquery/cloudquery |
| Steampipe | Go | 7k+ | Query cloud APIs using SQL | AGPL-3.0 | https://github.com/turbot/steampipe |
| Infracost | Go | 10k+ | Cloud cost estimation for IaC | Apache-2.0 | https://github.com/infracost/infracost |
| tfsec | Go | 6k+ | Terraform security scanner | MIT | https://github.com/aquasecurity/tfsec |
| checkov | Python | 7k+ | IaC static analysis (Terraform, K8s, etc.) | Apache-2.0 | https://github.com/bridgecrewio/checkov |
| KICS | Go | 2k+ | IaC security scanner | Apache-2.0 | https://github.com/Checkmarx/kics |
| Terrascan | Go | 4k+ | Static code analysis for IaC | Apache-2.0 | https://github.com/tenable/terrascan |
| Regula | Rego | 1k+ | IaC compliance checker using OPA | Apache-2.0 | — |
| driftctl | Go | 2k+ | Track infrastructure drift from IaC | Apache-2.0 | https://github.com/snyk/driftctl |

---

## 10. CI/CD & GitOps

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Jenkins | Java | 23k+ | The classic self-hosted CI/CD server | MIT | https://github.com/jenkinsci/jenkins |
| Woodpecker CI | Go | 4k+ | Community fork of Drone CI | Apache-2.0 | https://github.com/woodpecker-ci/woodpecker |
| Drone CI | Go | 32k+ | Container-native CI/CD | Apache-2.0 | https://github.com/harness/drone |
| Gitea Actions | Go | — | GitHub Actions-compatible CI in Gitea | MIT | — |
| Forgejo Actions | Go | — | Forgejo built-in CI | MIT | — |
| Act | Go | 56k+ | Run GitHub Actions locally | MIT | https://github.com/nektos/act |
| Concourse CI | Go | 7k+ | Continuous thing-doer (pipeline based) | Apache-2.0 | https://github.com/concourse/concourse |
| GoCD | Java | 7k+ | Continuous delivery server | Apache-2.0 | https://github.com/gocd/gocd |
| TeamCity CE | Java | — | JetBrains CI/CD (free tier) | Proprietary | — |
| CircleCI server | — | — | Self-hosted CircleCI | Proprietary | — |
| Buildkite | — | — | CI/CD with OSS agents | Proprietary/OSS | — |
| Zuul | Python | — | Project gating CI system | Apache-2.0 | https://opendev.org/zuul/zuul |
| Prow | Go | 4k+ | Kubernetes-based CI for GitHub | Apache-2.0 | https://github.com/kubernetes-sigs/prow |
| Spinnaker | Java | 9k+ | Multi-cloud CD platform by Netflix | Apache-2.0 | https://github.com/spinnaker/spinnaker |
| Weave GitOps | Go | 3k+ | GitOps for Kubernetes using Flux | Apache-2.0 | https://github.com/weaveworks/weave-gitops |
| Fleet | Go | 4k+ | Multi-cluster GitOps for Kubernetes | Apache-2.0 | https://github.com/rancher/fleet |
| Harness CD CE | Java | — | CD platform (open-source CE) | PolyForm | — |
| Argo CD | Go | 18k+ | Declarative GitOps CD | Apache-2.0 | https://github.com/argoproj/argo-cd |
| Argo Workflows | Go | 15k+ | Kubernetes-native workflow engine | Apache-2.0 | https://github.com/argoproj/argo-workflows |
| Tekton | Go | 8k+ | Cloud-native CI/CD framework | Apache-2.0 | https://github.com/tektoncd/pipeline |
| Buildbot | Python | 5k+ | Flexible CI framework in Python | GPL-2.0 | https://github.com/buildbot/buildbot |
| CruiseControl | Java | — | Original CI server concept | BSD | — |
| Laminar CI | C++ | 1k+ | Lightweight self-hosted CI service | GPL-3.0 | — |
| Earthly | Go | 11k+ | Portable CI/CD syntax (Docker-like) | MPL-2.0 | https://github.com/earthly/earthly |
| Dagger | Go | 12k+ | Portable pipelines as code | Apache-2.0 | https://github.com/dagger/dagger |
| WarpBuild | — | — | Fast GitHub Actions runner (OSS-friendly) | Proprietary | — |
| Depot | — | — | Fast Docker builds (free tier) | Proprietary | — |
| semantic-release | JavaScript | 20k+ | Automated versioning and publishing | MIT | https://github.com/semantic-release/semantic-release |
| release-please | TypeScript | 6k+ | Automated releases via PRs (Google) | Apache-2.0 | https://github.com/googleapis/release-please |
| goreleaser | Go | 14k+ | Release automation for Go projects | MIT | https://github.com/goreleaser/goreleaser |
| ship-it / shipjs | JavaScript | 2k+ | Automate JavaScript package shipping | MIT | — |
| changesets | JavaScript | 10k+ | Manage monorepo versioning/changelogs | MIT | https://github.com/changesets/changesets |
| nx | TypeScript | 24k+ | Smart monorepo build system | MIT | https://github.com/nrwl/nx |
| turborepo | TypeScript | 26k+ | High-performance monorepo build system | MIT | https://github.com/vercel/turborepo |
| moon | Rust | 3k+ | Monorepo tool for polyglot codebases | MIT | https://github.com/moonrepo/moon |


---

## 11. Monitoring & Observability

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Prometheus | Go | 56k+ | Industry-standard metrics monitoring | Apache-2.0 | https://github.com/prometheus/prometheus |
| Grafana | Go | 65k+ | Analytics and visualization dashboards | AGPL-3.0 | https://github.com/grafana/grafana |
| VictoriaMetrics | Go | 13k+ | Fast long-term Prometheus-compatible storage | Apache-2.0 | https://github.com/VictoriaMetrics/VictoriaMetrics |
| Thanos | Go | 13k+ | Highly available Prometheus at scale | Apache-2.0 | https://github.com/thanos-io/thanos |
| Cortex | Go | 5k+ | Multi-tenant Prometheus backend | Apache-2.0 | https://github.com/cortexlabs/cortex |
| Mimir | Go | 4k+ | Grafana's scalable Prometheus backend | AGPL-3.0 | https://github.com/grafana/mimir |
| OpenMetrics | — | 900+ | Standardized metrics exposition format | Apache-2.0 | — |
| OpenTelemetry | Go/Java | 5k+ | Vendor-neutral telemetry collection | Apache-2.0 | https://github.com/open-telemetry/opentelemetry-collector |
| Jaeger | Go | 20k+ | Distributed tracing system (CNCF) | Apache-2.0 | https://github.com/jaegertracing/jaeger |
| Zipkin | Java | 17k+ | Distributed tracing system | Apache-2.0 | https://github.com/openzipkin/zipkin |
| Tempo | Go | 4k+ | Distributed tracing backend by Grafana | AGPL-3.0 | https://github.com/grafana/tempo |
| Signoz | Go/TypeScript | 19k+ | Full-stack APM + traces + logs (OSS Datadog alt) | Apache-2.0 | https://github.com/SigNoz/signoz |
| Netdata | C | 70k+ | Real-time performance monitoring | GPL-3.0 | https://github.com/netdata/netdata |
| collectd | C | 3k+ | System stats collection daemon | MIT | https://github.com/collectd/collectd |
| node_exporter | Go | 11k+ | Hardware/OS metrics for Prometheus | Apache-2.0 | https://github.com/prometheus/node_exporter |
| blackbox_exporter | Go | 4k+ | Probing endpoints for Prometheus | Apache-2.0 | https://github.com/prometheus/blackbox_exporter |
| alertmanager | Go | 6k+ | Handles Prometheus alerts (routing/grouping) | Apache-2.0 | https://github.com/prometheus/alertmanager |
| karma | Go | 2k+ | Alertmanager multi-cluster dashboard | Apache-2.0 | https://github.com/prymitive/karma |
| Uptime Kuma | JavaScript | 60k+ | Self-hosted uptime/status monitor | MIT | https://github.com/louislam/uptime-kuma |
| Gatus | Go | 6k+ | Developer-oriented health dashboard | Apache-2.0 | https://github.com/TwiN/gatus |
| Cachet | PHP | 13k+ | Open-source status page | BSD-3 | https://github.com/cachethq/cachet |
| Statping-ng | Go | 4k+ | Status page with metrics | GPL-3.0 | https://github.com/statping-ng/statping-ng |
| Statuspal | — | — | Status page platform | Proprietary | — |
| Pocketbase Monitors | — | — | Status monitoring | Various | — |
| Healthchecks.io | Python | 8k+ | Cron job monitoring with dead man's switch | BSD-3 | https://github.com/healthchecks/healthchecks |
| Cabot | Python | 5k+ | Self-hosted monitoring with alerts | MIT | https://github.com/cabotapp/cabot |
| Zabbix | C/PHP | 4k+ | Network/application monitoring platform | GPL-2.0 | https://github.com/zabbix/zabbix |
| Nagios | C | 1k+ | Classic IT infra monitoring | GPL-2.0 | https://github.com/NagiosEnterprises/nagioscore |
| Icinga | C++ | 2k+ | Nagios fork with modern features | GPL-2.0 | https://github.com/Icinga/icinga2 |
| LibreNMS | PHP | 4k+ | Network management system | GPL-3.0 | https://github.com/librenms/librenms |
| Checkmk | Python | 1k+ | IT monitoring platform | GPL-2.0 | https://github.com/Checkmk/checkmk |
| OpenNMS | Java | 1k+ | Network management platform | AGPL-3.0 | https://github.com/OpenNMS/opennms |
| PRTG (free tier) | — | — | Network monitoring (limited free) | Proprietary | — |
| Graphite | Python | 6k+ | Scalable realtime graphing | Apache-2.0 | https://github.com/graphite-project/graphite-web |
| Telegraf | Go | 14k+ | Plugin-driven metrics collection agent | MIT | https://github.com/influxdata/telegraf |
| StatsD | JavaScript | 18k+ | Simple daemon for easy stats aggregation | MIT | https://github.com/statsd/statsd |
| Pyroscope | Go | 10k+ | Continuous profiling platform | AGPL-3.0 | https://github.com/grafana/pyroscope |
| Parca | Go | 4k+ | Open-source continuous profiling | Apache-2.0 | https://github.com/parca-dev/parca |
| pixie | C++ | 5k+ | Observability for Kubernetes via eBPF | Apache-2.0 | https://github.com/pixie-io/pixie |
| Groundcover | — | — | K8s monitoring using eBPF | Proprietary (free) | — |
| Beszel | Go | 7k+ | Lightweight server monitoring with Docker | MIT | https://github.com/henrygd/beszel |
| HertzBeat | Java | 6k+ | Real-time monitoring system | Apache-2.0 | https://github.com/apache/hertzbeat |
| coroot | Go | 5k+ | Zero-instrumentation observability tool | BUSL | https://github.com/coroot/coroot |
| vector | Rust | 17k+ | High-performance observability data pipeline | MPL-2.0 | https://github.com/vectordotdev/vector |
| OpenObserve | Rust | 13k+ | Cloud-native observability platform | AGPL-3.0 | https://github.com/openobserve/openobserve |

---

## 12. Logging

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Loki | Go | 24k+ | Like Prometheus, but for logs (Grafana) | AGPL-3.0 | https://github.com/grafana/loki |
| Elasticsearch | Java | 69k+ | Distributed search and analytics engine | SSPL/Apache | https://github.com/elastic/elasticsearch |
| OpenSearch | Java | 9k+ | OSS Elasticsearch fork by AWS | Apache-2.0 | https://github.com/opensearch-project/OpenSearch |
| Logstash | Ruby | 14k+ | Data collection, enrichment, transport | Apache-2.0 | https://github.com/elastic/logstash |
| Kibana | TypeScript | 19k+ | Elasticsearch visualization UI | SSPL | https://github.com/elastic/kibana |
| OpenSearch Dashboards | TypeScript | 2k+ | OpenSearch visualization UI | Apache-2.0 | https://github.com/opensearch-project/OpenSearch-Dashboards |
| Fluentd | Ruby | 13k+ | Unified logging layer | Apache-2.0 | https://github.com/fluent/fluentd |
| Fluent Bit | C | 6k+ | Lightweight Fluentd alternative | Apache-2.0 | https://github.com/fluent/fluent-bit |
| Logchef | Vue | 743 | Log analytics UI for ClickHouse | Apache-2.0 | https://github.com/mr-karan/logchef |
| Graylog | Java | 7k+ | Log management with alerting | SSPL | https://github.com/Graylog2/graylog2-server |
| Humio (CrowdStrike) | — | — | Streaming log management (free tier) | Proprietary | — |
| Parseable | Rust | 2k+ | Cloud-native log management | Apache-2.0 | https://github.com/parseablehq/parseable |
| Quickwit | Rust | 8k+ | Cloud-native search engine for logs | Apache-2.0 | https://github.com/quickwit-oss/quickwit |
| ClickHouse | C++ | 38k+ | Fast OLAP database (great for logs) | Apache-2.0 | https://github.com/ClickHouse/ClickHouse |
| rsyslog | C | 2k+ | High-performance syslog implementation | GPL/LGPL | https://github.com/rsyslog/rsyslog |
| syslog-ng | C | 2k+ | Flexible syslog daemon | GPL-2.0 | https://github.com/syslog-ng/syslog-ng |
| journald | C | — | systemd's binary journal system | LGPL-2.1 | — |
| Logrotate | C | 1k+ | Log rotation and compression utility | GPL-2.0 | https://github.com/logrotate/logrotate |
| multilog | C | — | Multi-log file management tool | Public Domain | — |
| s6-log | C | — | Event logger for s6 init system | ISC | — |
| GoAccess | C | 18k+ | Real-time web log analyzer | MIT | https://github.com/allinurl/goaccess |
| AWStats | Perl | 1k+ | Advanced web statistics | GPL-2.0 | https://github.com/eldy/awstats |
| pfSense/syslog | C | — | Syslog-ng for network appliances | Apache-2.0 | — |
| logfmt | Go | 1k+ | Structured logging format | MIT | https://github.com/go-logfmt/logfmt |
| zap | Go | 22k+ | Blazing fast structured logging in Go | MIT | https://github.com/uber-go/zap |
| zerolog | Go | 10k+ | Zero-allocation Go JSON logger | MIT | https://github.com/rs/zerolog |
| logrus | Go | 24k+ | Structured pluggable logging for Go | MIT | https://github.com/sirupsen/logrus |
| slog | Go | — | Go standard library structured logger | BSD-3 | — |
| structlog | Python | 3k+ | Structured logging for Python | MIT/Apache-2.0 | https://github.com/hynek/structlog |
| loguru | Python | 19k+ | Python logging with no boilerplate | MIT | https://github.com/Delgan/loguru |
| winston | JavaScript | 22k+ | Multi-transport Node.js logger | MIT | https://github.com/winstonjs/winston |
| pino | JavaScript | 14k+ | Super fast Node.js logger | MIT | https://github.com/pinojs/pino |
| log4j2 | Java | 3k+ | Apache logging framework for Java | Apache-2.0 | https://github.com/apache/logging-log4j2 |
| Logback | Java | 3k+ | Java logging framework | EPL-1.0 | https://github.com/qos-ch/logback |
| SLF4J | Java | 2k+ | Simple Logging Facade for Java | MIT | https://github.com/qos-ch/slf4j |

---

## 13. Databases - Relational

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| PostgreSQL | C | 16k+ | World's most advanced open-source RDBMS | PostgreSQL | https://github.com/postgres/postgres |
| MySQL | C/C++ | 10k+ | World's most popular open-source RDBMS | GPL-2.0 | https://github.com/mysql/mysql-server |
| MariaDB | C/C++ | 5k+ | MySQL-compatible, community-driven fork | GPL-2.0 | https://github.com/MariaDB/server |
| SQLite | C | 5k+ | Self-contained serverless SQL database | Public Domain | https://sqlite.org/src |
| DuckDB | C++ | 25k+ | OLAP database for analytical SQL queries | MIT | https://github.com/duckdb/duckdb |
| CockroachDB | Go | 30k+ | Distributed PostgreSQL-compatible SQL | BSL/CCL | https://github.com/cockroachdb/cockroach |
| YugabyteDB | C++ | 9k+ | Distributed PostgreSQL + Cassandra-compatible DB | Apache-2.0 | https://github.com/yugabyte/yugabyte-db |
| TiDB | Go | 37k+ | Distributed HTAP MySQL-compatible database | Apache-2.0 | https://github.com/pingcap/tidb |
| SingleStore (MemSQL) | — | — | Distributed database (free tier) | Proprietary | — |
| Citus | C | 10k+ | Distributed PostgreSQL extension (Citus Data) | AGPL-3.0 | — |
| TimescaleDB | C | 17k+ | Time-series on top of PostgreSQL | Apache-2.0 | https://github.com/timescale/timescaledb |
| PL/pgSQL | — | — | PostgreSQL's built-in procedural language | PostgreSQL | — |
| PostGIS | C | 3k+ | Spatial extension for PostgreSQL | GPL-2.0 | — |
| pgvector | C | 14k+ | Vector similarity search for PostgreSQL | MIT | https://github.com/pgvector/pgvector |
| pg_analytics | Rust | 3k+ | DuckDB-powered OLAP extension for Postgres | AGPL-3.0 | — |
| Supabase | TypeScript | 73k+ | Open-source Firebase alternative using Postgres | Apache-2.0 | https://github.com/supabase/supabase |
| Neon | Rust | 14k+ | Serverless PostgreSQL (open-source) | Apache-2.0 | https://github.com/neondatabase/neon |
| PgBouncer | C | 3k+ | Lightweight connection pooler for Postgres | ISC | — |
| pgpool-II | C | 1k+ | Connection pooling + replication for Postgres | BSD | — |
| Patroni | Python | 6k+ | HA PostgreSQL using distributed consensus | MIT | — |
| repmgr | C | 2k+ | PostgreSQL replication manager | GPL-3.0 | — |
| Barman | Python | 2k+ | PostgreSQL backup and recovery manager | GPL-3.0 | https://github.com/EnterpriseDB/barman |
| pg_dump / pg_restore | C | — | Native Postgres backup tools | PostgreSQL | — |
| pgBackRest | C | 3k+ | PostgreSQL backup solution | MIT | https://github.com/pgbackrest/pgbackrest |
| pgtune | — | — | Web tool for PostgreSQL tuning | MIT | — |
| Vitess | Go | 19k+ | Database clustering for MySQL at YouTube/GitHub | Apache-2.0 | https://github.com/vitessio/vitess |
| ProxySQL | C++ | 6k+ | High-performance MySQL/MariaDB proxy | GPL-3.0 | — |
| MaxScale | C++ | 1k+ | MariaDB's advanced database proxy | BSL-1.1 | — |
| Percona Server | C/C++ | 1k+ | MySQL/MongoDB enhanced open-source distribution | GPL-2.0 | — |
| Galera Cluster | C/C++ | 1k+ | Multi-master MySQL cluster | GPL-2.0 | — |
| Flyway | Java | 8k+ | Database schema migration tool | Apache-2.0 | — |
| Liquibase | Java | 4k+ | Database schema change management | Apache-2.0 | — |
| Atlas | Go | 5k+ | Database schema as code (OSS) | Apache-2.0 | — |
| Bytebase | Go | 11k+ | Database DevOps for teams | MIT | — |
| Adminer | PHP | 6k+ | Single-file database management UI | Apache-2.0/GPL-2.0 | — |
| pgAdmin | Python | 3k+ | PostgreSQL administration and management | PostgreSQL | — |
| DBeaver CE | Java | 40k+ | Universal database tool | Apache-2.0 | — |
| Beekeeper Studio CE | Vue | 15k+ | SQL editor and DB manager | MIT | — |
| TablePlus (OSS ver) | — | — | Modern DB GUI | Proprietary | — |
| dbmate | Go | 4k+ | Database migration tool | MIT | — |
| sql-migrate | Go | 3k+ | SQL schema migration library for Go | MIT | — |
| SQLX | Go | 15k+ | Extensions for Go's `database/sql` | MIT | — |
| GORM | Go | 37k+ | ORM library for Go | MIT | https://github.com/go-gorm/gorm |
| Ent | Go | 15k+ | Entity framework for Go | Apache-2.0 | — |
| SQLAlchemy | Python | 9k+ | SQL toolkit and ORM for Python | MIT | https://github.com/sqlalchemy/sqlalchemy |
| Alembic | Python | 2k+ | Database migration tool for SQLAlchemy | MIT | https://github.com/sqlalchemy/alembic |
| Peewee | Python | 11k+ | Small, expressive ORM for Python | MIT | — |
| Django ORM | Python | — | ORM built into Django framework | BSD-3 | — |
| Hibernate | Java | 6k+ | Object-relational mapper for Java | LGPL-2.1 | — |
| jOOQ | Java | 6k+ | Fluent SQL for Java | Apache-2.0 | — |
| Prisma | TypeScript | 40k+ | Next-gen ORM for Node.js | Apache-2.0 | — |
| Drizzle ORM | TypeScript | 24k+ | TypeScript ORM with SQL-first approach | Apache-2.0 | — |
| Kysely | TypeScript | 11k+ | Type-safe SQL query builder | MIT | — |
| Knex.js | JavaScript | 19k+ | SQL query builder for Node | MIT | — |
| Sequelize | JavaScript | 29k+ | Node.js ORM for SQL databases | MIT | — |
| TypeORM | TypeScript | 34k+ | ORM for TypeScript/JavaScript | MIT | — |
| MikroORM | TypeScript | 8k+ | TypeScript ORM based on Data Mapper | MIT | — |
| Doctrine ORM | PHP | 9k+ | PHP ORM (Symfony, Laravel alternative) | MIT | — |
| Eloquent | PHP | — | Laravel's ORM | MIT | — |

---

## 14. Databases - NoSQL

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| MongoDB | C++ | 26k+ | Document-oriented NoSQL database | SSPL | https://github.com/mongodb/mongo |
| FerretDB | Go | 9k+ | MongoDB-compatible built on PostgreSQL | Apache-2.0 | https://github.com/FerretDB/FerretDB |
| DocumentDB | — | — | AWS MongoDB-compatible (based on Mongo) | Apache-2.0 | — |
| CouchDB | Erlang | 6k+ | Document DB with HTTP API + sync | Apache-2.0 | https://github.com/apache/couchdb |
| PouchDB | JavaScript | 17k+ | CouchDB-compatible client-side DB | Apache-2.0 | https://github.com/pouchdb/pouchdb |
| RethinkDB | C++ | 27k+ | Real-time JSON database | Apache-2.0 | https://github.com/rethinkdb/rethinkdb |
| ArangoDB | C++ | 13k+ | Multi-model (docs/graphs/key-value) DB | Apache-2.0 | https://github.com/arangodb/arangodb |
| OrientDB | Java | 5k+ | Multi-model NoSQL database | Apache-2.0 | https://github.com/orientechnologies/orientdb |
| Couchbase CE | C/C++ | 5k+ | NoSQL JSON database with SQL++ | BSL | — |
| HBase | Java | 5k+ | Distributed NoSQL on top of HDFS | Apache-2.0 | https://github.com/apache/hbase |
| Cassandra | Java | 8k+ | Scalable distributed wide-column store | Apache-2.0 | https://github.com/apache/cassandra |
| ScyllaDB | C++ | 13k+ | Cassandra-compatible, written in C++ (10x faster) | AGPL-3.0 | https://github.com/scylladb/scylladb |
| Redis | C | 67k+ | In-memory data structure store (BSL now) | BSD/BSL-1.1 | https://github.com/redis/redis |
| Valkey | C | 14k+ | Redis fork, community-maintained | BSD-3 | https://github.com/valkey-io/valkey |
| Dragonfly | C++ | 25k+ | In-memory store, Redis/Memcached compatible | BSL-1.1 | https://github.com/dragonflydb/dragonfly |
| KeyDB | C++ | 9k+ | Multi-threaded Redis fork | BSD-3 | https://github.com/Snapchat/KeyDB |
| Memcached | C | 13k+ | Distributed memory object caching | BSD-3 | https://github.com/memcached/memcached |
| LevelDB | C++ | 36k+ | Fast key-value storage by Google | BSD-3 | https://github.com/google/leveldb |
| RocksDB | C++ | 29k+ | Facebook's embedded key-value storage | Apache-2.0 | https://github.com/facebook/rocksdb |
| LMDB | C | 3k+ | Lightning Memory-Mapped Database | OpenLDAP | https://github.com/LMDB/lmdb |
| BadgerDB | Go | 14k+ | Fast key-value DB written in Go | Apache-2.0 | https://github.com/dgraph-io/badger |
| BoltDB/bbolt | Go | 8k+ | Embedded key-value DB for Go | MIT | https://github.com/etcd-io/bbolt |
| etcd | Go | 48k+ | Distributed key-value store (K8s backbone) | Apache-2.0 | https://github.com/etcd-io/etcd |
| Consul KV | Go | 28k+ | Key-value store with service discovery | BSL-1.1 | — |
| ZooKeeper | Java | 12k+ | Distributed coordination service | Apache-2.0 | https://github.com/apache/zookeeper |
| DynamoDB Local | Java | — | Local emulator for Amazon DynamoDB | Apache-2.0 | — |
| Dynamo (open) | — | — | Various Amazon Dynamo-inspired OSS impls | Various | — |
| ScyllaDB Alternator | C++ | — | DynamoDB-compatible API in ScyllaDB | AGPL-3.0 | — |
| DynamoDBLocal | Java | — | AWS test harness for DynamoDB | Apache-2.0 | — |
| SurrealDB | Rust | 28k+ | Multi-model NewSQL database | BSL-1.1 | https://github.com/surrealdb/surrealdb |
| PlanetScale (Vitess) | Go | 19k+ | MySQL-compatible serverless DB | Apache-2.0 | https://github.com/vitessio/vitess |
| TiKV | Rust | 15k+ | Distributed transactional key-value database | Apache-2.0 | https://github.com/tikv/tikv |
| SpiceDB | Go | 5k+ | Permission database inspired by Zanzibar | Apache-2.0 | https://github.com/authzed/spicedb |
| Permify | Go | 5k+ | Open-source authorization service | Apache-2.0 | https://github.com/Permify/permify |
| Doris | C++ | 13k+ | Apache OLAP database (Palo fork) | Apache-2.0 | https://github.com/apache/doris |
| StarRocks | C++ | 9k+ | OLAP database for real-time analytics | Apache-2.0 | https://github.com/StarRocks/starrocks |
| Hive | Java | 5k+ | Petabyte-scale Hadoop data warehouse | Apache-2.0 | https://github.com/apache/hive |
| Impala | C++ | 1k+ | Massively parallel MPP SQL for Hadoop | Apache-2.0 | https://github.com/apache/impala |
| PrestoDB | Java | 15k+ | Distributed SQL query engine by Facebook | Apache-2.0 | https://github.com/prestodb/presto |
| Trino | Java | 10k+ | PrestoSQL rebranded/community fork | Apache-2.0 | https://github.com/trinodb/trino |
| Apache Kylin | Java | 4k+ | OLAP cube on Hadoop | Apache-2.0 | https://github.com/apache/kylin |
| Pinot | Java | 5k+ | Distributed OLAP datastore by LinkedIn | Apache-2.0 | https://github.com/apache/pinot |
| Druid | Java | 14k+ | Real-time analytics database | Apache-2.0 | https://github.com/apache/druid |
| Kudu | C++ | 2k+ | Columnar storage for Hadoop | Apache-2.0 | https://github.com/apache/kudu |
| FoundationDB | C++ | 14k+ | Distributed ACID key-value store | Apache-2.0 | https://github.com/apple/foundationdb |
| TigerBeetle | Zig | 9k+ | Distributed financial accounting database | Apache-2.0 | https://github.com/tigerbeetle/tigerbeetle |
| Garage | Rust | 3k+ | S3-compatible distributed object storage | AGPL-3.0 | https://git.deuxfleurs.fr/Deuxfleurs/garage |
| SeaweedFS | Go | 23k+ | Distributed file storage (S3-compatible) | Apache-2.0 | https://github.com/seaweedfs/seaweedfs |
| MinIO | Go | 49k+ | High-performance S3-compatible object store | AGPL-3.0 | https://github.com/minio/minio |
| Ceph | C++ | 14k+ | Unified distributed storage | LGPL-2.1 | https://github.com/ceph/ceph |
| GlusterFS | C | 4k+ | Open-source distributed filesystem | GPL-3.0 | https://github.com/gluster/glusterfs |

---

## 15. Databases - Time Series

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| InfluxDB | Go | 29k+ | Purpose-built time-series database | MIT/BSL | https://github.com/influxdata/influxdb |
| TimescaleDB | C | 17k+ | Time-series PostgreSQL extension | Apache-2.0 | https://github.com/timescale/timescaledb |
| Prometheus | Go | 56k+ | Monitoring system with time-series DB | Apache-2.0 | https://github.com/prometheus/prometheus |
| VictoriaMetrics | Go | 13k+ | Fast long-term TS metrics storage | Apache-2.0 | https://github.com/VictoriaMetrics/VictoriaMetrics |
| QuestDB | Java | 14k+ | High-performance time-series database | Apache-2.0 | https://github.com/questdb/questdb |
| TDengine | C | 23k+ | Time-series database for IoT | AGPL-3.0 | https://github.com/taosdata/TDengine |
| openTSDB | Java | 5k+ | Distributed time-series database on HBase | LGPL-2.1 | https://github.com/OpenTSDB/opentsdb |
| Graphite | Python | 6k+ | Scalable realtime graphing server | Apache-2.0 | https://github.com/graphite-project/graphite-web |
| Druid | Java | 14k+ | Real-time analytics with time-series support | Apache-2.0 | https://github.com/apache/druid |
| M3DB | Go | 4k+ | Distributed time-series storage by Uber | Apache-2.0 | https://github.com/m3db/m3 |
| CrateDB | Java | 4k+ | SQL for real-time machine data | Apache-2.0 | https://github.com/crate/crate |
| GridDB | C++ | 2k+ | IoT-focused time-series database | Apache-2.0 | https://github.com/griddb/griddb |
| Riak TS | Erlang | — | Distributed time-series on Riak | Apache-2.0 | — |

---

## 16. Databases - Graph

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Neo4j CE | Java | 13k+ | Graph database with Cypher query language | GPL-3.0 | https://github.com/neo4j/neo4j |
| ArangoDB | C++ | 13k+ | Multi-model including graph traversal | Apache-2.0 | https://github.com/arangodb/arangodb |
| JanusGraph | Java | 5k+ | Distributed graph database | Apache-2.0 | https://github.com/JanusGraph/janusgraph |
| TigerGraph | — | — | Graph analytics platform (free tier) | Proprietary | — |
| Dgraph | Go | 20k+ | Native GraphQL + graph database | Apache-2.0 | https://github.com/hypermodeinc/dgraph |
| Cayley | Go | 15k+ | Open-source graph inspired by Google's Knowledge Graph | Apache-2.0 | https://github.com/cayleygraph/cayley |
| RedisGraph | C | — | Sparse graph database as Redis module | Redis SSPL | — |
| AgensGraph | C | 1k+ | Graph extension for PostgreSQL | Apache-2.0 | https://github.com/bitnine-oss/agensgraph |
| Apache Giraph | Java | 1k+ | Large-scale graph processing system | Apache-2.0 | https://github.com/apache/giraph |
| GraphX (Spark) | Scala | — | Graph computation on Apache Spark | Apache-2.0 | — |
| NebulaGraph | C++ | 10k+ | Distributed graph database | Apache-2.0 | https://github.com/vesoft-inc/nebula |
| HugeGraph | Java | 3k+ | OLAP graph database by Baidu | Apache-2.0 | https://github.com/apache/incubator-hugegraph |
| OrientDB | Java | 5k+ | Multi-model with graph support | Apache-2.0 | https://github.com/orientechnologies/orientdb |
| CosmosDB (emulator) | — | — | Azure multi-model (local emulator) | MIT (emulator) | — |

---

## 17. Databases - Vector

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| pgvector | C | 14k+ | Vector similarity search for PostgreSQL | MIT | https://github.com/pgvector/pgvector |
| Qdrant | Rust | 22k+ | Vector database + search engine | Apache-2.0 | https://github.com/qdrant/qdrant |
| Weaviate | Go | 12k+ | Open-source vector database | BSD-3 | https://github.com/weaviate/weaviate |
| Chroma | Python | 16k+ | Embedding database for AI apps | Apache-2.0 | https://github.com/chroma-core/chroma |
| Milvus | C++ | 31k+ | Cloud-native vector database | Apache-2.0 | https://github.com/milvus-io/milvus |
| LanceDB | Rust | 6k+ | Developer-friendly vector DB for AI | Apache-2.0 | https://github.com/lancedb/lancedb |
| Pinecone (local) | — | — | Managed vector DB (proprietary) | Proprietary | — |
| Marqo | Python | 5k+ | Tensor search for end-to-end vector search | Apache-2.0 | https://github.com/marqo-ai/marqo |
| Vespa | Java | 5k+ | Big data serving engine for search/ML | Apache-2.0 | https://github.com/vespa-engine/vespa |
| OpenSearch (kNN) | Java | 9k+ | kNN plugin for vector search | Apache-2.0 | — |
| Deep Lake | Python | 8k+ | Lakehouse for deep learning | MPL-2.0 | https://github.com/activeloopai/deeplake |
| AnnLite | Python | 1k+ | Efficient approximate nearest neighbor | Apache-2.0 | — |
| Faiss | C++ | 33k+ | Facebook's library for efficient similarity search | MIT | https://github.com/facebookresearch/faiss |
| Annoy | C++ | 13k+ | Approximate nearest neighbor by Spotify | Apache-2.0 | https://github.com/spotify/annoy |
| ScaNN | C++ | 3k+ | Scalable nearest neighbor search by Google | Apache-2.0 | https://github.com/google-research/google-research/tree/master/scann |
| HNSW (hnswlib) | C++ | 4k+ | Hierarchical Navigable Small World index | Apache-2.0 | https://github.com/nmslib/hnswlib |
| VectorFlow | Python | 2k+ | Pipeline to vectorize and store documents | MIT | — |
| txtai | Python | 9k+ | Semantic search + vector database | Apache-2.0 | https://github.com/neuml/txtai |

---

## 18. Databases - Search

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Elasticsearch | Java | 69k+ | Distributed search and analytics | SSPL | https://github.com/elastic/elasticsearch |
| OpenSearch | Java | 9k+ | Apache-licensed Elasticsearch fork | Apache-2.0 | https://github.com/opensearch-project/OpenSearch |
| Solr | Java | 4k+ | Enterprise search platform by Apache | Apache-2.0 | https://github.com/apache/solr |
| Meilisearch | Rust | 48k+ | Blazing-fast developer-friendly search | MIT | https://github.com/meilisearch/meilisearch |
| Typesense | C++ | 21k+ | Open-source instant search engine | GPL-3.0 | https://github.com/typesense/typesense |
| Quickwit | Rust | 8k+ | Sub-second search for log data | Apache-2.0 | https://github.com/quickwit-oss/quickwit |
| Tantivy | Rust | 12k+ | Full-text search engine library in Rust | MIT | https://github.com/quickwit-oss/tantivy |
| Bleve | Go | 9k+ | Full-text search and indexing in Go | Apache-2.0 | https://github.com/blevesearch/bleve |
| Sphinx | C++ | 2k+ | Open-source full-text search | GPL-2.0 | https://github.com/sphinx-doc/sphinx |
| Manticore Search | C++ | 9k+ | Fast alternative to Elasticsearch | GPL-2.0 | https://github.com/manticoresoftware/manticoresearch |
| Xapian | C++ | 1k+ | Open-source probabilistic IR library | GPL-2.0 | https://github.com/xapian/xapian |
| Whoosh | Python | 3k+ | Pure Python full-text indexing | BSD-2 | https://github.com/whoosh-community/whoosh |
| Groonga | C | 1k+ | Columnstore + full-text search | LGPL-2.1 | — |
| Sonic | Rust | 20k+ | Lightweight fast search backend | MIT | https://github.com/valeriansaliou/sonic |
| ZincSearch | Go | 17k+ | Lightweight Elasticsearch alternative | Apache-2.0 | https://github.com/zincsearch/zincsearch |
| Toshi | Rust | 4k+ | Full-text search engine like Elasticsearch | MIT | — |
| RediSearch | C | — | Full-text search as Redis module | Redis SSPL | — |
| ParadeDB | Rust | 6k+ | Postgres-based Elasticsearch replacement | AGPL-3.0 | https://github.com/paradedb/paradedb |

---

## 19. Message Queues & Streaming

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Apache Kafka | Java/Scala | 28k+ | Distributed event streaming platform | Apache-2.0 | https://github.com/apache/kafka |
| Apache Pulsar | Java | 14k+ | Cloud-native distributed messaging | Apache-2.0 | https://github.com/apache/pulsar |
| RabbitMQ | Erlang | 12k+ | Feature-rich message broker | MPL-2.0 | https://github.com/rabbitmq/rabbitmq-server |
| NATS | Go | 16k+ | High-performance cloud-native messaging | Apache-2.0 | https://github.com/nats-io/nats-server |
| NSQ | Go | 25k+ | Realtime distributed messaging platform | MIT | https://github.com/nsqio/nsq |
| ZeroMQ | C++ | 9k+ | High-performance messaging library | MPL-2.0 | https://github.com/zeromq/libzmq |
| ActiveMQ | Java | 2k+ | Apache message broker | Apache-2.0 | https://github.com/apache/activemq |
| ActiveMQ Artemis | Java | 1k+ | Next-gen ActiveMQ with better performance | Apache-2.0 | https://github.com/apache/activemq-artemis |
| EMQ X (EMQX) | Erlang | 14k+ | MQTT broker for IoT | Apache-2.0 | https://github.com/emqx/emqx |
| VerneMQ | Erlang | 3k+ | Distributed MQTT broker | Apache-2.0 | https://github.com/vernemq/vernemq |
| Mosquitto | C | 9k+ | MQTT broker by Eclipse | EPL-2.0 | https://github.com/eclipse/mosquitto |
| Redis Streams | C | — | Stream data structure in Redis | BSD/BSL | — |
| Apache RocketMQ | Java | 21k+ | Fast distributed messaging by Alibaba | Apache-2.0 | https://github.com/apache/rocketmq |
| Memphis | Go | 3k+ | Dev-first message broker | Apache-2.0 | https://github.com/memphisdev/memphis |
| Redpanda | C++ | 9k+ | Kafka-compatible C++ streaming platform | BSL-1.1 | https://github.com/redpanda-data/redpanda |
| Benthos (Bento) | Go | 8k+ | Stream processor for complex pipelines | MIT | https://github.com/warpstreamlabs/bento |
| Flink | Java | 24k+ | Stateful stream processing | Apache-2.0 | https://github.com/apache/flink |
| Storm | Java/Python | 7k+ | Distributed realtime computation | Apache-2.0 | https://github.com/apache/storm |
| Samza | Java | 3k+ | Distributed stream processing by LinkedIn | Apache-2.0 | https://github.com/apache/samza |
| Spark Streaming | Scala | 40k+ | Real-time data processing on Spark | Apache-2.0 | — |
| Kafka Streams | Java | — | Stream processing library inside Kafka | Apache-2.0 | — |
| Hazelcast | Java | 6k+ | In-memory data grid + streaming | Apache-2.0 | https://github.com/hazelcast/hazelcast |
| Jet (Hazelcast) | Java | — | Distributed stream processing | Apache-2.0 | — |
| Aeron | Java | 7k+ | Efficient messaging transport | Apache-2.0 | https://github.com/real-logic/aeron |
| Chronicle Queue | Java | 3k+ | Ultra-low latency queue for Java | Apache-2.0 | https://github.com/OpenHFT/Chronicle-Queue |
| Disruptor | Java | 7k+ | High-performance inter-thread messaging | Apache-2.0 | https://github.com/LMAX-Exchange/disruptor |
| Dapr | Go | 24k+ | Distributed application runtime | Apache-2.0 | https://github.com/dapr/dapr |
| Temporal | Go | 12k+ | Durable workflow execution platform | MIT | https://github.com/temporalio/temporal |
| Conductor | Java | 9k+ | Microservices orchestration platform | Apache-2.0 | https://github.com/Netflix/conductor |
| Cadence | Go | 8k+ | Distributed workflow engine by Uber | MIT | https://github.com/uber/cadence |
| Prefect | Python | 17k+ | Dataflow automation platform | Apache-2.0 | https://github.com/PrefectHQ/prefect |
| Airflow | Python | 37k+ | Workflow orchestration by Apache | Apache-2.0 | https://github.com/apache/airflow |
| Dagster | Python | 11k+ | Data orchestration framework | Apache-2.0 | https://github.com/dagster-io/dagster |
| Celery | Python | 24k+ | Distributed task queue for Python | BSD-3 | https://github.com/celery/celery |
| Dramatiq | Python | 4k+ | Background task processing for Python | LGPL-3.0 | https://github.com/Bogdanp/dramatiq |
| Huey | Python | 5k+ | Lightweight task queue for Python | MIT | https://github.com/coleifer/huey |
| RQ (Redis Queue) | Python | 10k+ | Simple Python job queues with Redis | BSD-2 | https://github.com/rq/rq |
| Sidekiq (CE) | Ruby | 13k+ | Background job processing for Ruby | LGPL-3.0 | https://github.com/sidekiq/sidekiq |
| Resque | Ruby | 9k+ | Redis-backed Ruby library for job processing | MIT | https://github.com/resque/resque |
| Bull | JavaScript | 15k+ | Node.js job queue backed by Redis | MIT | https://github.com/OptimalBits/bull |
| BullMQ | TypeScript | 6k+ | Bull rewrite with TypeScript | MIT | https://github.com/taskforcesh/bullmq |
| Bee Queue | JavaScript | 3k+ | Fast Redis-backed job queue for Node | MIT | https://github.com/bee-queue/bee-queue |
| Faktory | Go | 6k+ | Language-agnostic job server | BSL-1.1 | https://github.com/contribsys/faktory |
| Machinery | Go | 7k+ | Async task queue/job queue for Go | MIT | https://github.com/RichardKnop/machinery |
| Asynq | Go | 10k+ | Simple, reliable async task queue for Go | MIT | https://github.com/hibiken/asynq |
| River | Go | 3k+ | Robust job queue for Go using Postgres | MIT | https://github.com/riverqueue/river |
| Dungbeetle | Go | 1.2k | Distributed job server for heavy SQL reads | MIT | — |

---

## 20. Caching & In-Memory

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Redis | C | 67k+ | In-memory data structure store | BSD/BSL-1.1 | https://github.com/redis/redis |
| Valkey | C | 14k+ | OSS Redis fork | BSD-3 | https://github.com/valkey-io/valkey |
| Dragonfly | C++ | 25k+ | Modern Redis/Memcached compatible store | BSL-1.1 | https://github.com/dragonflydb/dragonfly |
| KeyDB | C++ | 9k+ | Multithreaded Redis fork | BSD-3 | https://github.com/Snapchat/KeyDB |
| Memcached | C | 13k+ | Distributed memory cache | BSD-3 | https://github.com/memcached/memcached |
| Hazelcast IMDG | Java | 6k+ | In-memory data grid | Apache-2.0 | — |
| Apache Ignite | Java | 4k+ | Distributed database + cache | Apache-2.0 | https://github.com/apache/ignite |
| Ehcache | Java | 2k+ | Java caching library | Apache-2.0 | https://github.com/ehcache/ehcache3 |
| Caffeine | Java | 16k+ | High-performance Java caching | Apache-2.0 | https://github.com/ben-manes/caffeine |
| Guava Cache | Java | — | In-process caching for Java | Apache-2.0 | — |
| Ristretto | Go | 5k+ | High-performance Go cache library | Apache-2.0 | https://github.com/hypermodeinc/ristretto |
| groupcache | Go | 13k+ | Peer-to-peer caching library by Go team | Apache-2.0 | https://github.com/golang/groupcache |
| bigcache | Go | 7k+ | Efficient in-memory cache for Go | Apache-2.0 | https://github.com/allegro/bigcache |
| fastcache | Go | 2k+ | Fast thread-safe in-memory cache for big items | MIT | https://github.com/VictoriaMetrics/fastcache |
| go-cache | Go | 5k+ | In-memory key:value store for Go | MIT | https://github.com/patrickmn/go-cache |
| node-cache | JavaScript | 2k+ | Simple in-process caching for Node | MIT | https://github.com/node-cache/node-cache |
| lru-cache | JavaScript | 5k+ | LRU cache for Node | ISC | https://github.com/isaacs/node-lru-cache |
| aiocache | Python | 1k+ | Async cache for Python | BSD-3 | https://github.com/aio-libs/aiocache |
| cachetools | Python | 2k+ | Extensible caching library for Python | MIT | https://github.com/tkem/cachetools |
| dogpile.cache | Python | — | Caching with dogpile prevention | BSD-3 | — |
| Varnish | C | 4k+ | HTTP accelerator and reverse proxy cache | BSD-2 | https://github.com/varnishcache/varnish-cache |
| Squid | C | — | Full-featured caching proxy | GPL-2.0 | — |
| Nginx proxy cache | C | — | HTTP caching layer in Nginx | BSD-2 | — |
| Apache Traffic Server | C++ | 1k+ | High-performance caching proxy | Apache-2.0 | https://github.com/apache/trafficserver |
| Blobasaur | Rust | 43 | SQLite-backed blob store with Redis protocol | MIT | — |

---

## 21. Networking & Proxy

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Nginx | C | 22k+ | High-performance HTTP server and reverse proxy | BSD-2 | https://github.com/nginx/nginx |
| Apache HTTPD | C | 4k+ | The original web server | Apache-2.0 | https://github.com/apache/httpd |
| Caddy | Go | 58k+ | Modern web server with auto HTTPS | Apache-2.0 | https://github.com/caddyserver/caddy |
| Traefik | Go | 51k+ | Cloud-native edge router/reverse proxy | MIT | https://github.com/traefik/traefik |
| HAProxy | C | 5k+ | High-availability load balancer and proxy | GPL-2.0 | https://github.com/haproxy/haproxy |
| Envoy | C++ | 25k+ | L7 proxy and communication bus (CNCF) | Apache-2.0 | https://github.com/envoyproxy/envoy |
| Pingora | Rust | 22k+ | Cloudflare's Rust HTTP proxy framework | Apache-2.0 | https://github.com/cloudflare/pingora |
| Pound | C | 1k+ | Reverse proxy and load balancer | GPL-3.0 | — |
| Lighttpd | C | 1k+ | Lightweight high-performance web server | BSD-3 | https://github.com/lighttpd/lighttpd1.4 |
| Hiawatha | C | 1k+ | Security-focused web server | GPLv2 | — |
| OpenLiteSpeed | C | 1k+ | Open-source LiteSpeed server | GPLv3 | — |
| Squid | C | — | Caching and forwarding proxy | GPL-2.0 | — |
| Varnish | C | 4k+ | HTTP accelerator | BSD-2 | https://github.com/varnishcache/varnish-cache |
| WireGuard | C | 5k+ | Fast modern VPN built into Linux kernel | GPL-2.0 | https://git.zx2c4.com/wireguard-linux |
| OpenVPN | C | 10k+ | SSL-based VPN protocol | GPL-2.0 | https://github.com/OpenVPN/openvpn |
| Tailscale (OSS) | Go | 18k+ | Zero-config VPN using WireGuard | BSD-3 | https://github.com/tailscale/tailscale |
| Headscale | Go | 20k+ | Self-hosted Tailscale control server | BSD-3 | https://github.com/juanfont/headscale |
| Netbird | Go | 11k+ | P2P VPN using WireGuard | Apache-2.0 | https://github.com/netbirdio/netbird |
| Nebula | Go | 15k+ | Overlay networking by Slack | MIT | https://github.com/slackhq/nebula |
| ZeroTier | C | 14k+ | Global virtual networking | BSL-1.1 | — |
| frp | Go | 89k+ | Fast reverse proxy to NAT/firewall | Apache-2.0 | https://github.com/fatedier/frp |
| ngrok (OSS) | Go | 23k+ | Secure introspectable tunnel to localhost | MIT | https://github.com/inconshreveable/ngrok |
| bore | Rust | 8k+ | Simple TCP tunnels to localhost | MIT | https://github.com/ekzhang/bore |
| chisel | Go | 12k+ | Fast TCP/UDP tunnel over HTTP | MIT | https://github.com/jpillora/chisel |
| localtunnel | JavaScript | 18k+ | Expose localhost to internet | MIT | https://github.com/localtunnel/localtunnel |
| inlets | Go | 15k+ | Tunnel and load balancer for self-hosted | MIT | https://github.com/inlets/inlets |
| Rathole | Rust | 9k+ | Lightweight, stable reverse proxy | Apache-2.0 | https://github.com/rapiz1/rathole |
| Teleport | Go | 17k+ | Secure access for infrastructure | Apache-2.0 | https://github.com/gravitational/teleport |
| Warpgate | Rust | 6k+ | Smart SSH/HTTP bastion host | Apache-2.0 | https://github.com/warp-tech/warpgate |
| OpenSSH | C | 3k+ | Industry standard SSH implementation | BSD | https://github.com/openssh/openssh-portable |
| Dropbear | C | — | Lightweight SSH server for embedded | MIT | — |
| dnscrypt-proxy | Go | 11k+ | DNS proxy with DoH/DoT support | ISC | https://github.com/DNSCrypt/dnscrypt-proxy |
| CoreDNS | Go | 12k+ | Extensible DNS server (CNCF) | Apache-2.0 | https://github.com/coredns/coredns |
| PowerDNS | C++ | 3k+ | Versatile nameserver | GPL-2.0 | https://github.com/PowerDNS/pdns |
| BIND9 | C | 2k+ | Berkeley Internet Name Domain server | MPL-2.0 | https://gitlab.isc.org/isc-projects/bind9 |
| Knot DNS | C | 1k+ | High-performance authoritative DNS | GPL-3.0 | https://gitlab.nic.cz/knot/knot-dns |
| Unbound | C | 3k+ | Validating, recursive DNS resolver | BSD-3 | https://github.com/NLnetLabs/unbound |
| Pi-hole | Shell | 50k+ | Network-wide ad blocker via DNS | EUPL-1.2 | https://github.com/pi-hole/pi-hole |
| AdGuard Home | Go | 25k+ | Network-level ad and tracker blocker | GPL-3.0 | https://github.com/AdguardTeam/AdGuardHome |
| Blocky | Go | 5k+ | Fast and lightweight DNS proxy | Apache-2.0 | https://github.com/0xERR0R/blocky |
| iptables | C | — | Linux kernel netfilter CLI | GPL-2.0 | — |
| nftables | C | — | Successor to iptables | GPL-2.0 | — |
| pfSense | PHP | 3k+ | Open-source firewall/router | Apache-2.0 | https://github.com/pfsense/FreeBSD-ports |
| OPNsense | PHP | 3k+ | pfSense fork with modern UI | BSD-2 | https://github.com/opnsense/core |
| VyOS | Python | 2k+ | Open-source network OS for routers | LGPL-2.1 | https://github.com/vyos/vyos-build |
| OpenWrt | C | 7k+ | Open-source firmware for embedded devices | GPL-2.0 | https://github.com/openwrt/openwrt |
| FRRouting (FRR) | C | 4k+ | Full-featured IP routing protocol suite | GPL-2.0 | https://github.com/FRRouting/frr |
| BIRD | C | 1k+ | BGP/OSPF/RIP routing daemon | GPL-2.0 | https://gitlab.nic.cz/labs/bird |
| Quagga | C | 1k+ | Network routing software | GPL-2.0 | https://github.com/Quagga/quagga |
| Keepalived | C | 4k+ | VRRP HA and load-balancing for Linux | GPL-2.0 | https://github.com/acassen/keepalived |
| IPVS | C | — | IP Virtual Server in Linux kernel | GPL-2.0 | — |
| GoBGP | Go | 3k+ | BGP implementation in Go | Apache-2.0 | https://github.com/osrg/gobgp |
| Stunnel | C | 1k+ | Multi-platform TLS tunneling proxy | GPL-2.0 | https://github.com/mtrojnar/stunnel |
| Privoxy | C | — | Privacy-enhancing web proxy | GPL-2.0 | https://github.com/enkore/privoxy |
| Shadowsocks | Python/C | 37k+ | Secure SOCKS5 proxy | Apache-2.0 | https://github.com/shadowsocks/shadowsocks |
| V2Ray | Go | 23k+ | Modular proxy framework | MIT | https://github.com/v2ray/v2ray-core |
| Clash | Go | 20k+ | Rule-based proxy for multiple protocols | GPL-3.0 | https://github.com/Dreamacro/clash |
| Xray-core | Go | 28k+ | Network proxy toolkit | MPL-2.0 | https://github.com/XTLS/Xray-core |
| goproxy | Go | 16k+ | Golang HTTP/HTTPS/Websocket proxy | MIT | https://github.com/elazarl/goproxy |
| mitmproxy | Python | 37k+ | HTTP/HTTPS proxy for debugging | MIT | https://github.com/mitmproxy/mitmproxy |
| Fiddler Classic | — | — | HTTP debugging proxy (free) | Proprietary | — |
| Charles Proxy | — | — | HTTP proxy/monitor (paid) | Proprietary | — |
| Hoverfly | Go | 2k+ | API simulation using proxy | Apache-2.0 | https://github.com/SpectoLabs/hoverfly |
| toxiproxy | Go | 11k+ | TCP proxy for simulating network chaos | MIT | https://github.com/Shopify/toxiproxy |
| Wireshark | C | 8k+ | Network protocol analyzer | GPL-2.0 | https://gitlab.com/wireshark/wireshark |
| tcpdump | C | 2k+ | CLI packet analyzer | BSD-3 | https://github.com/the-tcpdump-group/tcpdump |
| nmap | C | 10k+ | Network scanner/security scanner | GPL-2.0 | https://github.com/nmap/nmap |
| masscan | C | 22k+ | Mass port scanner | AGPL-3.0 | https://github.com/robertdavidgraham/masscan |
| netcat (ncat) | C | — | Swiss army knife of networking | GPL-2.0 | — |
| socat | C | — | Multipurpose relay for bidirectional transfer | GPL-2.0 | — |
| iproute2 | C | — | Linux IP routing/network utilities | GPL-2.0 | — |
| iperf3 | C | 6k+ | Network bandwidth measurement tool | BSD-3 | https://github.com/esnet/iperf |
| httpie | Python | 33k+ | HTTP client for the API era | BSD-3 | https://github.com/httpie/cli |
| curl | C | 36k+ | Command-line URL transfer tool | MIT | https://github.com/curl/curl |
| wget | C | — | Non-interactive network downloader | GPL-3.0 | — |
| aria2 | C++ | 35k+ | Multi-protocol download utility | GPL-2.0 | https://github.com/aria2/aria2 |

---

## 22. Service Mesh & API Gateway

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Istio | Go | 36k+ | Service mesh with traffic management | Apache-2.0 | https://github.com/istio/istio |
| Linkerd | Rust/Go | 10k+ | Ultra-light service mesh (CNCF) | Apache-2.0 | https://github.com/linkerd/linkerd2 |
| Consul Connect | Go | 28k+ | Service mesh layer in Consul | BSL-1.1 | — |
| Kuma | Go | 4k+ | Multi-zone service mesh (CNCF) | Apache-2.0 | https://github.com/kumahq/kuma |
| Open Service Mesh | Go | 2k+ | Lightweight SMI-spec service mesh | Apache-2.0 | https://github.com/openservicemesh/osm |
| Cilium (mesh) | Go | 20k+ | eBPF-based service mesh | Apache-2.0 | — |
| Kong Gateway CE | Lua | 39k+ | Cloud-native API gateway | Apache-2.0 | https://github.com/Kong/kong |
| APISIX | Lua | 14k+ | Apache cloud-native API gateway | Apache-2.0 | https://github.com/apache/apisix |
| KrakenD CE | Go | 6k+ | Ultra-high performance API gateway | Apache-2.0 | https://github.com/krakend/krakend-ce |
| Traefik | Go | 51k+ | Cloud-native reverse proxy / API gateway | MIT | https://github.com/traefik/traefik |
| Nginx API GW | C | — | NGINX-based API gateway | BSD-2 | — |
| Oathkeeper | Go | 3k+ | Identity and access proxy | Apache-2.0 | https://github.com/ory/oathkeeper |
| Tyk | Go | 9k+ | Open-source API gateway | MPL-2.0 | https://github.com/TykTechnologies/tyk |
| Gravitee | Java | 4k+ | API management platform | Apache-2.0 | https://github.com/gravitee-io/gravitee-api-management |
| WSO2 API Manager | Java | 800+ | Full API management platform | Apache-2.0 | — |
| Apiman | Java | 900+ | API management platform | Apache-2.0 | — |
| Gloo Edge CE | Go | 4k+ | Envoy-based API gateway | Apache-2.0 | https://github.com/solo-io/gloo |
| Emissary-ingress | Go | 4k+ | Kubernetes-native API gateway | Apache-2.0 | https://github.com/emissary-ingress/emissary |
| Higress | Go | 3k+ | Cloud-native API gateway by Alibaba | Apache-2.0 | https://github.com/alibaba/higress |
| Lura (KrakenD) | Go | 6k+ | Open-source API gateway framework | Apache-2.0 | — |
| go-api-gateway | Go | 1k+ | Simple API gateway in Go | MIT | — |
| Fusio | PHP | 2k+ | Open-source API management platform | Apache-2.0 | https://github.com/apioo/fusio |

---

## 23. Security & Secrets

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| HashiCorp Vault | Go | 31k+ | Secrets management and encryption | BSL-1.1 | https://github.com/hashicorp/vault |
| OpenBao | Go | 3k+ | Open-source Vault fork | MPL-2.0 | https://github.com/openbao/openbao |
| Infisical | TypeScript | 16k+ | Open-source Secrets Manager (Vault alt.) | MIT | https://github.com/Infisical/infisical |
| Doppler | — | — | Secrets management platform (free tier) | Proprietary | — |
| SOPS | Go | 17k+ | Encrypt YAML/JSON/ENV secrets | MPL-2.0 | https://github.com/getsops/sops |
| age | Go | 18k+ | Simple, modern file encryption | BSD-3 | https://github.com/FiloSottile/age |
| sealed-secrets | Go | 8k+ | Kubernetes secrets encryption | Apache-2.0 | https://github.com/bitnami-labs/sealed-secrets |
| External Secrets | Go | 4k+ | K8s operator to sync secrets from external stores | Apache-2.0 | https://github.com/external-secrets/external-secrets |
| pass | Bash | — | Standard Unix password manager | GPL-2.0 | https://git.zx2c4.com/password-store/ |
| gopass | Go | 6k+ | Team password manager (pass fork) | MIT | https://github.com/gopasspw/gopass |
| Bitwarden (Vaultwarden) | Rust | 38k+ | OSS password manager server backend | AGPL-3.0 | https://github.com/dani-garcia/vaultwarden |
| KeePassXC | C++ | 21k+ | Cross-platform password manager | GPL-3.0 | https://github.com/keepassxreboot/keepassxc |
| Passbolt CE | PHP | 4k+ | Team password manager for developers | AGPL-3.0 | https://github.com/passbolt/passbolt_api |
| Psono | Python | 1k+ | Open-source password manager | Apache-2.0 | https://github.com/psono/psono-server |
| CertBot | Python | 12k+ | Automatic HTTPS with Let's Encrypt | Apache-2.0 | https://github.com/certbot/certbot |
| step-ca | Go | 6k+ | Small step CA - private certificate authority | Apache-2.0 | https://github.com/smallstep/certificates |
| CFSSL | Go | 8k+ | Cloudflare's TLS/PKI toolkit | BSD-2 | https://github.com/cloudflare/cfssl |
| Lemur | Python | 2k+ | TLS certificate management at Netflix | Apache-2.0 | https://github.com/Netflix/lemur |
| OpenSSL | C | 25k+ | Full-featured cryptography library | Apache-2.0 | https://github.com/openssl/openssl |
| LibreSSL | C | 1k+ | OpenSSL fork by OpenBSD team | OpenSSL | https://github.com/libressl/portable |
| GnuTLS | C | 1k+ | Transport Layer Security library | LGPL-2.1 | https://gitlab.com/gnutls/gnutls |
| WolfSSL | C | 2k+ | Lightweight SSL/TLS library | GPL-2.0 | https://github.com/wolfSSL/wolfssl |
| mbedTLS | C | 5k+ | TLS/SSL for embedded systems | Apache-2.0 | https://github.com/Mbed-TLS/mbedtls |
| Snyk CLI | TypeScript | 5k+ | Find & fix vulnerabilities in code | Apache-2.0 | https://github.com/snyk/cli |
| Trivy | Go | 24k+ | Container/IaC vulnerability scanner | Apache-2.0 | https://github.com/aquasecurity/trivy |
| Grype | Go | 8k+ | Vulnerability scanner for container images | Apache-2.0 | https://github.com/anchore/grype |
| Clair | Go | 10k+ | Static analysis of OCI images | Apache-2.0 | https://github.com/quay/clair |
| Anchore Engine | Python | 1k+ | Container image security scanning | Apache-2.0 | https://github.com/anchore/anchore-engine |
| Syft | Go | 6k+ | Generate Software Bill of Materials | Apache-2.0 | https://github.com/anchore/syft |
| CycloneDX | Various | 1k+ | SBOM standard and tooling | Apache-2.0 | https://github.com/CycloneDX |
| OWASP Dependency-Check | Java | 6k+ | Software composition analysis tool | Apache-2.0 | https://github.com/dependency-check/DependencyCheck |
| Bandit | Python | 6k+ | Python security linter | Apache-2.0 | https://github.com/PyCQA/bandit |
| Semgrep | OCaml | 10k+ | Static analysis / SAST tool | LGPL-2.1 | https://github.com/semgrep/semgrep |
| CodeQL | — | — | GitHub code analysis (free for OSS) | MIT | — |
| SonarQube CE | Java | 9k+ | Code quality and security analysis | GPL-3.0 | https://github.com/SonarSource/sonarqube |
| SpotBugs | Java | 3k+ | Find bugs in Java code | LGPL-2.1 | https://github.com/spotbugs/spotbugs |
| PMD | Java | 4k+ | Source code analyzer for Java | BSD-4 | https://github.com/pmd/pmd |
| ESLint | JavaScript | 25k+ | JavaScript code linting | MIT | https://github.com/eslint/eslint |
| Gosec | Go | 7k+ | Go security linting | Apache-2.0 | https://github.com/securego/gosec |
| Brakeman | Ruby | 7k+ | Security scanner for Ruby on Rails | MIT | https://github.com/presidentbeef/brakeman |
| Falco | C++ | 7k+ | Runtime security (CNCF) | Apache-2.0 | https://github.com/falcosecurity/falco |
| Wazuh | C | 10k+ | Open-source SIEM/XDR platform | GPL-2.0 | https://github.com/wazuh/wazuh |
| OSSEC | C | 4k+ | Host-based intrusion detection | GPL-2.0 | https://github.com/ossec/ossec-hids |
| Suricata | C | 4k+ | IDS/IPS/NSM security monitoring | GPL-2.0 | https://github.com/OISF/suricata |
| Snort | C | 2k+ | Intrusion prevention system | GPL-2.0 | https://github.com/snort3/snort3 |
| Zeek (Bro) | C++ | 7k+ | Network security monitoring platform | BSD-3 | https://github.com/zeek/zeek |
| AIDE | C | 1k+ | File integrity monitoring | GPL-2.0 | https://github.com/aide/aide |
| Lynis | Shell | 12k+ | Security auditing for Linux | GPL-3.0 | https://github.com/CISOfy/lynis |
| OpenSCAP | C | 1k+ | Security content automation | LGPL-2.1 | https://github.com/OpenSCAP/openscap |
| Nuclei | Go | 22k+ | Vulnerability scanner with templates | MIT | https://github.com/projectdiscovery/nuclei |
| Metasploit | Ruby | 34k+ | Penetration testing framework | BSD-3 | https://github.com/rapid7/metasploit-framework |
| Nessus (OpenVAS) | C | 3k+ | Open-source vulnerability scanner | GPL-2.0 | — |
| Burp Suite CE | Java | — | Web vulnerability scanner (free edition) | Proprietary | — |
| ZAP (OWASP) | Java | 12k+ | Web app security scanner | Apache-2.0 | https://github.com/zaproxy/zaproxy |
| SQLMap | Python | 32k+ | Automatic SQL injection testing | GPL-2.0 | https://github.com/sqlmapproject/sqlmap |
| Nikto | Perl | 8k+ | Web server scanner | GPL-2.0 | https://github.com/sullo/nikto |
| Amass | Go | 13k+ | Network surface mapping and asset discovery | Apache-2.0 | https://github.com/owasp-amass/amass |
| theHarvester | Python | 12k+ | Email, host, URL, name harvesting OSINT | GPL-2.0 | https://github.com/laramies/theHarvester |
| Maltego CE | Java | — | OSINT link analysis (free tier) | Proprietary | — |
| Shodan (API) | — | — | Internet-connected devices search engine | API | — |
| CyberChef | JavaScript | 30k+ | "The Cyber Swiss Army Knife" for data ops | Apache-2.0 | https://github.com/gchq/CyberChef |
| John the Ripper | C | 9k+ | Password security auditing/recovery | GPL-2.0 | https://github.com/openwall/john |
| Hashcat | C | 21k+ | Advanced CPU/GPU password recovery | MIT | https://github.com/hashcat/hashcat |
| Aircrack-ng | C | 5k+ | IEEE 802.11 WEP/WPA cracking | GPL-2.0 | https://github.com/aircrack-ng/aircrack-ng |
| Wireshark | C | 8k+ | Network protocol analyzer | GPL-2.0 | https://gitlab.com/wireshark/wireshark |
| pfxsigner | Go | 92 | Sign PDFs with PFX/PKCS#12 certs | MIT | https://github.com/zerodha/pfxsigner |

---

## 24. Authentication & Identity

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Keycloak | Java | 23k+ | Enterprise identity and access management | Apache-2.0 | https://github.com/keycloak/keycloak |
| Authentik | Python | 14k+ | Identity provider for all protocols | MIT | https://github.com/goauthentik/authentik |
| Authelia | Go | 22k+ | SSO + 2FA for apps behind proxy | Apache-2.0 | https://github.com/authelia/authelia |
| Casdoor | Go | 10k+ | SSO identity provider with OAuth/SAML | Apache-2.0 | https://github.com/casdoor/casdoor |
| Pomerium | Go | 4k+ | Identity-aware access proxy | Apache-2.0 | https://github.com/pomerium/pomerium |
| Zitadel | Go | 9k+ | Identity platform for cloud-native apps | Apache-2.0 | https://github.com/zitadel/zitadel |
| Logto | TypeScript | 9k+ | Auth infrastructure for apps | MPL-2.0 | https://github.com/logto-io/logto |
| SuperTokens | TypeScript | 13k+ | Open-source Auth0 alternative | Apache-2.0 | https://github.com/supertokens/supertokens-core |
| Ory Hydra | Go | 15k+ | OAuth 2.0 and OpenID Connect server | Apache-2.0 | https://github.com/ory/hydra |
| Ory Kratos | Go | 11k+ | User identity and management | Apache-2.0 | https://github.com/ory/kratos |
| Ory Keto | Go | 5k+ | Google Zanzibar-inspired permission system | Apache-2.0 | https://github.com/ory/keto |
| Ory Oathkeeper | Go | 3k+ | Identity and access proxy | Apache-2.0 | https://github.com/ory/oathkeeper |
| Dex | Go | 9k+ | OpenID Connect identity provider | Apache-2.0 | https://github.com/dexidp/dex |
| oauth2-proxy | Go | 10k+ | Reverse proxy with OAuth2 authentication | MIT | https://github.com/oauth2-proxy/oauth2-proxy |
| OpenID Connect | Various | — | Identity standard (many implementations) | Apache-2.0 | — |
| SAML2 (many impls) | Various | — | Enterprise SSO standard | Apache-2.0 | — |
| Okta (OSS SDKs) | Various | — | Identity platform (free tier) | Apache-2.0 | — |
| FusionAuth (CE) | Java | 1k+ | Auth platform with community edition | Apache-2.0 | https://github.com/FusionAuth |
| Gluu | Java | 1k+ | Identity and access management | MIT | https://github.com/GluuFederation |
| OpenLDAP | C | 1k+ | LDAP directory server | OpenLDAP | https://git.openldap.org/openldap/openldap |
| 389 Directory | C | 1k+ | Enterprise LDAP server | GPL-3.0 | https://github.com/389ds/389-ds-base |
| FreeIPA | Python | 1k+ | Identity management for Linux | GPL-3.0 | https://github.com/freeipa/freeipa |
| Samba | C | 2k+ | Windows interop + AD on Linux | GPL-3.0 | https://github.com/samba-team/samba |
| otpgateway | Go | 522 | Standalone OTP verification server | MIT | https://github.com/zerodha/otpgateway |
| TOTP (various) | Various | — | Time-based OTP implementations | MIT | — |
| WebAuthn (libraries) | Various | — | FIDO2 passwordless authentication | Apache-2.0 | — |
| Passkeys (Corbado) | — | — | Passkey infrastructure (free tier) | Proprietary | — |
| SpiceDB | Go | 5k+ | Zanzibar-inspired permission system | Apache-2.0 | https://github.com/authzed/spicedb |
| Cerbos | Go | 4k+ | Decentralized authorization service | Apache-2.0 | https://github.com/cerbos/cerbos |
| Casbin | Go | 17k+ | Authorization library with policy models | Apache-2.0 | https://github.com/casbin/casbin |
| Open Policy Agent | Go | 9k+ | General-purpose policy engine | Apache-2.0 | https://github.com/open-policy-agent/opa |
| Permit.io | — | — | Authorization platform (free tier) | Proprietary | — |
| simplesessions | Go | 80 | HTTP-agnostic session management | MIT | https://github.com/vividvilla/simplesessions |


---

## 25. Web Frameworks - Backend

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Django | Python | 80k+ | Batteries-included Python web framework | BSD-3 | https://github.com/django/django |
| FastAPI | Python | 79k+ | Fast modern API framework with OpenAPI | MIT | https://github.com/fastapi/fastapi |
| Flask | Python | 68k+ | Lightweight WSGI web framework | BSD-3 | https://github.com/pallets/flask |
| Starlette | Python | 10k+ | Lightweight ASGI framework for Python | BSD-3 | https://github.com/encode/starlette |
| Litestar | Python | 6k+ | Flexible ASGI framework | MIT | https://github.com/litestar-org/litestar |
| Sanic | Python | 18k+ | Async Python web framework | MIT | https://github.com/sanic-org/sanic |
| Tornado | Python | 22k+ | Async Python web framework | Apache-2.0 | https://github.com/tornadoweb/tornado |
| aiohttp | Python | 15k+ | Async HTTP client/server | Apache-2.0 | https://github.com/aio-libs/aiohttp |
| Falcon | Python | 9k+ | Minimalist REST framework for Python | Apache-2.0 | https://github.com/falconry/falcon |
| Bottle | Python | 8k+ | Fast simple micro-framework | MIT | https://github.com/bottlepy/bottle |
| Pyramid | Python | 4k+ | Flexible Python web framework | BSD-4 | https://github.com/Pylons/pyramid |
| CherryPy | Python | 1k+ | Object-oriented HTTP framework | BSD-3 | https://github.com/cherrypy/cherrypy |
| Quart | Python | 2k+ | Python async Flask | MIT | https://github.com/pallets/quart |
| Blacksheep | Python | 2k+ | Fast ASGI web framework | MIT | — |
| Express | JavaScript | 65k+ | Minimal Node.js web framework | MIT | https://github.com/expressjs/express |
| Fastify | JavaScript | 32k+ | Fast Node.js web framework | MIT | https://github.com/fastify/fastify |
| Hono | TypeScript | 22k+ | Ultrafast web framework for edge | MIT | https://github.com/honojs/hono |
| Koa | JavaScript | 35k+ | Next-gen Express by its team | MIT | https://github.com/koajs/koa |
| NestJS | TypeScript | 68k+ | Opinionated Node.js framework (Angular-style) | MIT | https://github.com/nestjs/nest |
| AdonisJS | TypeScript | 16k+ | Full-stack TypeScript framework | MIT | https://github.com/adonisjs/core |
| Strapi | TypeScript | 64k+ | Open-source headless CMS/API | MIT | https://github.com/strapi/strapi |
| Hapi | JavaScript | 14k+ | Rich framework for Node.js | BSD-3 | https://github.com/hapijs/hapi |
| Restify | JavaScript | 11k+ | Node.js framework for REST APIs | MIT | https://github.com/restify/node-restify |
| Sails.js | JavaScript | 22k+ | MVC Node.js framework | MIT | https://github.com/balderdashy/sails |
| LoopBack | TypeScript | 4k+ | Extensible Node.js API framework | MIT | https://github.com/loopbackio/loopback-next |
| Feathers | TypeScript | 15k+ | Real-time web framework | MIT | https://github.com/feathersjs/feathers |
| Ruby on Rails | Ruby | 56k+ | Full-stack MVC web framework | MIT | https://github.com/rails/rails |
| Sinatra | Ruby | 13k+ | DSL for Ruby web apps | MIT | https://github.com/sinatra/sinatra |
| Roda | Ruby | 2k+ | Routing tree web toolkit | MIT | https://github.com/jeremyevans/roda |
| Hanami | Ruby | 6k+ | Modern Ruby web framework | MIT | https://github.com/hanami/hanami |
| Grape | Ruby | 9k+ | REST-like API framework for Ruby | MIT | https://github.com/ruby-grape/grape |
| Spring Boot | Java | 74k+ | Java microservices framework | Apache-2.0 | https://github.com/spring-projects/spring-boot |
| Quarkus | Java | 14k+ | Kubernetes-native Java framework | Apache-2.0 | https://github.com/quarkusio/quarkus |
| Micronaut | Java | 6k+ | Full-stack JVM microservices framework | Apache-2.0 | https://github.com/micronaut-projects/micronaut-core |
| Helidon | Java | 3k+ | Cloud-native Java frameworks by Oracle | Apache-2.0 | https://github.com/helidon-io/helidon |
| Vert.x | Java | 14k+ | Reactive toolkit for JVM | Apache-2.0 | https://github.com/eclipse-vertx/vert.x |
| Ktor | Kotlin | 13k+ | Async Kotlin web framework | Apache-2.0 | https://github.com/ktorio/ktor |
| HTTP4K | Kotlin | 3k+ | Functional Kotlin HTTP toolkit | Apache-2.0 | https://github.com/http4k/http4k |
| Gin | Go | 78k+ | Fast HTTP web framework for Go | MIT | https://github.com/gin-gonic/gin |
| Echo | Go | 29k+ | High-performance Go web framework | MIT | https://github.com/labstack/echo |
| Fiber | Go | 34k+ | Express-inspired Go web framework | MIT | https://github.com/gofiber/fiber |
| Chi | Go | 18k+ | Lightweight composable router for Go | MIT | https://github.com/go-chi/chi |
| Gorilla Mux | Go | 21k+ | Powerful URL router for Go | BSD-3 | https://github.com/gorilla/mux |
| Beego | Go | 31k+ | Full MVC Go web framework | Apache-2.0 | https://github.com/beego/beego |
| Buffalo | Go | 8k+ | Go web development eco-system | MIT | https://github.com/gobuffalo/buffalo |
| Revel | Go | 13k+ | High-productivity Go web framework | MIT | https://github.com/revel/revel |
| Iris | Go | 25k+ | Fast community-driven Go web framework | BSD-3 | https://github.com/kataras/iris |
| fastglue | Go | 91 | Micro HTTP wrapper for fasthttp | MIT | https://github.com/zerodha/fastglue |
| Laravel | PHP | 78k+ | Elegant full-stack PHP framework | MIT | https://github.com/laravel/laravel |
| Symfony | PHP | 29k+ | Full-stack PHP web framework | MIT | https://github.com/symfony/symfony |
| CodeIgniter | PHP | 5k+ | Lightweight PHP framework | MIT | https://github.com/codeigniter4/CodeIgniter4 |
| Slim | PHP | 12k+ | Micro-framework for PHP | MIT | https://github.com/slimphp/Slim |
| Lumen | PHP | 7k+ | Laravel's micro-framework | MIT | https://github.com/laravel/lumen |
| Yii | PHP | 14k+ | High-performance PHP framework | BSD-3 | https://github.com/yiisoft/yii2 |
| CakePHP | PHP | 8k+ | MVC framework for PHP | MIT | https://github.com/cakephp/cakephp |
| Phalcon | C | 10k+ | PHP extension framework | BSD-3 | https://github.com/phalcon/cphalcon |
| Actix-web | Rust | 22k+ | Powerful actor-based Rust web framework | MIT/Apache-2.0 | https://github.com/actix/actix-web |
| Axum | Rust | 21k+ | Ergonomic Rust web application framework | MIT | https://github.com/tokio-rs/axum |
| Rocket | Rust | 24k+ | Simple, fast, type-safe Rust web framework | MIT/Apache-2.0 | https://github.com/rwf2/Rocket |
| Warp | Rust | 9k+ | Composable Rust web server | MIT | https://github.com/seanmonstar/warp |
| Tide | Rust | 5k+ | Async Rust web framework | MIT/Apache-2.0 | https://github.com/http-rs/tide |
| Phoenix | Elixir | 21k+ | Productive Elixir web framework | MIT | https://github.com/phoenixframework/phoenix |
| Plug | Elixir | 3k+ | Composable modules for web apps in Elixir | MIT | https://github.com/elixir-plug/plug |
| Cowboy | Erlang | 7k+ | Small fast HTTP server for Erlang | ISC | https://github.com/ninenines/cowboy |
| Yesod | Haskell | 2k+ | Type-safe Haskell web framework | MIT | https://github.com/yesodweb/yesod |
| Servant | Haskell | 2k+ | Type-level web API design DSL | BSD-3 | https://github.com/haskell-servant/servant |
| Scotty | Haskell | 2k+ | Haskell web framework inspired by Sinatra | BSD-3 | https://github.com/scotty-web/scotty |
| ASP.NET Core | C# | 35k+ | Cross-platform .NET web framework | MIT | https://github.com/dotnet/aspnetcore |
| Nancy | C# | 7k+ | Lightweight .NET web framework | MIT | https://github.com/NancyFx/Nancy |
| Giraffe | F# | 2k+ | Functional F# web framework on .NET | MIT | https://github.com/giraffe-fsharp/Giraffe |
| Vapor | Swift | 24k+ | Server-side Swift web framework | MIT | https://github.com/vapor/vapor |
| Perfect | Swift | 14k+ | Swift server framework | Apache-2.0 | https://github.com/PerfectlySoft/Perfect |
| Kitura | Swift | 7k+ | IBM's Swift server-side framework | Apache-2.0 | https://github.com/Kitura/Kitura |
| Crow | C++ | 10k+ | Fast, easy C++ microframework for web | BSD-3 | https://github.com/CrowCpp/Crow |
| Drogon | C++ | 11k+ | Fast async C++ web framework | MIT | https://github.com/drogonframework/drogon |
| Oat++ | C++ | 7k+ | High-performance C++ web framework | Apache-2.0 | https://github.com/oatpp/oatpp |
| Poco | C++ | 8k+ | Cross-platform C++ network/app libraries | BSL-1.0 | https://github.com/pocoproject/poco |
| Padrino | Ruby | 3k+ | Elegant Ruby web framework on Sinatra | MIT | https://github.com/padrino/padrino-framework |

---

## 26. Web Frameworks - Frontend

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| React | JavaScript | 229k+ | UI library by Meta with virtual DOM | MIT | https://github.com/facebook/react |
| Vue.js | JavaScript | 207k+ | Progressive JavaScript framework | MIT | https://github.com/vuejs/core |
| Angular | TypeScript | 96k+ | Full-featured framework by Google | MIT | https://github.com/angular/angular |
| Svelte | TypeScript | 80k+ | Compiler-based frontend framework | MIT | https://github.com/sveltejs/svelte |
| SolidJS | TypeScript | 32k+ | Fine-grained reactive UI framework | MIT | https://github.com/solidjs/solid |
| Qwik | TypeScript | 21k+ | Resumable framework for instant apps | MIT | https://github.com/QwikDev/qwik |
| Astro | TypeScript | 48k+ | Content-first static site generator | MIT | https://github.com/withastro/astro |
| Next.js | TypeScript | 128k+ | React-based full-stack framework | MIT | https://github.com/vercel/next.js |
| Nuxt | TypeScript | 55k+ | Vue.js meta-framework | MIT | https://github.com/nuxt/nuxt |
| SvelteKit | TypeScript | 18k+ | Full-stack Svelte framework | MIT | https://github.com/sveltejs/kit |
| Remix | TypeScript | 30k+ | Full-stack React framework | MIT | https://github.com/remix-run/remix |
| Gatsby | TypeScript | 55k+ | React static site generator | MIT | https://github.com/gatsbyjs/gatsby |
| Eleventy (11ty) | JavaScript | 17k+ | Simple static site generator | MIT | https://github.com/11ty/eleventy |
| Hugo | Go | 74k+ | World's fastest static site generator | Apache-2.0 | https://github.com/gohugoio/hugo |
| Jekyll | Ruby | 49k+ | Static site generator for GitHub Pages | MIT | https://github.com/jekyll/jekyll |
| Pelican | Python | 12k+ | Static site generator in Python | AGPL-3.0 | https://github.com/getpelican/pelican |
| MkDocs | Python | 19k+ | Project documentation with Markdown | BSD-2 | https://github.com/mkdocs/mkdocs |
| Docusaurus | TypeScript | 57k+ | Documentation websites by Meta | MIT | https://github.com/facebook/docusaurus |
| VitePress | TypeScript | 14k+ | Vite + Vue-powered static site generator | MIT | https://github.com/vuejs/vitepress |
| Hexo | JavaScript | 39k+ | Fast, simple blog framework | MIT | https://github.com/hexojs/hexo |
| Zola | Rust | 14k+ | Fast static site generator in Rust | MIT | https://github.com/getzola/zola |
| Cobalt | Rust | 3k+ | Static site generator in Rust | MIT | https://github.com/cobalt-org/cobalt.rs |
| Vite | TypeScript | 69k+ | Next-gen frontend build tool | MIT | https://github.com/vitejs/vite |
| esbuild | Go | 38k+ | Extremely fast JS/TS bundler | MIT | https://github.com/evanw/esbuild |
| Webpack | JavaScript | 64k+ | Module bundler for JavaScript | MIT | https://github.com/webpack/webpack |
| Rollup | JavaScript | 25k+ | ES module bundler | MIT | https://github.com/rollup/rollup |
| Parcel | JavaScript | 43k+ | Zero-config web bundler | MIT | https://github.com/parcel-bundler/parcel |
| Turbopack | Rust | — | Webpack successor by Vercel (Rust) | MPL-2.0 | — |
| Rspack | Rust | 10k+ | Webpack-compatible bundler in Rust | MIT | https://github.com/web-infra-dev/rspack |
| WMR | JavaScript | 10k+ | Swiss army knife for modern web apps | MIT | — |
| Snowpack | JavaScript | 20k+ | Frontend build tool for modern web dev | MIT | https://github.com/FredKSchott/snowpack |
| Tailwind CSS | CSS | 84k+ | Utility-first CSS framework | MIT | https://github.com/tailwindlabs/tailwindcss |
| UnoCSS | TypeScript | 17k+ | Atomic CSS engine, Tailwind-compatible | MIT | https://github.com/unocss/unocss |
| Bootstrap | JavaScript | 171k+ | Responsive CSS/JS framework | MIT | https://github.com/twbs/bootstrap |
| Bulma | CSS | 49k+ | Flexbox-based CSS framework | MIT | https://github.com/jgthms/bulma |
| Foundation | CSS | 29k+ | Advanced responsive CSS framework | MIT | https://github.com/foundation/foundation-sites |
| Materialize | JavaScript | 39k+ | Material Design CSS framework | MIT | https://github.com/Dogfalo/materialize |
| Ant Design | TypeScript | 93k+ | Enterprise-class UI design system | MIT | https://github.com/ant-design/ant-design |
| Material UI (MUI) | TypeScript | 94k+ | React components for Material Design | MIT | https://github.com/mui/material-ui |
| Chakra UI | TypeScript | 37k+ | Accessible component library | MIT | https://github.com/chakra-ui/chakra-ui |
| shadcn/ui | TypeScript | 78k+ | Copy-paste React components | MIT | https://github.com/shadcn-ui/ui |
| Radix UI | TypeScript | 15k+ | Accessible unstyled React primitives | MIT | https://github.com/radix-ui/primitives |
| Headless UI | TypeScript | 25k+ | Unstyled accessible UI components | MIT | https://github.com/tailwindlabs/headlessui |
| DaisyUI | CSS | 35k+ | Tailwind component library | MIT | https://github.com/saadeghi/daisyui |
| PrimeReact | TypeScript | 6k+ | Rich UI component suite | MIT | https://github.com/primefaces/primereact |
| Mantine | TypeScript | 27k+ | Full-featured React component library | MIT | https://github.com/mantinedev/mantine |
| Storybook | TypeScript | 84k+ | UI component dev and documentation | MIT | https://github.com/storybookjs/storybook |
| Framer Motion | TypeScript | 24k+ | Animation library for React | MIT | https://github.com/framer/motion |
| GSAP (free tier) | JavaScript | — | Professional animation library | GreenSock | — |
| Three.js | JavaScript | 102k+ | 3D graphics library for the web | MIT | https://github.com/mrdoob/three.js |
| Babylon.js | TypeScript | 23k+ | 3D engine for web and mobile | Apache-2.0 | https://github.com/BabylonJS/Babylon.js |
| D3.js | JavaScript | 108k+ | Data visualization with SVG/Canvas | ISC | https://github.com/d3/d3 |
| Chart.js | JavaScript | 64k+ | Simple flexible charting library | MIT | https://github.com/chartjs/Chart.js |
| Recharts | TypeScript | 24k+ | React charting built on D3 | MIT | https://github.com/recharts/recharts |
| ECharts | TypeScript | 59k+ | Apache powerful charting library | Apache-2.0 | https://github.com/apache/echarts |
| Plotly.js | JavaScript | 16k+ | Interactive scientific charts | MIT | https://github.com/plotly/plotly.js |
| Highcharts (OSS) | JavaScript | 11k+ | Feature-rich charting library | Custom OSS | — |
| Vega-Lite | TypeScript | 11k+ | Grammar for interactive visualizations | BSD-3 | https://github.com/vega/vega-lite |
| Observable Plot | JavaScript | 4k+ | D3-compatible data exploration | ISC | https://github.com/observablehq/plot |
| Leaflet | JavaScript | 41k+ | Interactive maps library | BSD-2 | https://github.com/Leaflet/Leaflet |
| OpenLayers | JavaScript | 11k+ | Feature-packed mapping library | BSD-2 | https://github.com/openlayers/openlayers |
| Mapbox GL (OSS) | JavaScript | — | Vector tile-based map renderer | BSD-3 | — |
| Deck.gl | JavaScript | 12k+ | WebGL-based visualization framework | MIT | https://github.com/visgl/deck.gl |
| Kepler.gl | JavaScript | 10k+ | Geospatial analysis data visualization | MIT | https://github.com/keplergl/kepler.gl |
| Socket.IO | TypeScript | 61k+ | Realtime bidirectional event-based comm | MIT | https://github.com/socketio/socket.io |
| ws | JavaScript | 21k+ | Simple WebSocket server for Node | MIT | https://github.com/websockets/ws |
| htmx | JavaScript | 42k+ | HTML extensions for AJAX/WebSockets | BSD-2 | https://github.com/bigskysoftware/htmx |
| Alpine.js | JavaScript | 28k+ | Minimal framework for behavior in HTML | MIT | https://github.com/alpinejs/alpine |
| Stimulus | JavaScript | 12k+ | Modest JS framework for HTML pages | MIT | https://github.com/hotwired/stimulus |
| Turbo | JavaScript | 13k+ | Speed of SPA with simplicity of server | MIT | https://github.com/hotwired/turbo |
| Lit | TypeScript | 18k+ | Simple web components library by Google | BSD-3 | https://github.com/lit/lit |
| Stencil | TypeScript | 12k+ | Web component compiler | MIT | https://github.com/ionic-team/stencil |
| WASM (via AssemblyScript) | TypeScript | 17k+ | Frontend logic in WebAssembly | Apache-2.0 | — |

---

## 27. CMS & Headless CMS

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| WordPress | PHP | 19k+ | World's most popular CMS | GPL-2.0 | https://github.com/WordPress/WordPress |
| Drupal | PHP | 4k+ | Enterprise CMS and framework | GPL-2.0 | https://github.com/drupal/drupal |
| Joomla | PHP | 4k+ | Content management system | GPL-2.0 | https://github.com/joomla/joomla-cms |
| TYPO3 | PHP | 1k+ | Enterprise CMS for large organizations | GPL-2.0 | https://github.com/TYPO3/typo3 |
| Concrete CMS | PHP | 1k+ | Easy to use CMS | MIT | https://github.com/concretecms/concretecms |
| Grav | PHP | 14k+ | Flat-file modern open source CMS | MIT | https://github.com/getgrav/grav |
| Pico | PHP | 4k+ | Stupidly simple flat-file CMS | MIT | https://github.com/picocms/Pico |
| Ghost | JavaScript | 47k+ | Open-source publishing platform | MIT | https://github.com/TryGhost/Ghost |
| Strapi | TypeScript | 64k+ | Node.js headless CMS | MIT | https://github.com/strapi/strapi |
| Directus | TypeScript | 29k+ | Open-source headless CMS | BSL-1.1 | https://github.com/directus/directus |
| Payload CMS | TypeScript | 29k+ | Code-first TypeScript headless CMS | MIT | https://github.com/payloadcms/payload |
| Sanity (OSS SDK) | TypeScript | 5k+ | Structured content platform | MIT | — |
| Contentful (OSS) | — | — | Headless CMS (proprietary, free tier) | Proprietary | — |
| Netlify CMS / Decap | JavaScript | 17k+ | Git-based CMS for static sites | MIT | https://github.com/decaporg/decap-cms |
| TinaCMS | TypeScript | 12k+ | Git-backed headless CMS | Apache-2.0 | https://github.com/tinacms/tinacms |
| Keystone.js | TypeScript | 9k+ | Node.js CMS with GraphQL API | MIT | https://github.com/keystonejs/keystone |
| Wagtail | Python | 18k+ | Django-based CMS | BSD-3 | https://github.com/wagtail/wagtail |
| Django CMS | Python | 10k+ | Enterprise Django CMS | BSD-3 | https://github.com/django-cms/django-cms |
| Mezzanine | Python | 5k+ | Django-based CMS | BSD-2 | https://github.com/stephenmcd/mezzanine |
| PocketBase | Go | 43k+ | Open-source backend-as-a-service | MIT | https://github.com/pocketbase/pocketbase |
| Appwrite | TypeScript | 43k+ | Open-source BaaS (Firebase alternative) | BSD-3 | https://github.com/appwrite/appwrite |
| Supabase | TypeScript | 73k+ | Open-source Firebase alternative | Apache-2.0 | https://github.com/supabase/supabase |
| Parse Server | JavaScript | 21k+ | Open-source Parse backend | BSD-3 | https://github.com/parse-community/parse-server |
| Nhost | TypeScript | 7k+ | Open-source Firebase alt with Hasura | MIT | https://github.com/nhost/nhost |
| Medusa | TypeScript | 26k+ | Open-source Shopify alternative | MIT | https://github.com/medusajs/medusa |
| Saleor | Python | 20k+ | GraphQL-first e-commerce platform | BSD-3 | https://github.com/saleor/saleor |
| OctoberCMS | PHP | 11k+ | Laravel-based CMS | MIT | https://github.com/octobercms/october |
| Statamic (OSS) | PHP | 3k+ | Flat-file CMS (free solo license) | Source available | — |

---

## 28. E-Commerce

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Medusa | TypeScript | 26k+ | Open-source Shopify alternative | MIT | https://github.com/medusajs/medusa |
| Saleor | Python | 20k+ | GraphQL-first headless e-commerce | BSD-3 | https://github.com/saleor/saleor |
| WooCommerce | PHP | 9k+ | WordPress e-commerce plugin | GPL-2.0 | https://github.com/woocommerce/woocommerce |
| Magento (Adobe Commerce) | PHP | 11k+ | Enterprise e-commerce platform | OSL-3.0 | https://github.com/magento/magento2 |
| PrestaShop | PHP | 8k+ | Open-source e-commerce solution | OSL-3.0 | https://github.com/PrestaShop/PrestaShop |
| OpenCart | PHP | 7k+ | Open-source online store solution | GPL-3.0 | https://github.com/opencart/opencart |
| osCommerce | PHP | 2k+ | Classic open-source e-commerce | GPL-2.0 | https://github.com/osCommerce/oscommerce2 |
| Bagisto | PHP | 11k+ | Laravel-based e-commerce framework | MIT | https://github.com/bagisto/bagisto |
| Aimeos | PHP | 4k+ | High-performance e-commerce framework | LGPL-3.0 | https://github.com/aimeos/aimeos |
| Sylius | PHP | 7k+ | Open-source e-commerce framework | MIT | https://github.com/Sylius/Sylius |
| Solidus | Ruby | 5k+ | E-commerce platform for Rails | BSD-3 | https://github.com/solidusio/solidus |
| Spree Commerce | Ruby | 13k+ | Rails-based e-commerce platform | BSD-3 | https://github.com/spree/spree |
| Reaction Commerce | JavaScript | 12k+ | Node.js + React e-commerce | GPL-3.0 | https://github.com/reactioncommerce/reaction |
| Vendure | TypeScript | 6k+ | Headless GraphQL e-commerce | MIT | https://github.com/vendure-ecommerce/vendure |
| Evershop | TypeScript | 4k+ | Node.js e-commerce with React | GPL-3.0 | https://github.com/evershopcommerce/evershop |
| Commerce.js (OSS) | JavaScript | 1k+ | Headless commerce SDK | MIT | — |
| Crystallize | — | — | Headless commerce platform (free tier) | Proprietary | — |
| Invoice Ninja | PHP | 8k+ | Open-source invoicing and payments | AAL | https://github.com/invoiceninja/invoiceninja |
| Crater | PHP | 8k+ | Invoice and expense management | AAL | https://github.com/crater-invoice/crater |

---

## 29. Mobile Development

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Flutter | Dart | 167k+ | Google's UI toolkit for cross-platform apps | BSD-3 | https://github.com/flutter/flutter |
| React Native | JavaScript | 119k+ | Meta's cross-platform mobile framework | MIT | https://github.com/facebook/react-native |
| Expo | TypeScript | 34k+ | React Native framework and platform | MIT | https://github.com/expo/expo |
| Ionic | TypeScript | 51k+ | Cross-platform mobile with web tech | MIT | https://github.com/ionic-team/ionic-framework |
| Capacitor | TypeScript | 12k+ | Cross-platform native runtime for web | MIT | https://github.com/ionic-team/capacitor |
| Cordova | JavaScript | 36k+ | Mobile app dev with HTML/CSS/JS | Apache-2.0 | https://github.com/apache/cordova |
| NativeScript | TypeScript | 23k+ | Native mobile apps using Angular/Vue/Svelte | Apache-2.0 | https://github.com/NativeScript/NativeScript |
| Xamarin | C# | 5k+ | .NET cross-platform framework (Microsoft) | MIT | https://github.com/xamarin |
| MAUI | C# | 22k+ | .NET Multi-platform App UI | MIT | https://github.com/dotnet/maui |
| Kotlin Multiplatform | Kotlin | 3k+ | Share code between Android, iOS, desktop | Apache-2.0 | https://github.com/JetBrains/kotlin |
| KMM (Kotlin) | Kotlin | — | Kotlin Multiplatform Mobile | Apache-2.0 | — |
| Compose Multiplatform | Kotlin | 16k+ | Declarative UI framework for KMM | Apache-2.0 | https://github.com/JetBrains/compose-multiplatform |
| Android Open Source | Java/Kotlin | 3k+ | AOSP Android platform | Apache-2.0 | — |
| LineageOS | Java | 3k+ | Custom Android distribution | Apache-2.0 | https://github.com/LineageOS |
| GrapheneOS | C | 2k+ | Privacy-focused Android fork | MIT | https://github.com/GrapheneOS |
| CalyxOS | Java | — | Privacy-focused Android | Apache-2.0 | — |
| /e/ OS | Java | — | Privacy Android fork | Apache-2.0 | — |
| postmarketOS | Shell | 4k+ | Linux for mobile phones | MIT/GPL | https://gitlab.com/postmarketOS |
| Mobian | Shell | — | Debian for mobile devices | GPL | — |
| PinePhone (Phosh) | C | 2k+ | GNOME mobile shell | GPL-3.0 | — |
| Tauri | Rust | 84k+ | Desktop/mobile apps with web frontend | MIT/Apache-2.0 | https://github.com/tauri-apps/tauri |
| Neutralinojs | C++ | 8k+ | Lightweight cross-platform desktop apps | MIT | https://github.com/neutralinojs/neutralinojs |
| flutter_curl | Dart | 65 | Flutter plugin using libcurl | MIT | https://github.com/zerodha/flutter_curl |
| flutter_fgbg | Dart | 91 | Foreground/background events for Flutter | MIT | https://github.com/zerodha/flutter_fgbg |
| autopilot (Flutter) | Dart | 127 | Flutter QA test driver | MIT | — |

---

## 30. Desktop Development

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Tauri | Rust | 84k+ | Build native desktop apps with web tech | MIT/Apache-2.0 | https://github.com/tauri-apps/tauri |
| Electron | TypeScript | 115k+ | Desktop apps with Node + Chromium | MIT | https://github.com/electron/electron |
| NW.js | JavaScript | 40k+ | Desktop apps with Node + Chromium alt | MIT | https://github.com/nwjs/nw.js |
| Qt (LGPL) | C++ | 10k+ | Cross-platform C++/QML framework | LGPL-3.0 | https://code.qt.io/cgit/ |
| GTK | C | 4k+ | GNOME UI toolkit | LGPL-2.1 | https://gitlab.gnome.org/GNOME/gtk |
| wxWidgets | C++ | 6k+ | Cross-platform C++ UI library | wxWindows | https://github.com/wxWidgets/wxWidgets |
| FLTK | C++ | 1k+ | Lightweight fast GUI library in C++ | LGPL-2.0 | https://github.com/fltk/fltk |
| Dear ImGui | C++ | 60k+ | Bloat-free immediate mode GUI for C++ | MIT | https://github.com/ocornut/imgui |
| nuklear | C | 9k+ | Minimal immediate mode GUI library in C | MIT | https://github.com/Immediate-Mode-UI/Nuklear |
| SDL2 | C | 5k+ | Hardware abstraction library for media | Zlib | https://github.com/libsdl-org/SDL |
| raylib | C | 22k+ | Simple game/media programming library | Zlib | https://github.com/raysan5/raylib |
| SFML | C++ | 11k+ | Simple and fast multimedia library | Zlib | https://github.com/SFML/SFML |
| Allegro | C | 2k+ | Cross-platform game/multimedia library | Zlib | https://github.com/liballeg/allegro5 |
| JavaFX | Java | 1k+ | Rich client platform for Java | GPL-2.0 | — |
| Swing | Java | — | Java GUI toolkit (built-in JDK) | GPL-2.0 | — |
| SWT | Java | — | Eclipse's native GUI widgets | EPL-2.0 | — |
| Compose Desktop | Kotlin | — | JetBrains declarative UI for desktop | Apache-2.0 | — |
| Avalonia UI | C# | 26k+ | Cross-platform XAML-based .NET UI | MIT | https://github.com/AvaloniaUI/Avalonia |
| MAUI | C# | 22k+ | .NET cross-platform native app UI | MIT | https://github.com/dotnet/maui |
| WinUI3 | C# | 3k+ | Windows native UI framework | MIT | — |
| GTK-rs | Rust | 3k+ | Rust bindings for GTK | MIT | https://github.com/gtk-rs/gtk-rs-core |
| egui | Rust | 23k+ | Immediate mode GUI for Rust | MIT/Apache-2.0 | https://github.com/emilk/egui |
| Iced | Rust | 25k+ | Cross-platform GUI library in Rust | MIT | https://github.com/iced-rs/iced |
| Slint | Rust | 17k+ | Declarative GUI toolkit for Rust/C++ | GPL-3.0/Commercial | https://github.com/slint-ui/slint |
| Druid | Rust | 9k+ | Data-first Rust-native UI toolkit | Apache-2.0 | https://github.com/apache/druid |
| Dioxus | Rust | 22k+ | React-like framework for Rust desktop/web | MIT | https://github.com/DioxusLabs/dioxus |
| Neutralinojs | C++ | 8k+ | Lightweight cross-platform desktop | MIT | https://github.com/neutralinojs/neutralinojs |
| Flutter Desktop | Dart | 167k+ | Flutter for Linux/macOS/Windows | BSD-3 | — |
| Wails | Go | 25k+ | Go desktop apps with web frontend | MIT | https://github.com/wailsapp/wails |
| Fyne | Go | 25k+ | Cross-platform GUI framework in Go | BSD-3 | https://github.com/fyne-io/fyne |
| gi (Go GTK) | Go | 3k+ | Go bindings for GObject/GTK | BSD-3 | — |

---

## 31. Data Engineering & Pipelines

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Apache Spark | Scala | 40k+ | Unified analytics engine for big data | Apache-2.0 | https://github.com/apache/spark |
| Apache Flink | Java | 24k+ | Stateful stream and batch processing | Apache-2.0 | https://github.com/apache/flink |
| Apache Beam | Java/Python | 8k+ | Unified model for batch and streaming | Apache-2.0 | https://github.com/apache/beam |
| Apache Hadoop | Java | 14k+ | Distributed storage and processing | Apache-2.0 | https://github.com/apache/hadoop |
| Apache Hive | Java | 5k+ | SQL-based data warehouse on Hadoop | Apache-2.0 | — |
| Apache Pig | Java | 1k+ | High-level data flow for Hadoop | Apache-2.0 | https://github.com/apache/pig |
| Apache Storm | Java | 7k+ | Distributed realtime computation | Apache-2.0 | — |
| Apache Samza | Java | 3k+ | Distributed stream processing | Apache-2.0 | https://github.com/apache/samza |
| Apache NiFi | Java | 4k+ | Data flow automation system | Apache-2.0 | https://github.com/apache/nifi |
| Apache Kafka | Java | 28k+ | Distributed event streaming | Apache-2.0 | https://github.com/apache/kafka |
| Apache Pulsar | Java | 14k+ | Cloud-native messaging/streaming | Apache-2.0 | https://github.com/apache/pulsar |
| Apache Iceberg | Java | 7k+ | Open table format for huge analytic tables | Apache-2.0 | https://github.com/apache/iceberg |
| Apache Hudi | Java | 5k+ | Data lake storage solution | Apache-2.0 | https://github.com/apache/hudi |
| Delta Lake | Scala | 8k+ | ACID transaction layer for data lakes | Apache-2.0 | https://github.com/delta-io/delta |
| Airflow | Python | 37k+ | Workflow orchestration platform | Apache-2.0 | https://github.com/apache/airflow |
| Prefect | Python | 17k+ | Modern workflow automation | Apache-2.0 | https://github.com/PrefectHQ/prefect |
| Dagster | Python | 11k+ | Data orchestration framework | Apache-2.0 | https://github.com/dagster-io/dagster |
| Luigi | Python | 17k+ | Pipeline framework by Spotify | Apache-2.0 | https://github.com/spotify/luigi |
| Mage.ai | Python | 8k+ | Modern data pipeline tool | Apache-2.0 | https://github.com/mage-ai/mage-ai |
| dbt (core) | Python | 10k+ | Transform data in warehouse with SQL | Apache-2.0 | https://github.com/dbt-labs/dbt-core |
| SQLMesh | Python | 2k+ | Data transformation framework | Apache-2.0 | https://github.com/TobikoData/sqlmesh |
| Great Expectations | Python | 10k+ | Data validation framework | Apache-2.0 | https://github.com/great-expectations/great_expectations |
| Deequ | Scala | 3k+ | Data quality library on Spark | Apache-2.0 | https://github.com/awslabs/deequ |
| OpenLineage | Python | 2k+ | Open standard for data lineage | Apache-2.0 | https://github.com/OpenLineage/OpenLineage |
| Marquez | Python | 2k+ | Open-source metadata service | Apache-2.0 | https://github.com/MarquezProject/marquez |
| DataHub | Python | 10k+ | Modern data catalog and metadata | Apache-2.0 | https://github.com/datahub-project/datahub |
| Amundsen | Python | 4k+ | Data discovery and metadata by Lyft | Apache-2.0 | https://github.com/amundsen-io/amundsen |
| OpenMetadata | Java | 5k+ | Open-source metadata management | Apache-2.0 | https://github.com/open-metadata/OpenMetadata |
| Apache Atlas | Java | 3k+ | Data governance and metadata framework | Apache-2.0 | https://github.com/apache/atlas |
| Apache Ranger | Java | 2k+ | Data security and governance | Apache-2.0 | https://github.com/apache/ranger |
| Trino | Java | 10k+ | Distributed SQL query engine | Apache-2.0 | https://github.com/trinodb/trino |
| PrestoDB | Java | 15k+ | Distributed SQL query engine by Meta | Apache-2.0 | https://github.com/prestodb/presto |
| DuckDB | C++ | 25k+ | In-process analytical database | MIT | https://github.com/duckdb/duckdb |
| ClickHouse | C++ | 38k+ | Fast OLAP database | Apache-2.0 | https://github.com/ClickHouse/ClickHouse |
| Apache Druid | Java | 14k+ | Real-time analytics database | Apache-2.0 | — |
| Apache Pinot | Java | 5k+ | Real-time OLAP datastore | Apache-2.0 | — |
| Apache Doris | C++ | 13k+ | High-performance real-time analytics | Apache-2.0 | — |
| StarRocks | C++ | 9k+ | OLAP for real-time analytics | Apache-2.0 | https://github.com/StarRocks/starrocks |
| Debezium | Java | 11k+ | CDC (Change Data Capture) platform | Apache-2.0 | https://github.com/debezium/debezium |
| Maxwell's Daemon | Java | 4k+ | MySQL → Kafka CDC tool | Apache-2.0 | — |
| Airbyte | Java | 16k+ | Open-source data integration platform | MIT | https://github.com/airbytehq/airbyte |
| Meltano | Python | 3k+ | ELT framework using Singer protocol | MIT | https://github.com/meltano/meltano |
| Singer | Python | 2k+ | Open-source ETL standard | Apache-2.0 | https://github.com/singer-io/getting-started |
| Stitch | — | — | Cloud ETL (Talend subsidiary, free tier) | Proprietary | — |
| Fivetran (OSS) | — | — | Data integration (proprietary) | Proprietary | — |
| Astronomer (OSS) | Python | — | Managed Airflow (OSS Astro CLI) | Apache-2.0 | — |
| pandas | Python | 43k+ | Data analysis and manipulation library | BSD-3 | https://github.com/pandas-dev/pandas |
| Polars | Rust | 30k+ | Lightning-fast DataFrame library in Rust | MIT | https://github.com/pola-rs/polars |
| Vaex | Python | 8k+ | Out-of-core DataFrame for big data | MIT | https://github.com/vaexio/vaex |
| Dask | Python | 12k+ | Parallel computing library in Python | BSD-3 | https://github.com/dask/dask |
| Ray | Python | 34k+ | Distributed computing for ML | Apache-2.0 | https://github.com/ray-project/ray |
| Modin | Python | 10k+ | Faster pandas using Ray or Dask | Apache-2.0 | https://github.com/modin-project/modin |
| PySpark | Python | — | Python API for Apache Spark | Apache-2.0 | — |
| Koalas (now Pyspark) | Python | 3k+ | pandas API on Apache Spark | Apache-2.0 | — |
| Arrow | C++ | 14k+ | In-memory columnar data format | Apache-2.0 | https://github.com/apache/arrow |
| Parquet | C++/Java | 2k+ | Columnar storage file format | Apache-2.0 | https://github.com/apache/parquet-format |
| ORC | C++/Java | 1k+ | Columnar storage for Hadoop | Apache-2.0 | https://github.com/apache/orc |
| Avro | Java | 3k+ | Data serialization system | Apache-2.0 | https://github.com/apache/avro |
| Protocol Buffers | C++ | 65k+ | Google's language-neutral serialization | BSD-3 | https://github.com/protocolbuffers/protobuf |
| FlatBuffers | C++ | 23k+ | Memory efficient serialization library | Apache-2.0 | https://github.com/google/flatbuffers |
| MessagePack | C | 3k+ | Efficient binary serialization format | Apache-2.0 | https://github.com/msgpack/msgpack |
| CBOR | C | 1k+ | Concise Binary Object Representation | Various | — |
| Cap'n Proto | C++ | 11k+ | Data serialization by Kenton Varda | MIT | https://github.com/capnproto/capnproto |
| csvtotable | Python | 1.2k | CSV to searchable HTML tables | MIT | https://github.com/vividvilla/csvtotable |

---

## 32. Data Visualization & BI

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Grafana | Go | 65k+ | Open-source observability and dashboards | AGPL-3.0 | https://github.com/grafana/grafana |
| Apache Superset | Python | 63k+ | Modern data exploration and BI | Apache-2.0 | https://github.com/apache/superset |
| Redash | Python | 26k+ | Query and visualize data from any source | BSD-2 | https://github.com/getredash/redash |
| Metabase | Clojure | 39k+ | Open-source BI tool, no SQL needed | AGPL-3.0 | https://github.com/metabase/metabase |
| Lightdash | TypeScript | 6k+ | Open-source BI built on dbt | MIT | https://github.com/lightdash/lightdash |
| Evidence | JavaScript | 4k+ | BI using Markdown and SQL | MIT | https://github.com/evidence-dev/evidence |
| Rill | Go | 4k+ | Business intelligence with DuckDB | Apache-2.0 | https://github.com/rilldata/rill |
| Cube | JavaScript | 17k+ | Semantic layer for data apps | Apache-2.0 | https://github.com/cube-js/cube |
| OpenBlocks (Lowcoder) | TypeScript | 8k+ | Low-code internal tool builder | Apache-2.0 | — |
| Appsmith | TypeScript | 34k+ | Open-source low-code for internal apps | Apache-2.0 | https://github.com/appsmithorg/appsmith |
| ToolJet | TypeScript | 32k+ | Open-source low-code framework | AGPL-3.0 | https://github.com/ToolJet/ToolJet |
| Budibase | JavaScript | 22k+ | Low-code platform for internal tools | GPL-3.0 | https://github.com/Budibase/budibase |
| Retool (OSS alt) | TypeScript | — | Internal tools platform (proprietary) | Proprietary | — |
| Observable | JavaScript | — | Data analysis notebooks (free tier) | Proprietary | — |
| Jupyter | Python | 12k+ | Interactive notebooks for analysis | BSD-3 | https://github.com/jupyter/notebook |
| JupyterHub | Python | 8k+ | Multi-user Jupyter for teams | BSD-3 | https://github.com/jupyterhub/jupyterhub |
| Voila | Python | 5k+ | Turn Jupyter notebooks into dashboards | BSD-3 | https://github.com/voila-dashboards/voila |
| Panel | Python | 5k+ | Python dashboarding framework | BSD-3 | https://github.com/holoviz/panel |
| Streamlit | Python | 36k+ | Python apps for ML/data science | Apache-2.0 | https://github.com/streamlit/streamlit |
| Dash (Plotly) | Python | 21k+ | Analytical web apps in Python | MIT | https://github.com/plotly/dash |
| Bokeh | Python | 19k+ | Interactive visualization library | BSD-3 | https://github.com/bokeh/bokeh |
| Altair | Python | 9k+ | Declarative statistical visualization | BSD-3 | https://github.com/vega/altair |
| Matplotlib | Python | 20k+ | Comprehensive 2D plotting for Python | PSF | https://github.com/matplotlib/matplotlib |
| Seaborn | Python | 12k+ | Statistical data visualization | BSD-3 | https://github.com/mwaskom/seaborn |
| Plotly (Python) | Python | 16k+ | Interactive graphing library | MIT | — |
| ggplot2 | R | 6k+ | Grammar of graphics for R | MIT | https://github.com/tidyverse/ggplot2 |
| Shiny (R) | R | 5k+ | Interactive web apps from R | GPL-3.0 | https://github.com/rstudio/shiny |
| D3.js | JavaScript | 108k+ | Data-driven document manipulation | ISC | https://github.com/d3/d3 |
| Vega-Lite | TypeScript | 11k+ | High-level grammar for visualization | BSD-3 | https://github.com/vega/vega-lite |
| Perspective | C++ | 8k+ | High-performance data visualization | Apache-2.0 | https://github.com/finos/perspective |
| Apache ECharts | TypeScript | 59k+ | Interactive charting library | Apache-2.0 | — |
| Recharts | TypeScript | 24k+ | Composable charting for React | MIT | https://github.com/recharts/recharts |

---

## 33. Machine Learning Frameworks

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| TensorFlow | Python/C++ | 186k+ | End-to-end open-source ML platform | Apache-2.0 | https://github.com/tensorflow/tensorflow |
| PyTorch | Python/C++ | 85k+ | Dynamic deep learning framework by Meta | BSD-3 | https://github.com/pytorch/pytorch |
| JAX | Python | 30k+ | Google's NumPy + autograd + XLA | Apache-2.0 | https://github.com/jax-ml/jax |
| MXNet | Python/C++ | 21k+ | Apache deep learning framework | Apache-2.0 | https://github.com/apache/mxnet |
| ONNX | C++ | 18k+ | Open Neural Network Exchange format | Apache-2.0 | https://github.com/onnx/onnx |
| Keras | Python | 61k+ | High-level neural networks API | Apache-2.0 | https://github.com/keras-team/keras |
| scikit-learn | Python | 59k+ | Machine learning library for Python | BSD-3 | https://github.com/scikit-learn/scikit-learn |
| XGBoost | C++ | 26k+ | Scalable gradient boosting | Apache-2.0 | https://github.com/dmlc/xgboost |
| LightGBM | C++ | 16k+ | Fast gradient boosting framework | MIT | https://github.com/microsoft/LightGBM |
| CatBoost | C++ | 8k+ | Gradient boosting by Yandex | Apache-2.0 | https://github.com/catboost/catboost |
| statsmodels | Python | 10k+ | Statistical modeling and testing | BSD-3 | https://github.com/statsmodels/statsmodels |
| Scipy | Python | 13k+ | Scientific computing for Python | BSD-3 | https://github.com/scipy/scipy |
| NumPy | Python | 28k+ | N-dimensional array computing for Python | BSD-3 | https://github.com/numpy/numpy |
| pandas | Python | 43k+ | Data analysis library | BSD-3 | https://github.com/pandas-dev/pandas |
| Polars | Rust | 30k+ | Fast DataFrames in Rust/Python | MIT | https://github.com/pola-rs/polars |
| Arrow | C++ | 14k+ | In-memory columnar data | Apache-2.0 | https://github.com/apache/arrow |
| RAPIDS | CUDA | 8k+ | GPU-accelerated data science | Apache-2.0 | https://github.com/rapidsai/cudf |
| cuML | CUDA | 4k+ | GPU ML library from RAPIDS | Apache-2.0 | — |
| Dask-ML | Python | 2k+ | Scalable ML with Dask | BSD-3 | — |
| H2O.ai | Java | 7k+ | Open-source ML platform | Apache-2.0 | https://github.com/h2oai/h2o-3 |
| Vowpal Wabbit | C++ | 8k+ | Online learning system by Microsoft | BSD-3 | https://github.com/VowpalWabbit/vowpal_wabbit |
| Smile | Java | 6k+ | Statistical ML library for JVM | Apache-2.0 | — |
| Weka | Java | 2k+ | Data mining with ML algorithms | GPL-3.0 | https://github.com/Waikato/weka-3.8 |
| RapidMiner (OSS) | Java | 2k+ | Data science platform | AGPL-3.0 | — |
| Orange3 | Python | 5k+ | Visual ML and data mining | GPL-3.0 | https://github.com/biolab/orange3 |
| KNIME | Java | 1k+ | Visual analytics platform | GPL-3.0 | — |
| Prophet | Python/R | 18k+ | Time-series forecasting by Meta | MIT | https://github.com/facebook/prophet |
| NeuralProphet | Python | 4k+ | Neural network-based forecasting | MIT | https://github.com/ourownstory/neural_prophet |
| Orbit | Python | 2k+ | Bayesian time series modeling | Apache-2.0 | — |
| statsforecast | Python | 4k+ | Fast statistical forecasting | MIT | https://github.com/Nixtla/statsforecast |
| PyCaret | Python | 9k+ | Low-code ML library | MIT | https://github.com/pycaret/pycaret |
| TPOT | Python | 9k+ | AutoML using genetic programming | LGPL-3.0 | https://github.com/EpistasisLab/tpot |
| Auto-sklearn | Python | 7k+ | Automated ML based on scikit-learn | BSD-3 | https://github.com/automl/auto-sklearn |
| FLAML | Python | 4k+ | Fast AutoML by Microsoft | MIT | https://github.com/microsoft/FLAML |
| Optuna | Python | 11k+ | Hyperparameter optimization framework | MIT | https://github.com/optuna/optuna |
| Ray Tune | Python | — | Scalable hyperparameter tuning | Apache-2.0 | — |
| Hyperopt | Python | 7k+ | Distributed async hyperparameter optimization | BSD-3 | https://github.com/hyperopt/hyperopt |
| Ax (Meta) | Python | 2k+ | Adaptive experimentation platform | MIT | https://github.com/facebook/Ax |
| BoTorch | Python | 3k+ | Bayesian optimization library | MIT | https://github.com/pytorch/botorch |
| SHAP | Python | 23k+ | Explain ML model predictions | MIT | https://github.com/shap/shap |
| LIME | Python | 11k+ | Locally Interpretable Model Explanations | BSD-2 | https://github.com/marcotcr/lime |
| Captum | Python | 5k+ | Model interpretability for PyTorch | BSD-3 | https://github.com/pytorch/captum |
| Alibi | Python | 2k+ | ML model explanations and outlier detection | Apache-2.0 | https://github.com/SeldonIO/alibi |
| ELI5 | Python | 3k+ | Debug ML classifiers and explain predictions | MIT | https://github.com/eli5-org/eli5 |
| Fairlearn | Python | 2k+ | Assess and improve ML fairness | MIT | https://github.com/fairlearn/fairlearn |
| AI Fairness 360 | Python | 2k+ | IBM toolkit for bias detection | Apache-2.0 | https://github.com/Trusted-AI/AIF360 |
| MLflow | Python | 19k+ | ML lifecycle management | Apache-2.0 | https://github.com/mlflow/mlflow |
| DVC | Python | 14k+ | Data version control for ML | Apache-2.0 | https://github.com/iterative/dvc |
| Weights & Biases (OSS) | Python | — | Experiment tracking (free tier) | Proprietary | — |
| ClearML | Python | 5k+ | MLOps platform (OSS) | Apache-2.0 | https://github.com/allegroai/clearml |
| Feast | Python | 5k+ | Open-source feature store | Apache-2.0 | https://github.com/feast-dev/feast |
| Hopsworks | Java/Python | 1k+ | Feature store and model registry | AGPL-3.0 | https://github.com/logicalclocks/hopsworks |
| Tecton (OSS SDK) | Python | — | Feature platform (proprietary) | Proprietary | — |

---

## 34. Deep Learning & Neural Networks

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| PyTorch | Python | 85k+ | Dynamic computation graph DL framework | BSD-3 | https://github.com/pytorch/pytorch |
| TensorFlow | Python | 186k+ | Static graph DL framework by Google | Apache-2.0 | https://github.com/tensorflow/tensorflow |
| JAX | Python | 30k+ | Autograd + XLA for high-performance ML | Apache-2.0 | https://github.com/jax-ml/jax |
| Flax | Python | 6k+ | Neural networks in JAX (Google Brain) | Apache-2.0 | https://github.com/google/flax |
| Haiku | Python | 3k+ | Neural networks in JAX (DeepMind) | Apache-2.0 | https://github.com/google-deepmind/dm-haiku |
| Equinox | Python | 2k+ | Neural networks in JAX (PyTree-based) | MIT | https://github.com/patrick-kidger/equinox |
| Lightning | Python | 27k+ | PyTorch wrapper for research scaling | Apache-2.0 | https://github.com/Lightning-AI/pytorch-lightning |
| fast.ai | Python | 26k+ | High-level API on top of PyTorch | Apache-2.0 | https://github.com/fastai/fastai |
| Ignite | Python | 5k+ | High-level PyTorch training library | BSD-3 | https://github.com/pytorch/ignite |
| Catalyst | Python | 3k+ | PyTorch DL research framework | Apache-2.0 | https://github.com/catalyst-team/catalyst |
| Hugging Face Transformers | Python | 136k+ | Pre-trained models for NLP/Vision/Speech | Apache-2.0 | https://github.com/huggingface/transformers |
| Diffusers | Python | 27k+ | Models for image/audio diffusion | Apache-2.0 | https://github.com/huggingface/diffusers |
| timm | Python | 32k+ | PyTorch image models | Apache-2.0 | https://github.com/huggingface/pytorch-image-models |
| torchvision | Python | 16k+ | Datasets, transforms, models for PyTorch | BSD-3 | https://github.com/pytorch/vision |
| torchaudio | Python | 2k+ | Audio processing for PyTorch | BSD-2 | https://github.com/pytorch/audio |
| torchtext | Python | 4k+ | Text processing for PyTorch | BSD-3 | https://github.com/pytorch/text |
| detectron2 | Python | 30k+ | Object detection research by Meta | Apache-2.0 | https://github.com/facebookresearch/detectron2 |
| MMDetection | Python | 30k+ | OpenMMLab detection toolbox | Apache-2.0 | https://github.com/open-mmlab/mmdetection |
| Ultralytics YOLO | Python | 34k+ | Object detection framework | AGPL-3.0 | https://github.com/ultralytics/ultralytics |
| OpenPCDet | Python | 4k+ | 3D object detection toolbox | Apache-2.0 | https://github.com/open-mmlab/OpenPCDet |
| Stable Baselines3 | Python | 9k+ | Reliable RL implementations in PyTorch | MIT | https://github.com/DLR-RM/stable-baselines3 |
| RLlib | Python | — | Scalable RL by Ray team | Apache-2.0 | — |
| Gymnasium (OpenAI Gym) | Python | 7k+ | RL environment toolkit | MIT | https://github.com/Farama-Foundation/Gymnasium |
| PettingZoo | Python | 3k+ | Multi-agent RL environments | MIT | https://github.com/Farama-Foundation/PettingZoo |
| Acme | Python | 3k+ | RL framework by DeepMind | Apache-2.0 | https://github.com/google-deepmind/acme |
| Dopamine | Python | 11k+ | RL framework by Google | Apache-2.0 | https://github.com/google/dopamine |
| SpinningUp | Python | 10k+ | RL educational toolkit by OpenAI | MIT | https://github.com/openai/spinningup |
| TensorBoard | Python | 7k+ | Visualization toolkit for ML training | Apache-2.0 | https://github.com/tensorflow/tensorboard |
| Netron | JavaScript | 29k+ | Visualizer for neural network models | MIT | https://github.com/lutzroeder/netron |
| ONNX Runtime | C++ | 14k+ | Cross-platform ML inference accelerator | MIT | https://github.com/microsoft/onnxruntime |
| TensorRT (OSS) | C++ | 10k+ | NVIDIA GPU inference optimizer | Apache-2.0 | — |
| OpenVINO | C++ | 7k+ | Intel neural network inference toolkit | Apache-2.0 | https://github.com/openvinotoolkit/openvino |
| TFLite | C++ | — | TensorFlow for mobile/edge inference | Apache-2.0 | — |
| CoreML Tools | Python | 4k+ | Convert models to Apple CoreML | BSD-3 | — |
| Apache TVM | C++ | 12k+ | ML compiler framework | Apache-2.0 | https://github.com/apache/tvm |
| Triton (language) | Python | 14k+ | Language for writing GPU kernels | MIT | https://github.com/triton-lang/triton |

---

## 35. MLOps & Model Serving

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| MLflow | Python | 19k+ | Open ML lifecycle platform | Apache-2.0 | https://github.com/mlflow/mlflow |
| DVC | Python | 14k+ | Data and model version control | Apache-2.0 | https://github.com/iterative/dvc |
| ClearML | Python | 5k+ | MLOps platform with experiment tracking | Apache-2.0 | https://github.com/allegroai/clearml |
| Kubeflow | Python | 14k+ | ML toolkit for Kubernetes | Apache-2.0 | https://github.com/kubeflow/kubeflow |
| Metaflow | Python | 8k+ | ML/data framework by Netflix | Apache-2.0 | https://github.com/Netflix/metaflow |
| ZenML | Python | 4k+ | MLOps framework for portable pipelines | Apache-2.0 | https://github.com/zenml-io/zenml |
| Seldon Core | Python | 4k+ | ML model deployment on Kubernetes | Apache-2.0 | https://github.com/SeldonIO/seldon-core |
| BentoML | Python | 7k+ | Unified ML model serving framework | Apache-2.0 | https://github.com/bentoml/BentoML |
| Ray Serve | Python | — | Scalable ML model serving on Ray | Apache-2.0 | — |
| Torchserve | Python | 4k+ | PyTorch model serving | Apache-2.0 | https://github.com/pytorch/serve |
| TF Serving | C++ | 6k+ | TensorFlow model serving | Apache-2.0 | https://github.com/tensorflow/serving |
| Triton Inference Server | C++ | 8k+ | NVIDIA model inference server | BSD-3 | https://github.com/triton-inference-server/server |
| Cortex | Python | 8k+ | Serverless ML deployments | Apache-2.0 | https://github.com/cortexlabs/cortex |
| FastAPI + Pydantic | Python | 79k+ | Common pattern for serving ML models | MIT | — |
| Feast | Python | 5k+ | Feature store for ML | Apache-2.0 | https://github.com/feast-dev/feast |
| Tecton | Python | — | Feature store platform (proprietary) | Proprietary | — |
| Hopsworks | Java | 1k+ | Feature store + model registry | AGPL-3.0 | https://github.com/logicalclocks/hopsworks |
| Evidently | Python | 5k+ | ML model monitoring | Apache-2.0 | https://github.com/evidentlyai/evidently |
| Whylogs | Python | 2k+ | Data logging for ML | Apache-2.0 | https://github.com/whylabs/whylogs |
| Great Expectations | Python | 10k+ | Data validation pipeline testing | Apache-2.0 | https://github.com/great-expectations/great_expectations |
| Arize AI (OSS SDK) | Python | — | ML observability (free tier) | Apache-2.0 | — |
| Weights & Biases | Python | — | Experiment tracking (free tier) | Proprietary | — |
| Neptune.ai | Python | — | Metadata store for ML (free tier) | Proprietary | — |
| Label Studio | Python | 21k+ | Open-source data labeling tool | Apache-2.0 | https://github.com/HumanSignal/label-studio |
| CVAT | Python | 12k+ | Computer vision annotation tool | MIT | https://github.com/cvat-ai/cvat |
| Labelme | Python | 12k+ | Image annotation by MIT CSAIL | MIT | https://github.com/wkentaro/labelme |
| Scale AI (OSS tools) | — | — | Data annotation platform | Proprietary | — |
| Roboflow (OSS) | Python | — | Computer vision dataset tools | Various | — |
| doccano | Python | 10k+ | Open-source annotation tool for NLP | MIT | https://github.com/doccano/doccano |
| Argilla | Python | 4k+ | Data curation for LLM/NLP | Apache-2.0 | https://github.com/argilla-io/argilla |
| Prodigy (trial) | Python | — | ML annotation tool | Proprietary | — |

---

## 36. LLM & Generative AI

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| llama.cpp | C++ | 72k+ | Run LLaMA models on CPU | MIT | https://github.com/ggml-org/llama.cpp |
| Ollama | Go | 102k+ | Run LLMs locally with simple API | MIT | https://github.com/ollama/ollama |
| LM Studio | — | — | Desktop app to run LLMs locally | Proprietary/free | — |
| GPT4All | C++ | 71k+ | Run LLMs locally, privacy-first | MIT | https://github.com/nomic-ai/gpt4all |
| LocalAI | Go | 27k+ | Local OpenAI-compatible API server | MIT | https://github.com/mudler/LocalAI |
| OpenLLM | Python | 10k+ | Run LLMs in production (BentoML) | Apache-2.0 | https://github.com/bentoml/OpenLLM |
| vLLM | Python | 42k+ | Fast LLM inference with PagedAttention | Apache-2.0 | https://github.com/vllm-project/vllm |
| Text Generation Inference | Python | 9k+ | HuggingFace production LLM serving | HF Research | https://github.com/huggingface/text-generation-inference |
| Mistral (OSS models) | Python | — | Open-weights frontier models | Apache-2.0 | — |
| LLaMA 3 (Meta) | Python | — | Open-weights language models | Custom | — |
| Gemma (Google) | Python | — | Open-weights models from Google | Custom | — |
| Falcon | Python | — | Open-weights LLM by TII | Custom | https://github.com/falconry/falcon |
| Phi (Microsoft) | Python | — | Small capable LLMs by Microsoft | MIT/Custom | — |
| Qwen (Alibaba) | Python | — | Open-weights LLMs by Alibaba | Apache-2.0 | — |
| DeepSeek | Python | — | Open-weights frontier models | MIT | — |
| LangChain | Python | 97k+ | Framework for LLM-powered applications | MIT | https://github.com/langchain-ai/langchain |
| LlamaIndex | Python | 38k+ | Data framework for LLM applications | MIT | https://github.com/run-llama/llama_index |
| Haystack | Python | 18k+ | LLM orchestration framework | Apache-2.0 | https://github.com/deepset-ai/haystack |
| Semantic Kernel | C# | 23k+ | LLM SDK for .NET/Python/Java | MIT | https://github.com/microsoft/semantic-kernel |
| Guidance | Python | 20k+ | Constrained generation for LLMs | MIT | https://github.com/guidance-ai/guidance |
| Outlines | Python | 10k+ | Structured text generation | Apache-2.0 | https://github.com/dottxt-ai/outlines |
| Instructor | Python | 9k+ | Structured LLM output extraction | MIT | https://github.com/instructor-ai/instructor |
| DSPy | Python | 21k+ | Programming with LLMs, not prompting | MIT | https://github.com/stanfordnlp/dspy |
| PromptFlow | Python | 10k+ | Build and test LLM workflows | MIT | https://github.com/microsoft/promptflow |
| AutoGen | Python | 34k+ | Multi-agent conversation framework | MIT | https://github.com/microsoft/autogen |
| CrewAI | Python | 26k+ | Orchestrate role-playing AI agents | MIT | https://github.com/crewAIInc/crewAI |
| SuperAGI | Python | 14k+ | Open-source autonomous AI framework | MIT | https://github.com/TransformerOptimus/SuperAGI |
| AgentGPT | TypeScript | 32k+ | Web-based autonomous AI agents | MIT | https://github.com/reworkd/AgentGPT |
| OpenDevin (OpenHands) | Python | 37k+ | AI software engineer agents | MIT | https://github.com/All-Hands-AI/OpenHands |
| SWE-agent | Python | 14k+ | AI agent for software engineering | MIT | https://github.com/SWE-agent/SWE-agent |
| Aider | Python | 26k+ | AI pair programming in the terminal | Apache-2.0 | https://github.com/Aider-AI/aider |
| Continue | TypeScript | 20k+ | Open-source AI coding copilot | Apache-2.0 | https://github.com/continuedev/continue |
| Tabby | Rust | 23k+ | Self-hosted GitHub Copilot alternative | Apache-2.0 | https://github.com/TabbyML/tabby |
| Cody (Sourcegraph) | TypeScript | 3k+ | Open-source AI coding assistant | Apache-2.0 | https://github.com/sourcegraph/cody |
| FauxPilot | Python | 14k+ | Self-hosted GitHub Copilot server | Apache-2.0 | https://github.com/fauxpilot/fauxpilot |
| PrivateGPT | Python | 54k+ | 100% local AI with your documents | Apache-2.0 | https://github.com/zylon-ai/private-gpt |
| AnythingLLM | JavaScript | 30k+ | All-in-one local LLM with RAG | MIT | https://github.com/Mintplex-Labs/anything-llm |
| Open-WebUI | Python | 52k+ | Browser UI for Ollama/OpenAI | MIT | https://github.com/open-webui/open-webui |
| LibreChat | TypeScript | 22k+ | ChatGPT clone with many integrations | MIT | https://github.com/danny-avila/LibreChat |
| Chatbot UI | TypeScript | 30k+ | Open-source ChatGPT UI | MIT | https://github.com/mckaywrigley/chatbot-ui |
| SillyTavern | JavaScript | 8k+ | Frontend for local AI roleplay | AGPL-3.0 | https://github.com/SillyTavern/SillyTavern |
| RAGFlow | Python | 30k+ | Deep RAG engine for document Q&A | Apache-2.0 | https://github.com/infiniflow/ragflow |
| Quivr | Python | 37k+ | Second brain powered by GenAI | Apache-2.0 | https://github.com/QuivrHQ/quivr |
| DocsGPT | Python | 15k+ | AI for documentation Q&A | MIT | https://github.com/arc53/DocsGPT |
| Flowise | TypeScript | 32k+ | LangChain visual builder (drag & drop) | Apache-2.0 | https://github.com/FlowiseAI/Flowise |
| Langflow | Python | 37k+ | LangChain UI flow builder | MIT | https://github.com/langflow-ai/langflow |
| Dify | Python | 67k+ | Open-source LLM app dev platform | Apache-2.0 | https://github.com/langgenius/dify |
| n8n | TypeScript | 51k+ | Workflow automation with AI integrations | Fair-code | https://github.com/n8n-io/n8n |
| Composio | Python | 12k+ | Tool integrations for AI agents | Apache-2.0 | https://github.com/ComposioHQ/composio |
| MemGPT (Letta) | Python | 12k+ | LLMs with self-editing memory | Apache-2.0 | https://github.com/letta-ai/letta |
| OpenGPTs | Python | 6k+ | Open-source GPTs builder (LangGraph) | MIT | — |
| LangGraph | Python | 7k+ | Stateful LLM workflows (LangChain) | MIT | https://github.com/langchain-ai/langgraph |
| AgentScope | Python | 5k+ | Multi-agent framework by Alibaba | Apache-2.0 | https://github.com/modelscope/agentscope |
| CAMEL | Python | 6k+ | Communicative agents for ML research | Apache-2.0 | https://github.com/camel-ai/camel |
| MetaGPT | Python | 46k+ | Multi-agent software company framework | MIT | https://github.com/FoundationAgents/MetaGPT |
| BabyAGI | Python | 20k+ | AI-powered task manager and orchestrator | MIT | https://github.com/yoheinakajima/babyagi |
| Stable Diffusion (web UI) | Python | 141k+ | A1111 Stable Diffusion WebUI | AGPL-3.0 | — |
| ComfyUI | Python | 60k+ | Node-based Stable Diffusion UI | GPL-3.0 | https://github.com/comfyanonymous/ComfyUI |
| InvokeAI | Python | 23k+ | Creative AI image generation tool | Apache-2.0 | https://github.com/invoke-ai/InvokeAI |
| Fooocus | Python | 41k+ | Simplified Stable Diffusion experience | GPL-3.0 | https://github.com/lllyasviel/Fooocus |
| Kohya_ss | Python | 26k+ | Stable Diffusion fine-tuning scripts | Apache-2.0 | https://github.com/bmaltais/kohya_ss |
| DreamBooth | Python | 8k+ | Fine-tune image models on concepts | Apache-2.0 | https://github.com/google/dreambooth |
| xFormers | Python | 8k+ | Flexible efficient transformer blocks | BSD-3 | https://github.com/facebookresearch/xformers |
| Bark | Python | 13k+ | Text-to-audio/speech model | MIT | https://github.com/suno-ai/bark |
| Coqui TTS | Python | 35k+ | Text-to-speech library and models | MPL-2.0 | https://github.com/coqui-ai/TTS |
| Whisper | Python | 71k+ | OpenAI speech recognition model | MIT | https://github.com/openai/whisper |
| MusicGen | Python | — | Meta's music generation model | CC-BY-NC | — |
| AudioCraft | Python | 22k+ | Meta's audio generation framework | MIT | https://github.com/facebookresearch/audiocraft |

---

## 37. NLP & Text Processing

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| spaCy | Python | 30k+ | Industrial-strength NLP library | MIT | https://github.com/explosion/spaCy |
| NLTK | Python | 13k+ | Natural Language Toolkit | Apache-2.0 | https://github.com/nltk/nltk |
| Gensim | Python | 15k+ | Topic modeling and document similarity | LGPL-2.1 | https://github.com/piskvorky/gensim |
| TextBlob | Python | 9k+ | Simple NLP for Python | MIT | https://github.com/sloria/TextBlob |
| Stanford NLP (Stanza) | Python | 7k+ | Stanford's NLP toolkit | Apache-2.0 | https://github.com/stanfordnlp/stanza |
| Flair | Python | 14k+ | State-of-the-art NLP library | MIT | https://github.com/flairNLP/flair |
| AllenNLP | Python | 12k+ | Research NLP framework | Apache-2.0 | https://github.com/allenai/allennlp |
| Transformers (HuggingFace) | Python | 136k+ | Pre-trained transformers | Apache-2.0 | — |
| Sentence-Transformers | Python | 15k+ | Sentence/text embedding with BERT | Apache-2.0 | https://github.com/UKPLab/sentence-transformers |
| BERTopic | Python | 6k+ | Topic modeling with BERT | MIT | https://github.com/MaartenGr/BERTopic |
| fastText | C++ | 26k+ | Library for word representation and text classification | MIT | https://github.com/facebookresearch/fastText |
| word2vec | C | — | Google's original word embeddings | Apache-2.0 | — |
| GloVe | C | 3k+ | Global Vectors for Word Representation | Apache-2.0 | https://github.com/stanfordnlp/GloVe |
| Jina | Python | 21k+ | Neural search and multimodal AI | Apache-2.0 | https://github.com/jina-ai/jina |
| txtai | Python | 9k+ | All-in-one embeddings database | Apache-2.0 | https://github.com/neuml/txtai |
| LangDetect | Python | 3k+ | Language detection library | Apache-2.0 | — |
| PyICU | Python | — | Python bindings for ICU (Unicode) | MIT | — |
| Polyglot | Python | 2k+ | Multilingual text analysis | GPL-3.0 | — |
| sacremoses | Python | 1k+ | Tokenization and normalization | LGPL-2.1 | — |
| SentencePiece | C++ | 10k+ | Unsupervised tokenizer by Google | Apache-2.0 | https://github.com/google/sentencepiece |
| tokenizers | Rust | 9k+ | HuggingFace fast tokenizer library | Apache-2.0 | https://github.com/huggingface/tokenizers |
| tiktoken | Python | 12k+ | OpenAI's fast BPE tokenizer | MIT | https://github.com/openai/tiktoken |
| spacy-llm | Python | 1k+ | Integrating LLMs with spaCy | MIT | — |
| Prodigy (trial) | Python | — | ML-powered annotation for NLP | Proprietary | — |
| doccano | Python | 10k+ | Open-source data labeling for NLP | MIT | https://github.com/doccano/doccano |
| Label Studio | Python | 21k+ | Flexible data labeling tool | Apache-2.0 | https://github.com/HumanSignal/label-studio |
| Argilla | Python | 4k+ | Data curation for NLP/LLMs | Apache-2.0 | https://github.com/argilla-io/argilla |
| Cleanlab | Python | 10k+ | Find and fix label errors in datasets | MIT | https://github.com/cleanlab/cleanlab |
| Rubrix | Python | — | (Now Argilla) NLP data annotation | Apache-2.0 | — |
| Snorkel | Python | 5k+ | Programmatic data labeling | Apache-2.0 | https://github.com/snorkel-team/snorkel |
| regex (Python) | Python | — | Alternate regex module for Python | PSF | — |
| pyparsing | Python | 2k+ | Python parsing library | MIT | — |
| ANTLR | Java | 16k+ | Parser generator for language grammars | BSD-2 | https://github.com/antlr/antlr4 |
| tree-sitter | C | 10k+ | Incremental parsing system | MIT | https://github.com/tree-sitter/tree-sitter |
| Lark | Python | 5k+ | Modern parsing library for Python | MIT | https://github.com/lark-parser/lark |
| PLY | Python | — | Python Lex-Yacc | BSD | — |
| pdfminer.six | Python | 5k+ | PDF text extraction library | MIT | https://github.com/pdfminer/pdfminer.six |
| PyPDF2 | Python | 7k+ | PDF reading/writing library | BSD-3 | https://github.com/py-pdf/pypdf |
| camelot | Python | 3k+ | Extract tables from PDFs | MIT | https://github.com/camelot-dev/camelot |
| tabula-py | Python | 2k+ | Extract tables from PDFs | MIT | https://github.com/chezou/tabula-py |
| pdfplumber | Python | 6k+ | Extract text/tables from PDFs | MIT | https://github.com/jsvine/pdfplumber |
| Docling | Python | 18k+ | Document parsing for LLM RAG | Apache-2.0 | https://github.com/docling-project/docling |
| unstructured | Python | 9k+ | Pre-process docs for ML/LLM | Apache-2.0 | https://github.com/Unstructured-IO/unstructured |
| LlamaParse | Python | — | LLM-based document parsing | Custom | — |
| markitdown | Python | 38k+ | Convert files to Markdown (Microsoft) | MIT | https://github.com/microsoft/markitdown |
| pandoc | Haskell | 33k+ | Universal document format converter | GPL-3.0 | https://github.com/jgm/pandoc |
| tesseract | C++ | 60k+ | OCR engine by Google | Apache-2.0 | https://github.com/tesseract-ocr/tesseract |
| EasyOCR | Python | 23k+ | Ready-to-use OCR with 80+ languages | Apache-2.0 | https://github.com/JaidedAI/EasyOCR |
| PaddleOCR | Python | 46k+ | Practical OCR toolkit by Baidu | Apache-2.0 | https://github.com/PaddlePaddle/PaddleOCR |
| docTR | Python | 4k+ | Document text recognition | Apache-2.0 | https://github.com/mindee/doctr |

---

## 38. Computer Vision

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| OpenCV | C++ | 79k+ | Open-source computer vision library | Apache-2.0 | https://github.com/opencv/opencv |
| Pillow (PIL) | Python | 12k+ | Python imaging library | HPND | https://github.com/python-pillow/Pillow |
| scikit-image | Python | 6k+ | Image processing in Python | BSD-3 | https://github.com/scikit-image/scikit-image |
| imageio | Python | 1k+ | Read/write images in Python | BSD-2 | https://github.com/imageio/imageio |
| albumentation | Python | 14k+ | Fast image augmentation library | MIT | https://github.com/albumentations-team/albumentations |
| imgaug | Python | 14k+ | Image augmentation for ML | MIT | https://github.com/aleju/imgaug |
| torchvision | Python | 16k+ | Computer vision for PyTorch | BSD-3 | https://github.com/pytorch/vision |
| detectron2 | Python | 30k+ | Object detection by Meta | Apache-2.0 | https://github.com/facebookresearch/detectron2 |
| MMDetection | Python | 30k+ | OpenMMLab detection toolbox | Apache-2.0 | https://github.com/open-mmlab/mmdetection |
| YOLOv8 (Ultralytics) | Python | 34k+ | Object detection/tracking/segmentation | AGPL-3.0 | https://github.com/ultralytics/ultralytics |
| DINO | Python | 10k+ | Self-supervised vision transformer | Apache-2.0 | https://github.com/facebookresearch/dino |
| SAM (Meta) | Python | 48k+ | Segment Anything Model | Apache-2.0 | https://github.com/facebookresearch/segment-anything |
| Grounding DINO | Python | 7k+ | Open-set object detection | Apache-2.0 | https://github.com/IDEA-Research/GroundingDINO |
| CLIP | Python | — | Vision-language model by OpenAI | MIT | — |
| OpenCLIP | Python | 10k+ | Open implementation of CLIP | MIT | https://github.com/mlfoundations/open_clip |
| DALL-E (API only) | — | — | Image generation by OpenAI | Proprietary | — |
| Stable Diffusion | Python | — | Open image generation model | CreativeML | — |
| ControlNet | Python | 29k+ | Control image generation with conditions | Apache-2.0 | https://github.com/lllyasviel/ControlNet |
| GFPGAN | Python | 36k+ | Face restoration using GANs | Apache-2.0 | https://github.com/TencentARC/GFPGAN |
| Real-ESRGAN | Python | 27k+ | AI image super-resolution | BSD-3 | https://github.com/xinntao/Real-ESRGAN |
| DeOldify | Python | 18k+ | AI colorization of old photos | MIT | https://github.com/jantic/DeOldify |
| face_recognition | Python | 52k+ | Face recognition library | MIT | https://github.com/ageitgey/face_recognition |
| DeepFace | Python | 13k+ | Facial recognition analysis framework | MIT | https://github.com/serengil/deepface |
| InsightFace | Python | 23k+ | 2D/3D face analysis library | MIT | https://github.com/deepinsight/insightface |
| MediaPipe | C++ | 28k+ | On-device ML framework by Google | Apache-2.0 | https://github.com/google-ai-edge/mediapipe |
| LabelImg | Python | 22k+ | Image annotation tool | MIT | https://github.com/HumanSignal/labelImg |
| CVAT | Python | 12k+ | Computer Vision Annotation Tool | MIT | https://github.com/cvat-ai/cvat |
| Roboflow (OSS) | Python | 2k+ | Dataset management for computer vision | Various | — |
| FiftyOne | Python | 8k+ | Dataset curation for CV | Apache-2.0 | https://github.com/voxel51/fiftyone |
| Supervision | Python | 24k+ | Reusable CV utilities by Roboflow | MIT | https://github.com/roboflow/supervision |
| ffmpeg | C | 43k+ | Complete multimedia processing solution | LGPL/GPL | https://github.com/FFmpeg/FFmpeg |
| OpenVINO | C++ | 7k+ | Intel inference toolkit | Apache-2.0 | https://github.com/openvinotoolkit/openvino |
| ONNX Runtime | C++ | 14k+ | Cross-platform inference accelerator | MIT | https://github.com/microsoft/onnxruntime |
| TensorRT-LLM | C++ | 10k+ | NVIDIA LLM acceleration library | Apache-2.0 | — |


---

## 39. Audio & Speech

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Whisper | Python | 71k+ | OpenAI automatic speech recognition | MIT | https://github.com/openai/whisper |
| faster-whisper | Python | 12k+ | Faster Whisper using CTranslate2 | MIT | https://github.com/SYSTRAN/faster-whisper |
| whisper.cpp | C++ | 36k+ | Whisper on CPU in C++ | MIT | https://github.com/ggml-org/whisper.cpp |
| Coqui TTS | Python | 35k+ | Text-to-speech with many voices | MPL-2.0 | https://github.com/coqui-ai/TTS |
| Mozilla TTS | Python | 10k+ | Deep learning toolkit for TTS | MPL-2.0 | https://github.com/mozilla/TTS |
| Bark | Python | 13k+ | High-quality text-to-audio model | MIT | https://github.com/suno-ai/bark |
| SpeechBrain | Python | 8k+ | Conversational AI toolkit | Apache-2.0 | https://github.com/speechbrain/speechbrain |
| Kaldi | C++ | 14k+ | ASR toolkit for speech | Apache-2.0 | https://github.com/kaldi-asr/kaldi |
| ESPnet | Python | 8k+ | End-to-end speech processing toolkit | Apache-2.0 | https://github.com/espnet/espnet |
| librosa | Python | 7k+ | Music and audio analysis | ISC | https://github.com/librosa/librosa |
| pyaudio | C | — | Python bindings for PortAudio | MIT | — |
| soundfile | Python | 700+ | Read/write sound files | BSD-3 | https://github.com/bastibe/python-soundfile |
| pydub | Python | 8k+ | Manipulate audio with a simple API | MIT | https://github.com/jiaaro/pydub |
| ffmpeg-python | Python | 10k+ | Python bindings for ffmpeg | Apache-2.0 | https://github.com/kkroening/ffmpeg-python |
| ffmpeg | C | 43k+ | Complete multimedia processing | LGPL/GPL | https://github.com/FFmpeg/FFmpeg |
| Audacity | C++ | 11k+ | Free, open-source audio editor | GPL-2.0 | https://github.com/audacity/audacity |
| Ardour | C++ | 3k+ | Professional digital audio workstation | GPL-2.0 | https://github.com/Ardour/ardour |
| LMMS | C++ | 8k+ | Open-source music production | GPL-2.0 | https://github.com/LMMS/lmms |
| VLC (libvlc) | C | 13k+ | Media player and library | LGPL-2.1 | — |
| GStreamer | C | 1k+ | Multimedia pipeline framework | LGPL-2.0 | https://gitlab.freedesktop.org/gstreamer/gstreamer |
| Pipewire | C | 4k+ | Low-latency audio/video server for Linux | MIT/LGPL | https://gitlab.freedesktop.org/pipewire/pipewire |
| PulseAudio | C | 1k+ | Sound server for Linux | LGPL-2.1 | — |
| JACK Audio | C | 1k+ | Low-latency professional audio server | GPL-2.0 | — |
| SuperCollider | C++ | 4k+ | Audio synthesis and composition | GPL-3.0 | https://github.com/supercollider/supercollider |
| Csound | C | 1k+ | Sound and music synthesis system | LGPL-2.1 | https://github.com/csound/csound |
| AudioCraft | Python | 22k+ | Meta's audio generation framework | MIT | https://github.com/facebookresearch/audiocraft |
| MusicGen | Python | — | Meta's music generation model | CC-BY-NC | — |
| Demucs | Python | 8k+ | Music source separation by Meta | MIT | https://github.com/facebookresearch/demucs |
| Spleeter | Python | 26k+ | Music source separation by Deezer | MIT | https://github.com/deezer/spleeter |
| vocal-remover | Python | 3k+ | AI vocal remover | MIT | — |
| pedalboard | Python | 5k+ | Spotify's audio processing library | GPL-3.0 | https://github.com/spotify/pedalboard |
| RNNoise | C | 4k+ | Noise suppression using RNN | BSD-3 | https://github.com/xiph/rnnoise |
| opus | C | 1k+ | High-quality open audio codec | BSD-3 | — |
| FLAC | C | 1k+ | Free Lossless Audio Codec | BSD/GPL | — |
| OGG Vorbis | C | 1k+ | Open audio compression format | BSD-3 | — |

---

## 40. CLI Tools & Utilities

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| fzf | Go | 65k+ | Command-line fuzzy finder | MIT | https://github.com/junegunn/fzf |
| ripgrep | Rust | 49k+ | Fast grep alternative | MIT/Unlicense | https://github.com/BurntSushi/ripgrep |
| fd | Rust | 34k+ | Fast find alternative | MIT | https://github.com/sharkdp/fd |
| bat | Rust | 50k+ | Cat with syntax highlighting | MIT | https://github.com/sharkdp/bat |
| eza | Rust | 12k+ | Modern ls replacement | MIT | — |
| delta | Rust | 23k+ | Beautiful git diffs | MIT | https://github.com/dandavison/delta |
| jq | C | 30k+ | Lightweight JSON processor | MIT | https://github.com/jqlang/jq |
| yq | Go | 12k+ | YAML/JSON/XML processor (like jq) | MIT | https://github.com/mikefarah/yq |
| fx | Go | 20k+ | Terminal JSON viewer | MIT | https://github.com/uber-go/fx |
| gron | Go | 14k+ | Make JSON greppable | MIT | https://github.com/tomnomnom/gron |
| xsv | Rust | 11k+ | Fast CSV command line toolkit | MIT/Unlicense | https://github.com/BurntSushi/xsv |
| miller (mlr) | C | 9k+ | Like awk/sed/cut/join for data files | BSD-2 | https://github.com/johnkerl/miller |
| q | Python | 11k+ | Run SQL queries on CSV/TSV files | GPL-3.0 | — |
| visidata | Python | 8k+ | Terminal spreadsheet multitool | GPL-3.0 | https://github.com/saulpw/visidata |
| dasel | Go | 7k+ | Select/put data using CSS-like selectors | MIT | https://github.com/TomWright/dasel |
| jo | C | 5k+ | Generate JSON from shell | GPL-2.0 | https://github.com/jpmens/jo |
| jid | Go | 6k+ | Interactive JSON incremental digger | MIT | https://github.com/simeji/jid |
| pup | Go | 4k+ | Parsing HTML at the command line | MIT | https://github.com/ericchiang/pup |
| htmlq | Rust | 5k+ | Like jq but for HTML | MIT | https://github.com/mgdm/htmlq |
| hyperfine | Rust | 21k+ | Command-line benchmarking tool | MIT | https://github.com/sharkdp/hyperfine |
| tokei | Rust | 11k+ | Count code lines in projects | MIT | https://github.com/XAMPPRocky/tokei |
| cloc | Perl | 18k+ | Count lines of code | GPL-2.0 | https://github.com/AlDanial/cloc |
| scc | Go | 6k+ | Sloc, Cloc and Code — fast code counter | MIT | https://github.com/boyter/scc |
| tre | Rust | 1k+ | Tree command with git support | MIT | — |
| broot | Rust | 11k+ | Navigate directory trees interactively | MIT | https://github.com/Canop/broot |
| ranger | Python | 14k+ | Terminal file manager | GPL-3.0 | https://github.com/ranger/ranger |
| lf | Go | 7k+ | Terminal file manager (inspired by ranger) | MIT | https://github.com/gokcehan/lf |
| nnn | C | 19k+ | n³ — The unorthodox terminal file manager | BSD-2 | https://github.com/jarun/nnn |
| yazi | Rust | 20k+ | Blazing-fast terminal file manager | MIT | https://github.com/sxyazi/yazi |
| mc | C | 6k+ | Midnight Commander — visual file manager | GPL-3.0 | https://github.com/MidnightCommander/mc |
| ncdu | C | 2k+ | NCurses disk usage analyzer | MIT | https://code.rocketnine.space/tslocum/ncdu |
| duf | Go | 13k+ | Disk usage with nice output | MIT | https://github.com/muesli/duf |
| dust | Rust | 9k+ | More intuitive disk usage | Apache-2.0 | https://github.com/bootandy/dust |
| watch | C | — | Execute a program periodically | GPL-2.0 | — |
| entr | C | 3k+ | Run arbitrary commands on file change | ISC | https://github.com/eradman/entr |
| watchexec | Rust | 5k+ | Execute commands in response to changes | Apache-2.0 | https://github.com/watchexec/watchexec |
| fswatch | C++ | 4k+ | File change monitor | GPL-3.0 | https://github.com/emcrisostomo/fswatch |
| inotify-tools | C | 2k+ | Linux inotify file watch utilities | GPL-2.0 | https://github.com/inotify-tools/inotify-tools |
| parallel (GNU) | Perl | — | Shell parallel command execution | GPL-3.0 | — |
| xargs | C | — | Build and execute commands from stdin | GPL-3.0 | — |
| rush | Go | 1k+ | Parallel command executor like GNU parallel | MIT | — |
| moreutils | C | — | Additional Unix utilities | GPL-2.0 | — |
| pv | C | — | Monitor data through a pipe | Artistic | — |
| progress | C | 2k+ | See progress of GNU coreutils | GPL-3.0 | — |
| cron | C | — | Classic job scheduler | Various | https://github.com/robfig/cron |
| cronie | C | 1k+ | Modern cron with PAM support | MIT | — |
| supercronic | Go | 5k+ | Cron for containers | MIT | https://github.com/aptible/supercronic |
| task-spooler | C | — | Unix batch system (job queue) | GPL-2.0 | — |
| tmux | C | 34k+ | Terminal multiplexer | ISC | https://github.com/tmux/tmux |
| screen | C | — | GNU Screen terminal multiplexer | GPL-3.0 | — |
| byobu | Shell | 1k+ | Text-based window manager on tmux/screen | GPL-3.0 | https://github.com/dustinkirkland/byobu |
| zellij | Rust | 22k+ | Terminal workspace with layouts | MIT | — |
| httpie | Python | 33k+ | HTTP client for humans | BSD-3 | https://github.com/httpie/cli |
| curlie | Go | 2k+ | httpie front-end for curl | MIT | https://github.com/rs/curlie |
| xh | Rust | 5k+ | Friendly HTTP client (httpie-compatible) | MIT | https://github.com/ducaale/xh |
| hey | Go | 17k+ | HTTP load generator | Apache-2.0 | https://github.com/rakyll/hey |
| wrk | C | 36k+ | HTTP benchmarking tool | Apache-2.0 | https://github.com/wg/wrk |
| vegeta | Go | 24k+ | HTTP load testing toolkit | MIT | https://github.com/tsenart/vegeta |
| k6 | Go | 26k+ | Performance testing tool for APIs | AGPL-3.0 | https://github.com/grafana/k6 |
| locust | Python | 24k+ | Scalable load testing with Python | MIT | https://github.com/locustio/locust |
| ab (Apache Bench) | C | — | Apache HTTP server benchmarking | Apache-2.0 | — |
| siege | C | 2k+ | HTTP/HTTPS stress tester | GPL-3.0 | — |
| gh | Go | 37k+ | GitHub CLI | MIT | https://github.com/cli/cli |
| glab | Go | 4k+ | GitLab CLI | MIT | https://gitlab.com/gitlab-org/cli |
| hub | Go | 23k+ | GitHub CLI wrapper (older) | MIT | https://github.com/mislav/hub |
| forgejo-cli | Go | — | Forgejo/Gitea CLI | MIT | — |
| act | Go | 56k+ | Run GitHub Actions locally | MIT | — |
| doctl | Go | 3k+ | DigitalOcean CLI | Apache-2.0 | https://github.com/digitalocean/doctl |
| aws-cli | Python | 15k+ | Official AWS CLI | Apache-2.0 | https://github.com/aws/aws-cli |
| azure-cli | Python | 4k+ | Microsoft Azure CLI | MIT | https://github.com/Azure/azure-cli |
| gcloud | Python | 1k+ | Google Cloud SDK CLI | Apache-2.0 | — |
| terraform | Go | 43k+ | Infrastructure as Code CLI | BSL-1.1 | — |
| tofu | Go | 23k+ | OpenTofu CLI | MPL-2.0 | — |
| ansible | Python | 63k+ | IT automation CLI | GPL-3.0 | — |
| helm | Go | 27k+ | Kubernetes package manager CLI | Apache-2.0 | — |
| kubectl | Go | — | Kubernetes CLI | Apache-2.0 | — |
| k9s | Go | 27k+ | Terminal K8s management UI | Apache-2.0 | https://github.com/derailed/k9s |
| kubectx/kubens | Go | 16k+ | K8s context switcher | Apache-2.0 | — |
| stern | Go | 5k+ | Multi pod log tailing for K8s | Apache-2.0 | https://github.com/stern/stern |
| kail | Go | 2k+ | Kubernetes tail — log streaming | MIT | — |
| lazykube | Go | — | Lazy K8s terminal UI | MIT | — |
| lazydocker | Go | 38k+ | Docker TUI | MIT | https://github.com/jesseduffield/lazydocker |
| ctop | Go | 15k+ | Container resource metrics TUI | MIT | https://github.com/bcicen/ctop |
| dive | Go | 44k+ | Explore Docker image layers | MIT | — |
| grex | Rust | 7k+ | Generate regex from test cases | MIT | https://github.com/pemistahl/grex |
| dagrex | Go | — | Regex playground tool | MIT | — |
| choose | Rust | 2k+ | Cut-like field selector | MIT | https://github.com/theryangeary/choose |
| sd | Rust | 5k+ | Intuitive find-and-replace CLI | MIT | https://github.com/chmln/sd |
| tr | C | — | Translate/delete characters (GNU) | GPL-3.0 | — |
| awk/gawk | C | 1k+ | Pattern scanning and processing | GPL-3.0 | — |
| sed | C | — | Stream editor for filtering text | GPL-3.0 | — |
| csvkit | Python | 6k+ | Suite of CLI tools for CSV files | MIT | https://github.com/wireservice/csvkit |
| xmlstarlet | C | 1k+ | XML processing command-line toolkit | MIT | https://sourceforge.net/projects/xmlstar/ |
| zstd | C | 23k+ | Fast lossless compression algorithm | BSD-3 | https://github.com/facebook/zstd |
| lz4 | C | 10k+ | Extremely fast compression algorithm | BSD-2 | https://github.com/lz4/lz4 |
| xz | C | 1k+ | High ratio compression utility | Public Domain | — |
| gzip/bzip2 | C | — | Classic Unix compression tools | GPL-2.0 | — |
| pigz | C | 3k+ | Parallel implementation of gzip | Zlib | https://github.com/madler/pigz |
| pbzip2 | C++ | — | Parallel bzip2 compression | BSD-like | — |
| rclone | Go | 47k+ | rsync for cloud storage (S3, GCS, etc.) | MIT | https://github.com/rclone/rclone |
| rsync | C | 3k+ | Fast incremental file transfer | GPL-3.0 | https://github.com/WayneD/rsync |
| unison | OCaml | 2k+ | File synchronization tool | GPL-3.0 | https://github.com/bcpierce00/unison |
| syncthing | Go | 64k+ | Decentralized continuous file synchronization | MPL-2.0 | https://github.com/syncthing/syncthing |
| restic | Go | 26k+ | Fast encrypted backup tool | BSD-2 | https://github.com/restic/restic |
| borg | Python | 11k+ | Deduplicating backup tool | BSD-3 | https://github.com/borgbackup/borg |
| duplicati | C# | 11k+ | Encrypted online backup solution | LGPL-2.1 | https://github.com/duplicati/duplicati |

---

## 41. File & Storage

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| MinIO | Go | 49k+ | High-performance S3-compatible object store | AGPL-3.0 | https://github.com/minio/minio |
| SeaweedFS | Go | 23k+ | Distributed storage (S3-compatible) | Apache-2.0 | https://github.com/seaweedfs/seaweedfs |
| Ceph | C++ | 14k+ | Unified distributed storage system | LGPL-2.1 | https://github.com/ceph/ceph |
| GlusterFS | C | 4k+ | Network-attached storage filesystem | GPL-3.0 | https://github.com/gluster/glusterfs |
| HDFS | Java | — | Hadoop Distributed File System | Apache-2.0 | — |
| Lustre | C | 1k+ | High-performance distributed filesystem | GPL-2.0 | https://github.com/lustre/lustre |
| BeeGFS | C | 1k+ | Parallel file system (formerly FhGFS) | GPL-2.0 | https://github.com/ThinkParQ/beegfs |
| OrangeFS | C | — | Scale-out NAS filesystem | LGPL-2.1 | — |
| ZFS | C | 4k+ | Advanced filesystem with snapshots | CDDL-1.0 | https://github.com/openzfs/zfs |
| Btrfs | C | 1k+ | Copy-on-write Linux filesystem | GPL-2.0 | https://github.com/btrfs/linux |
| ext4 | C | — | Linux's most common filesystem | GPL-2.0 | — |
| XFS | C | — | High-performance journaling filesystem | GPL-2.0 | — |
| NFS | C | — | Network File System | GPL-2.0 | — |
| Samba | C | 2k+ | Windows SMB/CIFS for Linux | GPL-3.0 | https://github.com/samba-team/samba |
| Nextcloud | PHP | 27k+ | Self-hosted Google Drive alternative | AGPL-3.0 | https://github.com/nextcloud/server |
| ownCloud | PHP | 8k+ | File sync and share platform | GPL-3.0 | https://github.com/owncloud/core |
| Seafile | C | 12k+ | File hosting and sync for teams | AGPL/GPLv2 | https://github.com/haiwen/seafile |
| Pydio Cells | Go | 2k+ | Enterprise file sharing platform | AGPL-3.0 | https://github.com/pydio/cells |
| FileBrowser | Go | 27k+ | Web-based file browser/manager | Apache-2.0 | https://github.com/filebrowser/filebrowser |
| Garage | Rust | 3k+ | S3-compatible distributed object storage | AGPL-3.0 | https://git.deuxfleurs.fr/Deuxfleurs/garage |
| rclone | Go | 47k+ | rsync for cloud storage | MIT | https://github.com/rclone/rclone |
| Cyberduck (OSS) | Java | 4k+ | FTP/SFTP/S3 browser (open-source) | GPL-3.0 | https://github.com/iterate-ch/cyberduck |
| s3cmd | Python | 4k+ | Command-line S3 client | GPL-2.0 | https://github.com/s3tools/s3cmd |
| s5cmd | Go | 3k+ | Parallel S3/GCS/Azure CLI tool | MIT | https://github.com/peak/s5cmd |
| simples3 | Go | 197 | Minimal S3 Go library | MIT | https://github.com/zerodha/simples3 |
| LVM | C | — | Linux Logical Volume Manager | GPL-2.0 | — |
| DRBD | C | 1k+ | Distributed Replicated Block Device | GPL-2.0 | https://github.com/LINBIT/drbd |
| OpenZFS | C | 4k+ | ZFS for Linux and macOS | CDDL-1.0 | https://github.com/openzfs/zfs |
| Longhorn | Go | 6k+ | Distributed block storage for K8s | Apache-2.0 | https://github.com/longhorn/longhorn |
| OpenEBS | Go | 9k+ | K8s storage with multiple engines | Apache-2.0 | https://github.com/openebs/openebs |
| Rook | Go | 12k+ | Cloud-native storage operator (Ceph) | Apache-2.0 | https://github.com/rook/rook |
| Velero | Go | 8k+ | K8s backup and disaster recovery | Apache-2.0 | https://github.com/vmware-tanzu/velero |
| blobasaur | Rust | 43 | SQLite blob store with Redis protocol | MIT | https://github.com/zerodha/blobasaur |
| stuffbin | Go | 200 | Embed static assets in Go binaries | MIT | https://github.com/knadh/stuffbin |
| indexed-cache | JavaScript | 127 | Sideload assets into IndexedDB | MIT | https://github.com/zerodha/indexed-cache |

---

## 42. Backup & Disaster Recovery

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Restic | Go | 26k+ | Fast, encrypted, deduplicated backups | BSD-2 | — |
| Borg | Python | 11k+ | Deduplicating archive program | BSD-3 | — |
| Duplicati | C# | 11k+ | Backup for cloud storage | LGPL-2.1 | — |
| Duplicacy | Go | 5k+ | Lock-free deduplicating backup | Apache-2.0 | https://github.com/gilbertchen/duplicacy |
| Rclone | Go | 47k+ | Cloud storage sync/backup | MIT | — |
| rsync | C | 3k+ | Incremental file sync | GPL-3.0 | https://github.com/WayneD/rsync |
| Bacula | C++ | 1k+ | Enterprise network backup | AGPL-3.0 | https://github.com/bacula/bacula |
| Amanda | C | 1k+ | Network backup solution | BSD/GPL | https://github.com/zmanda/amanda |
| BackupPC | Perl | 1k+ | High-performance backup system | GPL-2.0 | https://github.com/backuppc/backuppc |
| Barman | Python | 2k+ | PostgreSQL backup manager | GPL-3.0 | https://github.com/EnterpriseDB/barman |
| pgBackRest | C | 3k+ | PostgreSQL backup solution | MIT | https://github.com/pgbackrest/pgbackrest |
| mysqldump | C | — | MySQL backup utility (bundled) | GPL-2.0 | — |
| mydumper | C | 2k+ | Fast MySQL logical backup | GPL-2.0 | https://github.com/mydumper/mydumper |
| Velero | Go | 8k+ | K8s backup and migration | Apache-2.0 | https://github.com/vmware-tanzu/velero |
| Kasten K10 (free) | — | — | K8s backup platform (free tier) | Proprietary | — |
| DRBD | C | 1k+ | Replicated block storage for HA | GPL-2.0 | https://github.com/LINBIT/drbd |
| Corosync | C | — | Cluster infrastructure layer | BSD-2 | https://github.com/corosync/corosync |
| Pacemaker | C | 1k+ | Cluster resource manager | GPL-2.0 | https://github.com/ClusterLabs/pacemaker |
| Keepalived | C | 4k+ | HA via VRRP for Linux | GPL-2.0 | https://github.com/acassen/keepalived |
| HAProxy | C | 5k+ | Reliable load balancer for HA | GPL-2.0 | https://github.com/haproxy/haproxy |

---

## 43. Notification & Alerting

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Alertmanager | Go | 6k+ | Prometheus alert handler | Apache-2.0 | — |
| Grafana OnCall | Python | 3k+ | On-call scheduling and alert routing | AGPL-3.0 | https://github.com/grafana/oncall |
| Cabot | Python | 5k+ | Self-hosted Pagerduty alternative | MIT | https://github.com/cabotapp/cabot |
| Opsgenie (OSS SDK) | Various | — | Alert management (Atlassian, free tier) | Proprietary | — |
| PagerDuty (OSS) | Various | — | Incident management (proprietary) | Proprietary | — |
| Incident.io (OSS) | Go | — | Incident management tool | Proprietary | — |
| Rootly | — | — | Incident response platform | Proprietary | — |
| Ntfy | Go | 19k+ | Push notifications via HTTP | Apache-2.0 | https://github.com/binwiederhier/ntfy |
| Gotify | Go | 11k+ | Self-hosted push notification server | MIT | https://github.com/gotify/server |
| Apprise | Python | 11k+ | Notifications to 100+ services | MIT/BSD | https://github.com/caronc/apprise |
| Shoutrrr | Go | 700+ | Send notifications from CLI/code | MIT | https://github.com/nicholas-fedor/shoutrrr |
| calert | Go | 201 | Prometheus alerts → Google Chat | MIT | https://github.com/zerodha/calert |
| listmonk-messenger | Go | 73 | Webhook forwarder for messengers | MIT | https://github.com/zerodha/listmonk-messenger |
| casdoor notifications | Go | — | Notifications in identity platform | Apache-2.0 | — |
| Novu | TypeScript | 35k+ | Open-source notification infrastructure | MIT | https://github.com/novuhq/novu |
| Knock | TypeScript | — | Notification platform (free tier) | Proprietary | — |
| courier | — | — | Notification platform (free tier) | Proprietary | — |
| Webpush (libraries) | Various | — | Browser push notification libraries | MIT | — |
| Firebase (OSS SDK) | JavaScript | — | Push notifications (proprietary backend) | Apache-2.0 | — |
| OneSignal (OSS SDK) | Various | — | Push notifications (free tier) | Proprietary | — |

---

## 44. Email & Messaging

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| listmonk | Go | 19.5k+ | Self-hosted newsletter/mailing list | MIT | https://github.com/knadh/listmonk |
| Postal | Ruby | 15k+ | Full-featured mail delivery platform | Apache-2.0 | https://github.com/postalserver/postal |
| Mailu | Python | 6k+ | Simple and full-featured mail server | MIT | https://github.com/Mailu/Mailu |
| Mail-in-a-Box | Shell | 14k+ | Easy self-hosted email | CC0 | https://github.com/mail-in-a-box/mailinabox |
| Mailcow | PHP | 8k+ | Docker-based mail server suite | GPL-3.0 | https://github.com/mailcow/mailcow-dockerized |
| iRedMail | Shell | 2k+ | Full-featured mail server setup | GPL-3.0 | https://github.com/iredmail/iRedMail |
| Postfix | C | 2k+ | UNIX Mail Transfer Agent | IPL-1.0 | https://github.com/vdukhovni/postfix |
| Dovecot | C | 3k+ | IMAP/POP3 email server | MIT | https://github.com/dovecot/core |
| OpenSMTPD | C | 2k+ | OpenBSD's SMTP server | ISC | https://github.com/OpenSMTPD/OpenSMTPD |
| Exim | C | 1k+ | Message Transfer Agent | GPL-2.0 | https://github.com/Exim/exim |
| MailHog | Go | 14k+ | Email testing tool for development | MIT | https://github.com/mailhog/MailHog |
| Mailpit | Go | 6k+ | Email testing tool (MailHog successor) | MIT | https://github.com/axllent/mailpit |
| FakeSMTP | Java | 3k+ | Dummy SMTP server for testing | BSD-2 | https://github.com/Nilhcem/FakeSMTP |
| hedwig | Rust | 49 | Minimalist SMTP server | MIT | https://github.com/zerodha/hedwig |
| mox | Go | 3k+ | Modern full-featured SMTP/IMAP server | MIT | https://github.com/mjl-/mox |
| Haraka | JavaScript | 5k+ | Highly scalable Node.js email server | MIT | https://github.com/haraka/Haraka |
| Nodemailer | JavaScript | 16k+ | Email sending for Node.js | MIT | https://github.com/nodemailer/nodemailer |
| lettre | Rust | 2k+ | Email client library for Rust | MIT/Apache-2.0 | https://github.com/lettre/lettre |
| gomail | Go | 4k+ | Simple and efficient email in Go | MIT | https://github.com/go-gomail/gomail |
| Django email backends | Python | — | Built-in Django email utilities | BSD-3 | — |
| Python smtplib | Python | — | Python's built-in SMTP client | PSF | — |
| sendgrid (OSS SDK) | Various | — | Email delivery (free tier) | MIT | — |
| Mautic | PHP | 7k+ | Open-source marketing automation | Apache-2.0 | https://github.com/mautic/mautic |
| Chatwoot | Ruby | 22k+ | Open-source customer support platform | MIT | https://github.com/chatwoot/chatwoot |
| Zulip | Python | 21k+ | Open-source team messaging | Apache-2.0 | https://github.com/zulip/zulip |
| Rocket.Chat | TypeScript | 42k+ | Open-source team collaboration | MIT | https://github.com/RocketChat/Rocket.Chat |
| Mattermost | Go | 30k+ | Open-source Slack alternative | MIT | https://github.com/mattermost/mattermost |
| Matrix (Synapse) | Python | 12k+ | Open-source federated messaging | Apache-2.0 | https://github.com/element-hq/synapse |
| Element (Matrix client) | TypeScript | 11k+ | Matrix-based messaging client | Apache-2.0 | https://github.com/element-hq/element-web |
| Conduit | Rust | 5k+ | Simple Matrix homeserver in Rust | Apache-2.0 | https://gitlab.com/famedly/conduit |
| Signal server | Java | 11k+ | Signal messaging server (OSS backend) | AGPL-3.0 | https://github.com/signalapp/Signal-Server |
| Jitsi Meet | JavaScript | 23k+ | Video conferencing platform | Apache-2.0 | https://github.com/jitsi/jitsi-meet |
| BigBlueButton | JavaScript | 9k+ | Open-source virtual classroom | LGPL-3.0 | https://github.com/bigbluebutton/bigbluebutton |
| OpenVidu | Java | 1k+ | Video conferencing platform | Apache-2.0 | https://github.com/OpenVidu/openvidu |
| LiveKit | Go | 11k+ | Open-source WebRTC infrastructure | Apache-2.0 | https://github.com/livekit/livekit |
| Coturn | C | 11k+ | TURN/STUN server for WebRTC | BSD-3 | https://github.com/coturn/coturn |
| Twilio (OSS SDKs) | Various | — | CPaaS (proprietary, free tier) | MIT | — |
| Vonage/Nexmo (OSS SDK) | Various | — | Messaging API (proprietary) | MIT | — |
| whatomate | Go | 977 | Open-source WhatsApp integration | MIT | https://github.com/zerodha/whatomate |
| otpgateway | Go | 522 | Standalone OTP verification server | MIT | https://github.com/zerodha/otpgateway |

---

## 45. Video & Media

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| ffmpeg | C | 43k+ | Complete multimedia framework | LGPL/GPL | https://github.com/FFmpeg/FFmpeg |
| VLC | C | 13k+ | Cross-platform media player | GPL/LGPL | — |
| MPV | C | 28k+ | Free media player (mpv.io) | GPL-2.0 | https://github.com/mpv-player/mpv |
| GStreamer | C | 1k+ | Multimedia pipeline framework | LGPL-2.0 | https://gitlab.freedesktop.org/gstreamer/gstreamer |
| HandBrake | C | 18k+ | Video transcoder | GPL-2.0 | https://github.com/HandBrake/HandBrake |
| Kdenlive | C++ | 3k+ | Non-linear video editor | GPL-2.0 | https://github.com/KDE/kdenlive |
| OpenShot | Python | 5k+ | Open-source video editor | GPL-3.0 | https://github.com/OpenShot/openshot-qt |
| Shotcut | C++ | 11k+ | Free, open-source video editor | GPL-3.0 | https://github.com/mltframework/shotcut |
| Blender | C/Python | 13k+ | 3D creation suite (with video editing) | GPL-2.0 | https://projects.blender.org/blender/blender |
| Natron | C++ | 4k+ | Open-source compositing software | GPL-2.0 | https://github.com/NatronGitHub/Natron |
| OBS Studio | C | 60k+ | Open-source broadcasting/recording | GPL-2.0 | https://github.com/obsproject/obs-studio |
| Owncast | Go | 9k+ | Self-hosted live streaming platform | MIT | https://github.com/owncast/owncast |
| PeerTube | TypeScript | 13k+ | Decentralized video platform | AGPL-3.0 | https://github.com/Chocobozzz/PeerTube |
| MediaCMS | Python | 2k+ | Self-hosted video CMS platform | MIT | https://github.com/mediacms-io/mediacms |
| AVideo | PHP | 1k+ | Self-hosted video platform | GPL-3.0 | — |
| Navidrome | Go | 12k+ | Self-hosted music streaming server | GPL-3.0 | https://github.com/navidrome/navidrome |
| Jellyfin | C# | 34k+ | Free software media system | GPL-2.0 | https://github.com/jellyfin/jellyfin |
| Plex (OSS tools) | — | — | Media server (proprietary) | Proprietary | — |
| Kodi | C++ | 18k+ | Award-winning media center | GPL-2.0 | https://github.com/xbmc/xbmc |
| nginx-rtmp-module | C | 12k+ | RTMP server module for nginx | BSD-2 | https://github.com/arut/nginx-rtmp-module |
| SRS (Simple Realtime Server) | C++ | 25k+ | Live streaming server | MIT | https://github.com/ossrs/srs |
| MediaMTX | Go | 12k+ | WebRTC/RTSP/HLS/RTMP server | MIT | https://github.com/bluenviron/mediamtx |
| Wowza (trial) | — | — | Streaming media server | Proprietary | — |
| Shaka Player | JavaScript | 7k+ | Google's adaptive media player | Apache-2.0 | https://github.com/shaka-project/shaka-player |
| hls.js | JavaScript | 15k+ | HLS stream player for HTML5 | Apache-2.0 | https://github.com/video-dev/hls.js |
| Video.js | JavaScript | 37k+ | Open-source HTML5 video player | Apache-2.0 | https://github.com/videojs/video.js |
| Plyr | JavaScript | 26k+ | Simple, accessible media player | MIT | https://github.com/sampotts/plyr |
| dash.js | JavaScript | 5k+ | MPEG-DASH streaming reference client | BSD-3 | https://github.com/Dash-Industry-Forum/dash.js |
| ImageMagick | C | 7k+ | Image manipulation suite | Apache-2.0 | https://github.com/ImageMagick/ImageMagick |
| GraphicsMagick | C | 1k+ | Image processing system | MIT | https://sourceforge.net/projects/graphicsmagick/ |
| libvips | C | 9k+ | Fast image processing library | LGPL-2.1 | https://github.com/libvips/libvips |
| Sharp | C++ | 28k+ | Node.js image processing (libvips-based) | Apache-2.0 | https://github.com/lovell/sharp |
| Pillow | Python | 12k+ | Python imaging library | HPND | — |
| Inkscape | C++ | 4k+ | Open-source vector graphics editor | GPL-2.0 | https://gitlab.com/inkscape/inkscape |
| GIMP | C | 5k+ | GNU Image Manipulation Program | GPL-3.0 | https://gitlab.gnome.org/GNOME/gimp |
| Krita | C++ | 7k+ | Open-source professional painting app | GPL-3.0 | https://invent.kde.org/graphics/krita |
| RawTherapee | C++ | 3k+ | Raw image processing tool | GPL-3.0 | https://github.com/Beep6581/RawTherapee |
| darktable | C | 10k+ | Photographer's workflow app | GPL-3.0 | https://github.com/darktable-org/darktable |

---

## 46. Documentation & Knowledge Base

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Docusaurus | TypeScript | 57k+ | Meta's documentation framework | MIT | https://github.com/facebook/docusaurus |
| MkDocs | Python | 19k+ | Project documentation tool | BSD-2 | https://github.com/mkdocs/mkdocs |
| VitePress | TypeScript | 14k+ | Vite-powered static site docs | MIT | https://github.com/vuejs/vitepress |
| GitBook (OSS) | JavaScript | 2k+ | Modern documentation platform | Apache-2.0 | https://github.com/GitbookIO/gitbook |
| Confluence (OSS alt) | — | — | Team docs (many OSS alternatives) | Proprietary | — |
| Wiki.js | JavaScript | 24k+ | Modern, powerful wiki platform | AGPL-3.0 | https://github.com/requarks/wiki |
| BookStack | PHP | 15k+ | Simple, self-hosted wiki | MIT | https://github.com/BookStackApp/BookStack |
| Outline | TypeScript | 28k+ | Team knowledge base (Notion-like) | BSL-1.1 | https://github.com/outline/outline |
| Notion (OSS alt) | — | — | Notion alternatives | Various | — |
| AppFlowy | Rust | 60k+ | Notion alternative (self-hosted) | AGPL-3.0 | https://github.com/AppFlowy-IO/AppFlowy |
| AFFiNE | TypeScript | 45k+ | Notion/Miro alternative | MIT | https://github.com/toeverything/AFFiNE |
| Obsidian (free) | TypeScript | 11k+ | Markdown knowledge management | Proprietary | — |
| Logseq | Clojure | 31k+ | Open-source graph outliner | AGPL-3.0 | https://github.com/logseq/logseq |
| Joplin | TypeScript | 46k+ | Open-source note-taking app | AGPL-3.0 | https://github.com/laurent22/joplin |
| Standard Notes | TypeScript | 5k+ | End-to-end encrypted notes | AGPL-3.0 | https://github.com/standardnotes/app |
| Notable | TypeScript | 22k+ | Markdown note-taking app | AGPL-3.0 | — |
| Silverbullet | TypeScript | 4k+ | Markdown-based knowledge platform | MIT | https://github.com/silverbulletmd/silverbullet |
| Foam | TypeScript | 14k+ | VS Code Roam Research alternative | MIT | https://github.com/foambubble/foam |
| Zettlr | TypeScript | 10k+ | Academic Markdown editor | GPL-3.0 | https://github.com/Zettlr/Zettlr |
| Pandoc | Haskell | 33k+ | Universal document format converter | GPL-3.0 | — |
| Asciidoctor | Ruby | 4k+ | AsciiDoc processor | MIT | https://github.com/asciidoctor/asciidoctor |
| Sphinx | Python | 6k+ | Python documentation generator | BSD-2 | https://github.com/sphinx-doc/sphinx |
| pdoc | Python | 2k+ | Auto API docs from Python source | MIT | https://github.com/mitmproxy/pdoc |
| Swagger UI | JavaScript | 26k+ | OpenAPI/Swagger visualization | Apache-2.0 | https://github.com/swagger-api/swagger-ui |
| Redoc | TypeScript | 23k+ | OpenAPI docs generator | MIT | https://github.com/Redocly/redoc |
| Stoplight Elements | TypeScript | 1k+ | API reference docs component | Apache-2.0 | https://github.com/stoplightio/elements |
| Scalar | TypeScript | 6k+ | Beautiful API reference docs | MIT | https://github.com/scalar/scalar |
| ReadTheDocs | Python | 9k+ | Open-source documentation hosting | MIT | https://github.com/readthedocs/readthedocs.org |
| Nextra | TypeScript | 12k+ | Next.js-based documentation theme | MIT | https://github.com/shuding/nextra |
| Starlight | TypeScript | 6k+ | Astro-powered documentation theme | MIT | https://github.com/withastro/starlight |
| Mintlify | TypeScript | — | Docs as code platform (free tier) | Proprietary | — |
| Hedgedoc | TypeScript | 5k+ | Real-time collaborative Markdown editor | AGPL-3.0 | https://github.com/hedgedoc/hedgedoc |
| Etherpad | JavaScript | 16k+ | Real-time collaborative text editor | Apache-2.0 | https://github.com/ether/etherpad-lite |
| CodiMD | TypeScript | 9k+ | Collaborative Markdown editor | AGPL-3.0 | https://github.com/hackmdio/codimd |
| Cryptpad | JavaScript | 5k+ | Encrypted collaborative office suite | AGPL-3.0 | https://github.com/cryptpad/cryptpad |
| OnlyOffice | C++ | 5k+ | Open-source office suite for web | AGPL-3.0 | https://github.com/ONLYOFFICE/DocumentServer |
| LibreOffice | C++ | 3k+ | Complete office productivity suite | MPL-2.0 | https://github.com/LibreOffice/core |
| Collabora Online | C++ | 1k+ | LibreOffice in the browser | MPL-2.0 | https://github.com/CollaboraOnline/online |

---

## 47. Project Management & Collaboration

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Plane | TypeScript | 29k+ | Open-source JIRA alternative | AGPL-3.0 | https://github.com/makeplane/plane |
| Linear (OSS SDK) | TypeScript | — | Issue tracking (proprietary) | Proprietary | — |
| Taiga | Python | 3k+ | Agile project management | MPL-2.0 | https://github.com/kaleidos-ventures/taiga-back |
| OpenProject | Ruby | 9k+ | Open-source project management | GPL-3.0 | https://github.com/opf/openproject |
| GitLab Issues | Ruby | — | Built-in GitLab issue tracker | MIT | — |
| Gitea Issues | Go | — | Built-in Gitea issue tracker | MIT | — |
| Phabricator | PHP | 12k+ | Software development platform | Apache-2.0 | https://github.com/phacility/phabricator |
| Redmine | Ruby | 5k+ | Flexible project management | GPL-2.0 | https://github.com/redmine/redmine |
| Trac | Python | 1k+ | Wiki and issue tracker | BSD-3 | https://github.com/edgewall/trac |
| Maniphest | PHP | — | Task management (Phabricator module) | Apache-2.0 | — |
| YouTrack (free) | Java | — | JetBrains issue tracker (free tier) | Proprietary | — |
| Wekan | JavaScript | 19k+ | Open-source Kanban board | MIT | https://github.com/wekan/wekan |
| Focalboard | Go | 22k+ | Mattermost project management | MIT | https://github.com/mattermost/focalboard |
| Planka | JavaScript | 8k+ | Trello alternative self-hosted | AGPL-3.0 | https://github.com/plankanban/planka |
| Kanboard | PHP | 8k+ | Visual project management | MIT | https://github.com/kanboard/kanboard |
| Leantime | PHP | 4k+ | Lean project management for startups | AGPL-3.0 | https://github.com/Leantime/leantime |
| Vikunja | Go | 4k+ | Open-source to-do and project management | GPL-3.0 | https://github.com/go-vikunja/vikunja |
| Tasks.md | JavaScript | 1k+ | Markdown-based task management | MIT | https://github.com/BaldissaraMatheus/Tasks.md |
| Super Productivity | TypeScript | 10k+ | Todo app with Jira/GitHub integration | MIT | https://github.com/johannesjo/super-productivity |
| Habitica | JavaScript | 12k+ | Gamified habit tracker | GPL-3.0 | https://github.com/HabitRPG/habitica |
| Mattermost | Go | 30k+ | Slack alternative for teams | MIT | https://github.com/mattermost/mattermost |
| Rocket.Chat | TypeScript | 42k+ | Open platform for team communication | MIT | https://github.com/RocketChat/Rocket.Chat |
| Zulip | Python | 21k+ | Organized team chat | Apache-2.0 | https://github.com/zulip/zulip |
| Matrix/Element | Python/TypeScript | — | Federated team messaging | Apache-2.0 | — |
| Revolt | Rust | 2k+ | Open-source Discord alternative | AGPL-3.0 | https://github.com/revoltchat/revolt |
| Nextcloud Talk | PHP | 2k+ | Video calls in Nextcloud | AGPL-3.0 | — |
| Jitsi | JavaScript | 23k+ | Video conferencing platform | Apache-2.0 | — |
| libredesk | Go | 2.4k | Self-hosted customer support desk | MIT | https://github.com/abhinavxd/libredesk |
| flowctl | Go | 299 | Self-service workflow platform | MIT | https://github.com/zerodha/flowctl |

---

## 48. Finance & Payments

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| BTCPay Server | C# | 7k+ | Self-hosted Bitcoin payment processor | MIT | https://github.com/btcpayserver/btcpayserver |
| TigerBeetle | Zig | 9k+ | Distributed financial accounting database | Apache-2.0 | https://github.com/tigerbeetle/tigerbeetle |
| Akaunting | PHP | 8k+ | Open-source accounting for business | GPL-3.0 | https://github.com/akaunting/akaunting |
| Invoice Ninja | PHP | 8k+ | Open-source invoicing and payments | AAL | https://github.com/invoiceninja/invoiceninja |
| Crater | PHP | 8k+ | Invoice and expense management | AAL | https://github.com/crater-invoice/crater |
| Dolibarr | PHP | 5k+ | ERP & CRM for businesses | GPL-3.0 | https://github.com/Dolibarr/dolibarr |
| GNUCash | C | 5k+ | Personal and small business accounting | GPL-2.0 | https://github.com/Gnucash/gnucash |
| Ledger CLI | C++ | 5k+ | Double-entry accounting on CLI | BSD-3 | https://github.com/ledger/ledger |
| Beancount | Python | 4k+ | Plain text double-entry accounting | GPL-2.0 | https://github.com/beancount/beancount |
| hledger | Haskell | 3k+ | Plain text accounting tool | GPL-3.0 | https://github.com/simonmichael/hledger |
| Firefly III | PHP | 16k+ | Personal finance manager | AGPL-3.0 | https://github.com/firefly-iii/firefly-iii |
| Actual Budget | JavaScript | 13k+ | Local-first personal finance tool | MIT | https://github.com/actualbudget/actual |
| YNAB (OSS tools) | — | — | Budget management (proprietary) | Proprietary | — |
| Stripe SDK (OSS) | Various | — | Payment processing (proprietary backend) | MIT | — |
| Braintree SDK (OSS) | Various | — | Payment gateway SDK | MIT | — |
| Adyen SDK (OSS) | Various | — | Payment platform SDK | MIT | — |
| Razorpay SDK (OSS) | Various | — | India payment gateway SDK | MIT | — |
| Cashfree SDK (OSS) | Various | — | India payment gateway SDK | MIT | — |
| SigNoz | Go/Python | 19k+ | Full-stack APM for financial apps | Apache-2.0 | — |
| QuantLib | C++ | 5k+ | Quantitative finance library | BSD-3 | https://github.com/lballabio/QuantLib |
| zipline | Python | 17k+ | Backtesting library for Zipline/Quantopian | Apache-2.0 | https://github.com/quantopian/zipline |
| backtrader | Python | 13k+ | Python backtesting and trading | GPL-3.0 | https://github.com/mementum/backtrader |
| pyalgotrade | Python | 4k+ | Algorithmic trading library | Apache-2.0 | https://github.com/gbeced/pyalgotrade |
| ccxt | JavaScript | 32k+ | Cryptocurrency trading library | MIT | https://github.com/ccxt/ccxt |
| freqtrade | Python | 32k+ | Free crypto trading bot | GPL-3.0 | https://github.com/freqtrade/freqtrade |
| Jesse | Python | 6k+ | Advanced crypto trading framework | MIT | https://github.com/jesse-ai/jesse |
| Hummingbot | Python | 8k+ | Crypto market-making bot | Apache-2.0 | https://github.com/hummingbot/hummingbot |
| Vnpy | Python | 26k+ | Quantitative trading system | MIT | https://github.com/vnpy/vnpy |
| OpenBB Terminal | Python | 31k+ | Investment research platform | MIT | https://github.com/OpenBB-finance/OpenBB |
| rbiparser | Python | 63 | Parse RBI bank database (IFSC/MICR) | MIT | https://github.com/zerodha/rbiparser |

---

## 49. Analytics & Product Tracking

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Plausible | Elixir | 21k+ | Privacy-friendly Google Analytics alt | AGPL-3.0 | https://github.com/plausible/analytics |
| Umami | TypeScript | 22k+ | Self-hosted privacy analytics | MIT | https://github.com/umami-software/umami |
| Matomo | PHP | 20k+ | Open-source web analytics | GPL-3.0 | https://github.com/matomo-org/matomo |
| PostHog | Python/TypeScript | 23k+ | Open-source product analytics | MIT | https://github.com/PostHog/posthog |
| Countly CE | JavaScript | 5k+ | Product analytics and marketing | AGPL-3.0 | https://github.com/Countly/countly-server |
| Ackee | JavaScript | 4k+ | Self-hosted, privacy-focused analytics | MIT | https://github.com/electerious/Ackee |
| Shynet | Python | 3k+ | Privacy-focused analytics (no JS needed) | Apache-2.0 | https://github.com/milesmcc/shynet |
| GoatCounter | Go | 4k+ | Privacy-friendly web analytics | EUPL-1.2 | https://github.com/arp242/goatcounter |
| Metabase | Clojure | 39k+ | BI tool with usage analytics | AGPL-3.0 | https://github.com/metabase/metabase |
| Redash | Python | 26k+ | Query and visualize your data | BSD-2 | https://github.com/getredash/redash |
| GrowthBook | TypeScript | 6k+ | Open-source feature flags and A/B testing | MIT | https://github.com/growthbook/growthbook |
| Flagsmith | Python | 4k+ | Feature flags and remote config | BSD-3 | https://github.com/Flagsmith/flagsmith |
| Unleash | TypeScript | 10k+ | Open-source feature management | Apache-2.0 | https://github.com/Unleash/unleash |
| OpenFeature | Various | 1k+ | Open standard for feature flags | Apache-2.0 | https://github.com/open-feature/spec |
| Flipt | Go | 4k+ | Self-hosted feature flag service | GPL-3.0 | https://github.com/flipt-io/flipt |
| Optimizely (OSS SDK) | Various | — | A/B testing (proprietary backend) | Apache-2.0 | — |
| Snowplow | Scala | 7k+ | Open-source behavioral data platform | Apache-2.0 | https://github.com/snowplow/snowplow |
| Segment (analytics.js) | JavaScript | 6k+ | Analytics.js (open-source client) | MIT | — |
| Rudderstack | Go | 4k+ | Customer data platform (CDI) | SSPL/MIT | https://github.com/rudderlabs/rudder-server |
| Jitsu | Go | 4k+ | Open-source Segment alternative | MIT | https://github.com/jitsucom/jitsu |
| OpenMeter | Go | 2k+ | Usage metering for SaaS | Apache-2.0 | https://github.com/openmeterco/openmeter |
| Lago | Ruby | 7k+ | Open-source usage-based billing | AGPL-3.0 | https://github.com/getlago/lago |
| Stigg | TypeScript | — | Entitlement management (free tier) | Proprietary | — |

---

## 50. Testing & QA

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Pytest | Python | 12k+ | Python testing framework | MIT | https://github.com/pytest-dev/pytest |
| unittest | Python | — | Python built-in testing | PSF | — |
| Hypothesis | Python | 7k+ | Property-based testing for Python | MPL-2.0 | https://github.com/HypothesisWorks/hypothesis |
| Tavern | Python | 2k+ | API integration testing | MIT | https://github.com/taverntesting/tavern |
| Robot Framework | Python | 9k+ | Generic automation and testing | Apache-2.0 | https://github.com/robotframework/robotframework |
| Behave | Python | 3k+ | BDD testing for Python | BSD-3 | https://github.com/behave/behave |
| Cucumber | Java/Ruby | 3k+ | BDD testing framework | MIT | https://github.com/cucumber/cucumber |
| JUnit 5 | Java | 6k+ | Java unit testing framework | EPL-2.0 | https://github.com/junit-team/junit5 |
| TestNG | Java | 2k+ | Testing framework inspired by JUnit | Apache-2.0 | https://github.com/testng-team/testng |
| Mockito | Java | 14k+ | Mocking framework for Java | MIT | https://github.com/mockito/mockito |
| WireMock | Java | 6k+ | API mocking server | Apache-2.0 | https://github.com/wiremock/wiremock |
| Pact | Various | 4k+ | Consumer-driven contract testing | MIT | https://github.com/pact-foundation/pact-specification |
| Jest | JavaScript | 44k+ | JavaScript testing framework by Meta | MIT | https://github.com/jestjs/jest |
| Vitest | TypeScript | 14k+ | Vite-native fast unit testing | MIT | https://github.com/vitest-dev/vitest |
| Mocha | JavaScript | 22k+ | Feature-rich JavaScript test framework | MIT | https://github.com/mochajs/mocha |
| Chai | JavaScript | 8k+ | Assertion library for Node.js | MIT | https://github.com/chaijs/chai |
| Cypress | JavaScript | 47k+ | E2E testing for web apps | MIT | https://github.com/cypress-io/cypress |
| Playwright | TypeScript | 67k+ | Cross-browser testing by Microsoft | Apache-2.0 | https://github.com/microsoft/playwright |
| Selenium | Java | 30k+ | Browser automation framework | Apache-2.0 | https://github.com/SeleniumHQ/selenium |
| WebdriverIO | JavaScript | 9k+ | Next-gen browser/mobile automation | MIT | https://github.com/webdriverio/webdriverio |
| Puppeteer | TypeScript | 89k+ | Headless Chrome Node.js API | Apache-2.0 | https://github.com/puppeteer/puppeteer |
| Capybara | Ruby | 10k+ | Web app acceptance testing for Ruby | MIT | https://github.com/teamcapybara/capybara |
| Watir | Ruby | 1k+ | Web application testing for Ruby | MIT | https://github.com/watir/watir |
| RSpec | Ruby | 3k+ | Behavior-driven testing for Ruby | MIT | https://github.com/rspec/rspec |
| MiniTest | Ruby | 1k+ | Ruby's built-in test suite | MIT | — |
| Go testing | Go | — | Go standard library testing | BSD-3 | — |
| testify | Go | 23k+ | Test toolkit for Go | MIT | https://github.com/stretchr/testify |
| ginkgo | Go | 8k+ | Expressive BDD testing for Go | MIT | https://github.com/onsi/ginkgo |
| gomock | Go | 2k+ | Mocking framework for Go | Apache-2.0 | https://github.com/uber-go/mock |
| httptest | Go | — | Go HTTP testing utilities | BSD-3 | — |
| k6 | Go | 26k+ | Performance/load testing tool | AGPL-3.0 | https://github.com/grafana/k6 |
| Locust | Python | 24k+ | Scalable load testing in Python | MIT | — |
| Gatling | Scala | 6k+ | Load testing for web apps | Apache-2.0 | https://github.com/gatling/gatling |
| JMeter | Java | 8k+ | Load and performance testing | Apache-2.0 | https://github.com/apache/jmeter |
| Artillery | JavaScript | 8k+ | Modern load and smoke testing | MPL-2.0 | https://github.com/artilleryio/artillery |
| wrk | C | 36k+ | HTTP benchmarking tool | Apache-2.0 | https://github.com/wg/wrk |
| hey | Go | 17k+ | HTTP load generator | Apache-2.0 | https://github.com/rakyll/hey |
| vegeta | Go | 24k+ | HTTP load testing toolkit | MIT | https://github.com/tsenart/vegeta |
| Chaos Monkey | Java | 3k+ | Resilience testing by Netflix | Apache-2.0 | https://github.com/Netflix/chaosmonkey |
| toxiproxy | Go | 11k+ | TCP proxy for chaos engineering | MIT | https://github.com/Shopify/toxiproxy |
| Pumba | Go | 3k+ | Chaos testing for Docker | MIT | https://github.com/alexei-led/pumba |
| Litmus | Go | 4k+ | Kubernetes chaos engineering | Apache-2.0 | https://github.com/litmuschaos/litmus |
| Chaos Mesh | Go | 6k+ | Cloud-native chaos engineering | Apache-2.0 | https://github.com/chaos-mesh/chaos-mesh |
| PowerfulSeal | Python | 2k+ | Kubernetes testing framework | Apache-2.0 | https://github.com/powerfulseal/powerfulseal |
| Dredd | JavaScript | 4k+ | HTTP API testing framework | MIT | https://github.com/apiaryio/dredd |
| Hoverfly | Go | 2k+ | API simulation and testing | Apache-2.0 | https://github.com/SpectoLabs/hoverfly |
| Pact | Various | 4k+ | Consumer-driven contract testing | MIT | https://github.com/pact-foundation/pact-specification |
| Postman (OSS tests) | JavaScript | — | API testing platform (free tier) | Proprietary | — |
| Bruno | JavaScript | 26k+ | Open-source API client (Postman alt.) | MIT | https://github.com/usebruno/bruno |
| Hoppscotch | TypeScript | 66k+ | Open-source API development ecosystem | MIT | https://github.com/hoppscotch/hoppscotch |
| Insomnia (OSS) | TypeScript | 34k+ | API design and testing platform | Apache-2.0 | https://github.com/Kong/insomnia |
| Thunder Client | TypeScript | 5k+ | VS Code extension for REST APIs | MIT | — |
| Rest Client | TypeScript | 5k+ | VS Code REST client extension | MIT | — |
| HTTPie Desktop | Python | — | HTTP client (desktop + open-source CLI) | BSD-3 | — |
| autopilot (Flutter) | Dart | 127 | Flutter QA test driver | MIT | — |

---

## 51. Go Libraries

| Project | Stars | Description | License | Link |
|---------|-------|-------------|---------|---------|
| koanf | 3.9k | Lightweight extensible configuration | MIT | https://github.com/knadh/koanf |
| Viper | 26k+ | Complete Go configuration solution | MIT | https://github.com/spf13/viper |
| cobra | 37k+ | CLI application framework for Go | Apache-2.0 | https://github.com/spf13/cobra |
| urfave/cli | 21k+ | Simple CLI app framework | MIT | https://github.com/urfave/cli |
| pflag | 2k+ | Drop-in replacement for Go's flag package | BSD-3 | https://github.com/spf13/pflag |
| zerolog | 10k+ | Zero allocation JSON logger | MIT | https://github.com/rs/zerolog |
| zap | 22k+ | Blazing fast structured logger | MIT | https://github.com/uber-go/zap |
| logrus | 24k+ | Structured pluggable logger | MIT | https://github.com/sirupsen/logrus |
| slog | — | Standard library structured logger | BSD-3 | — |
| testify | 23k+ | Testing toolkit | MIT | https://github.com/stretchr/testify |
| ginkgo | 8k+ | BDD testing framework | MIT | https://github.com/onsi/ginkgo |
| gomock | 2k+ | Mocking framework | Apache-2.0 | https://github.com/uber-go/mock |
| go-sqlmock | 6k+ | SQL mock library for testing | MIT | https://github.com/DATA-DOG/go-sqlmock |
| httptest | — | HTTP testing utilities | BSD-3 | — |
| Gin | 78k+ | HTTP web framework | MIT | https://github.com/gin-gonic/gin |
| Echo | 29k+ | High-performance web framework | MIT | https://github.com/labstack/echo |
| Fiber | 34k+ | Express-inspired framework | MIT | https://github.com/gofiber/fiber |
| Chi | 18k+ | Lightweight composable router | MIT | https://github.com/go-chi/chi |
| fasthttp | 21k+ | Fast alternative to net/http | MIT | https://github.com/valyala/fasthttp |
| fastglue | 91 | Micro HTTP framework wrapping fasthttp | MIT | https://github.com/zerodha/fastglue |
| GORM | 37k+ | ORM library | MIT | https://github.com/go-gorm/gorm |
| sqlx | 15k+ | Extensions for database/sql | MIT | https://github.com/jmoiron/sqlx |
| ent | 15k+ | Entity framework | Apache-2.0 | https://github.com/ent/ent |
| goyesql | 72 | Parse named SQL queries | MIT | https://github.com/knadh/goyesql |
| squirrel | 7k+ | Fluent SQL query builder | MIT | https://github.com/Masterminds/squirrel |
| bun | 3k+ | SQL-first Golang ORM | MIT | https://github.com/uptrace/bun |
| pgx | 11k+ | PostgreSQL driver and toolkit | MIT | https://github.com/jackc/pgx |
| go-redis | 20k+ | Type-safe Redis client | BSD-2 | https://github.com/redis/go-redis |
| mongo-driver | 8k+ | Official MongoDB Go driver | Apache-2.0 | https://github.com/mongodb/mongo-go-driver |
| asynq | 10k+ | Async task queue using Redis | MIT | — |
| Tasqueue | 462 | Background job library | MIT | https://github.com/knadh/tasqueue |
| river | 3k+ | Postgres-backed job queue | MIT | — |
| machinery | 7k+ | Async task/job queue | MIT | — |
| cron | 5k+ | Cron library for Go | MIT | https://github.com/robfig/cron |
| robfig/cron | 13k+ | Cron parser and scheduler | MIT | https://github.com/robfig/cron |
| simplesessions | 80 | Session management library | MIT | https://github.com/vividvilla/simplesessions |
| jwt-go | 7k+ | JWT implementation for Go | MIT | https://github.com/golang-jwt/jwt |
| casbin | 17k+ | Authorization framework | Apache-2.0 | — |
| crypto | — | Go standard cryptography packages | BSD-3 | — |
| gorilla/websocket | 22k+ | WebSocket implementation | BSD-2 | https://github.com/gorilla/websocket |
| nhooyr/websocket | 5k+ | Minimal WebSocket library | MIT | https://github.com/coder/websocket |
| graphql-go | 9k+ | GraphQL for Go | BSD-2 | https://github.com/graphql-go/graphql |
| gqlgen | 9k+ | Go generate-based GraphQL server | MIT | https://github.com/99designs/gqlgen |
| protobuf (Go) | 5k+ | Protocol Buffers for Go | BSD-3 | — |
| grpc-go | 21k+ | gRPC for Go | Apache-2.0 | https://github.com/grpc/grpc-go |
| connect-go | 3k+ | gRPC-compatible HTTP API library | Apache-2.0 | https://github.com/connectrpc/connect-go |
| tonic | — | (Rust) gRPC implementation | MIT/Apache-2.0 | https://github.com/hyperium/tonic |
| validator | 17k+ | Value validation for Go structs | MIT | https://github.com/go-playground/validator |
| mapstructure | 7k+ | Decode generic map to Go struct | MIT | https://github.com/mitchellh/mapstructure |
| copier | 5k+ | Copy values between structs | MIT | https://github.com/jinzhu/copier |
| lo | 17k+ | Lodash-like library for Go | MIT | https://github.com/samber/lo |
| samber/lo | 17k+ | Generic utility functions for Go | MIT | https://github.com/samber/lo |
| fx | 5k+ | Dependency injection for Go | MIT | https://github.com/uber-go/fx |
| wire | 12k+ | Dependency injection code generation | Apache-2.0 | https://github.com/google/wire |
| dig | 3k+ | DI container library | MIT | https://github.com/uber-go/dig |
| errgroup | — | Error propagation for goroutines | BSD-3 | — |
| multierr | 2k+ | Multi-error propagation library | MIT | https://github.com/uber-go/multierr |
| pkg/errors | 8k+ | Error handling with stack traces | BSD-2 | https://github.com/pkg/errors |
| go-playground/errors | — | Errors with stack traces | MIT | — |
| retry-go | 2k+ | Simple retry library | MIT | — |
| backoff | 2k+ | Exponential backoff for Go | MIT | https://github.com/cenkalti/backoff |
| sync | — | Go sync primitives | BSD-3 | — |
| ratelimit | 5k+ | Leaky bucket rate limiter | MIT | — |
| golang-lru | 4k+ | LRU cache for Go | MPL-2.0 | https://github.com/hashicorp/golang-lru |
| ristretto | 5k+ | High-performance cache library | Apache-2.0 | — |
| bigcache | 7k+ | Efficient in-memory cache | Apache-2.0 | https://github.com/allegro/bigcache |
| uuid | 5k+ | UUID generation and parsing | MIT | https://github.com/google/uuid |
| ulid | 3k+ | Universally Unique Lexicographically Sortable ID | MIT | https://github.com/oklog/ulid |
| ksuid | 5k+ | K-Sortable Unique Identifier | MIT | https://github.com/segmentio/ksuid |
| gocsv | 2k+ | CSV serialization for Go structs | MIT | https://github.com/gocarina/gocsv |
| encoding/json | — | JSON encoding/decoding (stdlib) | BSD-3 | — |
| json-iterator | 13k+ | High-performance JSON for Go | MIT | https://github.com/json-iterator/go |
| sonic | 7k+ | Bytedance JSON library for Go | Apache-2.0 | https://github.com/bytedance/sonic |
| go-yaml | 7k+ | YAML support for Go | MIT | https://github.com/go-yaml/yaml |
| toml | 5k+ | TOML encoding for Go | MIT | https://github.com/BurntSushi/toml |
| envconfig | 5k+ | Map environment vars to struct | MIT | https://github.com/kelseyhightower/envconfig |
| godotenv | 8k+ | Load .env files in Go | MIT | https://github.com/joho/godotenv |
| lzo1z | 5 | Pure Go LZO1Z compression | MIT | https://github.com/zerodha/lzo1z |
| simples3 | 197 | Minimal S3 library | MIT | https://github.com/zerodha/simples3 |
| stuffbin | 200 | Compress+embed assets in binary | MIT | https://github.com/knadh/stuffbin |
| querytostruct | 22 | Unmarshal query strings to structs | MIT | https://github.com/zerodha/querytostruct |
| shelf | 40 | Symlinks manager | MIT | https://github.com/zerodha/shelf |
| simplehealth | 13 | Health-check endpoints | MIT | https://github.com/zerodha/simplehealth |
| nomctx | 58 | Switch Nomad clusters/namespaces | MIT | https://github.com/zerodha/nomctx |
| kubekutr | 162 | K8s manifest templating | MIT | https://github.com/zerodha/kubekutr |
| consul-cfg | 17 | TOML/JSON/YAML to Consul KV | MIT | https://github.com/zerodha/consul-cfg |

---

## 52. Python Libraries

| Project | Stars | Description | License | Link |
|---------|-------|-------------|---------|---------|
| requests | 52k+ | HTTP for Humans | Apache-2.0 | https://github.com/psf/requests |
| httpx | 13k+ | Next-gen HTTP client for Python | BSD-3 | https://github.com/encode/httpx |
| aiohttp | 15k+ | Async HTTP client/server | Apache-2.0 | https://github.com/aio-libs/aiohttp |
| urllib3 | 4k+ | Powerful HTTP client | MIT | https://github.com/urllib3/urllib3 |
| pydantic | 21k+ | Data validation using Python type hints | MIT | https://github.com/pydantic/pydantic |
| attrs | 5k+ | Python class decorator library | MIT | https://github.com/python-attrs/attrs |
| dataclasses | — | Built-in Python dataclasses | PSF | — |
| marshmallow | 7k+ | ORM-agnostic serialization | MIT | https://github.com/marshmallow-code/marshmallow |
| SQLAlchemy | 9k+ | SQL toolkit and ORM | MIT | https://github.com/sqlalchemy/sqlalchemy |
| Alembic | 2k+ | Database migration tool | MIT | https://github.com/sqlalchemy/alembic |
| psycopg2 | 3k+ | PostgreSQL adapter for Python | LGPL-3.0 | https://github.com/psycopg/psycopg2 |
| asyncpg | 7k+ | Async PostgreSQL driver | Apache-2.0 | https://github.com/MagicStack/asyncpg |
| aiomysql | 2k+ | Async MySQL driver | MIT | https://github.com/aio-libs/aiomysql |
| pymongo | 4k+ | Official MongoDB Python driver | Apache-2.0 | https://github.com/mongodb/mongo-python-driver |
| motor | 2k+ | Async MongoDB driver | Apache-2.0 | https://github.com/mongodb/motor |
| redis-py | 12k+ | Redis Python client | MIT | https://github.com/redis/redis-py |
| celery | 24k+ | Distributed task queue | BSD-3 | — |
| dramatiq | 4k+ | Background task processing | LGPL-3.0 | — |
| rq | 10k+ | Redis Queue for Python | BSD-2 | — |
| fastapi | 79k+ | Fast API framework | MIT | — |
| flask | 68k+ | Micro web framework | BSD-3 | — |
| django | 80k+ | Full-stack web framework | BSD-3 | — |
| starlette | 10k+ | ASGI framework/toolkit | BSD-3 | — |
| uvicorn | 8k+ | ASGI server for Python | BSD-3 | https://github.com/encode/uvicorn |
| gunicorn | 9k+ | Python WSGI HTTP server | MIT | https://github.com/benoitc/gunicorn |
| pytest | 12k+ | Testing framework | MIT | — |
| hypothesis | 7k+ | Property-based testing | MPL-2.0 | — |
| faker | 17k+ | Fake data generation | MIT | https://github.com/joke2k/faker |
| factory_boy | 3k+ | Test fixtures for Python | MIT | https://github.com/FactoryBoy/factory_boy |
| Pydantic v2 | 21k+ | Fast data validation | MIT | — |
| typer | 16k+ | CLI apps with type hints | MIT | https://github.com/fastapi/typer |
| click | 15k+ | CLI creation kit | BSD-3 | https://github.com/pallets/click |
| argparse | — | Python CLI argument parsing (stdlib) | PSF | — |
| rich | 49k+ | Beautiful terminal output | MIT | https://github.com/Textualize/rich |
| tqdm | 28k+ | Progress bars for Python | MIT | https://github.com/tqdm/tqdm |
| loguru | 19k+ | Better logging for Python | MIT | https://github.com/Delgan/loguru |
| structlog | 3k+ | Structured logging | MIT/Apache | https://github.com/hynek/structlog |
| boto3 | 9k+ | AWS SDK for Python | Apache-2.0 | https://github.com/boto/boto3 |
| google-cloud-python | 7k+ | GCP Python SDK | Apache-2.0 | https://github.com/googleapis/google-cloud-python |
| azure-sdk-for-python | 4k+ | Azure SDK for Python | MIT | https://github.com/Azure/azure-sdk-for-python |
| paramiko | 9k+ | SSH2 protocol library | LGPL-2.1 | https://github.com/paramiko/paramiko |
| fabric | 15k+ | Streamlined SSH for deployment | BSD-2 | https://github.com/fabric/fabric |
| ansible | 63k+ | IT automation (Python) | GPL-3.0 | — |
| cryptography | 6k+ | Cryptographic library for Python | Apache-2.0/BSD | https://github.com/pyca/cryptography |
| pyOpenSSL | 1k+ | Python bindings for OpenSSL | Apache-2.0 | https://github.com/pyca/pyopenssl |
| jwt | 5k+ | JSON Web Tokens in Python | MIT | — |
| python-jose | 1k+ | JOSE library for Python | MIT | https://github.com/mpdavis/python-jose |
| passlib | 2k+ | Password hashing library | BSD-2 | https://github.com/glic3rinu/passlib |
| bcrypt | 2k+ | bcrypt hashing for Python | Apache-2.0 | https://github.com/pyca/bcrypt |
| arrow | 8k+ | Better date and time for Python | Apache-2.0 | https://github.com/arrow-py/arrow |
| pendulum | 6k+ | Python datetimes made easy | MIT | https://github.com/sdispater/pendulum |
| dateutil | 2k+ | Extensions to Python datetime | Apache-2.0 | https://github.com/dateutil/dateutil |
| pytz | 2k+ | Timezone library for Python | MIT | https://github.com/stub42/pytz |
| schedule | 12k+ | Job scheduling for Python | MIT | https://github.com/dbader/schedule |
| apscheduler | 6k+ | Advanced Python Scheduler | MIT | https://github.com/agronholm/apscheduler |
| celery beat | — | Periodic task scheduler for Celery | BSD-3 | — |
| pillow | 12k+ | Python imaging library | HPND | — |
| numpy | 28k+ | N-dimensional arrays | BSD-3 | — |
| pandas | 43k+ | Data analysis library | BSD-3 | https://github.com/pandas-dev/pandas |
| polars | 30k+ | Lightning DataFrames in Rust | MIT | — |
| scipy | 13k+ | Scientific computing | BSD-3 | — |
| matplotlib | 20k+ | 2D plotting library | PSF | — |
| seaborn | 12k+ | Statistical visualization | BSD-3 | — |
| plotly | 16k+ | Interactive graphing | MIT | — |
| bokeh | 19k+ | Interactive visualization | BSD-3 | — |
| altair | 9k+ | Declarative visualization | BSD-3 | — |
| streamlit | 36k+ | Web apps for data science | Apache-2.0 | — |
| dash | 21k+ | Analytical web apps | MIT | — |
| scikit-learn | 59k+ | ML for Python | BSD-3 | https://github.com/scikit-learn/scikit-learn |
| xgboost | 26k+ | Gradient boosting | Apache-2.0 | — |
| lightgbm | 16k+ | Fast gradient boosting | MIT | — |
| catboost | 8k+ | Gradient boosting by Yandex | Apache-2.0 | — |
| transformers | 136k+ | Pre-trained models | Apache-2.0 | — |
| torch | 85k+ | PyTorch for Python | BSD-3 | — |
| tensorflow | 186k+ | TensorFlow for Python | Apache-2.0 | — |
| jax | 30k+ | Autograd + XLA | Apache-2.0 | — |
| langchain | 97k+ | LLM application framework | MIT | — |
| llama-index | 38k+ | LLM data framework | MIT | — |
| openai | 23k+ | OpenAI Python SDK | MIT | https://github.com/openai/openai-python |
| anthropic | 5k+ | Anthropic Python SDK | MIT | https://github.com/anthropics/anthropic-sdk-python |
| rbiparser | 63 | Parse RBI bank database | MIT | https://github.com/zerodha/rbiparser |
| csvtotable | 1.2k | CSV to HTML table | MIT | https://github.com/vividvilla/csvtotable |

---

## 53. Rust Libraries

| Project | Stars | Description | License | Link |
|---------|-------|-------------|---------|---------|
| serde | 9k+ | Serialization framework | MIT/Apache-2.0 | https://github.com/serde-rs/serde |
| serde_json | 5k+ | JSON serialization | MIT/Apache-2.0 | https://github.com/serde-rs/json |
| tokio | 27k+ | Async runtime for Rust | MIT | https://github.com/tokio-rs/tokio |
| async-std | 3k+ | Async version of standard library | Apache-2.0/MIT | https://github.com/async-rs/async-std |
| rayon | 11k+ | Data parallelism library | MIT/Apache-2.0 | https://github.com/rayon-rs/rayon |
| crossbeam | 8k+ | Concurrent data structures | MIT/Apache-2.0 | https://github.com/crossbeam-rs/crossbeam |
| reqwest | 10k+ | HTTP client library | MIT/Apache-2.0 | https://github.com/seanmonstar/reqwest |
| hyper | 14k+ | Fast HTTP for Rust | MIT | https://github.com/hyperium/hyper |
| actix-web | 22k+ | Web framework | MIT/Apache-2.0 | — |
| axum | 21k+ | Web application framework | MIT | — |
| rocket | 24k+ | Web framework | MIT/Apache-2.0 | — |
| warp | 9k+ | Composable web server | MIT | — |
| sqlx | 13k+ | Async database library | MIT/Apache-2.0 | https://github.com/jmoiron/sqlx |
| diesel | 12k+ | ORM for Rust | MIT/Apache-2.0 | https://github.com/diesel-rs/diesel |
| sea-orm | 7k+ | Async ORM for Rust | MIT/Apache-2.0 | https://github.com/SeaQL/sea-orm |
| deadpool | 1k+ | Async connection pool | MIT/Apache-2.0 | https://github.com/bikeshedder/deadpool |
| redis-rs | 4k+ | Redis client for Rust | MIT | https://github.com/redis-rs/redis-rs |
| mongodb (Rust) | 1k+ | MongoDB driver for Rust | Apache-2.0 | https://github.com/mongodb/mongo-rust-driver |
| clap | 14k+ | CLI argument parsing | MIT/Apache-2.0 | https://github.com/clap-rs/clap |
| anyhow | 9k+ | Error handling | MIT/Apache-2.0 | https://github.com/dtolnay/anyhow |
| thiserror | 6k+ | Error derive macro | MIT/Apache-2.0 | https://github.com/dtolnay/thiserror |
| tracing | 5k+ | Application-level tracing | MIT | https://github.com/tokio-rs/tracing |
| log | 2k+ | Logging facade | MIT/Apache-2.0 | https://github.com/rust-lang/log |
| env_logger | 1k+ | Env-variable-based logging | MIT/Apache-2.0 | https://github.com/rust-cli/env_logger |
| chrono | 3k+ | Date and time library | MIT/Apache-2.0 | https://github.com/chronotope/chrono |
| uuid | 2k+ | UUID generation | MIT/Apache-2.0 | https://github.com/google/uuid |
| rand | 2k+ | Random number generation | MIT/Apache-2.0 | https://github.com/rust-random/rand |
| regex | 3k+ | Regular expressions | MIT/Apache-2.0 | https://github.com/rust-lang/regex |
| nom | 9k+ | Parser combinators | MIT | https://github.com/rust-bakery/nom |
| pest | 4k+ | PEG parser generator | MIT/Apache-2.0 | https://github.com/pest-parser/pest |
| chumsky | 4k+ | Parser library | MIT | https://github.com/zesterer/chumsky |
| hashbrown | 2k+ | High-performance hash maps | MIT/Apache-2.0 | https://github.com/rust-lang/hashbrown |
| indexmap | 2k+ | Hash table preserving insertion order | MIT/Apache-2.0 | https://github.com/indexmap-rs/indexmap |
| dashmap | 3k+ | Concurrent hash map | MIT | https://github.com/xacrimon/dashmap |
| once_cell | 2k+ | Single-assignment cells | MIT/Apache-2.0 | https://github.com/matklad/once_cell |
| lazy_static | 2k+ | Macro for lazy statics | MIT/Apache-2.0 | https://github.com/rust-lang-nursery/lazy-static.rs |
| bytemuck | 1k+ | Cast bytes safely | MIT/Zlib/Apache-2.0 | https://github.com/Lokathor/bytemuck |
| bytes | 2k+ | Byte buffer manipulation | MIT | https://github.com/tokio-rs/bytes |
| itertools | 2k+ | Iterator utility functions | MIT/Apache-2.0 | https://github.com/rust-itertools/itertools |
| futures | 5k+ | Async/await utilities | MIT/Apache-2.0 | https://github.com/rust-lang/futures-rs |
| pin-project | 1k+ | Pin projection for structs | MIT/Apache-2.0 | https://github.com/taiki-e/pin-project |
| tower | 3k+ | Modular, reusable networking services | MIT | https://github.com/tower-rs/tower |
| tonic | 9k+ | gRPC implementation | MIT | https://github.com/hyperium/tonic |
| prost | 3k+ | Protocol Buffers for Rust | Apache-2.0 | https://github.com/tokio-rs/prost |
| jsonwebtoken | 1k+ | JWT creation/validation | MIT | https://github.com/Keats/jsonwebtoken |
| argon2 | 1k+ | Argon2 password hashing | MIT/Apache-2.0 | https://github.com/RustCrypto/password-hashes |
| bcrypt | 1k+ | bcrypt hashing | MIT | https://github.com/pyca/bcrypt |
| ring | 3k+ | Cryptographic operations | ISC-like | https://github.com/briansmith/ring |
| rustls | 5k+ | Modern TLS library | MIT/Apache-2.0 | https://github.com/rustls/rustls |
| native-tls | 500+ | TLS using OS native libs | MIT/Apache-2.0 | — |
| blobasaur | 43 | SQLite blob store with Redis protocol | MIT | https://github.com/zerodha/blobasaur |
| hedwig | 49 | Minimalist SMTP server | MIT | https://github.com/zerodha/hedwig |

---

## 54. JavaScript/TypeScript Libraries

| Project | Stars | Description | License | Link |
|---------|-------|-------------|---------|---------|
| lodash | 59k+ | Utility library for JS | MIT | https://github.com/lodash/lodash |
| ramda | 23k+ | Functional programming for JS | MIT | https://github.com/ramda/ramda |
| underscore | 27k+ | JS utility belt | MIT | https://github.com/jashkenas/underscore |
| date-fns | 34k+ | Modern date utility library | MIT | https://github.com/date-fns/date-fns |
| moment | 47k+ | Date/time library (deprecated) | MIT | https://github.com/moment/moment |
| dayjs | 46k+ | Immutable date library (moment alt.) | MIT | https://github.com/iamkun/dayjs |
| luxon | 15k+ | Dates and times for modern JS | MIT | https://github.com/moment/luxon |
| immer | 28k+ | Immutable state by mutation | MIT | https://github.com/immerjs/immer |
| immutable.js | 33k+ | Immutable data structures | MIT | https://github.com/immutable-js/immutable-js |
| rxjs | 30k+ | Reactive extensions for JS | Apache-2.0 | https://github.com/ReactiveX/rxjs |
| xstate | 27k+ | State machines and statecharts | MIT | https://github.com/statelyai/xstate |
| zustand | 48k+ | Minimal state management for React | MIT | https://github.com/pmndrs/zustand |
| jotai | 18k+ | Atomic state management for React | MIT | https://github.com/pmndrs/jotai |
| recoil | 19k+ | Experimental state management by Meta | MIT | https://github.com/facebookexperimental/Recoil |
| redux | 60k+ | Predictable state container | MIT | https://github.com/reduxjs/redux |
| mobx | 27k+ | Simple, scalable state management | MIT | https://github.com/mobxjs/mobx |
| pinia | 13k+ | Intuitive Vue store | MIT | https://github.com/vuejs/pinia |
| vuex | 28k+ | State management for Vue.js | MIT | https://github.com/vuejs/vuex |
| ngrx | 8k+ | State management for Angular | MIT | https://github.com/ngrx/platform |
| axios | 105k+ | Promise-based HTTP client | MIT | https://github.com/axios/axios |
| fetch (native) | — | Built-in browser/node fetch API | — | — |
| ky | 11k+ | Tiny HTTP client based on fetch | MIT | https://github.com/sindresorhus/ky |
| got | 14k+ | HTTP client for Node.js | MIT | https://github.com/sindresorhus/got |
| node-fetch | 8k+ | Node.js window.fetch | MIT | https://github.com/node-fetch/node-fetch |
| undici | 6k+ | HTTP/1.1 client for Node.js | MIT | https://github.com/nodejs/undici |
| zod | 33k+ | TypeScript schema validation | MIT | https://github.com/colinhacks/zod |
| yup | 21k+ | JS/TS schema validation | MIT | https://github.com/jquense/yup |
| joi | 20k+ | Schema validation for JS | BSD-3 | https://github.com/hapijs/joi |
| valibot | 6k+ | Modular schema validation | MIT | https://github.com/fabian-hiller/valibot |
| class-validator | 10k+ | Decorator-based validation | MIT | https://github.com/typestack/class-validator |
| superstruct | 7k+ | Simple and composable validation | MIT | https://github.com/ianstormtaylor/superstruct |
| socket.io | 61k+ | Real-time bidirectional event library | MIT | — |
| ws | 21k+ | Simple WebSocket for Node.js | MIT | https://github.com/websockets/ws |
| jsonwebtoken | 17k+ | JWT implementation | MIT | https://github.com/Keats/jsonwebtoken |
| passport | 22k+ | Authentication middleware for Node | MIT | https://github.com/jaredhanson/passport |
| express-session | 6k+ | Session middleware | MIT | https://github.com/expressjs/session |
| dotenv | 18k+ | Load environment variables | BSD-2 | https://github.com/motdotla/dotenv |
| cross-env | 9k+ | Cross-platform env vars | MIT | https://github.com/kentcdodds/cross-env |
| chalk | 21k+ | Terminal string styling | MIT | https://github.com/chalk/chalk |
| ora | 9k+ | Elegant terminal spinner | MIT | https://github.com/sindresorhus/ora |
| inquirer | 19k+ | Interactive CLI prompts | MIT | https://github.com/SBoudrias/Inquirer.js |
| commander | 26k+ | Node CLI framework | MIT | https://github.com/tj/commander.js |
| yargs | 11k+ | CLI argument parsing | MIT | https://github.com/yargs/yargs |
| sharp | 28k+ | High-performance image processing | Apache-2.0 | — |
| jimp | 13k+ | Image processing in pure JS | MIT | https://github.com/jimp-dev/jimp |
| uuid | 14k+ | UUID generation | MIT | https://github.com/google/uuid |
| nanoid | 23k+ | Tiny unique string ID generator | MIT | https://github.com/ai/nanoid |
| short-uuid | 2k+ | Short UUIDs | MIT | — |
| bull | 15k+ | Redis-backed job queue | MIT | — |
| bullmq | 6k+ | Next-gen job queue | MIT | — |
| node-cron | 6k+ | Cron for Node.js | ISC | — |
| agenda | 9k+ | Light-weight job scheduling | MIT | https://github.com/agenda/agenda |
| puppeteer | 89k+ | Headless Chrome automation | Apache-2.0 | — |
| playwright | 67k+ | Cross-browser automation | Apache-2.0 | — |
| cheerio | 28k+ | jQuery-style HTML parsing | MIT | https://github.com/cheeriojs/cheerio |
| jsdom | 20k+ | JS implementation of DOM | MIT | https://github.com/jsdom/jsdom |
| p-queue | 5k+ | Promise queue with concurrency | MIT | https://github.com/sindresorhus/p-queue |
| p-limit | 4k+ | Limit concurrent async operations | MIT | https://github.com/sindresorhus/p-limit |
| bottleneck | 2k+ | Async rate limiter | MIT | https://github.com/SGrondin/bottleneck |
| pino | 14k+ | Super fast logger for Node | MIT | https://github.com/pinojs/pino |
| winston | 22k+ | Multi-transport Node logger | MIT | https://github.com/winstonjs/winston |
| morgan | 8k+ | HTTP request logger middleware | MIT | https://github.com/expressjs/morgan |
| nodemailer | 16k+ | Email sending for Node | MIT | — |
| multer | 11k+ | Multipart/form-data middleware | MIT | https://github.com/expressjs/multer |
| formidable | 7k+ | Form parsing for Node.js | MIT | https://github.com/node-formidable/formidable |
| mongoose | 26k+ | MongoDB object modeling | MIT | https://github.com/Automattic/mongoose |
| typegoose | 4k+ | TypeScript-first Mongoose | MIT | https://github.com/typegoose/typegoose |
| knex | 19k+ | SQL query builder | MIT | https://github.com/knex/knex |
| objection | 7k+ | SQL ORM built on Knex | MIT | https://github.com/Vincit/objection.js |
| bookshelf | 6k+ | Node.js ORM for SQL | MIT | https://github.com/bookshelf/bookshelf |
| prisma | 40k+ | Next-gen ORM for Node | Apache-2.0 | https://github.com/prisma/prisma |
| drizzle | 24k+ | TypeScript ORM | Apache-2.0 | https://github.com/drizzle-team/drizzle-orm |
| kysely | 11k+ | Type-safe SQL query builder | MIT | https://github.com/kysely-org/kysely |
| sequelize | 29k+ | Multi-dialect SQL
 ORM | MIT |
| typeorm | 34k+ | ORM for TypeScript | MIT | https://github.com/typeorm/typeorm |
| mikro-orm | 8k+ | TypeScript ORM | MIT | https://github.com/mikro-orm/mikro-orm |
| trace-chart | 25 | Financial charting library | MIT | https://github.com/zerodha/trace-chart |
| indexed-cache | 127 | Sideload assets to IndexedDB | MIT | https://github.com/zerodha/indexed-cache |
| tagflow | 20 | HTML string to Flutter widgets | MIT | https://github.com/zerodha/tagflow |

---

## 55. DevEx & Developer Portals

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Backstage | TypeScript | 28k+ | Open-source developer portal by Spotify | Apache-2.0 | https://github.com/backstage/backstage |
| Port | TypeScript | 1k+ | Internal developer portal (free tier) | Proprietary | — |
| Cortex | TypeScript | — | Service catalog for teams | Proprietary | https://github.com/cortexlabs/cortex |
| Compass (Atlassian) | — | — | Developer experience platform | Proprietary | — |
| OpsLevel | — | — | Service catalog (free tier) | Proprietary | — |
| Rely.io | — | — | Internal developer portal | Proprietary | — |
| Roadie | TypeScript | — | SaaS Backstage platform | Proprietary | — |
| Platformer | Go | — | Developer platform (free tier) | Proprietary | — |
| Kratix | Go | 3k+ | Platform engineering framework | Apache-2.0 | https://github.com/syntasso/kratix |
| Humanitec | — | — | Platform orchestration | Proprietary | — |
| Porter | Go | 4k+ | Self-hosted PaaS on Kubernetes | MIT | https://github.com/porter-dev/porter |
| Dokku | Shell | 29k+ | Mini Heroku on your own server | MIT | https://github.com/dokku/dokku |
| CapRover | JavaScript | 13k+ | Free and open PaaS (App/DB deployment) | Apache-2.0 | https://github.com/caprover/caprover |
| Coolify | PHP | 21k+ | Self-hosted Heroku/Netlify alternative | Apache-2.0 | https://github.com/coollabsio/coolify |
| Railway (OSS tools) | — | — | App deployment platform (free tier) | Proprietary | — |
| Render (OSS tools) | — | — | Cloud platform (free tier) | Proprietary | — |
| Fly.io (OSS tools) | — | — | App hosting (free tier) | Proprietary | — |
| Kamal | Ruby | 12k+ | Deploy Docker apps anywhere (by Rails team) | MIT | https://github.com/basecamp/kamal |
| Ansible Semaphore | Go | 10k+ | Modern web UI for Ansible | MIT | https://github.com/semaphoreui/semaphore |
| Rundeck | Java | 5k+ | Operations runbook automation | Apache-2.0 | https://github.com/rundeck/rundeck |
| StackStorm | Python | 6k+ | Event-driven DevOps automation | Apache-2.0 | https://github.com/StackStorm/st2 |
| Waypoint | Go | 5k+ | Deploy app to any platform (HashiCorp) | BSL-1.1 | https://github.com/hashicorp/waypoint |
| Score | Go | 1k+ | Developer-centric workload specification | Apache-2.0 | https://github.com/score-spec/spec |
| Tilt | Go | 8k+ | Microservice dev environment | Apache-2.0 | https://github.com/tilt-dev/tilt |
| Skaffold | Go | 15k+ | Kubernetes dev workflow | Apache-2.0 | https://github.com/GoogleContainerTools/skaffold |
| Garden | TypeScript | 4k+ | Dev env + CI for Kubernetes apps | MPL-2.0 | https://github.com/garden-io/garden |
| DevSpace | Go | 4k+ | K8s development tool | Apache-2.0 | https://github.com/loft-sh/devspace |
| Telepresence | Go | 6k+ | Local dev against remote Kubernetes | Apache-2.0 | https://github.com/telepresenceio/telepresence |
| kubectl-dev | Go | — | Development helpers for kubectl | MIT | — |
| devpod | Go | 8k+ | Codespaces on any infrastructure | MPL-2.0 | https://github.com/loft-sh/devpod |
| Coder | Go | 9k+ | Self-hosted remote development | AGPL-3.0 | https://github.com/coder/coder |
| Gitpod | TypeScript | 13k+ | Cloud dev environments | AGPL-3.0 | https://github.com/gitpod-io/gitpod |
| code-server | TypeScript | 68k+ | VS Code in the browser | MIT | https://github.com/coder/code-server |
| Eclipse Che | Java | 7k+ | Kubernetes-native IDE | EPL-2.0 | https://github.com/eclipse-che/che |
| Theia | TypeScript | 20k+ | Cloud & desktop IDE framework | EPL-2.0 | https://github.com/eclipse-theia/theia |
| Windmill | TypeScript | 10k+ | Dev platform for scripts and flows | AGPL-3.0 | https://github.com/windmill-labs/windmill |
| Pipedream | JavaScript | 9k+ | Workflow automation for developers | Apache-2.0 | https://github.com/PipedreamHQ/pipedream |
| n8n | TypeScript | 51k+ | Fair-code workflow automation | Fair-code | https://github.com/n8n-io/n8n |
| Node-RED | JavaScript | 20k+ | Flow-based programming for IoT/API | Apache-2.0 | https://github.com/node-red/node-red |
| Huginn | Ruby | 43k+ | Build agents for automation | MIT | https://github.com/huginn/huginn |
| Automatisch | TypeScript | 4k+ | Self-hosted Zapier alternative | AGPL-3.0 | https://github.com/automatisch/automatisch |
| Activepieces | TypeScript | 9k+ | Open-source business automation | MIT | https://github.com/activepieces/activepieces |
| Temporal | Go | 12k+ | Durable workflow execution | MIT | https://github.com/temporalio/temporal |
| Cadence | Go | 8k+ | Distributed workflow orchestration | MIT | https://github.com/uber/cadence |
| Conductor | Java | 9k+ | Microservices orchestration | Apache-2.0 | https://github.com/Netflix/conductor |
| Prefect | Python | 17k+ | Python workflow automation | Apache-2.0 | https://github.com/PrefectHQ/prefect |
| Dagster | Python | 11k+ | Data orchestration platform | Apache-2.0 | https://github.com/dagster-io/dagster |
| Airbyte | Java | 16k+ | Open data integration platform | MIT | https://github.com/airbytehq/airbyte |
| OpenAPI Generator | Java | 22k+ | Generate SDKs from OpenAPI spec | Apache-2.0 | https://github.com/OpenAPITools/openapi-generator |
| Swagger Codegen | Java | 17k+ | API client code generation | Apache-2.0 | https://github.com/swagger-api/swagger-codegen |
| Prism | TypeScript | 4k+ | API mock server from OpenAPI spec | Apache-2.0 | https://github.com/stoplightio/prism |
| OpenAPI Validator | Various | 2k+ | Validate OpenAPI specifications | Apache-2.0 | — |
| Spectral | TypeScript | 7k+ | JSON/YAML linter for API specs | Apache-2.0 | https://github.com/stoplightio/spectral |
| ReadMe | — | — | API documentation platform | Proprietary | — |
| Scalar | TypeScript | 6k+ | Beautiful API reference docs | MIT | https://github.com/scalar/scalar |
| HTTPie | Python | 33k+ | HTTP client for the API age | BSD-3 | — |
| Hoppscotch | TypeScript | 66k+ | Open-source API development | MIT | https://github.com/hoppscotch/hoppscotch |
| Bruno | JavaScript | 26k+ | Postman alternative (OSS) | MIT | https://github.com/usebruno/bruno |
| Insomnia | TypeScript | 34k+ | API design and testing | Apache-2.0 | — |
| hodor | TypeScript | 95 | AI code reviewer for PRs/MRs | MIT | https://github.com/zerodha/hodor |
| gotp | HTML/Go | 43 | Live-preview Go templates | MIT | https://github.com/zerodha/gotp |
| damon | Go | 18 | Automate Nomad tasks via events | MIT | https://github.com/zerodha/damon |
| mvm | Go | 14 | CLI for sandbox microVMs | MIT | https://github.com/zerodha/mvm |

---

## 56. Zerodha FOSS Stack (Original Reference)

> The tools that inspired this list — Zerodha's internal open-source projects. All MIT licensed, self-hosted, production-proven at scale.

| Project | Language | Stars | Description | GitHub | Link |
|---------|----------|-------|-------------|--------|---------|
| **listmonk** | Go | 19.5k | High-performance newsletter & mailing list manager | zerodha/listmonk | https://github.com/knadh/listmonk |
| **koanf** | Go | 3.9k | Lightweight extensible config management (Viper alternative) | knadh/koanf | https://github.com/knadh/koanf |
| **logchef** | Vue | 743 | Log analytics UI for ClickHouse | zerodha/logchef | https://github.com/zerodha/logchef |
| **dungbeetle** | Go | 1.2k | Distributed job server for heavy SQL reads | zerodha/dungbeetle | https://github.com/zerodha/dungbeetle |
| **libredesk** | Go | 2.4k | Open-source self-hosted customer support desk | zerodha/libredesk | https://github.com/abhinavxd/libredesk |
| **flowctl** | Go | 299 | Self-service workflow execution platform | zerodha/flowctl | https://github.com/zerodha/flowctl |
| **otpgateway** | Go | 522 | Standalone OTP & address verification server | zerodha/otpgateway | https://github.com/zerodha/otpgateway |
| **hedwig** | Rust | 49 | High-performance minimalist SMTP server | zerodha/hedwig | https://github.com/zerodha/hedwig |
| **calert** | Go | 201 | Prometheus alertmanager → Google Chat | zerodha/calert | https://github.com/zerodha/calert |
| **whatomate** | Go | 977 | Open-source WhatsApp integration | zerodha/whatomate | https://github.com/zerodha/whatomate |
| **blobasaur** | Rust | 43 | SQLite-based blob store with Redis protocol | zerodha/blobasaur | https://github.com/zerodha/blobasaur |
| **simples3** | Go | 197 | Minimal S3 Go library with V4 signing | zerodha/simples3 | https://github.com/zerodha/simples3 |
| **stuffbin** | Go | 200 | Embed & compress static assets into Go binaries | zerodha/stuffbin | https://github.com/knadh/stuffbin |
| **indexed-cache** | JavaScript | 127 | Sideload static assets into browser IndexedDB | zerodha/indexed-cache | https://github.com/zerodha/indexed-cache |
| **kaf-relay** | Go | 96 | Sync Kafka topics across clusters in realtime | zerodha/kaf-relay | https://github.com/zerodha/kaf-relay |
| **nomctx** | Go | 58 | Switch clusters/namespaces in Nomad quickly | zerodha/nomctx | https://github.com/zerodha/nomctx |
| **nomad-events-sink** | Go | 55 | Nomad events → external sinks | zerodha/nomad-events-sink | https://github.com/zerodha/nomad-events-sink |
| **damon** | Go | 18 | Automate routine Nomad tasks via cluster events | zerodha/damon | https://github.com/zerodha/damon |
| **toru** | Go | 30 | Go module proxy with caching & rewrite | zerodha/toru | https://github.com/zerodha/toru |
| **mvm** | Go | 14 | CLI to create sandbox microVMs from container images | zerodha/mvm | https://github.com/zerodha/mvm |
| **store-exporter** | Go | 34 | Metrics from datastores in Prometheus format | zerodha/store-exporter | https://github.com/zerodha/store-exporter |
| **aws-exporter** | Go | 25 | AWS cost & EC2 metrics for Prometheus | zerodha/aws-exporter | https://github.com/zerodha/aws-exporter |
| **grafana-export** | Go | 43 | Download all Grafana dashboards to S3 | zerodha/grafana-export | https://github.com/zerodha/grafana-export |
| **nomadboard** | Go | 7 | Read-only status page for Nomad clusters | zerodha/nomadboard | https://github.com/zerodha/nomadboard |
| **kubekutr** | Go | 162 | Cookie-cutter templating for K8s manifests | zerodha/kubekutr | https://github.com/zerodha/kubekutr |
| **pfxsigner** | Go | 92 | Sign PDFs with PFX/PKCS#12 digital certs | zerodha/pfxsigner | https://github.com/zerodha/pfxsigner |
| **simplesessions** | Go | 80 | HTTP-agnostic session management library | zerodha/simplesessions | https://github.com/vividvilla/simplesessions |
| **simplehealth** | Go | 13 | Health-check endpoints in Prometheus/JSON | zerodha/simplehealth | https://github.com/zerodha/simplehealth |
| **fastglue** | Go | 91 | Micro HTTP framework wrapping fasthttp | zerodha/fastglue | https://github.com/zerodha/fastglue |
| **goyesql** | Go | 72 | Parse named SQL queries, auto-prepare & scan | knadh/goyesql | https://github.com/knadh/goyesql |
| **querytostruct** | Go | 22 | Unmarshal query strings into structs | zerodha/querytostruct | https://github.com/zerodha/querytostruct |
| **lzo1z** | Go | 5 | Pure Go LZO1Z compression library | zerodha/lzo1z | https://github.com/zerodha/lzo1z |
| **Tasqueue** | Go | 462 | Background job library with pluggable brokers | knadh/Tasqueue | https://github.com/knadh/tasqueue |
| **hodor** | TypeScript | 95 | Agentic code reviewer for GitHub PRs & GitLab MRs | zerodha/hodor | https://github.com/zerodha/hodor |
| **csvtotable** | Python | 1.2k | Convert CSV to searchable sortable HTML table | vividvilla/csvtotable | https://github.com/vividvilla/csvtotable |
| **gotp** | HTML | 43 | Live preview Go templates with custom data | zerodha/gotp | https://github.com/zerodha/gotp |
| **consul-cfg** | Go | 17 | Convert TOML/JSON/YAML to Consul KV pairs | zerodha/consul-cfg | https://github.com/zerodha/consul-cfg |
| **shelf** | Go | 40 | Symlinks manager | zerodha/shelf | https://github.com/zerodha/shelf |
| **rbiparser** | Python | 63 | Download & parse RBI bank database | zerodha/rbiparser | https://github.com/zerodha/rbiparser |
| **flutter_curl** | Dart | 65 | Flutter plugin using libcurl for HTTP | zerodha/flutter_curl | https://github.com/zerodha/flutter_curl |
| **flutter_fgbg** | Dart | 91 | Detect app foreground/background events | zerodha/flutter_fgbg | https://github.com/zerodha/flutter_fgbg |
| **flutter_displaymode** | Dart | 225 | Set display mode in Android via Flutter | zerodha/flutter_displaymode | https://github.com/zerodha/flutter_displaymode |
| **autopilot** | Dart | 127 | Flutter QA test driver | zerodha/autopilot | https://github.com/zerodha/autopilot |
| **tagflow** | Dart | 20 | HTML string → Flutter widgets | zerodha/tagflow | https://github.com/zerodha/tagflow |
| **trace-chart** | JavaScript | 25 | Lightweight financial charting for global markets | zerodha/trace-chart | https://github.com/zerodha/trace-chart |
| **store_keeper** | Dart | 37 | State management for Flutter apps | zerodha/store_keeper | https://github.com/zerodha/store_keeper |
| **terraform-provider-warpgate** | Go | 20 | Terraform provider for Warpgate | zerodha/terraform-provider-warpgate | https://github.com/zerodha/terraform-provider-warpgate |
| **eks-gitops** | Dockerfile | 11 | Deploy utilities for EKS clusters | zerodha/eks-gitops | https://github.com/zerodha/eks-gitops |
| **localhashi** | Jinja | 14 | Vagrant local Nomad/Consul clusters for dev | zerodha/localhashi | https://github.com/zerodha/localhashi |
| **kaf-ansible** | Jinja | 10 | Ansible for Zookeeper, Kafka, kaf CLI | zerodha/kaf-ansible | https://github.com/zerodha/kaf-ansible |
| **linkpage** | Go | 131 | Self-hosted LinkTree alternative | zerodha/linkpage | https://github.com/zerodha/linkpage |
| **lil** | Go | 57 | Simple self-hosted URL shortener | zerodha/lil | https://github.com/zerodha/lil |
| **listmonk-messenger** | Go | 73 | Webhook forwarder from listmonk to messengers | zerodha/listmonk-messenger | https://github.com/zerodha/listmonk-messenger |

---

## 57. Bonus: IoT, Embedded & Edge

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Arduino | C++ | 15k+ | Open-source electronics platform | GPL/LGPL | https://github.com/arduino/Arduino |
| PlatformIO | Python | 8k+ | Professional embedded development | Apache-2.0 | https://github.com/platformio/platformio-core |
| Zephyr RTOS | C | 11k+ | Linux Foundation RTOS for embedded | Apache-2.0 | https://github.com/zephyrproject-rtos/zephyr |
| FreeRTOS | C | 4k+ | Free real-time OS for microcontrollers | MIT | https://github.com/FreeRTOS/FreeRTOS |
| RT-Thread | C | 10k+ | Open-source IoT RTOS | Apache-2.0 | https://github.com/RT-Thread/rt-thread |
| Mbed OS | C++ | 4k+ | ARM's embedded OS | Apache-2.0 | https://github.com/ARMmbed/mbed-os |
| RIOT | C | 5k+ | Friendly OS for the IoT | LGPL-2.1 | https://github.com/RIOT-OS/RIOT |
| Contiki-NG | C | 2k+ | OS for IoT networking | BSD-3 | https://github.com/contiki-ng/contiki-ng |
| TinyOS | nesC | 1k+ | OS for sensor networks | BSD-3 | — |
| OpenWrt | C | 7k+ | Linux OS for embedded devices/routers | GPL-2.0 | https://github.com/openwrt/openwrt |
| ESP-IDF | C | 13k+ | Espressif IoT Development Framework | Apache-2.0 | https://github.com/espressif/esp-idf |
| Mongoose OS | C | 2k+ | OS for microcontrollers | Apache-2.0 | https://github.com/mongoose-os/mongoose-os |
| Node-RED | JavaScript | 20k+ | Flow-based low-code for IoT | Apache-2.0 | https://github.com/node-red/node-red |
| Eclipse Mosquitto | C | 9k+ | Lightweight MQTT broker | EPL-2.0 | https://github.com/eclipse/mosquitto |
| EMQ X (EMQX) | Erlang | 14k+ | Scalable MQTT broker for IoT | Apache-2.0 | https://github.com/emqx/emqx |
| Home Assistant | Python | 73k+ | Open-source home automation | Apache-2.0 | https://github.com/home-assistant/core |
| openHAB | Java | 4k+ | Open Home Automation Bus | EPL-2.0 | https://github.com/openhab/openhab-core |
| Domoticz | C++ | 3k+ | Home automation system | GPLv3 | https://github.com/domoticz/domoticz |
| Tasmota | C | 23k+ | Open-source firmware for ESP8266/ESP32 | GPL-3.0 | https://github.com/arendst/Tasmota |
| ESPHome | C++ | 8k+ | YAML-configured firmware for ESP32 | MIT | https://github.com/esphome/esphome |
| KiCad | C++ | 5k+ | Electronics design automation suite | GPL-3.0 | https://gitlab.com/kicad/code/kicad |
| FreeCAD | C++ | 22k+ | Open-source CAD/CAE tool | LGPL-2.0 | https://github.com/FreeCAD/FreeCAD |
| OpenSCAD | C++ | 7k+ | Programmer's solid 3D CAD modeller | GPL-2.0 | https://github.com/openscad/openscad |
| EdgeX Foundry | Go | 2k+ | IoT edge computing platform | Apache-2.0 | https://github.com/edgexfoundry/edgex-go |
| Thingsboard | Java | 17k+ | Open-source IoT platform | Apache-2.0 | https://github.com/thingsboard/thingsboard |
| Mainflux | Go | 2k+ | Industrial IoT messaging and device mgmt | Apache-2.0 | https://github.com/absmach/magistrala |
| Chirpstack | Go | 4k+ | Open-source LoRaWAN network server | MIT | https://github.com/chirpstack/chirpstack |
| tinyml (various) | C | — | ML on microcontrollers ecosystem | Various | — |
| TensorFlow Lite | C++ | — | ML for mobile and embedded | Apache-2.0 | — |
| MicroPython | C | 19k+ | Python for microcontrollers | MIT | https://github.com/micropython/micropython |
| CircuitPython | C | 4k+ | Python for hardware by Adafruit | MIT | https://github.com/adafruit/circuitpython |
| Raspberry Pi OS | C/Shell | — | Official RPi Linux distribution | Various | — |
| DietPi | Shell | 5k+ | Optimized Linux for single-board computers | GPL-2.0 | https://github.com/MichaIng/DietPi |
| Armbian | Shell | 5k+ | Linux for ARM development boards | GPL-2.0 | https://github.com/armbian/build |
| balenaOS | Shell | 1k+ | Container OS for IoT devices | Apache-2.0 | https://github.com/balena-os/balena |

---

## 58. Bonus: Blockchain & Web3 (OSS Only)

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Bitcoin Core | C++ | 79k+ | Bitcoin reference implementation | MIT | https://github.com/bitcoin/bitcoin |
| Ethereum (go-ethereum) | Go | 47k+ | Go Ethereum client | LGPL-3.0 | https://github.com/ethereum/go-ethereum |
| Solana | Rust | 13k+ | High-performance blockchain | Apache-2.0 | https://github.com/solana-labs/solana |
| Hyperledger Fabric | Go | 16k+ | Enterprise permissioned blockchain | Apache-2.0 | https://github.com/hyperledger/fabric |
| Hyperledger Besu | Java | 2k+ | Enterprise Ethereum client | Apache-2.0 | https://github.com/hyperledger/besu |
| Corda | Kotlin | 4k+ | Open-source DLT platform | Apache-2.0 | https://github.com/corda/corda |
| Substrate | Rust | 9k+ | Blockchain SDK by Parity | GPL-3.0 | https://github.com/paritytech/polkadot-sdk |
| Cosmos SDK | Go | 6k+ | Framework for building blockchains | Apache-2.0 | https://github.com/cosmos/cosmos-sdk |
| Tendermint | Go | 6k+ | Byzantine fault-tolerant consensus | Apache-2.0 | https://github.com/cometbft/cometbft |
| IPFS | Go | 23k+ | Distributed peer-to-peer filesystem | MIT/Apache | https://github.com/ipfs/kubo |
| libp2p | Go | 4k+ | Modular peer-to-peer networking | MIT/Apache | https://github.com/libp2p/go-libp2p |
| Filecoin | Go | 3k+ | Decentralized storage network | MIT | https://github.com/filecoin-project/lotus |
| NEAR Protocol | Rust | 2k+ | Layer-1 proof-of-stake blockchain | Apache-2.0 | https://github.com/near/nearcore |
| Hardhat | TypeScript | 7k+ | Ethereum development environment | MIT | https://github.com/NomicFoundation/hardhat |
| Truffle | JavaScript | 14k+ | Ethereum development framework | MIT | https://github.com/trufflesuite/truffle |
| Foundry | Rust | 9k+ | Ethereum development toolkit in Rust | MIT | https://github.com/foundry-rs/foundry |
| OpenZeppelin | Solidity | 25k+ | Secure smart contract library | MIT | https://github.com/OpenZeppelin/openzeppelin-contracts |
| ethers.js | TypeScript | 8k+ | JavaScript Ethereum library | MIT | https://github.com/ethers-io/ethers.js |
| web3.js | JavaScript | 20k+ | Ethereum JavaScript API | LGPL-3.0 | https://github.com/web3/web3.js |
| Solidity | C++ | 24k+ | Smart contract programming language | GPL-3.0 | https://github.com/ethereum/solidity |
| Vyper | Python | 5k+ | Pythonic smart contract language | Apache-2.0 | https://github.com/vyperlang/vyper |

---

## 59. Bonus: Scientific Computing & HPC

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| NumPy | Python | 28k+ | N-dimensional arrays for Python | BSD-3 | https://github.com/numpy/numpy |
| SciPy | Python | 13k+ | Scientific computing library | BSD-3 | — |
| SymPy | Python | 13k+ | Symbolic mathematics in Python | BSD-3 | https://github.com/sympy/sympy |
| Sage Math | Python | 2k+ | Open-source mathematics software | GPL-3.0 | https://github.com/sagemath/sage |
| GNU Octave | C++ | 1k+ | Scientific programming (MATLAB-compatible) | GPL-3.0 | https://github.com/gnu-octave/octave |
| R | C | 4k+ | Statistical computing environment | GPL-2.0 | — |
| Julia | Julia | 44k+ | High-performance scientific language | MIT | https://github.com/JuliaLang/julia |
| Fortran (gfortran) | Fortran | — | Scientific computing language | GPL-3.0 | — |
| OpenMPI | C | 2k+ | High-performance message passing | BSD-3 | https://github.com/open-mpi/ompi |
| MPICH | C | 1k+ | MPI implementation | BSD-3 | https://github.com/pmodels/mpich |
| OpenMP | — | — | Multi-platform shared-memory multiprocessing | — | — |
| PETSc | C | 1k+ | Portable Extensible Toolkit for Scientific Computing | BSD-2 | https://gitlab.com/petsc/petsc |
| Trilinos | C++ | 1k+ | Scientific computing framework | BSD-3 | https://github.com/trilinos/Trilinos |
| deal.II | C++ | 1k+ | Finite element library | LGPL-2.1 | https://github.com/dealii/dealii |
| FEniCS | C++/Python | 1k+ | Computing platform for PDEs | LGPL-3.0 | https://github.com/FEniCS/dolfinx |
| OpenFOAM | C++ | 2k+ | CFD toolbox for fluid dynamics | GPL-3.0 | https://develop.openfoam.com/Development/openfoam |
| OpenSees | C++ | 1k+ | Structural earthquake engineering | BSD-3 | — |
| LAMMPS | C++ | 2k+ | Molecular dynamics simulator | GPL-2.0 | https://github.com/lammps/lammps |
| GROMACS | C++ | 2k+ | Molecular dynamics simulation | LGPL-2.1 | https://gitlab.com/gromacs/gromacs |
| NAMD | C++ | — | Molecular dynamics simulation | Free academic | — |
| BLAST | C++ | — | Bioinformatics sequence alignment | Public Domain | — |
| Biopython | Python | 4k+ | Biology tools for Python | BSD-like | https://github.com/biopython/biopython |
| Bioconductor | R | — | Bioinformatics tools in R | Artistic-2.0 | — |
| Galaxy | Python | 1k+ | Scientific workflow platform | AFL-3.0 | https://github.com/galaxyproject/galaxy |
| Nextflow | Groovy | 3k+ | Data-driven computational pipelines | Apache-2.0 | https://github.com/nextflow-io/nextflow |
| Snakemake | Python | 2k+ | Workflow management for bioinformatics | MIT | https://github.com/snakemake/snakemake |
| Singularity/Apptainer | Go | 2k+ | HPC container runtime | BSD-3 | — |
| SLURM | C | 1k+ | Workload manager for HPC clusters | GPL-2.0 | https://github.com/SchedMD/slurm |
| PBS/Torque | C | 1k+ | HPC job scheduler | GPL/OpenPBS | — |

---

## 60. Bonus: Game Development

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| Godot Engine | C++ | 92k+ | Free, open-source 2D/3D game engine | MIT | https://github.com/godotengine/godot |
| Bevy | Rust | 37k+ | Data-driven game engine in Rust | MIT/Apache-2.0 | https://github.com/bevyengine/bevy |
| LibGDX | Java | 24k+ | Cross-platform Java game framework | Apache-2.0 | https://github.com/libgdx/libgdx |
| LÖVE (Love2D) | C++ | 4k+ | 2D game framework using Lua | Zlib | https://github.com/love2d/love |
| Raylib | C | 22k+ | Simple library for game programming | Zlib | — |
| SFML | C++ | 11k+ | Simple Fast Multimedia Library | Zlib | https://github.com/SFML/SFML |
| SDL2 | C | 5k+ | Hardware abstraction for media/game | Zlib | https://github.com/libsdl-org/SDL |
| Allegro | C | 2k+ | Cross-platform game programming library | Zlib | https://github.com/liballeg/allegro5 |
| OpenAL | C | 1k+ | Cross-platform 3D audio API | LGPL-2.1 | — |
| Bullet Physics | C++ | 12k+ | Real-time physics simulation | Zlib | https://github.com/bulletphysics/bullet3 |
| Box2D | C++ | 8k+ | 2D rigid body physics | MIT | https://github.com/erincatto/box2d |
| Chipmunk2D | C | 2k+ | Fast, lightweight 2D physics | MIT | https://github.com/slembcke/Chipmunk2D |
| Ogre3D | C++ | 4k+ | Scene-oriented 3D rendering engine | MIT | https://github.com/OGRECave/ogre |
| Irrlicht | C++ | 1k+ | High-performance realtime 3D engine | Zlib | https://github.com/zaki/irrlicht |
| OpenMW | C++ | 6k+ | Open-source Morrowind game engine | GPL-3.0 | https://gitlab.com/OpenMW/openmw |
| Spring RTS | C++ | 1k+ | Real-time strategy game engine | GPL-2.0 | — |
| Flixel | HaXe | 3k+ | Free 2D game library | MIT | — |
| Phaser | JavaScript | 37k+ | HTML5 game framework | MIT | https://github.com/phaserjs/phaser |
| PixiJS | TypeScript | 44k+ | 2D WebGL renderer for the web | MIT | https://github.com/pixijs/pixijs |
| Babylon.js | TypeScript | 23k+ | Powerful 3D engine for web and mobile | Apache-2.0 | https://github.com/BabylonJS/Babylon.js |
| Three.js | JavaScript | 102k+ | 3D library for JavaScript | MIT | https://github.com/mrdoob/three.js |
| PlayCanvas | JavaScript | 9k+ | WebGL game engine | MIT | https://github.com/playcanvas/engine |
| A-Frame | JavaScript | 16k+ | Web framework for VR experiences | MIT | https://github.com/aframevr/aframe |
| cocos2d-x | C++ | 18k+ | Cross-platform 2D game engine | MIT | https://github.com/cocos2d/cocos2d-x |
| MonoGame | C# | 11k+ | Open-source port of XNA framework | Microsoft Public | https://github.com/MonoGame/MonoGame |
| FNA | C# | 2k+ | XNA reimplementation | MS-PL | https://github.com/FNA-XNA/FNA |
| Panda3D | C++/Python | 4k+ | Game engine by Disney/CMU | BSD-3 | https://github.com/panda3d/panda3d |
| Defold | C++ | 5k+ | Cross-platform game engine | Apache-2.0 | https://github.com/defold/defold |
| Solar2D (Corona) | Lua | 2k+ | Cross-platform framework | MIT | — |
| Tiled | C++ | 12k+ | Flexible map editor for games | GPL-2.0 | https://github.com/mapeditor/tiled |
| LDtk | Haxe | 4k+ | Modern 2D level editor | MIT | https://github.com/deepnight/ldtk |
| FMOD (OSS SDK) | — | — | Adaptive audio for games | Proprietary | — |

---

## Summary Statistics

| Category | Count | — |
|----------|-------|---------|
| Operating Systems & Distros | 30+ | — |
| Shell & Terminal Tools | 60+ | — |
| Editors & IDEs | 40+ | — |
| Version Control & Git | 45+ | — |
| Languages & Runtimes | 70+ | — |
| Package Managers & Build | 55+ | — |
| Containers & Virtualization | 55+ | — |
| Kubernetes & Orchestration | 80+ | — |
| Infrastructure as Code | 35+ | — |
| CI/CD & GitOps | 45+ | — |
| Monitoring & Observability | 45+ | — |
| Logging | 35+ | — |
| Databases (All types) | 200+ | — |
| Message Queues & Streaming | 55+ | — |
| Caching & In-Memory | 25+ | — |
| Networking & Proxy | 80+ | — |
| Service Mesh & API Gateway | 25+ | — |
| Security & Secrets | 75+ | — |
| Authentication & Identity | 40+ | — |
| Web Frameworks Backend | 90+ | — |
| Web Frameworks Frontend | 80+ | — |
| CMS & Headless CMS | 30+ | — |
| E-Commerce | 20+ | — |
| Mobile Development | 30+ | — |
| Desktop Development | 35+ | — |
| Data Engineering | 75+ | — |
| Data Visualization & BI | 40+ | — |
| Machine Learning | 70+ | — |
| Deep Learning & Neural Nets | 50+ | — |
| MLOps & Model Serving | 40+ | — |
| LLM & Generative AI | 80+ | — |
| NLP & Text Processing | 55+ | — |
| Computer Vision | 45+ | — |
| Audio & Speech | 40+ | — |
| CLI Tools & Utilities | 100+ | — |
| File & Storage | 40+ | — |
| Backup & DR | 20+ | — |
| Notification & Alerting | 20+ | — |
| Email & Messaging | 45+ | — |
| Video & Media | 40+ | — |
| Documentation | 40+ | — |
| Project Management | 35+ | — |
| Finance & Payments | 30+ | — |
| Analytics & Tracking | 25+ | — |
| Testing & QA | 65+ | — |
| Go Libraries | 90+ | — |
| Python Libraries | 100+ | — |
| Rust Libraries | 60+ | — |
| JS/TS Libraries | 85+ | — |
| DevEx & Developer Portals | 65+ | — |
| Zerodha FOSS Stack | 55+ | — |
| IoT & Embedded | 40+ | — |
| Blockchain & Web3 | 20+ | — |
| Scientific Computing & HPC | 35+ | — |
| Game Development | 35+ | — |
| **TOTAL** | **~3000+** | — |

---

> **Disclaimer:** Star counts and license info are approximate at time of writing — always verify current license terms before production or commercial use. "Proprietary (free tier)" means the core product is closed-source but has a free tier available.

---

# Part 2: Notable Builders, Ecosystems & Foundation Projects

> Curated beyond the domain categories above: individual prolific OSS builders, company-specific OSS ecosystems, and the flagship projects of major foundations — included because they're useful jumping-off points, not because they're uncategorizable elsewhere.

## Table of Contents (Part 2)
61. [Kailash Nadh — Personal FOSS Projects](#61-kailash-nadh--personal-foss-projects-knadh)
62. [Zerodha FOSS Stack — Full](#62-zerodha-foss-stack--full--updated-april-2026)
63. [Similar OSS-First Indie Builders & Companies](#63-similar-oss-first-indie-builders--companies)
64. [Bonus: Mr. Karan (Zerodha SRE) — Personal OSS](#64-bonus-mr-karan-zerodha-sre--personal-oss-projects)
65. [Bonus: @vividvilla (Zerodha Dev) — Personal OSS](#65-bonus-vividvilla-zerodha-dev--personal-oss)
66. [Bonus: More OSS Tools From Indian Developer Community](#66-bonus-more-oss-tools-from-indian-developer-community)


## 61. Kailash Nadh — Personal FOSS Projects (knadh)

> Kailash Nadh is the CTO of Zerodha. These are his personal open-source projects spanning Go, Rust, JavaScript, Python and more — all MIT/BSD/Apache licensed, minimal-dependency, and self-hostable.

| Project | Language | Stars | Description | License | Year | Link |
|---------|----------|-------|-------------|---------|------|---------|
| **listmonk** | Go | 19.5k | High-performance self-hosted newsletter & mailing list manager. Single binary. | AGPL-3.0 | 2019 | https://github.com/knadh/listmonk |
| **koanf** | Go | 3.9k | Lightweight extensible config management for Go. Supports JSON/TOML/YAML/env/S3. | MIT | 2019 | https://github.com/knadh/koanf |
| **dns.toys** | Go | — | DNS server offering useful services over the DNS protocol (weather, time, units) | MIT | 2022 | https://github.com/knadh/dns.toys |
| **dictpress** | Go | — | Standalone webserver for building and publishing searchable dictionary websites | MIT | 2022 | https://github.com/knadh/dictpress |
| **goyesql** | Go | 72 | Parse SQL files with multiple named queries; auto-prepare and scan into structs | BSD-2 | 2019 | https://github.com/knadh/goyesql |
| **otpgateway** | Go | 522 | Standalone OTP & address verification server with pluggable providers | MIT | 2019 | https://github.com/zerodha/otpgateway |
| **stuffbin** | Go | 200 | Compress and embed static files into Go binaries with virtual filesystem | Other | 2019 | https://github.com/knadh/stuffbin |
| **querytostruct** | Go | 22 | Unmarshal query strings into Go structs | MIT | 2019 | https://github.com/zerodha/querytostruct |
| **smtppool** | Go | — | High-throughput Go SMTP pool library with graceful idle/error/retry handling | MIT | 2020 | https://github.com/knadh/smtppool |
| **paginator** | Go | — | Tiny Go package for pagination queries and page number generation | MIT | 2019 | https://github.com/knadh/paginator |
| **go-i18n** | Go | — | Tiny i18n library for loading JSON language translation files in Go | MIT | 2023 | https://github.com/knadh/go-i18n |
| **tinyauth** | Go | — | Tiny, opinionated authentication library for Go (WIP) | MIT | 2020 | https://github.com/knadh/tinyauth |
| **profiler** | Go | — | Simple wrapper over Go runtime/pprof for concurrent profiles | MIT | 2022 | https://github.com/knadh/profiler |
| **chunkedreader** | Go | — | Lightweight bufio wrapper for fixed-size byte stream chunks | MIT | 2015 | https://github.com/knadh/chunkedreader |
| **go-pop3** | Go | — | Simple Go POP3 client library for reading emails | MIT | 2021 | https://github.com/knadh/go-pop3 |
| **gtbump** | Go | — | git tag bump — bump semantic version tags and generate Markdown changelogs | MIT | 2019 | https://github.com/knadh/gtbump |
| **pfxsigner** | Go | 92 | CLI + web server for signing PDFs with PFX/PKCS#12 digital certificates | AGPL-3.0 | 2020 | https://github.com/zerodha/pfxsigner |
| **shelf** | Go | 40 | A good symlinks manager | MIT | 2021 | https://github.com/zerodha/shelf |
| **git-bars** | Go | — | Visualize git commit activity as terminal bar charts | MIT | 2018 | https://github.com/knadh/git-bars |
| **rconceptnet** | Rust | — | Simple, performant ConceptNet CLI and server in Rust using SQLite | MIT | 2026 | https://github.com/knadh/rconceptnet |
| **oat** | JS/CSS/HTML | — | Ultra-lightweight zero-dependency semantic HTML/CSS/JS UI library (~8KB min+gz) | MIT | 2026 | https://github.com/knadh/oat |
| **tinyrouter.js** | JavaScript | — | Tiny zero-dependency frontend routing library on top of window.history | MIT | 2025 | https://github.com/knadh/tinyrouter.js |
| **highlighted-input.js** | JavaScript | — | Super tiny JS lib that highlights keywords/tags in `<input>` fields | MIT | 2025 | https://github.com/knadh/highlighted-input.js |
| **floatype.js** | JavaScript | — | Tiny zero-dep floating autocomplete widget for textareas | MIT | 2023 | https://github.com/knadh/floatype.js |
| **autocomp.js** | JavaScript | — | Super tiny JS autocomplete/autosuggestion library (~800 bytes min+gzip) | MIT | 2023 | https://github.com/knadh/autocomp.js |
| **dragmove.js** | JavaScript | — | Super tiny JS library to make DOM elements draggable (~500 bytes min+gz) | MIT | 2020 | https://github.com/knadh/dragmove.js |
| **indexed-cache** | JavaScript | 127 | Sideload static assets and cache them in browser IndexedDB | MIT | 2021 | https://github.com/zerodha/indexed-cache |
| **tg-archive** | Python | — | Export Telegram group chats into static websites like mailing list archives | MIT | 2021 | https://github.com/knadh/tg-archive |
| **dirmaker** | Python | — | Simple opinionated static site generator for directory websites | MIT | 2021 | https://github.com/knadh/dirmaker |
| **indic.page** | — | — | Directory of Indic (Indian) language computing resources | MIT | 2020 | — |
| **mlphone** | Python/PHP | — | Phonetic algorithm for indexing Malayalam words (like Metaphone for English) | MIT | 2012 | https://github.com/knadh/mlphone |
| **knphone** | Go | — | Phonetic algorithm for indexing Kannada words by pronunciation | MIT | 2019 | https://github.com/knadh/knphone |
| **ml2en** | Python/PHP/JS | — | Transliterate Malayalam script to Roman/Latin characters (Manglish) | MIT | 2012 | https://github.com/knadh/ml2en |
| **dont.build** | — | — | Opinionated decision system: should you build this feature or not? | MIT | 2022 | — |
| **yesqlr** | Rust | — | Parse SQL files with named queries. Port of goyesql in Rust | MIT | 2024 | https://github.com/knadh/yesqlr |
| **tinyi18n-rs** | Rust | — | Tiny Rust i18n library loading JSON language maps | MIT | 2026 | — |
| **csv2json** | Zig | — | Fast utility converting CSV files to JSON line files (Zig experiment) | MIT | 2021 | https://github.com/knadh/csv2json |
| **zig-releaser** | Shell | — | Use GoReleaser to build/release/publish Zig projects | MIT | 2021 | https://github.com/knadh/zig-releaser |
| **niltalk** | Go/Vue | — | Instant disposable single-binary web-based live chat server | MIT | 2015 | https://github.com/knadh/niltalk |
| **hugo-ink** | HTML | — | Crisp, minimal personal website/blog theme for Hugo | MIT | 2019 | https://github.com/knadh/hugo-ink |
| **wordpluck** | JavaScript | — | Browser-based typing game (revived from 2012 project) | MIT | 2019 | https://github.com/knadh/wordpluck |
| **bigreddy** | Go | — | Generates pseudo-philosophical and pseudo-poetic ramblings | MIT | 2018 | https://github.com/knadh/bigreddy |
| **approve-pr-creation-from-issue** | YAML | — | GitHub Action: force contributors to get approval from Issue before raising PR | MIT | 2026 | — |
| **localStorageDB** | JavaScript | — | Simple database layer for localStorage/sessionStorage (tables, queries) | MIT | 2011 | https://github.com/knadh/localStorageDB |
| **tinytabs** | JavaScript | — | Tiny (~750 bytes) JS library for tabbed UIs, zero dependencies | MIT | 2011 | https://github.com/knadh/tinytabs |
| **funding.json** | — | — | Open spec for OSS projects to publish funding requirements as JSON manifest | MIT | 2023 | — |
| **HUML** | — | — | Simple strict serialization language for documents/datasets/config | MIT | 2025 | — |
| **ooru.space** | — | — | Open-source open-data directory of public community spaces across India | MIT | 2026 | — |
| **scylladb-metrics** | Python | — | Script for generating docs for Prometheus metrics exported by ScyllaDB | MIT | 2023 | — |
| **jsonconfig** | Go | — | Tiny JSON config file parser with comments support for Go | MIT | 2015 | — |
| **boastMachine** | PHP | — | One of the earliest OSS blogging systems (2002); powered 500k+ blogs | GPL | 2002 | — |

---

## 62. Zerodha FOSS Stack — Full & Updated (April 2026)

> All tools actively maintained, dog-fooded in production at Zerodha. Stars are live as of April 2026.

### Apps

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **libredesk** | Go | 2401 | Modern open-source self-hosted customer support desk. Single binary. | AGPL-3.0 | https://github.com/abhinavxd/libredesk |
| **flowctl** | Go | 299 | Open-source self-service workflow execution platform | Apache-2.0 | https://github.com/zerodha/flowctl |
| **whatomate** | Go | 977 | Open-source WhatsApp integration platform | AGPL-3.0 | https://github.com/zerodha/whatomate |
| **logchef** | Vue | 743 | Lightweight single-binary log analytics for ClickHouse; high-perf querying | AGPL-3.0 | https://github.com/zerodha/logchef |
| **listmonk** | Go | 19503 | High-performance self-hosted newsletter & mailing list manager | AGPL-3.0 | https://github.com/knadh/listmonk |
| **linkpage** | Go | 131 | FOSS self-hosted alternative to LinkTree / Campsite.bio | BSD-2 | https://github.com/zerodha/linkpage |
| **oore.build** | Rust | 15 | Self-hosted Flutter-first mobile CI and internal app distribution platform | MIT | — |
| **exampro** | Python | 55 | Proctored exams for Frappe Framework | MIT | — |

### Services

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **dungbeetle** | Go | 1223 | Distributed job server for queuing heavy SQL read jobs asynchronously | MIT | https://github.com/zerodha/dungbeetle |
| **kaf-relay** | Go | 96 | Replicate and sync Kafka topics between clusters in realtime; hot failovers | MIT | https://github.com/zerodha/kaf-relay |
| **terraform-provider-warpgate** | Go | 20 | Terraform Provider for Warpgate SSH bastion | — | https://github.com/zerodha/terraform-provider-warpgate |
| **hedwig** | Rust | 49 | High-performance minimalist SMTP server | AGPL-3.0 | https://github.com/zerodha/hedwig |
| **blobasaur** | Rust | 43 | Blob store based on SQLite, compatible with Redis protocol | AGPL-3.0 | https://github.com/zerodha/blobasaur |
| **otpgateway** | Go | 522 | Standalone OTP & address verification server with pluggable providers | MIT | https://github.com/zerodha/otpgateway |
| **calert** | Go | 201 | Send alert notifications to Google Chat via Prometheus Alertmanager | MIT | https://github.com/zerodha/calert |
| **toru** | Go | 30 | Go module proxy with caching and rewrite capabilities | MIT | https://github.com/zerodha/toru |
| **damon** | Go | 18 | Automate routine Nomad tasks by responding to cluster events | AGPL-3.0 | https://github.com/zerodha/damon |
| **listmonk-messenger** | Go | 73 | Webhook server: forward listmonk webhooks to different messengers | MIT | https://github.com/zerodha/listmonk-messenger |
| **nomad-events-sink** | Go | 55 | Events collection agent: Nomad Events → external sinks (HTTP etc.) | MIT | https://github.com/zerodha/nomad-events-sink |
| **store-exporter** | Go | 34 | Extract metrics from arbitrary datastores in Prometheus format | MIT | https://github.com/zerodha/store-exporter |

### Utils

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **nomadboard** | Go | 7 | Read-only status page for HashiCorp Nomad clusters with multi-DC support | MIT | https://github.com/zerodha/nomadboard |
| **mvm** | Go | 14 | Quick CLI to create development sandbox microVMs from container images | MIT | https://github.com/zerodha/mvm |
| **hodor** | TypeScript | 95 | Agentic code reviewer for GitHub PRs & GitLab MRs; multi-step reasoning | — | https://github.com/zerodha/hodor |
| **pi-sre-mode** | TypeScript | 10 | Pi-native incident investigation workflow with private overlay support | MIT | — |
| **gotp** | HTML | 43 | Live preview Go templates with custom data | MIT | https://github.com/zerodha/gotp |
| **autopilot** | Dart | 127 | Flutter QA test driver without sharing app source code | MIT | https://github.com/zerodha/autopilot |
| **nomctx** | Go | 58 | Faster switching between clusters and namespaces in Nomad | MIT | https://github.com/zerodha/nomctx |
| **stuffbin** | Go | 200 | Compress and embed static files into Go binaries | Other | https://github.com/knadh/stuffbin |
| **rbiparser** | Python | 63 | Download, parse, sanitize RBI bank database Excel sheets (IFSC/MICR) | — | https://github.com/zerodha/rbiparser |
| **kaf-ansible** | Jinja | 10 | Ansible scripts for setting up Zookeeper, Kafka, kaf CLI | MIT | https://github.com/zerodha/kaf-ansible |
| **vendor-payments** | Python | 35 | Frappe app: vendor payment workflows and reports | MIT | — |
| **localhashi** | Jinja | 14 | Vagrant setup for local Nomad/Consul clusters for dev/testing | MIT | https://github.com/zerodha/localhashi |
| **eks-gitops** | Dockerfile | 11 | Utilities for deployments in EKS clusters | MIT | https://github.com/zerodha/eks-gitops |
| **pfxsigner** | Go | 92 | CLI + web server for digitally signing PDFs with PFX certificates | AGPL-3.0 | https://github.com/zerodha/pfxsigner |
| **kubekutr** | Go | 162 | Cookie-cutter templating tool for scaffolding Kubernetes manifests | MIT | https://github.com/zerodha/kubekutr |
| **shelf** | Go | 40 | A good symlinks manager | MIT | https://github.com/zerodha/shelf |
| **kong-service-exporter** | Python | 13 | Export a service registry Markdown file from Kong's config | MIT | — |
| **csvtotable** | Python | 1172 | Convert CSV files to searchable and sortable HTML table | MIT | https://github.com/vividvilla/csvtotable |
| **grafana-export** | Go | 43 | Download all Grafana dashboards and backup to S3 | BSD-0 | https://github.com/zerodha/grafana-export |
| **faqgenerator** | Python | 9 | Simple FAQ generator for Zerodha Kite connect Forum | MIT | — |
| **aws-exporter** | Go | 25 | AWS Cost Explorer and EC2 metrics exporter for Prometheus | MIT | https://github.com/zerodha/aws-exporter |
| **rms-consolidated-scrips-status** | Python | 22 | Parse Zerodha consolidated Google sheets; render scrip category details | MIT | — |
| **consul-cfg** | Go | 17 | Convert TOML/JSON/YAML config to Consul KV pairs via CLI | MIT | https://github.com/zerodha/consul-cfg |
| **osticket-archive** | PHP | 9 | Archive closed osTicket tickets to disk as JSON; delete from DB | — | — |

### Libraries

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **flutter_curl** | Dart | 65 | Flutter plugin using libcurl for HTTP calls | MIT | https://github.com/zerodha/flutter_curl |
| **koanf** | Go | 3961 | Lightweight extensible configuration management library for Go | MIT | https://github.com/knadh/koanf |
| **flutter_fgbg** | Dart | 91 | Flutter plugin to detect foreground/background app events | MIT | https://github.com/zerodha/flutter_fgbg |
| **frappe-attachments-s3** | Python | 158 | Frappe app to upload file attachments in doctypes to S3 | Other | — |
| **lzo1z** | Go | 5 | Pure Go LZO1Z compression and decompression library | MIT | https://github.com/zerodha/lzo1z |
| **Tasqueue** | Go | 462 | Background jobs library for Go with pluggable brokers/stores | BSD-2 | https://github.com/knadh/tasqueue |
| **simples3** | Go | 197 | Simple no-frills AWS S3 Go library using REST with V4 signing | Other | https://github.com/zerodha/simples3 |
| **tagflow** | Dart | 20 | Flutter package: parse HTML strings → Flutter widgets | MIT | https://github.com/zerodha/tagflow |
| **flutter_displaymode** | Dart | 225 | Flutter plugin to set display mode in Android | MIT | https://github.com/zerodha/flutter_displaymode |
| **anpec** | Kotlin | 5 | Flutter plugin for Android device performance classification | MIT | — |
| **trace-chart** | JavaScript | 25 | Lightweight customizable financial charting library for global markets | Apache-2.0 | https://github.com/zerodha/trace-chart |
| **simplesessions** | Go | 80 | Go session management library; HTTP/framework/store agnostic | MIT | https://github.com/vividvilla/simplesessions |
| **pdf_text_overlay** | Python | 41 | Python library to write text on top of PDF files | MIT | — |
| **fastglue** | Go | 91 | Opinionated wrapper gluing fasthttp + fasthttprouter as micro HTTP framework | MIT | https://github.com/zerodha/fastglue |
| **store_keeper** | Dart | 37 | Easy and flexible state management system for Flutter apps | MIT | https://github.com/zerodha/store_keeper |
| **duckdb-fnv** | Python | 6 | DuckDB extension to calculate FNV hash and FNV partition buckets | MIT | — |
| **slim-ui** | Vue | 66 | Simple components library for lightweight Vue.js projects | — | — |
| **frappe_tinymce** | Python | 48 | Frappe app to replace default text editor with TinyMCE | Other | — |
| **recharge** | Dart | 49 | Simple library to hot-reload Dart code on file changes | MIT | — |
| **optionchainstream** | Python | 159 | Live streaming option chain for equity derivatives via Kite WebSocket + Redis | MIT | — |
| **goyesql** | Go | 72 | Parse SQL files with named queries; auto-prepare and scan to structs | BSD-2 | https://github.com/knadh/goyesql |
| **indexed-cache** | JavaScript | 127 | Sideload static assets and cache in browser IndexedDB | MIT | https://github.com/zerodha/indexed-cache |
| **querytostruct** | Go | 22 | Unmarshal and scan querystrings into Go structs | MIT | https://github.com/zerodha/querytostruct |
| **go-frappe-client** | Go | 13 | Frappe client written in Go | MIT | — |
| **terraform-provider-kite** | Go | 25 | Terraform provider for managing long-term portfolio with Zerodha Kite | MIT | — |
| **simplehealth** | Go | 13 | Tiny lib exposing health-check endpoints in Prometheus/JSON format | MIT | https://github.com/zerodha/simplehealth |
| **subscription_coupons** | Python | 17 | Subscription discount coupon code manager | Other | — |
| **frappe_discourse** | Python | 19 | Frappe app for Single Sign-On with Discourse | Other | — |
| **lil** | Go | 57 | Simple URL shortener built with Go | — | https://github.com/zerodha/lil |

---

## 63. Similar OSS-First Indie Builders & Companies

> Open-source-first companies and individual builders who, like Zerodha/knadh, ship production-grade FOSS tools.

### 63a. Mailchimp / Chargebee OSS Alternatives Ecosystem

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **Mautic** | PHP | 7k+ | Open-source marketing automation platform | Apache-2.0 | https://github.com/mautic/mautic |
| **Postal** | Ruby | 15k+ | Full-featured open-source mail delivery platform | Apache-2.0 | https://github.com/postalserver/postal |
| **Mailu** | Python | 6k+ | Simple and full-featured mail server stack | MIT | https://github.com/Mailu/Mailu |
| **listmonk** | Go | 19.5k | Self-hosted newsletter manager | AGPL-3.0 | https://github.com/knadh/listmonk |
| **Cal.com** | TypeScript | 32k+ | Open-source Calendly alternative | AGPL-3.0 | https://github.com/calcom/cal.com |
| **Formbricks** | TypeScript | 9k+ | Open-source survey and experience management | MIT | https://github.com/formbricks/formbricks |
| **Typebot** | TypeScript | 7k+ | Open-source chatbot builder | AGPL-3.0 | https://github.com/baptisteArno/typebot.io |
| **Documenso** | TypeScript | 9k+ | Open-source DocuSign alternative | AGPL-3.0 | https://github.com/documenso/documenso |
| **OpenSign** | JavaScript | 4k+ | Open-source document signing | AGPL-3.0 | https://github.com/OpenSignLabs/OpenSign |
| **Lago** | Ruby/TypeScript | 7k+ | Open-source usage-based billing | AGPL-3.0 | https://github.com/getlago/lago |
| **Invoice Ninja** | PHP | 8k+ | Open-source invoicing and payments | AAL | https://github.com/invoiceninja/invoiceninja |
| **Crater** | PHP | 8k+ | Invoice and expense management | AAL | https://github.com/crater-invoice/crater |

### 63b. HashiCorp-alike OSS Infra Tools

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **OpenTofu** | Go | 23k+ | Open-source Terraform fork | MPL-2.0 | https://github.com/opentofu/opentofu |
| **OpenBao** | Go | 3k+ | Open-source HashiCorp Vault fork | MPL-2.0 | https://github.com/openbao/openbao |
| **Infisical** | TypeScript | 16k+ | Open-source secrets manager | MIT | https://github.com/Infisical/infisical |
| **Netbird** | Go | 11k+ | Open-source WireGuard-based VPN mesh | Apache-2.0 | https://github.com/netbirdio/netbird |
| **Headscale** | Go | 20k+ | Self-hosted Tailscale control server | BSD-3 | https://github.com/juanfont/headscale |
| **Warpgate** | Rust | 6k+ | Smart SSH/HTTPS/MySQL bastion host | Apache-2.0 | https://github.com/warp-tech/warpgate |
| **Teleport** | Go | 17k+ | Open-source zero-trust infrastructure access | Apache-2.0 | https://github.com/gravitational/teleport |
| **Boundary** | Go | 4k+ | HashiCorp identity-based access proxy | MPL-2.0 | https://github.com/hashicorp/boundary |
| **Consul** | Go | 28k+ | Service mesh and service discovery | BSL-1.1 | https://github.com/hashicorp/consul |
| **Nomad** | Go | 15k+ | Flexible multi-platform workload orchestrator | BSL-1.1 | https://github.com/hashicorp/nomad |

### 63c. Supabase / PocketBase Ecosystem

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **Supabase** | TypeScript | 73k+ | Open-source Firebase alternative using Postgres | Apache-2.0 | https://github.com/supabase/supabase |
| **PocketBase** | Go | 43k+ | Open-source backend-as-a-service in a single file | MIT | https://github.com/pocketbase/pocketbase |
| **Appwrite** | TypeScript | 43k+ | Open-source Firebase alternative | BSD-3 | https://github.com/appwrite/appwrite |
| **Nhost** | TypeScript | 7k+ | Open-source Firebase alt with Hasura | MIT | https://github.com/nhost/nhost |
| **Directus** | TypeScript | 29k+ | Open-source headless CMS and data platform | BSL-1.1 | https://github.com/directus/directus |
| **Payload CMS** | TypeScript | 29k+ | Code-first TypeScript headless CMS | MIT | https://github.com/payloadcms/payload |
| **Hasura** | Haskell | 31k+ | Instant GraphQL on Postgres + REST | Apache-2.0 | https://github.com/hasura/graphql-engine |
| **PostgREST** | Haskell | 24k+ | REST API from any PostgreSQL database | MIT | https://github.com/PostgREST/postgrest |
| **Postgraphile** | TypeScript | 12k+ | Instant GraphQL from PostgreSQL | MIT | https://github.com/graphile/postgraphile |
| **Pocketbase** | Go | 43k+ | Open-source realtime backend | MIT | — |
| **Convex** | TypeScript | — | Open-source reactive backend | Apache-2.0 | https://github.com/get-convex/convex-backend |
| **Neon** | Rust | 14k+ | Serverless open-source PostgreSQL | Apache-2.0 | https://github.com/neondatabase/neon |

### 63d. Grafana Labs OSS Ecosystem

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **Grafana** | Go | 65k+ | Open-source analytics and visualization | AGPL-3.0 | https://github.com/grafana/grafana |
| **Loki** | Go | 24k+ | Like Prometheus but for logs | AGPL-3.0 | https://github.com/grafana/loki |
| **Tempo** | Go | 4k+ | Distributed tracing backend | AGPL-3.0 | https://github.com/grafana/tempo |
| **Mimir** | Go | 4k+ | Scalable long-term Prometheus backend | AGPL-3.0 | https://github.com/grafana/mimir |
| **Beyla** | Go | 2k+ | eBPF-based auto-instrumentation for Go/Java/Python | Apache-2.0 | https://github.com/grafana/beyla |
| **Alloy** | Go | 2k+ | OpenTelemetry collector distribution | Apache-2.0 | https://github.com/grafana/alloy |
| **k6** | Go | 26k+ | Load and performance testing tool | AGPL-3.0 | https://github.com/grafana/k6 |
| **Pyroscope** | Go | 10k+ | Continuous profiling platform | AGPL-3.0 | https://github.com/grafana/pyroscope |
| **OnCall** | Python | 3k+ | On-call scheduling and alert routing | AGPL-3.0 | https://github.com/grafana/oncall |
| **Faro** | TypeScript | 1k+ | Frontend observability SDK | Apache-2.0 | https://github.com/grafana/faro-web-sdk |

### 63e. CNCF Graduated & Incubating Projects

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **Kubernetes** | Go | 111k+ | Container orchestration | Apache-2.0 | https://github.com/kubernetes/kubernetes |
| **Prometheus** | Go | 56k+ | Monitoring and alerting | Apache-2.0 | https://github.com/prometheus/prometheus |
| **Envoy** | C++ | 25k+ | Cloud-native proxy | Apache-2.0 | https://github.com/envoyproxy/envoy |
| **CoreDNS** | Go | 12k+ | Extensible DNS server | Apache-2.0 | https://github.com/coredns/coredns |
| **containerd** | Go | 17k+ | Container runtime | Apache-2.0 | https://github.com/containerd/containerd |
| **Fluentd** | Ruby | 13k+ | Unified logging layer | Apache-2.0 | https://github.com/fluent/fluentd |
| **Jaeger** | Go | 20k+ | Distributed tracing | Apache-2.0 | https://github.com/jaegertracing/jaeger |
| **Vitess** | Go | 19k+ | Database clustering for MySQL | Apache-2.0 | https://github.com/vitessio/vitess |
| **NATS** | Go | 16k+ | Cloud-native messaging | Apache-2.0 | https://github.com/nats-io/nats-server |
| **Linkerd** | Rust/Go | 10k+ | Ultra-light service mesh | Apache-2.0 | https://github.com/linkerd/linkerd2 |
| **Argo CD** | Go | 18k+ | Declarative GitOps CD | Apache-2.0 | https://github.com/argoproj/argo-cd |
| **Flux** | Go | 16k+ | GitOps toolkit for Kubernetes | Apache-2.0 | https://github.com/fluxcd/flux2 |
| **Cilium** | Go | 20k+ | eBPF networking and security | Apache-2.0 | https://github.com/cilium/cilium |
| **Falco** | C++ | 7k+ | Runtime security | Apache-2.0 | https://github.com/falcosecurity/falco |
| **OpenTelemetry** | Various | 5k+ | Vendor-neutral telemetry | Apache-2.0 | https://github.com/open-telemetry/opentelemetry-collector |
| **KEDA** | Go | 9k+ | Event-driven autoscaling | Apache-2.0 | https://github.com/kedacore/keda |
| **Crossplane** | Go | 10k+ | Cloud-native control planes | Apache-2.0 | https://github.com/crossplane/crossplane |
| **Thanos** | Go | 13k+ | Highly available Prometheus | Apache-2.0 | https://github.com/thanos-io/thanos |
| **Longhorn** | Go | 6k+ | Distributed block storage for K8s | Apache-2.0 | https://github.com/longhorn/longhorn |
| **cert-manager** | Go | 12k+ | Automatic TLS certificates | Apache-2.0 | https://github.com/cert-manager/cert-manager |

### 63f. Linux Foundation Top Projects

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **Linux Kernel** | C | 175k+ | The OS kernel | GPL-2.0 | https://github.com/torvalds/linux |
| **Node.js** | C++ | 107k+ | JavaScript runtime | MIT | https://github.com/nodejs/node |
| **Hyperledger Fabric** | Go | 16k+ | Enterprise blockchain | Apache-2.0 | https://github.com/hyperledger/fabric |
| **ONAP** | Java | — | Network automation platform | Apache-2.0 | — |
| **EdgeX Foundry** | Go | 2k+ | IoT edge computing platform | Apache-2.0 | https://github.com/edgexfoundry/edgex-go |
| **Zephyr RTOS** | C | 11k+ | Real-time OS for embedded | Apache-2.0 | https://github.com/zephyrproject-rtos/zephyr |
| **ACRN** | C | 1k+ | Embedded hypervisor | BSD-3 | — |
| **OpenDaylight** | Java | 1k+ | SDN platform | EPL-1.0 | — |
| **OPNFV** | — | — | Network functions virtualization | Apache-2.0 | — |
| **Akraino** | — | — | Edge stack infrastructure | Apache-2.0 | — |
| **LF Energy** | — | — | Open-source energy platform | Apache-2.0 | — |
| **OpenSSF** | — | — | Open-source security foundation | Various | — |
| **SPDX** | — | — | Software bill of materials standard | Apache-2.0 | — |

### 63g. Apache Software Foundation Top Projects

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **Apache Kafka** | Java | 28k+ | Distributed event streaming | Apache-2.0 | https://github.com/apache/kafka |
| **Apache Spark** | Scala | 40k+ | Unified analytics engine | Apache-2.0 | https://github.com/apache/spark |
| **Apache Flink** | Java | 24k+ | Stream and batch processing | Apache-2.0 | https://github.com/apache/flink |
| **Apache Airflow** | Python | 37k+ | Workflow orchestration | Apache-2.0 | — |
| **Apache Cassandra** | Java | 8k+ | Distributed NoSQL database | Apache-2.0 | — |
| **Apache Solr** | Java | 4k+ | Enterprise search platform | Apache-2.0 | — |
| **Apache Pulsar** | Java | 14k+ | Cloud-native messaging | Apache-2.0 | https://github.com/apache/pulsar |
| **Apache Iceberg** | Java | 7k+ | Open table format for analytics | Apache-2.0 | https://github.com/apache/iceberg |
| **Apache Druid** | Java | 14k+ | Real-time analytics database | Apache-2.0 | — |
| **Apache Arrow** | C++ | 14k+ | In-memory columnar data format | Apache-2.0 | — |
| **Apache Beam** | Java/Python | 8k+ | Unified batch and streaming | Apache-2.0 | https://github.com/apache/beam |
| **Apache Hudi** | Java | 5k+ | Data lake storage solution | Apache-2.0 | https://github.com/apache/hudi |
| **Apache Superset** | Python | 63k+ | Modern data exploration and BI | Apache-2.0 | https://github.com/apache/superset |
| **Apache NiFi** | Java | 4k+ | Data flow automation | Apache-2.0 | https://github.com/apache/nifi |
| **Apache Groovy** | Java | 5k+ | JVM dynamic language | Apache-2.0 | — |
| **Apache Maven** | Java | 4k+ | Build and project management | Apache-2.0 | — |
| **Apache Tomcat** | Java | 7k+ | Java servlet container | Apache-2.0 | — |
| **Apache HTTP Server** | C | 4k+ | World's most used web server | Apache-2.0 | — |
| **Apache Hadoop** | Java | 14k+ | Distributed processing framework | Apache-2.0 | https://github.com/apache/hadoop |
| **Apache Hive** | Java | 5k+ | SQL-based data warehouse | Apache-2.0 | — |
| **Apache ZooKeeper** | Java | 12k+ | Distributed coordination service | Apache-2.0 | — |
| **Apache Lucene** | Java | 2k+ | Full-text search engine library | Apache-2.0 | — |

### 63h. Self-Hosting / HomeLab Essentials

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **Nextcloud** | PHP | 27k+ | Self-hosted Google Drive/Calendar/Contacts | AGPL-3.0 | https://github.com/nextcloud/server |
| **Jellyfin** | C# | 34k+ | Free software media system | GPL-2.0 | https://github.com/jellyfin/jellyfin |
| **Home Assistant** | Python | 73k+ | Open-source home automation | Apache-2.0 | https://github.com/home-assistant/core |
| **Pi-hole** | Shell | 50k+ | Network-wide ad blocker via DNS | EUPL-1.2 | https://github.com/pi-hole/pi-hole |
| **AdGuard Home** | Go | 25k+ | Network-level ad/tracker blocker | GPL-3.0 | https://github.com/AdguardTeam/AdGuardHome |
| **Uptime Kuma** | JavaScript | 60k+ | Self-hosted uptime monitoring | MIT | https://github.com/louislam/uptime-kuma |
| **Portainer CE** | Go | 30k+ | Container management UI | Zlib | https://github.com/portainer/portainer |
| **Traefik** | Go | 51k+ | Cloud-native reverse proxy | MIT | https://github.com/traefik/traefik |
| **Nginx Proxy Manager** | JavaScript | 23k+ | Easy reverse proxy with GUI | MIT | https://github.com/NginxProxyManager/nginx-proxy-manager |
| **Vaultwarden** | Rust | 38k+ | Self-hosted Bitwarden server | AGPL-3.0 | — |
| **Paperless-ngx** | Python | 22k+ | Document management system | GPL-3.0 | https://github.com/paperless-ngx/paperless-ngx |
| **Immich** | TypeScript | 58k+ | Self-hosted photo and video backup | AGPL-3.0 | https://github.com/immich-app/immich |
| **Photoprism** | Go | 35k+ | AI-powered photo app | AGPL-3.0 | https://github.com/photoprism/photoprism |
| **Plex (OSS tools)** | — | — | Media server (proprietary) | Proprietary | — |
| **Navidrome** | Go | 12k+ | Self-hosted music streaming | GPL-3.0 | https://github.com/navidrome/navidrome |
| **Kavita** | C# | 7k+ | Self-hosted digital library | GPL-2.0 | https://github.com/Kareadita/Kavita |
| **Mealie** | Python | 7k+ | Self-hosted recipe manager | AGPL-3.0 | https://github.com/mealie-recipes/mealie |
| **Firefly III** | PHP | 16k+ | Personal finance manager | AGPL-3.0 | https://github.com/firefly-iii/firefly-iii |
| **Grocy** | PHP | 7k+ | Grocery and household management | MIT | https://github.com/grocy/grocy |
| **Vikunja** | Go | 4k+ | Open-source to-do and project mgmt | GPL-3.0 | https://github.com/go-vikunja/vikunja |
| **SearXNG** | Python | 13k+ | Privacy-respecting metasearch engine | AGPL-3.0 | https://github.com/searxng/searxng |
| **Whoogle** | Python | 10k+ | Self-hosted Google search proxy | MIT | https://github.com/benbusby/whoogle-search |
| **FreshRSS** | PHP | 10k+ | Self-hosted RSS/Atom aggregator | AGPL-3.0 | https://github.com/FreshRSS/FreshRSS |
| **Miniflux** | Go | 7k+ | Minimalist RSS reader | Apache-2.0 | https://github.com/miniflux/v2 |
| **Gitea** | Go | 45k+ | Self-hosted Git service | MIT | https://github.com/go-gitea/gitea |
| **Forgejo** | Go | 3k+ | Community-driven Gitea fork | MIT | https://codeberg.org/forgejo/forgejo |
| **Dashy** | Vue | 17k+ | Personal dashboard for self-hosted services | MIT | https://github.com/Lissy93/dashy |
| **Homer** | Vue | 9k+ | Simple static homepage for servers | Apache-2.0 | https://github.com/bastienwirtz/homer |
| **Heimdall** | PHP | 7k+ | Application dashboard | MIT | https://github.com/linuxserver/Heimdall |
| **Homarr** | TypeScript | 6k+ | Sleek homelab dashboard | MIT | https://github.com/homarr-labs/homarr |
| **Organizr** | PHP | 5k+ | Dashboard for self-hosted services | GPL-3.0 | https://github.com/causefx/Organizr |
| **Syncthing** | Go | 64k+ | Decentralized continuous file sync | MPL-2.0 | — |
| **Restic** | Go | 26k+ | Fast encrypted backup | BSD-2 | — |
| **Duplicati** | C# | 11k+ | Encrypted online backup | LGPL-2.1 | — |
| **WireGuard** | C | 5k+ | Fast modern VPN | GPL-2.0 | https://git.zx2c4.com/wireguard-linux |
| **OpenVPN** | C | 10k+ | SSL-based VPN | GPL-2.0 | https://github.com/OpenVPN/openvpn |
| **Authelia** | Go | 22k+ | SSO + 2FA authentication proxy | Apache-2.0 | https://github.com/authelia/authelia |
| **Authentik** | Python | 14k+ | Flexible identity provider | MIT | https://github.com/goauthentik/authentik |

### 63i. Dev Tools Built by Small OSS Teams

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **Hoppscotch** | TypeScript | 66k+ | Open-source API development ecosystem | MIT | https://github.com/hoppscotch/hoppscotch |
| **Bruno** | JavaScript | 26k+ | Offline API client (Postman alternative) | MIT | https://github.com/usebruno/bruno |
| **Insomnia** | TypeScript | 34k+ | API design and testing platform | Apache-2.0 | — |
| **Zed** | Rust | 51k+ | High-performance multiplayer code editor | AGPL-3.0 | https://github.com/zed-industries/zed |
| **Helix** | Rust | 33k+ | Post-modern modal text editor | MPL-2.0 | https://github.com/helix-editor/helix |
| **Lapce** | Rust | 35k+ | Lightning-fast code editor | Apache-2.0 | https://github.com/lapce/lapce |
| **Warp** | Rust | — | Modern terminal (free, partially open) | Proprietary | https://github.com/seanmonstar/warp |
| **WezTerm** | Rust | 17k+ | GPU-accelerated terminal | MIT | https://github.com/wez/wezterm |
| **Ghostty** | Zig | 25k+ | Fast native terminal emulator | MIT | https://github.com/ghostty-org/ghostty |
| **Atuin** | Rust | 20k+ | Encrypted shell history sync | MIT | — |
| **Starship** | Rust | 46k+ | Cross-shell minimal prompt | ISC | https://github.com/starship/starship |
| **lazygit** | Go | 51k+ | Terminal UI for Git | MIT | https://github.com/jesseduffield/lazygit |
| **gitui** | Rust | 18k+ | Blazing-fast terminal Git UI | MIT | https://github.com/gitui-org/gitui |
| **delta** | Rust | 23k+ | Beautiful git diffs pager | MIT | https://github.com/dandavison/delta |
| **mise** | Rust | 11k+ | Dev tools version manager | MIT | https://github.com/jdx/mise |
| **uv** | Rust | 40k+ | Ultra-fast Python package manager | MIT/Apache-2.0 | https://github.com/astral-sh/uv |
| **Ruff** | Rust | 34k+ | Extremely fast Python linter | MIT | https://github.com/astral-sh/ruff |
| **Biome** | Rust | 16k+ | Toolchain for web projects (linter/formatter) | MIT | https://github.com/biomejs/biome |
| **Oxlint** | Rust | 12k+ | Extremely fast JavaScript linter | MIT | https://github.com/oxc-project/oxc |
| **SWC** | Rust | 31k+ | Super-fast JS/TS compiler | Apache-2.0 | https://github.com/swc-project/swc |
| **Turbopack** | Rust | — | Next-gen webpack alternative | MPL-2.0 | — |
| **Bun** | Zig | 74k+ | Fast all-in-one JS runtime | MIT | https://github.com/oven-sh/bun |
| **Deno** | Rust | 96k+ | Secure JS/TS runtime | MIT | https://github.com/denoland/deno |
| **just** | Rust | 22k+ | Command runner (Makefile alternative) | CC0 | — |
| **Task** | Go | 11k+ | Task runner / build tool | MIT | https://github.com/go-task/task |
| **Earthly** | Go | 11k+ | Repeatable CI/CD builds | MPL-2.0 | https://github.com/earthly/earthly |
| **Dagger** | Go | 12k+ | Portable dev pipelines as code | Apache-2.0 | https://github.com/dagger/dagger |
| **Tilt** | Go | 8k+ | Microservices dev environment | Apache-2.0 | https://github.com/tilt-dev/tilt |
| **Skaffold** | Go | 15k+ | Kubernetes dev workflow tool | Apache-2.0 | https://github.com/GoogleContainerTools/skaffold |
| **DevPod** | Go | 8k+ | Codespaces on any infrastructure | MPL-2.0 | — |
| **Coolify** | PHP | 21k+ | Self-hosted Heroku/Netlify alternative | Apache-2.0 | https://github.com/coollabsio/coolify |
| **Dokku** | Shell | 29k+ | Mini Heroku on your own server | MIT | https://github.com/dokku/dokku |
| **Kamal** | Ruby | 12k+ | Deploy Docker apps anywhere | MIT | https://github.com/basecamp/kamal |
| **Ansible Semaphore** | Go | 10k+ | Modern web UI for Ansible | MIT | https://github.com/semaphoreui/semaphore |

---

## 64. Bonus: Mr. Karan (Zerodha SRE) — Personal OSS Projects

> @mr-karan — SRE at Zerodha, active OSS contributor with a focus on infrastructure tools.

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **doggo** | Go | 2k+ | Human-friendly DNS client for terminal | MIT | https://github.com/mr-karan/doggo |
| **natsbench** | Go | — | NATS benchmarking tool | MIT | — |
| **nomadreader** | Go | — | Nomad job spec reader and validator | MIT | — |
| **coredns-nomad** | Go | — | CoreDNS plugin for Nomad service discovery | MIT | — |
| **toru** | Go | 30 | Go module proxy (Zerodha project) | MIT | https://github.com/zerodha/toru |
| **dnstrace** | Go | — | DNS packet tracer | MIT | — |

---

## 65. Bonus: @vividvilla (Zerodha Dev) — Personal OSS

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **csvtotable** | Python | 1172 | Convert CSV to searchable sortable HTML table | MIT | https://github.com/vividvilla/csvtotable |
| **Aqua** | Go | — | Simple session middleware for Go | MIT | — |

---

## 66. Bonus: More OSS Tools From Indian Developer Community

| Project | Language | Stars | Description | License | Link |
|---------|----------|-------|-------------|---------|---------|
| **Hasura** | Haskell | 31k+ | Instant GraphQL API over Postgres (Bengaluru-founded) | Apache-2.0 | https://github.com/hasura/graphql-engine |
| **Chatwoot** | Ruby | 22k+ | Open-source customer support platform (Kerala-founded) | MIT | https://github.com/chatwoot/chatwoot |
| **Frappe Framework** | Python | 7k+ | Full-stack web framework (Mumbai) | MIT | https://github.com/frappe/frappe |
| **ERPNext** | Python | 22k+ | Open-source ERP built on Frappe | GPL-3.0 | https://github.com/frappe/erpnext |
| **Plane** | TypeScript | 29k+ | Open-source JIRA alternative (India) | AGPL-3.0 | https://github.com/makeplane/plane |
| **AppFlowy** | Rust | 60k+ | Open-source Notion alternative | AGPL-3.0 | https://github.com/AppFlowy-IO/AppFlowy |
| **Glific** | Elixir | 1k+ | Two-way communication platform for NGOs | AGPL-3.0 | https://github.com/glific/glific |
| **Fiftyone** | Python | 8k+ | Dataset curation for computer vision | Apache-2.0 | — |
| **Dyte** | TypeScript | — | Programmable live video (OSS SDK) | Apache-2.0 | — |
| **100ms** | TypeScript | 1k+ | Live video SDK (OSS client) | MIT | — |
| **Ente** | Flutter/Go | 15k+ | End-to-end encrypted photos (OSS) | AGPL-3.0 | https://github.com/ente-io/ente |
| **Shifu** | Go | 1k+ | Kubernetes-native IoT development framework | Apache-2.0 | https://github.com/Edgenesis/shifu |
| **MojoAuth** | — | — | Passwordless authentication (OSS SDK) | Apache-2.0 | — |
| **Boxyhq** | TypeScript | 3k+ | Enterprise SSO and directory sync | Apache-2.0 | https://github.com/boxyhq/jackson |
| **OpenMetadata** | Java | 5k+ | Open metadata management (India-founded) | Apache-2.0 | https://github.com/open-metadata/OpenMetadata |

---

## Updated Summary Statistics

| Category | Tools Count | — |
|----------|-------------|---------|
| Sections 1–60 (original) | ~4800+ | — |
| Kailash Nadh Personal Projects (§61) | 50+ | — |
| Zerodha Full Updated Stack (§62) | 75+ | — |
| Mailchimp/Chargebee OSS Alternatives (§63a) | 12+ | — |
| HashiCorp-alike OSS Tools (§63b) | 10+ | — |
| Supabase/PocketBase Ecosystem (§63c) | 12+ | — |
| Grafana Labs OSS (§63d) | 10+ | — |
| CNCF Graduated Projects (§63e) | 20+ | — |
| Linux Foundation Projects (§63f) | 13+ | — |
| Apache Software Foundation (§63g) | 22+ | — |
| Self-Hosting / HomeLab (§63h) | 38+ | — |
| Dev Tools by Small OSS Teams (§63i) | 34+ | — |
| Zerodha Dev Personal Projects (§64-66) | 20+ | — |
| **GRAND TOTAL (Part 1 + Part 2)** | **~3200+** | — |

---

> **Zero Vendor Lock-in Principle:** Every tool marked with an OSS license is self-hostable, forkable, and free from proprietary lock-in. Tools marked "Proprietary (free tier)" are included for completeness but are not recommended if lock-in-free is a hard requirement.

> **Note on origin:** A number of the tools above (Zerodha's stack, Hasura, Chatwoot, Frappe/ERPNext, Plane, Ente, and others) come out of the Indian OSS ecosystem — included here on technical merit, called out because it's a genuinely underrated source of production-grade FOSS.

Star counts and license labels throughout this document are approximate as of when each section was compiled — verify current numbers and license terms before relying on them for a production or commercial decision.


---

# Part 3: Unique & Notable Repos — A Systems Engineer's Learning Collection

> A hand-curated collection of ~1,066 repos picked for having a genuinely novel idea, an interesting architecture, or real production value — not for popularity. Good for browsing when you want to learn how something is actually built, not just find a tool to install.

## Table of Contents

- [AI / ML / Agents](#ai-ml-agents)
- [Security & Recon](#security-recon)
- [Storage & Databases](#storage-databases)
- [Networking & Infra](#networking-infra)
- [Messaging & Queues](#messaging-queues)
- [Systems & Low-Level](#systems-low-level)
- [Dev Tooling & CLI](#dev-tooling-cli)
- [Go Ecosystem](#go-ecosystem)
- [Tiny JS Libraries](#tiny-js-libraries)
- [Self-Hosted Apps & Platforms](#self-hosted-apps-platforms)
- [Mobile & Flutter/Android](#mobile-flutterandroid)
- [Payments & Fintech](#payments-fintech)
- [Geospatial & Maps](#geospatial-maps)
- [IoT & Embedded](#iot-embedded)
- [Indic Language & Local Computing](#indic-language-local-computing)
- [Laravel / PHP Ecosystem](#laravel-php-ecosystem)
- [Frappe / Zerodha Ecosystem](#frappe-zerodha-ecosystem)
- [Knadh Personal Projects](#knadh-personal-projects)
- [Awesome-Lists & Resources](#awesome-lists-resources)
- [Miscellaneous Notable Repos](#miscellaneous-notable-repos)
- [Other Tools Referenced (name only — link not independently verified)](#other-tools-referenced-name-only--link-not-independently-verified)

## AI / ML / Agents

| Repo | Description | Link |
|------|-------------|------|
| **activepieces** | AI agents + MCP + workflow automation, ~400 MCP servers. Open-source alternative to Zapier/Make with AI-first design. | [↗](https://github.com/activepieces/activepieces) |
| **Aditya-ds-1806/dictpress-tts** | TTS plugin for dictpress | [↗](https://github.com/Aditya-ds-1806/dictpress-tts) |
| **aesthetics** | Image Aesthetics Toolkit with Fisher Vector implementation and AVA dataset downloader. | [↗](https://github.com/ylogx/aesthetics) |
| **agentfield** | Build, run, scale AI agents like APIs and microservices — observable, auditable, identity-aware from day one. | [↗](https://github.com/Agent-Field/agentfield) |
| **agents** | Cloudflare's framework for building and deploying AI agents on their edge network. Distributed agent infra. | [↗](https://github.com/cloudflare/agents) |
| **anthropics/knowledge-work-plugins** | Open-source plugins for Claude Cowork | [↗](https://github.com/anthropics/knowledge-work-plugins) |
| **anything-llm** | All-in-one on-device AI productivity — local LLMs, privacy-first, no setup. Self-hosted ChatGPT. | [↗](https://github.com/Mintplex-Labs/anything-llm) |
| **apache/beam** | Apache Beam — unified batch and streaming data processing model — runs on Spark Flink Dataflow | [↗](https://github.com/apache/beam) |
| **Budibase/budibase** | AI agents/automations/apps for operations (low-code) | [↗](https://github.com/Budibase/budibase) |
| **claude-fleet** | Run hundreds of Claude Code sessions concurrently. Parallel AI agent orchestration at batch scale. | [↗](https://github.com/nammayatri/claude-fleet) |
| **coroot/coroot** | Coroot — eBPF-based APM with AI root cause analysis — metrics logs traces profiling in one tool | [↗](https://github.com/coroot/coroot) |
| **dataelement/bisheng** | Open LLM devops platform for enterprise AI (RAG/agent/workflow) | [↗](https://github.com/dataelement/bisheng) |
| **detectron2** | Facebook's object detection + segmentation platform. The reference for CV research implementation. | [↗](https://github.com/facebookresearch/detectron2) |
| **dialog** | RAG LLM Ops app for easy deployment and testing. Prod-ready RAG pipeline with observability. | [↗](https://github.com/talkdai/dialog) |
| **dopamine** | Google's RL research framework for fast prototyping of reinforcement learning algorithms. | [↗](https://github.com/google/dopamine) |
| **fish-speech** | State-of-the-art open-source TTS. Clone voices, generate speech. Production-quality. | [↗](https://github.com/fishaudio/fish-speech) |
| **FoundationDB/fdb-record-layer** | FDB Record Layer — structured layer on FoundationDB — used at Apple for CloudKit data model | [↗](https://github.com/FoundationDB/fdb-record-layer) |
| **going-doer/Paper2Code** | Automate code generation from ML research papers | [↗](https://github.com/going-doer/Paper2Code) |
| **Hannibal046/Awesome-LLM** | Curated list of Large Language Model resources | [↗](https://github.com/Hannibal046/Awesome-LLM) |
| **hodor** | Agentic code reviewer for GitHub PRs — multi-step reasoning, catches bugs needing cross-file analysis. | [↗](https://github.com/mr-karan/hodor) |
| **immich-app/immich** | Immich — self-hosted Google Photos alternative — mobile backup ML face recognition shared albums | [↗](https://github.com/immich-app/immich) |
| **karpathy/autoresearch** | AI agents for automated research on single-GPU training | [↗](https://github.com/karpathy/autoresearch) |
| **karpathy/nanoGPT** | Simplest fastest repo for training/finetuning GPTs | [↗](https://github.com/karpathy/nanoGPT) |
| **langdrive** | Train LLMs on private data via API call. Simple training endpoint abstraction. | [↗](https://github.com/addy-ai/langdrive) |
| **LEANN** | 97% storage savings for RAG on personal devices. MLsys 2026 research paper implementation — cutting edge private RAG. | [↗](https://github.com/yichuan-w/LEANN) |
| **lutzroeder/netron** | Neural network and ML model visualizer | [↗](https://github.com/lutzroeder/netron) |
| **map-anything** | Universal feed-forward metric 3D reconstruction from Meta. Neural 3D mapping. | [↗](https://github.com/facebookresearch/map-anything) |
| **marimo** | Reactive Python notebook — cells auto-rerun when dependencies change. Git-friendly, deployable as app. Better Jupyter. | [↗](https://github.com/marimo-team/marimo) |
| **mem0** | Universal memory layer for AI agents — persistent structured memory across sessions. Core infra for stateful agents. | [↗](https://github.com/mem0ai/mem0) |
| **metaflow** | Netflix's framework for building, managing, deploying AI/ML systems. Production ML workflow tool. | [↗](https://github.com/Netflix/metaflow) |
| **mlflow** | The open-source AI/ML engineering platform. Track experiments, evaluate LLMs, deploy models. De facto standard. | [↗](https://github.com/mlflow/mlflow) |
| **mvdust3r** | Single-stage 3D scene reconstruction from sparse views in 2 seconds. Meta Reality Labs research. | [↗](https://github.com/facebookresearch/mvdust3r) |
| **nautex** | MCP server guiding coding agents through requirements → implementation plan pipeline. Agent-native dev tooling. | [↗](https://github.com/hmldns/nautex) |
| **neurolink** | Juspay's streaming AI platform with token management. Research into AI inference economics. | [↗](https://github.com/juspay/neurolink) |
| **NousResearch/hermes-agent** | AI agent framework | [↗](https://github.com/NousResearch/hermes-agent) |
| **ocean** | Meta's in-house CV + AR framework in C++. Platform-independent CV at Meta scale. | [↗](https://github.com/facebookresearch/ocean) |
| **ocrmypdf/OCRmyPDF** | Add OCR text layer to scanned PDFs | [↗](https://github.com/ocrmypdf/OCRmyPDF) |
| **open-policy-agent/opa** | OPA — Open Policy Agent — general-purpose policy engine for Kubernetes API authz cloud config | [↗](https://github.com/open-policy-agent/opa) |
| **open-webui** | User-friendly AI interface supporting Ollama, OpenAI API, and others. The de facto local AI UI. | [↗](https://github.com/open-webui/open-webui) |
| **opendataloader-project/opendataloader-pdf** | PDF parser for AI-ready data | [↗](https://github.com/opendataloader-project/opendataloader-pdf) |
| **opensearch-ai** | Perplexity clone but personalised. SearchGPT pattern open-sourced. | [↗](https://github.com/supermemoryai/opensearch-ai) |
| **PaddleOCR** | Powerful OCR toolkit — 100+ languages, bridges images/PDFs to LLMs. Turn any doc into structured data. | [↗](https://github.com/PaddlePaddle/PaddleOCR) |
| **photoprism/photoprism** | PhotoPrism — AI photo manager self-hosted — face recognition geotagging EXIF WebDAV | [↗](https://github.com/photoprism/photoprism) |
| **pistoBot** | Create an AI that chats like you — fine-tune on your own chat history. Personal AI twin. | [↗](https://github.com/pistocop/pistoBot) |
| **PrivacyGuard** | Facebook Research: privacy attack analysis on ML models — membership inference, extraction attacks. Defensive ML security. | [↗](https://github.com/facebookresearch/PrivacyGuard) |
| **pyre-check** | Facebook's performant Python type checker. Understand how static analysis at scale works. | [↗](https://github.com/facebook/pyre-check) |
| **pyrefly** | Facebook's new fast Python type checker and language server. Compare with pyre-check — different approach. | [↗](https://github.com/facebook/pyrefly) |
| **react-doctor** | Let coding agents diagnose and fix React code. Agent-native debugging tool. | [↗](https://github.com/millionco/react-doctor) |
| **rhnvrm/pi-mesh** | Multi-agent coordination for Pi — presence messaging file reservations | [↗](https://github.com/rhnvrm/pi-mesh) |
| **rhnvrm/stock-market-circulars** | Automated processing and publishing of NSE/BSE/SEBI regulatory circulars with AI summaries | [↗](https://github.com/rhnvrm/stock-market-circulars) |
| **safishamsi/graphify** | AI coding assistant skill – turn code/schemas into queryable graphs | [↗](https://github.com/safishamsi/graphify) |
| **sentrysearch** | Semantic video search using Gemini Embedding / Qwen3-VL. Novel multimodal search use case. | [↗](https://github.com/ssrajadh/sentrysearch) |
| **skales** | Local AI desktop agent for Windows/macOS/Linux — multi-agent teams, 15+ providers, no Docker. | [↗](https://github.com/skalesapp/skales) |
| **stevelaskaridis/awesome-mobile-llm** | Awesome Mobile LLMs collection | [↗](https://github.com/stevelaskaridis/awesome-mobile-llm) |
| **system-prompts-and-models-of-ai-tools** | Leaked/reverse-engineered system prompts of Cursor, Claude Code, Devin, Copilot, Windsurf, etc. Competitive intelligence for AI tools. | [↗](https://github.com/x1xhlol/system-prompts-and-models-of-ai-tools) |
| **usestrix/strix** | Open-source AI vulnerability finding and fixing | [↗](https://github.com/usestrix/strix) |
| **Vane** | AI-powered answering engine — a Perplexity-style search+answer system. | [↗](https://github.com/ItzCrazyKns/Vane) |
| **viveknaskar/everything-ai-ml** | Curated AI/ML/LLM/RAG learning resources | [↗](https://github.com/viveknaskar/everything-ai-ml) |
| **voicebox** | Open-source AI voice studio — clone, dictate, create voices. Full voice AI pipeline. | [↗](https://github.com/jamiepine/voicebox) |
| **zerodha/gchatgpt** | Google Chat bot for OpenAI ChatGPT | [↗](https://github.com/zerodha/gchatgpt) |

---

## Security & Recon

| Repo | Description | Link |
|------|-------------|------|
| **ajinasokan/flutter_local_auth** | Flutter local auth for devices without fingerprint flag | [↗](https://github.com/ajinasokan/flutter_local_auth) |
| **appwrite/appwrite** | Appwrite — open-source backend platform — databases auth storage functions messaging all-in-one | [↗](https://github.com/appwrite/appwrite) |
| **aquasecurity/tracee** | Tracee — eBPF-based runtime security and forensics — detects suspicious syscall patterns at kernel level | [↗](https://github.com/aquasecurity/tracee) |
| **Bubka/2FAuth** | Web app to manage 2FA accounts and generate security codes | [↗](https://github.com/Bubka/2FAuth) |
| **casdoor** | Agent-first IAM / SSO server. Supports MCP, OAuth, OIDC, SAML, LDAP, WebAuthn, Face ID all in one. Very complete. | [↗](https://github.com/casdoor/casdoor) |
| **cert-manager/cert-manager** | cert-manager — Kubernetes TLS certificate controller — auto-renew from Let's Encrypt Vault ACME | [↗](https://github.com/cert-manager/cert-manager) |
| **chriskiehl/netstat-open-source** | Similar: suricata/suricata — open-source IDS/IPS network security monitoring engine | [↗](https://github.com/chriskiehl/netstat-open-source) |
| **cilium/cilium** | Cilium — eBPF-based Kubernetes networking observability and security — replaces kube-proxy at scale | [↗](https://github.com/cilium/cilium) |
| **cilium/hubble** | Hubble — eBPF-based network and security observability for Kubernetes built on Cilium | [↗](https://github.com/cilium/hubble) |
| **cockpit-project/cockpit** | Cockpit — web-based Linux server admin UI — manages services storage networking firewall from browser | [↗](https://github.com/cockpit-project/cockpit) |
| **CyberChef** | GCHQ's cyber Swiss army knife — encode, decode, encrypt, analyse in-browser without any install. | [↗](https://github.com/gchq/CyberChef) |
| **external-secrets/external-secrets** | External Secrets Operator — sync secrets from Vault AWS SSM GCP into Kubernetes Secrets | [↗](https://github.com/external-secrets/external-secrets) |
| **falcosecurity/falco** | Falco — runtime security using eBPF and syscall tracing — detects anomalous container behavior | [↗](https://github.com/falcosecurity/falco) |
| **infisical** | Open-source secrets + certificates + privileged access management. More complete than Vault for most teams, easier to self-host. | [↗](https://github.com/Infisical/infisical) |
| **iris-web** | Collaborative incident response platform. Manage IR workflows, timelines, IOCs, evidence as a team. | [↗](https://github.com/dfir-iris/iris-web) |
| **kiln** | Encrypt, share, and run with secure environment variables from CLI. Solves secrets in CI/CD pipelines elegantly. | [↗](https://github.com/Thunderbottom/kiln) |
| **laravel/breeze** | Minimal Laravel auth scaffolding (Blade/Vue/React + Tailwind) | [↗](https://github.com/laravel/breeze) |
| **laravel/breeze-next** | Breeze auth starter kit frontend in Next.js | [↗](https://github.com/laravel/breeze-next) |
| **laravel/fortify** | Backend controllers/scaffolding for Laravel auth | [↗](https://github.com/laravel/fortify) |
| **laravel/jetstream** | Tailwind scaffolding for Laravel with teams and 2FA | [↗](https://github.com/laravel/jetstream) |
| **laravel/sanctum** | Featherweight auth system for SPAs and simple APIs | [↗](https://github.com/laravel/sanctum) |
| **laravel/socialite** | OAuth 1 and 2 social authentication for Laravel | [↗](https://github.com/laravel/socialite) |
| **lfi-to-rce-scenario** | Dockerized intentionally vulnerable PHP app showing LFI→RCE exploit chain. Study the attack to defend against it. | [↗](https://github.com/moeinfatehi/lfi-to-rce-scenario) |
| **mantis** | PhonePe's security framework: discovery → recon → vuln scanning pipeline. Automated, chained recon. | [↗](https://github.com/PhonePe/mantis) |
| **nhost/nhost** | nhost — open-source Firebase alternative with GraphQL — Hasura + Auth + Storage + Functions | [↗](https://github.com/nhost/nhost) |
| **otpgateway** | Standalone server for OTP + address verification with pluggable providers — SMS, email, bank penny drop. Pluggable design. | [↗](https://github.com/knadh/otpgateway) |
| **passetto** | Simple encryption service by Juspay. Microservice for encrypting/decrypting data — useful pattern for PCI compliance. | [↗](https://github.com/juspay/passetto) |
| **PayloadsAllTheThings** | Curated payloads and bypasses for web app security. The reference for pentesters doing manual testing. | [↗](https://github.com/swisskyrepo/PayloadsAllTheThings) |
| **reconftw** | Automated full recon pipeline — runs best-of-breed tools in sequence for a target domain. | [↗](https://github.com/six2dez/reconftw) |
| **sessy** | Open-source email observability for AWS SES — see deliverability, bounces, complaints you'd normally be blind to. | [↗](https://github.com/marckohlbrugge/sessy) |
| **supabase/supabase** | Supabase — open-source Firebase alternative — Postgres + Auth + Storage + Realtime + Edge Functions | [↗](https://github.com/supabase/supabase) |
| **tetragon/tetragon** | Tetragon — eBPF security observability and runtime enforcement — Cilium's security layer | [↗](https://github.com/tetragon/tetragon) |
| **threat-forge** | Open-source threat modeling with canvas UI, YAML files, AI STRIDE analysis. The missing open alternative to Microsoft TMT. | [↗](https://github.com/exit-zero-labs/threat-forge) |
| **UTMStack** | Enterprise SIEM + SOAR + compliance in one stack. Real-time correlation, threat intel, incident response. | [↗](https://github.com/utmstack/UTMStack) |
| **vaib25vicky/awesome-mobile-security** | Android and iOS security resources and tools | [↗](https://github.com/vaib25vicky/awesome-mobile-security) |
| **vault** | HashiCorp Vault — the reference secrets management tool. Encryption as a service, dynamic secrets, PKI. | [↗](https://github.com/hashicorp/vault) |
| **vinifera** | GitHub recon/monitoring for finding internal leaks in your own org. Defensive OSINT tool from Zomato. | [↗](https://github.com/Zomato/vinifera) |
| **wazuh** | Open-source unified XDR + SIEM. Endpoint detection, log analysis, compliance — enterprise-grade, fully free. | [↗](https://github.com/wazuh/wazuh) |
| **web-check** | All-in-one OSINT for any URL — DNS, headers, SSL, ports, tech stack, trackers, all at once. | [↗](https://github.com/Lissy93/web-check) |
| **willkk/opendrm** | Open-source DRM/Key System implementation | [↗](https://github.com/willkk/opendrm) |

---

## Storage & Databases

| Repo | Description | Link |
|------|-------------|------|
| **advcopy** | Postgres extension to COPY data directly to/from S3. Extends Postgres SQL with cloud storage awareness. | [↗](https://github.com/satya10x/advcopy) |
| **apache/pulsar** | Apache Pulsar — distributed pub-sub messaging — decouples compute and storage unlike Kafka | [↗](https://github.com/apache/pulsar) |
| **apache/superset** | Apache Superset — modern open-source BI and data exploration platform — SQL-first dashboards | [↗](https://github.com/apache/superset) |
| **barreldb** | Bitcask paper implemented in Go. Learn append-only log storage, hash index, compaction — the real internals of fast KV stores. | [↗](https://github.com/mr-karan/barreldb) |
| **ceph/ceph** | Ceph — unified distributed object block and file storage — no single point of failure used in Proxmox and OpenStack | [↗](https://github.com/ceph/ceph) |
| **chrislusf/seaweedfs** | SeaweedFS (canonical) — fast distributed storage blobs objects files data lake billions of files | [↗](https://github.com/chrislusf/seaweedfs) |
| **citusdata/citus** | Citus — PostgreSQL extension for horizontal sharding and distributed queries — turns Postgres into distributed DB | [↗](https://github.com/citusdata/citus) |
| **ClickHouse/ClickHouse** | ClickHouse — fastest open-source columnar OLAP database — 100x faster than Postgres for analytical queries | [↗](https://github.com/ClickHouse/ClickHouse) |
| **cloudserver** | Node.js implementation of the Amazon S3 protocol, works with Azure and GCP backends. Teaches S3 API design. | [↗](https://github.com/scality/cloudserver) |
| **cockroachdb/cockroach** | CockroachDB — distributed fault-tolerant SQL on transactional KV store — survives datacenter failure with ACID | [↗](https://github.com/cockroachdb/cockroach) |
| **cube-js/cube** | Cube — semantic layer for data — headless BI translating SQL across databases with caching | [↗](https://github.com/cube-js/cube) |
| **DatabendLabs/databend** | Databend — elastic cloud-native data warehouse in Rust — S3 as storage layer serverless query engine | [↗](https://github.com/DatabendLabs/databend) |
| **dbt-labs/dbt-core** | dbt-core — SQL-first data transformation — build test document analytics engineering models | [↗](https://github.com/dbt-labs/dbt-core) |
| **delta-io/delta** | Delta Lake — open-source ACID table storage layer on data lakes — Databricks open standard | [↗](https://github.com/delta-io/delta) |
| **dhamaniasad/awesome-postgres** | Curated PostgreSQL software libraries and tools | [↗](https://github.com/dhamaniasad/awesome-postgres) |
| **duckdb/duckdb** | DuckDB — in-process OLAP database — runs inside Python Go R no server blazing fast for analytics | [↗](https://github.com/duckdb/duckdb) |
| **dungbeetle** | Distributed job server for **heavy SQL read jobs only** — queues reporting queries, separates them from OLTP. Real architectural pattern. | [↗](https://github.com/zerodha/dungbeetle) |
| **duplicati/duplicati** | Duplicati — backup to cloud services — AES-256 deduplication supports S3 B2 OneDrive SFTP | [↗](https://github.com/duplicati/duplicati) |
| **elasticsearch** | The reference distributed full-text search engine. Read it to understand inverted indexes, sharding, and relevance scoring. | [↗](https://github.com/elastic/elasticsearch) |
| **foundationdb** | Apple's distributed transactional KV store. Powers iCloud. Unique: ACID transactions across a distributed KV — rare combination. | [↗](https://github.com/apple/foundationdb) |
| **garage** | S3-compatible object store for **small, geo-distributed** self-hosted deployments. Unlike MinIO which wants big infra. | [↗](https://github.com/deuxfleurs-org/garage) |
| **gluster/glusterfs** | GlusterFS — scale-out network-attached filesystem — POSIX distributed storage bricks and volumes | [↗](https://github.com/gluster/glusterfs) |
| **gnata** | Pure-Go JSONata 2.x for high-throughput streaming. JSONata is the JSON query language — this impl handles streams. | [↗](https://github.com/RecoLabs/gnata) |
| **goyesql** | Parse SQL files with named queries into structs. Keeps SQL out of Go code, in `.sql` files, queryable by name. | [↗](https://github.com/knadh/goyesql) |
| **grafana/mimir** | Grafana Mimir — horizontally scalable Prometheus — long-term metrics storage with object store backend | [↗](https://github.com/grafana/mimir) |
| **grafana/tempo** | Grafana Tempo — distributed tracing backend — ingest store query traces at scale with S3 backend | [↗](https://github.com/grafana/tempo) |
| **hasura/graphql-engine** | Hasura — instant GraphQL and REST APIs over Postgres — introspects schema generates APIs | [↗](https://github.com/hasura/graphql-engine) |
| **iamd3vil/blobasaur** | Blob store on SQLite with Redis protocol compatibility | [↗](https://github.com/iamd3vil/blobasaur) |
| **juicedata/juicefs** | JuiceFS — POSIX-compatible distributed filesystem on top of object storage (S3/Redis/Postgres) — HDFS alternative | [↗](https://github.com/juicedata/juicefs) |
| **lancedb** | Embedded vector DB for multimodal AI — no server, runs inside your app like SQLite but for embeddings. | [↗](https://github.com/lancedb/lancedb) |
| **logchef** | Single-binary log analytics on ClickHouse. Query logs with SQL, no Kibana/Elasticsearch complexity. | [↗](https://github.com/mr-karan/logchef) |
| **MaterializeInc/materialize** | Materialize — streaming SQL database that maintains live views — real-time materialized views on streaming data | [↗](https://github.com/MaterializeInc/materialize) |
| **minio/minio** | MinIO — high-performance S3-compatible object storage (now AGPL — check license for use case) | [↗](https://github.com/minio/minio) |
| **OpenObserve/openobserve** | OpenObserve — logs metrics traces in Rust — 140x lower storage cost than Elasticsearch | [↗](https://github.com/OpenObserve/openobserve) |
| **pingcap/tidb** | TiDB — distributed HTAP database — MySQL-compatible horizontal scaling separates compute and storage | [↗](https://github.com/pingcap/tidb) |
| **postgres_for_everything** | Not a tool — a philosophy repo. Argues and shows how Postgres replaces Redis, queues, search, cron, etc. Architecture thinking. | [↗](https://github.com/Olshansk/postgres_for_everything) |
| **punisher** | Load-test / stress-test your database. Unique name, real use: see how your DB breaks before prod does. | [↗](https://github.com/mbulat/punisher) |
| **questdb/questdb** | QuestDB — high-performance time-series DB — SQL with nanosecond precision fastest ingestion in class | [↗](https://github.com/questdb/questdb) |
| **quickwit-oss/quickwit** | Quickwit — cloud-native log search on object storage — Elasticsearch alternative with S3 as storage layer | [↗](https://github.com/quickwit-oss/quickwit) |
| **rclone/rclone** | rclone — rsync for cloud storage — sync to S3 GCS Azure SFTP 70+ backends command line | [↗](https://github.com/rclone/rclone) |
| **restic/restic** | restic — fast encrypted deduplicated backup to S3 SFTP B2 local — incremental immutable backups | [↗](https://github.com/restic/restic) |
| **risingwavelabs/risingwave** | RisingWave — distributed SQL database for stream processing — PostgreSQL-compatible real-time analytics | [↗](https://github.com/risingwavelabs/risingwave) |
| **rustfs** | S3-compatible object storage in Rust — claims 2.3x faster than MinIO for small objects. Alternative implementation study. | [↗](https://github.com/rustfs/rustfs) |
| **seaweedfs/seaweedfs** | SeaweedFS — distributed storage for billions of objects with O(1) disk access S3/POSIX/FUSE support | [↗](https://github.com/seaweedfs/seaweedfs) |
| **shridarpatil/postal_db** | Indian Pincode database for Frappe | [↗](https://github.com/shridarpatil/postal_db) |
| **StarRocks/starrocks** | StarRocks — MPP analytical database — real-time analytics with native vectorized execution sub-second queries | [↗](https://github.com/StarRocks/starrocks) |
| **storj/storj** | Storj — decentralized encrypted cloud object storage — S3-compatible geo-distributed affordable | [↗](https://github.com/storj/storj) |
| **taosdata/TDengine** | TDengine — open-source time-series database optimized for IoT and industrial telemetry — 10x faster than InfluxDB | [↗](https://github.com/taosdata/TDengine) |
| **thanos-io/thanos** | Thanos — highly available Prometheus with long-term storage — sidecar federation global query view | [↗](https://github.com/thanos-io/thanos) |
| **timescale/timescaledb** | TimescaleDB — PostgreSQL extension for time-series — SQL with automatic partitioning compression | [↗](https://github.com/timescale/timescaledb) |
| **treeverse/lakeFS** | lakeFS — Git-like version control for object storage (S3 GCS Azure) — branch commit rollback for data | [↗](https://github.com/treeverse/lakeFS) |
| **trino** | Distributed SQL query engine for big data (ex-PrestoSQL). Federated queries across Hive, S3, Postgres, etc. in one SQL. | [↗](https://github.com/trinodb/trino) |
| **valkey** | The Redis fork after the license switch, now under Linux Foundation. Fully Redis-compatible, community-driven. | [↗](https://github.com/valkey-io/valkey) |
| **VictoriaMetrics/VictoriaMetrics** | VictoriaMetrics — fast cost-effective monitoring with PromQL — better long-term storage than Prometheus | [↗](https://github.com/VictoriaMetrics/VictoriaMetrics) |
| **yesqlr** | Same concept as goyesql but in Rust. See how the same idea is expressed in two languages. | [↗](https://github.com/knadh/yesqlr) |
| **yugabyte/yugabyte-db** | YugabyteDB — distributed SQL on Spanner-inspired architecture — PostgreSQL and Cassandra APIs | [↗](https://github.com/yugabyte/yugabyte-db) |
| **zerodha/frappe-attachments-s3** | Upload Frappe doctype attachments to S3 | [↗](https://github.com/zerodha/frappe-attachments-s3) |

---

## Networking & Infra

| Repo | Description | Link |
|------|-------------|------|
| **AdguardTeam/AdGuardHome** | AdGuard Home — network-wide DNS-based blocker — more features than Pi-hole DoH DoT support | [↗](https://github.com/AdguardTeam/AdGuardHome) |
| **caddy** | Web server with **automatic HTTPS** built-in. Handles cert renewal, ACME, HTTP/1-2-3 all in one binary. | [↗](https://github.com/caddyserver/caddy) |
| **envoyproxy/envoy** | Envoy — cloud-native edge and service proxy — L7 proxy used in Istio Consul service meshes | [↗](https://github.com/envoyproxy/envoy) |
| **fastcache** | HTTP response caching middleware for fastglue. "Dumb" caching — minimal logic, maximum speed. | [↗](https://github.com/zerodha/fastcache) |
| **fastglue** | Micro framework wrapping fasthttp + fasthttprouter. Teaches you how to build opinionated wrappers on top of raw libs. | [↗](https://github.com/zerodha/fastglue) |
| **fasthttp** | Go HTTP package with zero memory allocations in hot paths. Up to 10x faster than `net/http`. How? Avoids GC pressure by reusing objects. | [↗](https://github.com/valyala/fasthttp) |
| **fatedier/frp** | frp — fast reverse proxy to expose local servers behind NAT — HTTP HTTPS TCP UDP tunneling | [↗](https://github.com/fatedier/frp) |
| **FerretDB/FerretDB** | FerretDB — MongoDB wire protocol proxy over PostgreSQL — truly open-source MongoDB alternative | [↗](https://github.com/FerretDB/FerretDB) |
| **gnet** | Event-driven, non-blocking networking in pure Go. Reactor pattern implementation — different mental model from standard Go concurrency. | [↗](https://github.com/panjf2000/gnet) |
| **gravitl/netmaker** | Netmaker — WireGuard-based virtual network platform — automates mesh VPN across clouds and on-prem | [↗](https://github.com/gravitl/netmaker) |
| **hashicorp/consul** | Consul — service discovery and service mesh — KV store health check DNS interface multi-datacenter | [↗](https://github.com/hashicorp/consul) |
| **jc21/nginx-proxy-manager** | Nginx Proxy Manager — web UI for reverse proxy and SSL — easy Nginx frontend for self-hosters | [↗](https://github.com/jc21/nginx-proxy-manager) |
| **lura** | Ultra-performant API Gateway in Go, Linux Foundation project. Not Nginx, not Kong — a composable gateway in code. | [↗](https://github.com/luraproject/lura) |
| **nbio** | Pure Go 1M+ connections solution. TLS, HTTP1, WebSocket. Non-blocking I/O model study. | [↗](https://github.com/lesismal/nbio) |
| **nicholasess/pihole** | Pi-hole — network-wide DNS ad blocker — blocks ads at DNS level for all devices on network | [↗](https://github.com/nicholasess/pihole) |
| **nyquist/awesome-networking** | Curated list of computer networking resources | [↗](https://github.com/nyquist/awesome-networking) |
| **openstack/openstack** | OpenStack — open-source cloud OS managing compute storage networking across datacenter racks | [↗](https://github.com/openstack/openstack) |
| **poweradmin/poweradmin** | Poweradmin — web-based DNS management interface for PowerDNS — manage zones records from browser | [↗](https://github.com/poweradmin/poweradmin) |
| **PowerDNS/pdns** | PowerDNS — authoritative DNS server + recursor — used at scale with multiple database backends | [↗](https://github.com/PowerDNS/pdns) |
| **SagerNet/sing-box** | sing-box — universal proxy platform — VLESS VMess Trojan shadowsocks all in one | [↗](https://github.com/SagerNet/sing-box) |
| **tailscale/tailscale** | Tailscale — WireGuard-based mesh VPN — zero-config peer-to-peer overlay network NAT traversal | [↗](https://github.com/tailscale/tailscale) |
| **traefik** | Cloud-native reverse proxy with **auto service discovery** for containers. Reads Docker labels → configures itself. | [↗](https://github.com/traefik/traefik) |
| **turbo** | SPA speed without JavaScript — HTML over the wire. Different paradigm: server renders, Turbo patches the DOM. | [↗](https://github.com/hotwired/turbo) |
| **websocket** | Gorilla WebSocket — the reference Go WebSocket impl. Read the source to understand the WS handshake and framing protocol. | [↗](https://github.com/gorilla/websocket) |
| **yusing/godoxy** | High-performance reverse proxy and container orchestrator | [↗](https://github.com/yusing/godoxy) |
| **zuul** | Netflix's gateway service — dynamic routing, resiliency, security. The OG API gateway pattern paper. | [↗](https://github.com/Netflix/zuul) |

---

## Messaging & Queues

| Repo | Description | Link |
|------|-------------|------|
| **apache/kafka** | Apache Kafka — distributed event streaming platform — de facto backbone for data pipelines at scale | [↗](https://github.com/apache/kafka) |
| **element-hq/element-web** | Element — Matrix client for web — reference frontend for decentralized E2E messaging | [↗](https://github.com/element-hq/element-web) |
| **franz-go** | Feature-complete pure-Go Kafka client from 0.8 through 4.2+. Implements the full Kafka protocol — great protocol study. | [↗](https://github.com/twmb/franz-go) |
| **Haraka** | Fast, event-driven SMTP server in Node.js. Extensible plugin system. Understand how email servers actually work. | [↗](https://github.com/haraka/Haraka) |
| **hedwig** | Minimalist high-performance SMTP server. Contrast with Haraka — two different design philosophies for same problem. | [↗](https://github.com/iamd3vil/hedwig) |
| **kaf-relay** | Replicate Kafka topics between clusters in real-time with hot failovers and topic remapping. Solves multi-cluster Kafka ops. | [↗](https://github.com/zerodha/kaf-relay) |
| **laravel/vonage-notification-channel** | Vonage SMS notification channel for Laravel | [↗](https://github.com/laravel/vonage-notification-channel) |
| **maddy** | Composable all-in-one mail server. Handles SMTP, IMAP, auth, DKIM, DMARC — single binary mail stack. | [↗](https://github.com/foxcpp/maddy) |
| **matrix-org/synapse** | Synapse — reference Matrix homeserver in Python — federated decentralized messaging protocol | [↗](https://github.com/matrix-org/synapse) |
| **MQTTX** | All-in-one MQTT 5.0 client — desktop, CLI, WebSocket. Best tool for working with IoT/MQTT protocols. | [↗](https://github.com/emqx/MQTTX) |
| **mr-karan/calert** | Send Prometheus Alertmanager alerts to Google Chat | [↗](https://github.com/mr-karan/calert) |
| **nats-server** | High-performance cloud-native messaging. Simpler than Kafka, faster for many use cases. Used in edge/IoT/cloud at scale. | [↗](https://github.com/nats-io/nats-server) |
| **notification-service** | gRPC bidirectional streaming notification service using Redis Streams as broker. Real implementation of push notifications at scale. | [↗](https://github.com/nammayatri/notification-service) |
| **papercups-io/papercups** | Open-source live customer chat | [↗](https://github.com/papercups-io/papercups) |
| **postal** | Full-featured open-source mail delivery platform. Incoming + outgoing, bounce handling, webhooks — the full picture. | [↗](https://github.com/postalserver/postal) |
| **RocketChat/Rocket.Chat** | Secure open-source team messaging platform | [↗](https://github.com/RocketChat/Rocket.Chat) |
| **signalapp/Signal-Server** | Signal Server — reference E2E encrypted messaging server — sealed sender double ratchet protocol | [↗](https://github.com/signalapp/Signal-Server) |
| **smtppool** | High-throughput Go SMTP pool with graceful idle timeout and retry handling. The missing piece for bulk email sending. | [↗](https://github.com/knadh/smtppool) |
| **Tasqueue** | Background jobs library for Go with pluggable brokers — Redis, NATS, etc. Clean interface design for job queuing. | [↗](https://github.com/kalbhor/Tasqueue) |
| **The-Commit-Company/raven** | Simple open-source team messaging platform | [↗](https://github.com/The-Commit-Company/raven) |
| **wireapp/wire-server** | Wire — secure messaging server — federated E2E-encrypted real-time communication | [↗](https://github.com/wireapp/wire-server) |

---

## Systems & Low-Level

| Repo | Description | Link |
|------|-------------|------|
| **45drives/cockpit-zfs-manager** | Cockpit ZFS Manager — web UI for ZFS pool management on Linux via Cockpit | [↗](https://github.com/45drives/cockpit-zfs-manager) |
| **antlir** | Facebook's Linux image builder. Build reproducible, hermetic OS images. Used internally at Meta at massive scale. | [↗](https://github.com/facebookincubator/antlir) |
| **apkc** | Bare-bones Android build system **without Android Studio**. Build APKs from command line with minimal tooling. | [↗](https://github.com/ajinasokan/apkc) |
| **below** | Facebook's **time-traveling** Linux resource monitor. Record system state, scrub back in time. Invaluable for post-incident analysis. | [↗](https://github.com/facebookincubator/below) |
| **borgbackup/borg** | BorgBackup — deduplicating archiving backup with compression encryption — gold standard for Linux backup | [↗](https://github.com/borgbackup/borg) |
| **cadvisor** | Google's container resource usage analyzer. Understands cgroups, namespace isolation, and surfaces per-container metrics. | [↗](https://github.com/google/cadvisor) |
| **chaosmonkey** | Netflix's original chaos engineering tool. Randomly kills prod instances. The tool that invented the chaos engineering discipline. | [↗](https://github.com/Netflix/chaosmonkey) |
| **container** | Apple's tool for running Linux containers as lightweight VMs on Mac, written in Swift for Apple Silicon. Different approach from Docker Desktop. | [↗](https://github.com/apple/container) |
| **distroless** | Docker images **without the OS** — just your language runtime. Smallest attack surface possible. Google's approach to secure containers. | [↗](https://github.com/GoogleContainerTools/distroless) |
| **fboss** | Facebook's open-source network switch OS software. Controls real data center switches. Rare peek into hyperscaler networking stack. | [↗](https://github.com/facebook/fboss) |
| **FRRouting/frr** | FRRouting — free range routing — BGP OSPF IS-IS RIP EIGRP all in one Linux routing suite | [↗](https://github.com/FRRouting/frr) |
| **goharbor/harbor** | Harbor — CNCF container image registry with vulnerability scanning RBAC content trust replication | [↗](https://github.com/goharbor/harbor) |
| **humpback** | Lightweight platform for managing containerized services — simpler than k8s for small fleets. | [↗](https://github.com/humpback/humpback) |
| **iovisor/bcc** | BCC — toolkit for eBPF-based kernel tracing — create efficient kernel instrumentation in C and Python | [↗](https://github.com/iovisor/bcc) |
| **iovisor/bpftrace** | bpftrace — high-level tracing language for eBPF — like awk for the Linux kernel | [↗](https://github.com/iovisor/bpftrace) |
| **lima-vm/lima** | Lima — Linux VMs on macOS with auto file-sharing port-forwarding and containerd (like WSL2 for Mac) | [↗](https://github.com/lima-vm/lima) |
| **multipass/multipass** | Canonical Multipass — instant Ubuntu VMs on Mac Windows Linux with cloud-init support | [↗](https://github.com/multipass/multipass) |
| **mvm** | CLI to create sandbox microVMs from container images instantly. Faster and more isolated than containers alone. | [↗](https://github.com/cvhariharan/mvm) |
| **netbootxyz/netboot.xyz** | netboot.xyz — network boot OS installer — PXE boot any Linux distro Windows from one endpoint | [↗](https://github.com/netbootxyz/netboot.xyz) |
| **nicholasgasior/openvpn-install** | OpenVPN install script — one-command OpenVPN server setup on Linux | [↗](https://github.com/nicholasgasior/openvpn-install) |
| **proxmox/proxmox-ve** | ,Proxmox VE — open-source KVM + LXC hypervisor with web UI ZFS Ceph clustering live migration (proxmox.com) | [↗](https://github.com/proxmox/proxmox-ve) |
| **stuffbin** | Compress and embed static files into Go binaries with a virtual FS. How to ship single-binary Go apps with assets. | [↗](https://github.com/knadh/stuffbin) |
| **vates/xen-orchestra** | Xen Orchestra — web UI for XCP-ng and XenServer with full backup VM migration and pool management | [↗](https://github.com/vates/xen-orchestra) |
| **virt-manager/virt-manager** | virt-manager — desktop UI for managing KVM/QEMU VMs via libvirt on Linux | [↗](https://github.com/virt-manager/virt-manager) |
| **xcp-ng/xcp-ng** | ,XCP-ng — community-driven open-source fork of Citrix XenServer enterprise hypervisor with Xen kernel | [↗](https://github.com/xcp-ng/xcp-ng) |

---

## Dev Tooling & CLI

| Repo | Description | Link |
|------|-------------|------|
| **ansible/ansible** | Ansible — agentless IT automation over SSH — playbooks for config management deployment orchestration | [↗](https://github.com/ansible/ansible) |
| **approve-pr-creation-from-issue** | GitHub Action that forces contributors to get explicit approval before raising a PR. Governance automation. | [↗](https://github.com/knadh/approve-pr-creation-from-issue) |
| **argoproj/argo-cd** | ArgoCD — GitOps continuous delivery for Kubernetes — declarative desired state from Git | [↗](https://github.com/argoproj/argo-cd) |
| **autopilot** | Flutter QA test driver — tests without sharing source code. Black-box testing approach. | [↗](https://github.com/ajinasokan/autopilot) |
| **build-your-own-x** | Master programming by recreating your favorite technologies from scratch. The ultimate learning repo. | [↗](https://github.com/codecrafters-io/build-your-own-x) |
| **changedetection.io** | Website change detection — price drops, restock alerts, content changes, defacement monitoring. | [↗](https://github.com/dgtlmoon/changedetection.io) |
| **cluster-api/cluster-api** | Cluster API — declarative Kubernetes cluster lifecycle management — provision upgrade delete clusters as CRDs | [↗](https://github.com/cluster-api/cluster-api) |
| **containerd/containerd** | containerd — CNCF container runtime used by Kubernetes Docker and others as the standard CRI | [↗](https://github.com/containerd/containerd) |
| **crikket** | Instant bug reporting and feedback tool. Open-source jam.dev / marker.io alternative. | [↗](https://github.com/redpangilinan/crikket) |
| **crossplane/crossplane** | Crossplane — control plane framework — provision cloud infrastructure from Kubernetes YAML | [↗](https://github.com/crossplane/crossplane) |
| **damon** | Automate routine Nomad tasks by responding to cluster events. Event-driven Nomad ops automation. | [↗](https://github.com/Thunderbottom/damon) |
| **distribution/distribution** | OCI Distribution Spec — reference implementation of container registry — the protocol Docker Hub uses | [↗](https://github.com/distribution/distribution) |
| **dns.toys** | DNS server offering utilities over the DNS protocol — weather, time, unit conversion via `dig`. Mind-bending concept. | [↗](https://github.com/knadh/dns.toys) |
| **dnSpy** | .NET debugger and assembly editor. Decompile, edit, and debug .NET binaries live. | [↗](https://github.com/dnSpy/dnSpy) |
| **doggo** | Human-friendly command-line DNS client in Go. Like `dig` but readable output, colors, JSON. | [↗](https://github.com/mr-karan/doggo) |
| **dont.build** | Decision system for whether to build a software feature. Anti-tool — helps you NOT build things unnecessarily. | [↗](https://github.com/knadh/dont.build) |
| **dontspend.money** | Same anti-tool philosophy but for buying decisions. Interesting UX design pattern for decision tools. | [↗](https://github.com/realvinay/dontspend.money) |
| **easeprobe** | Standalone lightweight health/status checking tool in Go. Self-contained monitoring with notifications. | [↗](https://github.com/megaease/easeprobe) |
| **engineering-blogs** | Curated list of engineering blogs from top tech companies. Continuous learning feed. | [↗](https://github.com/kilimchoi/engineering-blogs) |
| **flannel-io/flannel** | Flannel — simple overlay network for Kubernetes — VXLAN-based pod networking easy to operate | [↗](https://github.com/flannel-io/flannel) |
| **flipper** | Facebook's desktop debugging platform for mobile developers. Inspect network, layout, DB, logs from one UI. | [↗](https://github.com/facebook/flipper) |
| **fluxcd/flux2** | Flux — CNCF GitOps toolkit for Kubernetes — reconciles cluster state from Git continuously | [↗](https://github.com/fluxcd/flux2) |
| **git-bars** | Visualise git commit activity as ASCII bars in terminal. Tiny, useful insight from git history. | [↗](https://github.com/knadh/git-bars) |
| **gotp** | Live-preview Go templates with custom data. Essential when debugging `text/template` or `html/template`. | [↗](https://github.com/vividvilla/gotp) |
| **grafana-export** | Downloads all Grafana dashboards and backs them to S3. Infra automation micro-tool. | [↗](https://github.com/Thunderbottom/grafana-export) |
| **gtbump** | Git tag bump + semantic versioning + Markdown changelog generator. One tool for release management. | [↗](https://github.com/knadh/gtbump) |
| **harvester/harvester** | SUSE Harvester — open-source HCI on Kubernetes using KubeVirt + Longhorn for VMs and storage | [↗](https://github.com/harvester/harvester) |
| **hashicorp/terraform** | Terraform — de facto IaC tool for multi-cloud provisioning (BSL license — OpenTofu for OSS) | [↗](https://github.com/hashicorp/terraform) |
| **healthchecks** | Open-source cron job monitoring — pings to verify jobs ran on time. The "dead man's switch" for cron. | [↗](https://github.com/healthchecks/healthchecks) |
| **helm/helm** | Helm — Kubernetes package manager — charts for deploying complex apps with versioned releases | [↗](https://github.com/helm/helm) |
| **home-assistant/core** | Home Assistant — open-source home automation — local-first 3000+ integrations no cloud required | [↗](https://github.com/home-assistant/core) |
| **hoppscotch** | Open-source Postman alternative — offline, on-prem, CLI. Lighter, faster, open. | [↗](https://github.com/hoppscotch/hoppscotch) |
| **hq** | jq/yq-like processor for HUML (a human-readable markup). Extends the jq idea to a new format. | [↗](https://github.com/rhnvrm/hq) |
| **iamd3vil/lift** | CLI client for Liftbridge messaging | [↗](https://github.com/iamd3vil/lift) |
| **influxdata/influxdb** | InfluxDB — open-source time-series platform — metrics events traces at scale used in IoT and DevOps | [↗](https://github.com/influxdata/influxdb) |
| **jadx** | Dex to Java decompiler. Reverse engineer Android APKs back to readable Java. | [↗](https://github.com/skylot/jadx) |
| **k3s-io/k3s** | K3s — lightweight certified Kubernetes for edge IoT homelab — single binary under 100MB | [↗](https://github.com/k3s-io/k3s) |
| **knadh/pfxsigner** | CLI + web server for digitally signing PDFs with PFX/PKCS#12 | [↗](https://github.com/knadh/pfxsigner) |
| **knadh/tuwunel-admin** | Web admin UI for tuwunel Matrix server | [↗](https://github.com/knadh/tuwunel-admin) |
| **kubespray/kubespray** | Kubespray — production-grade Kubernetes cluster via Ansible — bare metal cloud hybrid | [↗](https://github.com/kubespray/kubespray) |
| **kubevirt/kubevirt** | KubeVirt — run VMs natively inside Kubernetes pods using KVM libvirt — VM and container unified | [↗](https://github.com/kubevirt/kubevirt) |
| **kustomize/kustomize** | Kustomize — Kubernetes config management via overlays — no templating pure YAML patches | [↗](https://github.com/kustomize/kustomize) |
| **laravel/cloud-cli** | CLI utility for Laravel Cloud | [↗](https://github.com/laravel/cloud-cli) |
| **laravel/forge-cli** | Laravel Forge CLI | [↗](https://github.com/laravel/forge-cli) |
| **laravel/installer** | Laravel application installer CLI | [↗](https://github.com/laravel/installer) |
| **laravel/sail** | Docker dev environment for Laravel | [↗](https://github.com/laravel/sail) |
| **longhorn/longhorn** | Longhorn — CNCF distributed block storage for Kubernetes — built-in UI backup scheduling snapshot | [↗](https://github.com/longhorn/longhorn) |
| **luzo** | Design API workflows like a flowchart, debug them like a timeline. Visual API orchestration concept. | [↗](https://github.com/JanaSundar/luzo) |
| **Maestro** | Painless E2E mobile and web automation. YAML-defined flows, works without app source code. | [↗](https://github.com/mobile-dev-inc/Maestro) |
| **mavrick202/awesome-kubernetes** | Kubernetes resources and references | [↗](https://github.com/mavrick202/awesome-kubernetes) |
| **metallb/metallb** | MetalLB — bare metal load-balancer for Kubernetes — gives LoadBalancer IPs on on-prem clusters | [↗](https://github.com/metallb/metallb) |
| **n8n-io/n8n** | n8n — self-hostable workflow automation — code-friendly Zapier alternative with 400+ integrations | [↗](https://github.com/n8n-io/n8n) |
| **nomctx** | Fast cluster/namespace context switching for Nomad — like kubectx but for Nomad. | [↗](https://github.com/mr-karan/nomctx) |
| **nttgin/BGPalerter** | BGPalerter — self-configuring BGP monitoring tool — detect BGP hijacks route leaks in real-time | [↗](https://github.com/nttgin/BGPalerter) |
| **opencontainers/runc** | runc — reference OCI container runtime — what Docker and containerd call to spawn containers | [↗](https://github.com/opencontainers/runc) |
| **openebs/openebs** | OpenEBS — container-native storage for Kubernetes with Mayastor (NVMe-oF) Jiva cStor and LocalPV engines | [↗](https://github.com/openebs/openebs) |
| **opentofu/opentofu** | OpenTofu — open-source Terraform fork under Linux Foundation — truly open BSL-free IaC | [↗](https://github.com/opentofu/opentofu) |
| **pixie-io/pixie** | Pixie — eBPF-based Kubernetes observability — auto-capture telemetry without code instrumentation | [↗](https://github.com/pixie-io/pixie) |
| **playground** | Docker Compose collection of tech stack samples. Quickly spin up Kafka, Redis, Postgres etc. without manual setup. | [↗](https://github.com/luisaveiro/playground) |
| **present-md** | Markdown-powered presentations running in the browser. Zero-config dev presentations. | [↗](https://github.com/arpitbbhayani/present-md) |
| **pterodactyl/panel** | Open-source game server management panel with Docker isolation | [↗](https://github.com/pterodactyl/panel) |
| **pulumi/pulumi** | Pulumi — IaC using real programming languages (Python Go TypeScript) — same power as Terraform | [↗](https://github.com/pulumi/pulumi) |
| **rancher/rancher** | Rancher — complete open-source Kubernetes management platform — multi-cluster fleet management | [↗](https://github.com/rancher/rancher) |
| **reactotron** | Desktop app for inspecting React/React Native apps. State, API calls, benchmarks, custom commands. | [↗](https://github.com/infinitered/reactotron) |
| **rook/rook** | Rook — Kubernetes storage operator for Ceph — turns raw disks into cloud-native storage via CSI | [↗](https://github.com/rook/rook) |
| **saltstack/salt** | SaltStack — event-driven IT automation remote execution and config management at scale | [↗](https://github.com/saltstack/salt) |
| **SFTPGo/sftpgo** | SFTPGo — fully featured SFTP FTP WebDAV server with S3 GCS Azure backends and web admin UI | [↗](https://github.com/SFTPGo/sftpgo) |
| **shridarpatil/erpnext-docker** | Dockerizing ERPNext | [↗](https://github.com/shridarpatil/erpnext-docker) |
| **shridarpatil/frappe-docker** | Dockerizing Frappe | [↗](https://github.com/shridarpatil/frappe-docker) |
| **swig** | Connect C/C++ programs with Python, Java, Go, Ruby, etc. — the universal FFI glue tool. | [↗](https://github.com/swig/swig) |
| **swiggy-analytics** | Analyse your Swiggy food orders. Fun personal data analysis tool — and a good patterns example. | [↗](https://github.com/mr-karan/swiggy-analytics) |
| **system-design-101** | Complex systems explained with visuals and simple terms. Interview prep + real learning. | [↗](https://github.com/ByteByteGoHq/system-design-101) |
| **talos-systems/talos** | Talos Linux — immutable minimal OS designed only for running Kubernetes — API-driven no SSH | [↗](https://github.com/talos-systems/talos) |
| **thoughtworks/build-your-own-radar** | Interactive tech radar generator | [↗](https://github.com/thoughtworks/build-your-own-radar) |
| **tomhuang12/awesome-k8s-resources** | Curated Kubernetes tools and resources | [↗](https://github.com/tomhuang12/awesome-k8s-resources) |
| **turborepo** | Monorepo build system in Rust — incremental builds, caching, task orchestration for JS/TS. | [↗](https://github.com/vercel/turborepo) |
| **veggiemonk/awesome-docker** | Curated list of Docker resources and projects | [↗](https://github.com/veggiemonk/awesome-docker) |
| **volsync/volsync** | VolSync — Kubernetes async replication for PVCs using restic rclone rsyncd — DR across clusters | [↗](https://github.com/volsync/volsync) |
| **zerodha/jpdfsign** | CLI wrapper for digitally signing PDFs with iTextPDF | [↗](https://github.com/zerodha/jpdfsign) |
| **zerodha/jpdfsigner** | HTTP server + CLI for digitally signing PDFs | [↗](https://github.com/zerodha/jpdfsigner) |
| **zerodha/opentffoundation-manifesto** | OpenTF manifesto (Terraform BSL license protest) | [↗](https://github.com/zerodha/opentffoundation-manifesto) |

---

## Go Ecosystem

| Repo | Description | Link |
|------|-------------|------|
| **athens** | Go module datastore and proxy. Run your own private Go module proxy — for air-gapped or corporate environments. | [↗](https://github.com/gomods/athens) |
| **chunkedreader** | Light bufio wrapper for reading byte streams in fixed chunks. Useful for protocol parsers. | [↗](https://github.com/knadh/chunkedreader) |
| **go-i18n** | Tiny i18n via simple JSON language files for Go. Minimal alternative to bloated i18n libraries. | [↗](https://github.com/knadh/go-i18n) |
| **go-pop3** | Simple Go POP3 client. Understand how POP3 actually works. | [↗](https://github.com/knadh/go-pop3) |
| **go-redis** | The official Redis Go client. Essential if you use Redis in Go. | [↗](https://github.com/redis/go-redis) |
| **goatcounter** | Easy web analytics with **no personal data tracking**. GDPR-friendly analytics, shows you how to do privacy-first analytics. | [↗](https://github.com/arp242/goatcounter) |
| **indexed-cache** | JS library for caching static assets in browser IndexedDB for longer-term storage. Service-worker-less offline caching. | [↗](https://github.com/knadh/indexed-cache) |
| **jsonconfig** | Tiny JSON config parser with **comment support** for Go. JSON doesn't allow comments — this adds that. | [↗](https://github.com/knadh/jsonconfig) |
| **knadh/go-get-youtube** | Go library for downloading YouTube videos | [↗](https://github.com/knadh/go-get-youtube) |
| **koanf** | Lightweight config management in Go — JSON, TOML, YAML, env, CLI, S3 all unified. Better viper alternative. | [↗](https://github.com/knadh/koanf) |
| **lil** | Simple URL shortener in Go. Read source to understand clean Go web service structure. | [↗](https://github.com/vividvilla/lil) |
| **localStorageDB** | Database layer for localStorage — tables, queries on top of browser storage. Interesting browser-side DB pattern. | [↗](https://github.com/knadh/localStorageDB) |
| **logf** | Extremely fast, zero-alloc logfmt logging in Go. Study zero-allocation techniques. | [↗](https://github.com/zerodha/logf) |
| **niltalk** | Instant, disposable live chat server — single binary, Go + VueJS. Room self-destructs. | [↗](https://github.com/knadh/niltalk) |
| **onelog** | Dead simple, super fast, zero-allocation logger in Go. Compare with zap — different tradeoffs. | [↗](https://github.com/francoispqt/onelog) |
| **paginator** | Tiny Go package for pagination + page number generation. The right way to do DB pagination in Go. | [↗](https://github.com/knadh/paginator) |
| **profiler** | Simple wrapper over Go `runtime/pprof` for concurrent profiling. How to instrument Go programs for perf analysis. | [↗](https://github.com/knadh/profiler) |
| **querytostruct** | Unmarshal query strings into Go structs. Tiny but saves a lot of boilerplate. | [↗](https://github.com/knadh/querytostruct) |
| **remogatto/cloud** | Golang client for ownCloud/Nextcloud instances | [↗](https://github.com/remogatto/cloud) |
| **simplesessions** | Go session management completely agnostic of HTTP framework and backend store. Interface-first design. | [↗](https://github.com/zerodha/simplesessions) |
| **zap** | Uber's blazing fast structured leveled logging. The reference implementation of high-perf Go logging. | [↗](https://github.com/uber-go/zap) |

---

## Tiny JS Libraries

| Repo | Description | Link |
|------|-------------|------|
| **autocomp.js** | Autocomplete, ~800 bytes, zero deps | [↗](https://github.com/knadh/autocomp.js) |
| **cobe** | 5KB WebGL globe lib | [↗](https://github.com/shuding/cobe) |
| **dayjs** | 2kB date-time library, Moment.js API compatible | [↗](https://github.com/iamkun/dayjs) |
| **dragmove.js** | Make DOM elements draggable, ~500 bytes, zero deps | [↗](https://github.com/knadh/dragmove.js) |
| **floatype.js** | Floating autocomplete widget for textareas, zero deps | [↗](https://github.com/knadh/floatype.js) |
| **highlighted-input.js** | Highlight keywords/tags inside an `<input>`, zero deps | [↗](https://github.com/knadh/highlighted-input.js) |
| **oat** | Full UI library, ~8KB, zero deps, semantic HTML | [↗](https://github.com/knadh/oat) |
| **tinyprogressbar** | Progress bar, 640 bytes | [↗](https://github.com/knadh/tinyprogressbar) |
| **tinyrouter.js** | Frontend routing on `window.history`, zero deps | [↗](https://github.com/knadh/tinyrouter.js) |
| **tinytabs** | Tabbed UI rendering, ~750 bytes | [↗](https://github.com/knadh/tinytabs) |

---

## Self-Hosted Apps & Platforms

| Repo | Description | Link |
|------|-------------|------|
| **apache/airflow** | Apache Airflow — platform to programmatically author schedule and monitor data workflows as DAGs | [↗](https://github.com/apache/airflow) |
| **BookStackApp/BookStack** | Open-source wiki/documentation platform | [↗](https://github.com/BookStackApp/BookStack) |
| **codigee-devs/self-hosted-flutter-ci-cd-with-fastlane** | Flutter CI/CD with Fastlane self-hosted runner | [↗](https://github.com/codigee-devs/self-hosted-flutter-ci-cd-with-fastlane) |
| **commafeed** | Google Reader-inspired self-hosted RSS reader. The best self-hosted RSS. | [↗](https://github.com/Athou/commafeed) |
| **ConvertX** | Self-hosted online file converter supporting 1000+ formats. No cloud dependency for conversions. | [↗](https://github.com/C4illin/ConvertX) |
| **coolify** | Self-hostable PaaS — Vercel/Heroku/Netlify alternative, 280+ one-click services. The most complete self-host platform. | [↗](https://github.com/coollabsio/coolify) |
| **cvhariharan/flowctl** | Self-service workflow execution platform | [↗](https://github.com/cvhariharan/flowctl) |
| **dagster-io/dagster** | Dagster — data orchestration platform with asset graph — software-defined data pipelines | [↗](https://github.com/dagster-io/dagster) |
| **DataHubProject/datahub** | DataHub — metadata platform for data discovery lineage and governance — open-source data catalog | [↗](https://github.com/DataHubProject/datahub) |
| **directus/directus** | Directus — open-source headless CMS and data platform — REST + GraphQL on any SQL database | [↗](https://github.com/directus/directus) |
| **discourse/discourse** | Open-source community discussion platform | [↗](https://github.com/discourse/discourse) |
| **dockge** | Fancy self-hosted Docker Compose stack manager — reactive UI, compose.yaml oriented. | [↗](https://github.com/louislam/dockge) |
| **dyrectorio** | Self-hosted continuous delivery + deployment platform with version management. CD without GitHub Actions lock-in. | [↗](https://github.com/dyrector-io/dyrectorio) |
| **ente** | End-to-end encrypted cloud — photos, auth secrets, files. Google Photos alternative with provable privacy. | [↗](https://github.com/ente-io/ente) |
| **flarum/flarum** | Simple community forum software | [↗](https://github.com/flarum/flarum) |
| **frappe/erpnext** | Free open-source Enterprise Resource Planning (ERP) | [↗](https://github.com/frappe/erpnext) |
| **freyja-lang/pyroscope** | Pyroscope — continuous profiling platform — CPU memory allocation profiling in production always-on | [↗](https://github.com/freyja-lang/pyroscope) |
| **gitea** | Self-hosted Git service — GitHub/GitLab alternative. Full: code review, CI/CD, package registry. | [↗](https://github.com/go-gitea/gitea) |
| **grafana** | The reference observability platform. Metrics, logs, traces from any source, composable dashboards. | [↗](https://github.com/grafana/grafana) |
| **jellyfin/jellyfin** | Jellyfin — free self-hosted media server — fork of Emby no subscriptions streams any device | [↗](https://github.com/jellyfin/jellyfin) |
| **juanfont/headscale** | Headscale — self-hosted Tailscale control plane — run your own coordination server for Tailscale clients | [↗](https://github.com/juanfont/headscale) |
| **juspay/hyperswitch-docs** | Hyperswitch payments platform documentation | [↗](https://github.com/juspay/hyperswitch-docs) |
| **keystonejs/keystone** | KeystoneJS — CMS and app framework — GraphQL API auto-generated from schema definition | [↗](https://github.com/keystonejs/keystone) |
| **koel/koel** | Self-hosted music streaming solution | [↗](https://github.com/koel/koel) |
| **krayin/laravel-crm** | Free open-source Laravel CRM for SMEs/Enterprises | [↗](https://github.com/krayin/laravel-crm) |
| **kubero** | Self-hosted PaaS on Kubernetes — Heroku/Netlify alternative for k8s users. | [↗](https://github.com/kubero-dev/kubero) |
| **laravel/horizon** | Dashboard and config for Laravel queues | [↗](https://github.com/laravel/horizon) |
| **libredesk** | Self-hosted omnichannel customer support desk — live chat, email, single binary. | [↗](https://github.com/abhinavxd/libredesk) |
| **listmonk** | High-performance newsletter + mailing list in a single binary. 100k+ subscribers, self-hosted. | [↗](https://github.com/knadh/listmonk) |
| **listmonk-mcp** | MCP server for Listmonk — control your newsletter via AI agents. Agent-native email marketing. | [↗](https://github.com/rhnvrm/listmonk-mcp) |
| **louislam/uptime-kuma** | Uptime Kuma — self-hosted monitoring tool — ping HTTP port TCP checks with status page | [↗](https://github.com/louislam/uptime-kuma) |
| **metabase** | Easy open-source BI and embedded analytics. Non-engineers can query your DB with zero SQL. | [↗](https://github.com/metabase/metabase) |
| **monicahq/monica** | Personal CRM for managing relationships | [↗](https://github.com/monicahq/monica) |
| **navidrome/navidrome** | Navidrome — self-hosted music server — Subsonic API compatible lightweight modern UI | [↗](https://github.com/navidrome/navidrome) |
| **neko** | Self-hosted virtual browser in Docker via WebRTC. Share a browser session, run a remote browser. Wild concept. | [↗](https://github.com/m1k1o/neko) |
| **nextcloud/server** | Nextcloud — self-hosted cloud files calendar contacts talk — Google Drive/Workspace alternative | [↗](https://github.com/nextcloud/server) |
| **nixos-unified-template** | Multi-platform Nix config template. Reproducible development environments across machines. | [↗](https://github.com/juspay/nixos-unified-template) |
| **open-metadata/OpenMetadata** | OpenMetadata — unified metadata governance discovery and observability platform — single source of truth | [↗](https://github.com/open-metadata/OpenMetadata) |
| **opennebula/one** | OpenNebula — open-source cloud and edge computing platform for enterprise VM management | [↗](https://github.com/opennebula/one) |
| **opentelemetry-collector** | The OTel collector — ingest, process, export telemetry from anywhere to anywhere. | [↗](https://github.com/open-telemetry/opentelemetry-collector) |
| **orangehrm/orangehrm** | Comprehensive open-source HRM system | [↗](https://github.com/orangehrm/orangehrm) |
| **oVirt/ovirt-engine** | oVirt — Red Hat-sponsored KVM-based datacenter virtualization management platform | [↗](https://github.com/oVirt/ovirt-engine) |
| **owncast** | Self-hosted live video streaming + chat. Control your stream, Twitch alternative. | [↗](https://github.com/owncast/owncast) |
| **owncloud/core** | ownCloud — enterprise self-hosted file sync and share — CalDAV CardDAV WebDAV | [↗](https://github.com/owncloud/core) |
| **OxiCloud** | Rust-built self-hosted cloud — files, photos, calendar, contacts. CalDAV/CardDAV support. | [↗](https://github.com/DioCrafts/OxiCloud) |
| **paperless-ngx** | Document management system — scan, OCR, index, archive all your documents. | [↗](https://github.com/paperless-ngx/paperless-ngx) |
| **payloadcms/payload** | Payload CMS — code-first headless CMS — TypeScript-native full-stack backend platform | [↗](https://github.com/payloadcms/payload) |
| **pgrok/pgrok** | pgrok — poor man's ngrok — self-hosted HTTP tunnel for exposing localhost to internet | [↗](https://github.com/pgrok/pgrok) |
| **plane** | Open-source Jira/Linear/Monday alternative. Project management platform. | [↗](https://github.com/makeplane/plane) |
| **pocketbase** | **Realtime backend in 1 file** — DB, auth, storage, realtime, admin UI. Zero infra. Impressive engineering. | [↗](https://github.com/pocketbase/pocketbase) |
| **posthog** | All-in-one developer platform — analytics, session replay, flags, A/B testing, error tracking, data warehouse. Self-hostable. | [↗](https://github.com/PostHog/posthog) |
| **redash** | Connect to any data source, visualize, dashboard, share. Multi-source data exploration. | [↗](https://github.com/getredash/redash) |
| **rhnvrm/linkpage** | Self-hosted alternative to LinkTree/Campsite.bio | [↗](https://github.com/rhnvrm/linkpage) |
| **sentry** | Developer-first error tracking + performance monitoring. The reference open-source APM/error tracker. | [↗](https://github.com/getsentry/sentry) |
| **sharry** | Self-hosted file sharing web app. Send large files securely without cloud services. | [↗](https://github.com/eikek/sharry) |
| **shridarpatil/crm** | Free open-source CRM (Frappe-based) | [↗](https://github.com/shridarpatil/crm) |
| **signoz/signoz** | SigNoz — OpenTelemetry-native APM — logs traces metrics in one self-hosted alternative to DataDog | [↗](https://github.com/signoz/signoz) |
| **strapi/strapi** | Strapi — open-source headless CMS — content API with admin UI for any frontend | [↗](https://github.com/strapi/strapi) |
| **telegramdesktop/tdesktop** | Telegram Desktop — reference client for studying efficient cross-platform C++ app with MTProto protocol | [↗](https://github.com/telegramdesktop/tdesktop) |
| **tg-archive** | Export Telegram group chats into static websites like mailing list archives. | [↗](https://github.com/knadh/tg-archive) |
| **trigger.dev** | Build and deploy fully-managed AI agents and workflows. Background jobs + AI agent platform. | [↗](https://github.com/triggerdotdev/trigger.dev) |
| **twenty** | Open-source Salesforce alternative, designed for AI. CRM built for agent integration. | [↗](https://github.com/twentyhq/twenty) |
| **uptrace** | Open-source APM — OpenTelemetry traces, metrics, logs in one place. | [↗](https://github.com/uptrace/uptrace) |
| **wagtail/wagtail** | Wagtail — Django-based open-source CMS — used by NASA Google Mozilla for content management | [↗](https://github.com/wagtail/wagtail) |
| **wayback** | Archive content to Internet Archive, IPFS, archive.today via IM-style interface. Privacy-first archiving. | [↗](https://github.com/wabarc/wayback) |
| **windmill** | Open-source developer platform — scripts → webhooks, workflows, UIs. 13x faster than Airflow. Retool alternative. | [↗](https://github.com/windmill-labs/windmill) |
| **zammad** | Web-based open-source helpdesk/customer support. Full ticketing system. | [↗](https://github.com/zammad/zammad) |
| **zerodha/erpnext** | Open-source ERP (Frappe-based fork) | [↗](https://github.com/zerodha/erpnext) |
| **zettel** | Notes organiser based on Zettelkasten methodology. Knowledge management system. | [↗](https://github.com/hackstream/zettel) |

---

## Mobile & Flutter/Android

| Repo | Description | Link |
|------|-------------|------|
| **aaassseee/screen_brightness** | Flutter plugin for controlling screen brightness | [↗](https://github.com/aaassseee/screen_brightness) |
| **ajinasokan/ditto** | Simple dictionary app built with Flutter — powers Olam and Alar mobile apps | [↗](https://github.com/ajinasokan/ditto) |
| **ajinasokan/flutter_displaymode** | Flutter plugin to set display mode (resolution + refresh rate) on Android — unlock 90/120Hz | [↗](https://github.com/ajinasokan/flutter_displaymode) |
| **ajinasokan/page_keeper** | Page state keeper for Flutter | [↗](https://github.com/ajinasokan/page_keeper) |
| **ajinasokan/recharge** | Hot reload Dart code on file changes — like air/nodemon for Dart | [↗](https://github.com/ajinasokan/recharge) |
| **ajinasokan/store_keeper** | Easy flexible state management system for Flutter apps | [↗](https://github.com/ajinasokan/store_keeper) |
| **anpec** | Flutter plugin for Android device performance classification — know your hardware tier in-app. | [↗](https://github.com/devaryakjha/anpec) |
| **binaryshrey/Awesome-Android-Open-Source-Projects** | Curated awesome Android open-source projects | [↗](https://github.com/binaryshrey/Awesome-Android-Open-Source-Projects) |
| **budtmo/docker-android** | Android in Docker with noVNC and video recording | [↗](https://github.com/budtmo/docker-android) |
| **capcom6/android-sms-gateway** | SMS Gateway for Android via API (direct or cloud) | [↗](https://github.com/capcom6/android-sms-gateway) |
| **dartgen** | Inline generator collection for Dart/Flutter — code generation at build time. | [↗](https://github.com/ajinasokan/dartgen) |
| **expo** | Universal native apps framework for React — runs Android, iOS, web from one codebase. | [↗](https://github.com/expo/expo) |
| **expo-react-native-cicd** | Free Expo EAS alternative — full CI/CD for React Native via GitHub Actions. Save $100s/month. | [↗](https://github.com/TanayK07/expo-react-native-cicd) |
| **flutter-shadcn-ui** | shadcn/ui ported to Flutter. The design system from web world, brought to mobile. | [↗](https://github.com/nank1ro/flutter-shadcn-ui) |
| **flutter_inappwebview** | Flutter plugin for inline webview, headless webview, in-app browser. Full webview control. | [↗](https://github.com/pichillilorenzo/flutter_inappwebview) |
| **gronxb/hot-updater** | Self-hostable OTA update for React Native (CodePush alt) | [↗](https://github.com/gronxb/hot-updater) |
| **hermes** | Facebook's JavaScript engine optimised for React Native — smaller bytecode, faster startup than V8. | [↗](https://github.com/facebook/hermes) |
| **HQarroum/docker-android** | Minimal customizable Docker image running Android emulator | [↗](https://github.com/HQarroum/docker-android) |
| **JStumpp/awesome-android** | Curated list of awesome Android packages and resources | [↗](https://github.com/JStumpp/awesome-android) |
| **juspay/flutter_hyperswitch** | Flutter Hyperswitch payments SDK | [↗](https://github.com/juspay/flutter_hyperswitch) |
| **LiveContainer** | Run iOS apps **without actually installing them**. Containerized iOS app execution — rare concept. | [↗](https://github.com/LiveContainer/LiveContainer) |
| **localizely/flutter-ota-sample-app** | Flutter OTA translation update sample | [↗](https://github.com/localizely/flutter-ota-sample-app) |
| **mingchen/docker-android-build-box** | Docker image with Android/Flutter/Kotlin SDK | [↗](https://github.com/mingchen/docker-android-build-box) |
| **MobileDevOps/flutter-sdk-image** | Docker image with Flutter SDK for Android builds | [↗](https://github.com/MobileDevOps/flutter-sdk-image) |
| **oore.build** | Self-hosted Flutter-first mobile CI + internal app distribution platform. | [↗](https://github.com/devaryakjha/oore.build) |
| **overlay_webview** | Flutter WebView as overlay without performance overhead. Different rendering approach. | [↗](https://github.com/ajinasokan/overlay_webview) |
| **philip-brink/DragAndDropLists** | Flutter drag-and-drop reordering for two-level lists | [↗](https://github.com/philip-brink/DragAndDropLists) |
| **pinchtab** | Browser automation bridge + multi-instance orchestrator with stealth injection. | [↗](https://github.com/pinchtab/pinchtab) |
| **PulseAPK-Core** | Cross-platform tool for APK decompilation, analysis, and rebuilding. | [↗](https://github.com/deemoun/PulseAPK-Core) |
| **rafosw/APKdevastate** | Advanced APK payload analysis software | [↗](https://github.com/rafosw/APKdevastate) |
| **Sayegh7/move_to_background** | Flutter plugin to send app to background | [↗](https://github.com/Sayegh7/move_to_background) |
| **SimformSolutionsPvtLtd/Awesome-Mobile-Libraries** | iOS/Android/Flutter/React Native open-source libraries | [↗](https://github.com/SimformSolutionsPvtLtd/Awesome-Mobile-Libraries) |
| **uber-apk-signer** | CLI for signing and zip-aligning APKs. Supports v1/v2/v3 signing schemes. | [↗](https://github.com/patrickfav/uber-apk-signer) |
| **vercel-labs/zero-native** | Desktop + mobile apps with Zig and web UI | [↗](https://github.com/vercel-labs/zero-native) |
| **yogeshpaliyal/awesome-mobile-system-design** | Mobile design systems resources and patterns | [↗](https://github.com/yogeshpaliyal/awesome-mobile-system-design) |

---

## Payments & Fintech

| Repo | Description | Link |
|------|-------------|------|
| **akaunting/akaunting** | Online accounting software | [↗](https://github.com/akaunting/akaunting) |
| **bagisto/bagisto** | Free open-source Laravel eCommerce platform | [↗](https://github.com/bagisto/bagisto) |
| **Blair2004/NexoPOS** | Web-based POS system (Laravel + TailwindCSS + Vue) | [↗](https://github.com/Blair2004/NexoPOS) |
| **dub** | Modern link attribution platform — link shortening + analytics + conversion tracking. | [↗](https://github.com/dubinc/dub) |
| **gokiteconnect** | Official Go client for Zerodha Kite Connect trading APIs. Algorithmic trading in Go. | [↗](https://github.com/zerodha/gokiteconnect) |
| **gUPI-recon** | GUI tool for UPI payment address discovery and recon. Unique defensive/research tool for UPI ecosystem. | [↗](https://github.com/kinshukdua/gUPI-recon) |
| **hyperswitch** | Open-source payments switch in Rust — route payments across gateways (Stripe, Razorpay, etc.). From Juspay. | [↗](https://github.com/juspay/hyperswitch) |
| **juspay/decision-engine** | Open-source routing system for payment processing | [↗](https://github.com/juspay/decision-engine) |
| **laravel/cashier-paddle** | Expressive interface to Paddle subscription billing | [↗](https://github.com/laravel/cashier-paddle) |
| **nammayatri** | Open-source direct-to-driver mobility platform — the real codebase powering auto-rickshaw apps in India. | [↗](https://github.com/nammayatri/nammayatri) |
| **paykit** | TypeScript billing framework — code-first products, Stripe + webhooks + usage state. | [↗](https://github.com/getpaykit/paykit) |
| **polar** | Turn your software into a business — subscriptions, donations, issue funding, all in one. | [↗](https://github.com/polarsource/polar) |
| **zerodha/javakiteconnect** | Official Java client for Kite Connect API | [↗](https://github.com/zerodha/javakiteconnect) |
| **zerodha/phpkiteconnect** | Official PHP client for Kite Connect trading API | [↗](https://github.com/zerodha/phpkiteconnect) |
| **zerodha/vendor-payments** | Vendor payment workflow and tracking (Frappe app) | [↗](https://github.com/zerodha/vendor-payments) |

---

## Geospatial & Maps

| Repo | Description | Link |
|------|-------------|------|
| **h3** | Uber's hexagonal hierarchical geospatial indexing. Map the earth in hex cells — used in logistics, ridehailing. | [↗](https://github.com/uber/h3) |
| **LocationsCode** | Convert GPS coordinates into 8 characters. Location encoding algorithm. | [↗](https://github.com/buonaldo/LocationsCode) |
| **OpenTripPlanner** | Open-source multi-modal trip planner — bus, train, walking combined routing. | [↗](https://github.com/nammayatri/OpenTripPlanner) |
| **osrm-backend** | Open Source Routing Machine C++ backend — fastest open-source route engine. How maps calculate directions. | [↗](https://github.com/Project-OSRM/osrm-backend) |

---

## IoT & Embedded

| Repo | Description | Link |
|------|-------------|------|
| **bytecodealliance/wasmer** | Wasmer — universal WebAssembly runtime — run WASM anywhere server edge IoT | [↗](https://github.com/bytecodealliance/wasmer) |
| **capacitive-soil-moisture-sensor** | Compact, battery-powered soil moisture sensor hardware design. Hardware + firmware together. | [↗](https://github.com/RonMcKay/capacitive-soil-moisture-sensor) |
| **iot-app-kit** | AWS library for web apps visualising industrial data — IoT dashboards. | [↗](https://github.com/awslabs/iot-app-kit) |
| **kata-containers/kata-containers** | Kata Containers — lightweight VMs as container runtime — hardware isolation for untrusted workloads | [↗](https://github.com/kata-containers/kata-containers) |
| **mongoose-os** | IoT firmware framework — ESP32, ESP8266, STM32. AWS IoT, Azure, Google IoT Core. Code in C or JS. | [↗](https://github.com/cesanta/mongoose-os) |
| **openremote** | 100% open-source IoT platform — device integration, intelligence, custom apps. | [↗](https://github.com/openremote/openremote) |

---

## Indic Language & Local Computing

| Repo | Description | Link |
|------|-------------|------|
| **datuk** | Unicode Malayalam–Malayalam dictionary dataset. Language data asset. | [↗](https://github.com/knadh/datuk) |
| **dictpress** | Stand-alone web server for building full dictionary websites + APIs for any language. | [↗](https://github.com/knadh/dictpress) |
| **govarnam** | Cross-platform transliteration library — Manglish→Malayalam, Thanglish→Tamil, Hinglish→Hindi + 10 more. | [↗](https://github.com/varnamproject/govarnam) |
| **indic-trans** | State-of-the-art transliteration across all Indian languages including English. | [↗](https://github.com/libindic/indic-trans) |
| **indic.page** | Directory of Indic language computing resources. Hub for Indian language tech. | [↗](https://github.com/knadh/indic.page) |
| **inltk** | NLP toolkit for Indic languages — out-of-the-box NLP tasks for Indian languages. | [↗](https://github.com/goru001/inltk) |
| **knphone** | Same phonetic algorithm concept for Kannada. | [↗](https://github.com/knadh/knphone) |
| **ml2en** | Transliterate Malayalam script to Manglish (Roman). Python, PHP, JS versions. | [↗](https://github.com/knadh/ml2en) |
| **mlphone** | Phonetic algorithm for Malayalam (like Metaphone for English). Index Malayalam words by pronunciation. | [↗](https://github.com/knadh/mlphone) |
| **rconceptnet** | ConceptNet CLI and server in Rust with SQLite. Knowledge graph for semantic relationships. | [↗](https://github.com/knadh/rconceptnet) |

---

## Laravel / PHP Ecosystem

| Repo | Description | Link |
|------|-------------|------|
| **laravel/dusk** | Laravel end-to-end browser testing and automation | [↗](https://github.com/laravel/dusk) |
| **laravel/echo** | Laravel Echo for Reverb/Pusher/Ably realtime events | [↗](https://github.com/laravel/echo) |
| **laravel/envoy** | Elegant SSH task runner for PHP | [↗](https://github.com/laravel/envoy) |
| **laravel/folio** | Page-based file routing for Laravel | [↗](https://github.com/laravel/folio) |
| **laravel/forge-sdk** | Official Laravel Forge PHP SDK | [↗](https://github.com/laravel/forge-sdk) |
| **laravel/framework** | Laravel framework core | [↗](https://github.com/laravel/framework) |
| **laravel/laravel** | Laravel web application framework | [↗](https://github.com/laravel/laravel) |
| **laravel/nova-log-viewer** | Laravel Nova log viewing tool | [↗](https://github.com/laravel/nova-log-viewer) |
| **laravel/nova-pennant** | Pennant resource tool for Laravel Nova | [↗](https://github.com/laravel/nova-pennant) |
| **laravel/octane** | High-performance app server for Laravel (Swoole/RoadRunner) | [↗](https://github.com/laravel/octane) |
| **laravel/passkeys** | Passkeys client for Laravel applications | [↗](https://github.com/laravel/passkeys) |
| **laravel/pint** | Opinionated PHP code style fixer | [↗](https://github.com/laravel/pint) |
| **laravel/pulse** | Real-time application performance monitoring for Laravel | [↗](https://github.com/laravel/pulse) |
| **laravel/ranger** | Introspection library for Laravel apps | [↗](https://github.com/laravel/ranger) |
| **laravel/scout** | Driver-based Eloquent model search | [↗](https://github.com/laravel/scout) |
| **laravel/stream** | Streaming hooks for React and Vue | [↗](https://github.com/laravel/stream) |
| **laravel/surveyor** | Static analysis tool for PHP and Laravel code | [↗](https://github.com/laravel/surveyor) |
| **laravel/telescope** | Debug assistant/profiler for Laravel | [↗](https://github.com/laravel/telescope) |
| **laravel/tinker** | Powerful REPL for Laravel | [↗](https://github.com/laravel/tinker) |
| **laravel/ui** | Laravel UI utilities and presets | [↗](https://github.com/laravel/ui) |
| **laravel/valet** | Local Laravel development environment for Mac | [↗](https://github.com/laravel/valet) |
| **laravel/vapor-core** | Core service providers and runtime for Laravel Vapor (serverless) | [↗](https://github.com/laravel/vapor-core) |
| **laravel/wayfinder** | Laravel URL generation and route binding helper | [↗](https://github.com/laravel/wayfinder) |
| **livewire/livewire** | Full-stack Laravel framework for dynamic UIs without full JS SPA | [↗](https://github.com/livewire/livewire) |
| **spatie/crawler** | PHP web crawler | [↗](https://github.com/spatie/crawler) |
| **spatie/laravel-route-discovery** | Auto-discover routes in Laravel apps | [↗](https://github.com/spatie/laravel-route-discovery) |

---

## Frappe / Zerodha Ecosystem

| Repo | Description | Link |
|------|-------------|------|
| **frappe/frappe** | Low-code web framework for real-world applications | [↗](https://github.com/frappe/frappe) |
| **shridarpatil/frappe-go** | Build Go APIs for Frappe | [↗](https://github.com/shridarpatil/frappe-go) |
| **shridarpatil/frappe_disable_signup** | Disable Frappe signup by email domain | [↗](https://github.com/shridarpatil/frappe_disable_signup) |
| **shridarpatil/frappe_discourse** | Frappe SSO integration for Discourse | [↗](https://github.com/shridarpatil/frappe_discourse) |
| **shridarpatil/frappe_private_attachments** | Make all Frappe attachments private by default | [↗](https://github.com/shridarpatil/frappe_private_attachments) |
| **shridarpatil/frappe_tinymce** | Replace Frappe default editor with TinyMCE | [↗](https://github.com/shridarpatil/frappe_tinymce) |
| **shridarpatil/frappe_whatsapp** | WhatsApp Cloud integration for Frappe | [↗](https://github.com/shridarpatil/frappe_whatsapp) |
| **shridarpatil/frappe_whatsapp_chatbot** | WhatsApp chatbot for Frappe | [↗](https://github.com/shridarpatil/frappe_whatsapp_chatbot) |
| **shridarpatil/godev** | Hot reload tool for Go | [↗](https://github.com/shridarpatil/godev) |
| **shridarpatil/goframework** | Go framework skeleton | [↗](https://github.com/shridarpatil/goframework) |
| **shridarpatil/loom** | Loom concurrency testing tool fork | [↗](https://github.com/shridarpatil/loom) |
| **shridarpatil/rpc** | RPC implementation | [↗](https://github.com/shridarpatil/rpc) |
| **shridarpatil/whatomate** | Open-source WhatsApp integration | [↗](https://github.com/shridarpatil/whatomate) |
| **shridarpatil/whatsapp_chat** | WhatsApp chat integration | [↗](https://github.com/shridarpatil/whatsapp_chat) |
| **zerodha/frappe_docs** | Frappe framework documentation | [↗](https://github.com/zerodha/frappe_docs) |
| **zerodha/lms** | Open-source Learning Management System (Frappe-based) | [↗](https://github.com/zerodha/lms) |

---

## Knadh Personal Projects

| Repo | Description | Link |
|------|-------------|------|
| **knadh/bigreddy** | Generates pseudo-philosophical ramblings | [↗](https://github.com/knadh/bigreddy) |
| **knadh/boastmachine** | Legacy blogging package (earliest web blogging systems 2002) | [↗](https://github.com/knadh/boastmachine) |
| **knadh/csssprite** | Merge images into CSS sprite | [↗](https://github.com/knadh/csssprite) |
| **knadh/dictpress-tts** | TTS plugin for dictpress | [↗](https://github.com/knadh/dictpress-tts) |
| **knadh/dirmaker** | Static site generator for directory websites | [↗](https://github.com/knadh/dirmaker) |
| **knadh/jqdialog** | jQuery plugin for dialog boxes (alert/confirm/prompt replacement) | [↗](https://github.com/knadh/jqdialog) |
| **knadh/listmonk-heroku-deploy** | Listmonk install button for Heroku | [↗](https://github.com/knadh/listmonk-heroku-deploy) |
| **knadh/listmonk-site** | Static website + docs for listmonk | [↗](https://github.com/knadh/listmonk-site) |
| **knadh/otpgateway-solsms** | SMS provider for otpgateway (SolutionsInfini India) | [↗](https://github.com/knadh/otpgateway-solsms) |
| **knadh/scylladb-metrics** | Docs generator for ScyllaDB Prometheus metrics | [↗](https://github.com/knadh/scylladb-metrics) |
| **knadh/simplemysql** | Ultra simple Python MySQLdb wrapper | [↗](https://github.com/knadh/simplemysql) |
| **knadh/simpleplanner** | Simple task planner | [↗](https://github.com/knadh/simpleplanner) |
| **knadh/stringvalidator.py** | Simple string validator for basic data validation | [↗](https://github.com/knadh/stringvalidator.py) |
| **knadh/tinyauth** | Tiny opinionated authentication library for Go | [↗](https://github.com/knadh/tinyauth) |
| **knadh/tinyi18n-rs** | Tiny Rust i18n library (JSON language maps) | [↗](https://github.com/knadh/tinyi18n-rs) |
| **knadh/tinytooltip** | Tiny jQuery tooltip plugin | [↗](https://github.com/knadh/tinytooltip) |
| **knadh/unipdf** | Go PDF library for creating and processing PDFs | [↗](https://github.com/knadh/unipdf) |
| **knadh/wordpluck** | Browser-based typing game | [↗](https://github.com/knadh/wordpluck) |

---

## Awesome-Lists & Resources

| Repo | Description | Link |
|------|-------------|------|
| **0PandaDev/awesome-windows** | Curated tools and apps for Windows 10/11 | [↗](https://github.com/0PandaDev/awesome-windows) |
| **anderspitman/awesome-tunneling** | Curated list of all tunneling solutions — ngrok alternatives comparison and decision guide | [↗](https://github.com/anderspitman/awesome-tunneling) |
| **avelino/awesome-go** | Curated Go frameworks libraries and software | [↗](https://github.com/avelino/awesome-go) |
| **awesome-selfhosted/awesome-selfhosted** | List of self-hostable free software services and web apps | [↗](https://github.com/awesome-selfhosted/awesome-selfhosted) |
| **enaqx/awesome-react** | Curated React ecosystem resources | [↗](https://github.com/enaqx/awesome-react) |
| **FlxPeters/awsome-grafana** | Curated Grafana resources | [↗](https://github.com/FlxPeters/awsome-grafana) |
| **HaralDev/Space-Systems-Engineering-Resources** | Space mission design resources and scripts | [↗](https://github.com/HaralDev/Space-Systems-Engineering-Resources) |
| **Kavex/GameDev-Resources** | Curated game development resources | [↗](https://github.com/Kavex/GameDev-Resources) |
| **luong-komorebi/Awesome-Linux-Software** | List of awesome Linux software | [↗](https://github.com/luong-komorebi/Awesome-Linux-Software) |
| **markets/awesome-ruby** | Curated list of awesome Ruby libraries and tools | [↗](https://github.com/markets/awesome-ruby) |
| **oz123/awesome-c** | Curated list of awesome C frameworks and libraries | [↗](https://github.com/oz123/awesome-c) |
| **rust-unofficial/awesome-rust** | Curated Rust code and resources | [↗](https://github.com/rust-unofficial/awesome-rust) |
| **stackshareio/awesome-stacks** | Curated tech stacks for different applications | [↗](https://github.com/stackshareio/awesome-stacks) |
| **unicodeveloper/awesome-nextjs** | Curated Next.js resources | [↗](https://github.com/unicodeveloper/awesome-nextjs) |
| **VoltAgent/awesome-design-md** | Collection of DESIGN.md files for brand design systems | [↗](https://github.com/VoltAgent/awesome-design-md) |
| **vuejs/awesome-vue** | Curated Vue.js resources | [↗](https://github.com/vuejs/awesome-vue) |
| **ziadoz/awesome-php** | Curated PHP libraries and resources | [↗](https://github.com/ziadoz/awesome-php) |

---

## Miscellaneous Notable Repos

| Repo | Description | Link |
|------|-------------|------|
| **45drives/cockpit-navigator** | Cockpit Navigator — file browser plugin for Cockpit web console — browse and manage server files | [↗](https://github.com/45drives/cockpit-navigator) |
| **agmmnn/tauri-ui** | Tauri + shadcn/ui starter (Vite/Next/Astro/TanStack) | [↗](https://github.com/agmmnn/tauri-ui) |
| **ajaydubey777/SystemDesignArchitecture** | System design architecture reference | [↗](https://github.com/ajaydubey777/SystemDesignArchitecture) |
| **angristan/wireguard-install** | WireGuard server installer — one-command WireGuard setup with client config generation | [↗](https://github.com/angristan/wireguard-install) |
| **apache/arrow** | Apache Arrow — in-memory columnar format for analytics — zero-copy IPC and vectorized execution | [↗](https://github.com/apache/arrow) |
| **apache/cassandra** | Apache Cassandra — leaderless distributed wide-column store — used at Netflix Apple Discord at billion-row scale | [↗](https://github.com/apache/cassandra) |
| **apache/flink** | Apache Flink — stateful stream processing at scale — used by Alibaba Uber Netflix for real-time ETL | [↗](https://github.com/apache/flink) |
| **apache/iceberg** | Apache Iceberg — open table format for huge analytic datasets — ACID on data lakes used at Netflix Apple | [↗](https://github.com/apache/iceberg) |
| **apache/skywalking** | Apache SkyWalking — full-stack APM and distributed tracing — widely used in China Java ecosystem | [↗](https://github.com/apache/skywalking) |
| **apache/spark** | Apache Spark — unified analytics engine for large-scale batch and streaming data processing | [↗](https://github.com/apache/spark) |
| **Avnsh1111/Instagram-Reels-Scraper-Auto-Poster** | Scrape and auto-post Instagram Reels | [↗](https://github.com/Avnsh1111/Instagram-Reels-Scraper-Auto-Poster) |
| **bytecodealliance/wasmtime** | Wasmtime — fast secure WebAssembly runtime — W3C spec compliant WASI support | [↗](https://github.com/bytecodealliance/wasmtime) |
| **calcom/cal.diy** | Open-source scheduling infrastructure | [↗](https://github.com/calcom/cal.diy) |
| **canonical/microceph** | MicroCeph — minimal Ceph deployment via snap — single command Ceph cluster for homelab or edge | [↗](https://github.com/canonical/microceph) |
| **chenglou/pretext** | Fast accurate text measurement and layout engine | [↗](https://github.com/chenglou/pretext) |
| **ChristopherDosin/laravel-cloud** | Laravel Cloud - Forge Pro attempt for load balancing/scaling | [↗](https://github.com/ChristopherDosin/laravel-cloud) |
| **cloudflare/boringtun** | BoringTun — Cloudflare WireGuard userspace implementation in Rust — used in Cloudflare WARP | [↗](https://github.com/cloudflare/boringtun) |
| **csv2json** | Fast CSV→JSON line converter — an experiment in Zig lang. | [↗](https://github.com/knadh/csv2json) |
| **deepflowio/deepflow** | DeepFlow — zero-code eBPF observability — auto distributed tracing across any language without instrumentation | [↗](https://github.com/deepflowio/deepflow) |
| **Digital** | Digital logic designer and circuit simulator. Design circuits, simulate — browser-based. | [↗](https://github.com/hneemann/Digital) |
| **eisenzopf/rvoip** | VoIP library in Rust | [↗](https://github.com/eisenzopf/rvoip) |
| **ekzhang/bore** | bore — minimal TCP tunnel to expose local ports to remote server — simple ngrok alternative in Rust | [↗](https://github.com/ekzhang/bore) |
| **ElasticRun/barista** | Frappe app for automated functional testing | [↗](https://github.com/ElasticRun/barista) |
| **epsilon-records/epsilon.fm** | Open-source music distribution management | [↗](https://github.com/epsilon-records/epsilon.fm) |
| **facebookincubator/katran** | Katran — Facebook's L4 load balancer using eBPF/XDP — powers Facebook's production LB layer | [↗](https://github.com/facebookincubator/katran) |
| **fika** | Statically typed functional programming language for the web. Reading a new language design is always instructive. | [↗](https://github.com/fika-lang/fika) |
| **firecracker-microvm/firecracker** | Firecracker — AWS microVM for serverless — boots in 125ms minimal attack surface powers Lambda and Fargate | [↗](https://github.com/firecracker-microvm/firecracker) |
| **fossunited/mon_events** | Manage FOSS events (hackathons/meetups) | [↗](https://github.com/fossunited/mon_events) |
| **glincker/thesvg** | 6047+ brand SVG icons tree-shakeable and typed | [↗](https://github.com/glincker/thesvg) |
| **grafana/loki** | Grafana Loki — log aggregation like Prometheus but for logs — label-based no full-text index | [↗](https://github.com/grafana/loki) |
| **graphweaver** | Turn multiple data sources into a single GraphQL API — data federation layer. | [↗](https://github.com/exogee-technology/graphweaver) |
| **grokability/snipe-it** | Free open-source IT asset/license management | [↗](https://github.com/grokability/snipe-it) |
| **hasanharman/isomiddleearth** | Isometric Middle-earth world builder | [↗](https://github.com/hasanharman/isomiddleearth) |
| **helix-editor/helix** | Helix — post-modern modal text editor in Rust — treesitter and LSP built-in no plugins needed | [↗](https://github.com/helix-editor/helix) |
| **hetzner/hcloud-go** | Hetzner Cloud Go client — programmatic access to Hetzner's affordable bare metal and cloud VMs | [↗](https://github.com/hetzner/hcloud-go) |
| **hollow** | Netflix Java lib — disseminate in-memory datasets from single producer to many consumers for high-perf read-only access. Unique data distribution pattern. | [↗](https://github.com/Netflix/hollow) |
| **homebridge/homebridge** | Homebridge — add HomeKit support to non-Apple devices — bridge for smart home without vendor lock-in | [↗](https://github.com/homebridge/homebridge) |
| **iamd3vil/shelf** | Symlinks manager | [↗](https://github.com/iamd3vil/shelf) |
| **InvoiceShelf/InvoiceShelf** | Open-source invoicing solution | [↗](https://github.com/InvoiceShelf/InvoiceShelf) |
| **istio/istio** | Istio — service mesh with mTLS observability traffic management — Envoy sidecar for every pod | [↗](https://github.com/istio/istio) |
| **iv-org/invidious** | Alternative YouTube front-end | [↗](https://github.com/iv-org/invidious) |
| **iVideoGameBoss/iRoopDeepFaceCam** | Real-time face swap using insightface | [↗](https://github.com/iVideoGameBoss/iRoopDeepFaceCam) |
| **jaegertracing/jaeger** | Jaeger — distributed tracing system from Uber — trace requests across microservices end-to-end | [↗](https://github.com/jaegertracing/jaeger) |
| **jikan-me/jikan-rest** | REST API for MyAnimeList (Jikan) | [↗](https://github.com/jikan-me/jikan-rest) |
| **joeirimpan/listmonk-messenger** | Webhook handler for listmonk to forward to messengers | [↗](https://github.com/joeirimpan/listmonk-messenger) |
| **keep-hq/keep** | Keep — open-source AIOps and alert management — correlate deduplicate route alerts from any source | [↗](https://github.com/keep-hq/keep) |
| **lapce/lapce** | Lapce — lightning-fast code editor in Rust — GPU rendering native performance remote development | [↗](https://github.com/lapce/lapce) |
| **libbpf/libbpf** | libbpf — CO-RE eBPF library — stable ABI for writing portable eBPF programs | [↗](https://github.com/libbpf/libbpf) |
| **linkerd/linkerd2** | Linkerd — ultralight service mesh in Rust — zero-config mTLS latency-aware load balancing | [↗](https://github.com/linkerd/linkerd2) |
| **matijakolaric-com/django-music-publisher** | Music metadata management and royalty processing | [↗](https://github.com/matijakolaric-com/django-music-publisher) |
| **mr-karan/kong-service-exporter** | Export Kong service registry to Markdown | [↗](https://github.com/mr-karan/kong-service-exporter) |
| **neovim/neovim** | Neovim — hyperextensible Vim-based text editor — Lua scripting LSP treesitter async built-in | [↗](https://github.com/neovim/neovim) |
| **netbirdio/netbird** | NetBird — open-source Tailscale alternative — WireGuard overlay network with access policies | [↗](https://github.com/netbirdio/netbird) |
| **netdata/netdata** | Netdata — real-time distributed performance monitoring — per-second metrics zero config 2000+ integrations | [↗](https://github.com/netdata/netdata) |
| **OISF/suricata** | Suricata — high-performance multi-threaded IDS IPS NSM — stateful inspection deep packet analysis | [↗](https://github.com/OISF/suricata) |
| **openstatus/openstatus** | OpenStatus — open-source status page and uptime monitoring — API checks from edge locations | [↗](https://github.com/openstatus/openstatus) |
| **opentelemetry/opentelemetry-collector** | OTel Collector — vendor-neutral telemetry pipeline — ingest from anything export to anything | [↗](https://github.com/opentelemetry/opentelemetry-collector) |
| **openzipkin/zipkin** | Zipkin — distributed tracing from Twitter — latency analysis across service calls | [↗](https://github.com/openzipkin/zipkin) |
| **packer/packer** | Packer — build identical machine images for multiple platforms from single config — AMIs OVAs ISOs | [↗](https://github.com/packer/packer) |
| **Paymenter/Paymenter** | Free open-source webshop solution for hosting providers | [↗](https://github.com/Paymenter/Paymenter) |
| **pdf-scanner** | Makes PDFs look scanned — adds noise, skew, texture. Surprisingly useful for document workflows. | [↗](https://github.com/domdomegg/pdf-scanner) |
| **phw/peek** | Animated GIF screen recorder | [↗](https://github.com/phw/peek) |
| **plex/plex** | ,Plex — popular media server (freemium) — reference for comparing with Jellyfin Emby | [↗](https://github.com/plex/plex) |
| **prefecthq/prefect** | Prefect — Python-native workflow orchestration — modern Airflow alternative with dynamic DAGs | [↗](https://github.com/prefecthq/prefect) |
| **projectdiscovery/nuclei** | Nuclei — fast customizable vulnerability scanner with 10000+ community templates | [↗](https://github.com/projectdiscovery/nuclei) |
| **prometheus/prometheus** | Prometheus — de facto open-source metrics collection and alerting — pull-based time-series TSDB | [↗](https://github.com/prometheus/prometheus) |
| **purescript-presto** | Write apps like mathematical equations — functional reactive programming for UI. Juspay's unique approach. | [↗](https://github.com/juspay/purescript-presto) |
| **quic-pt** | QUIC Pluggable Transport for Tor — use QUIC to defeat traffic analysis and censorship. | [↗](https://github.com/ahf/quic-pt) |
| **rhnvrm/lzo1z** | Pure Go LZO1Z compression and decompression library — lossless compression algorithm port | [↗](https://github.com/rhnvrm/lzo1z) |
| **rhnvrm/simplelock** | i3lock wrapper with multiple modes (xkcd/unsplash) | [↗](https://github.com/rhnvrm/simplelock) |
| **shorebirdtech/updater** | libupdater for Shorebird OTA | [↗](https://github.com/shorebirdtech/updater) |
| **signalapp/libsignal** | libsignal — Signal Protocol library in Rust — double ratchet X3DH for E2E encryption | [↗](https://github.com/signalapp/libsignal) |
| **stalwartlabs/mail-parser** | Fast robust email parsing library for Rust | [↗](https://github.com/stalwartlabs/mail-parser) |
| **sumeetpatil/bitcoinalert** | Zebpay Bitcoin price alert | [↗](https://github.com/sumeetpatil/bitcoinalert) |
| **sundowndev/phoneinfoga** | Phone number information gathering framework | [↗](https://github.com/sundowndev/phoneinfoga) |
| **SuryaXanden/scylladb** | ScyllaDB — Cassandra-compatible DB in C++ — shard-per-core reactor pattern 10x throughput vs Cassandra | [↗](https://github.com/SuryaXanden/scylladb) |
| **Suwayomi/Suwayomi-Server** | Tachiyomi manga reader rewrite for desktop | [↗](https://github.com/Suwayomi/Suwayomi-Server) |
| **syncthing/syncthing** | Syncthing — continuous P2P file sync between devices — no central server Dropbox alternative | [↗](https://github.com/syncthing/syncthing) |
| **themeselection/materio-vuetify-vuejs-laravel-admin-template-free** | Free Vuetify + Laravel admin template | [↗](https://github.com/themeselection/materio-vuetify-vuejs-laravel-admin-template-free) |
| **three.wasm** | 8x faster JavaScript 3D library via WebAssembly. How WASM accelerates JS-native libraries. | [↗](https://github.com/mrdoob/three.wasm) |
| **tonarino/innernet** | innernet — private WireGuard-based network in Rust — structured overlay with server-managed access | [↗](https://github.com/tonarino/innernet) |
| **tonhowtf/omniget** | Open-source video/music/course downloader | [↗](https://github.com/tonhowtf/omniget) |
| **trpc/trpc** | tRPC — end-to-end typesafe APIs — TypeScript types flow from server to client without codegen | [↗](https://github.com/trpc/trpc) |
| **tuwunel** | Official successor to conduwuit — Matrix/Element server implementation. | [↗](https://github.com/matrix-construct/tuwunel) |
| **vectordotdev/vector** | Vector — high-performance observability pipeline — collect transform route logs metrics traces | [↗](https://github.com/vectordotdev/vector) |
| **voter-verifier-rb** | ElasticSearch system for matching people to voter registration records. Domain-specific fuzzy matching. | [↗](https://github.com/civiccc/voter-verifier-rb) |
| **win7 / Windows-11-Web** | Windows 7/11 simulated fully in browser. Engineering challenge: full desktop OS UX in HTML/CSS/JS. | [↗](https://github.com/khang-nd/win7) |
| **WireGuard/wireguard-go** | WireGuard-Go — pure Go WireGuard implementation — study the protocol implementation | [↗](https://github.com/WireGuard/wireguard-go) |
| **wslyvh/nexth** | Next.js + Ethereum starter kit with Viem/Wagmi/Web3Modal/SIWE | [↗](https://github.com/wslyvh/nexth) |
| **zed-industries/zed** | High-performance multiplayer code editor | [↗](https://github.com/zed-industries/zed) |
| **zeek/zeek** | Zeek — network analysis framework — scripting language for protocol analysis and anomaly detection | [↗](https://github.com/zeek/zeek) |
| **zig-releaser** | Use GoReleaser to build, release, publish Zig projects. Cross-language toolchain integration. | [↗](https://github.com/knadh/zig-releaser) |
| **zipdf / zigpdf** | High-performance PDF generation in Zig with declarative templates. Learning Zig through a real use case. | [↗](https://github.com/shridarpatil/zigpdf) |

---

## Other Tools Referenced (name only — link not independently verified)

> These tools were listed in the source collection under an account handle that didn't match the tool's actual public repository, so rather than publish a possibly-wrong link, only the name and description are kept here. Most are well-known projects — search the name directly to find the real repo.

| Tool | Description | Category |
|------|-------------|----------|
| **accelerate** | HuggingFace Accelerate — distributed training on any hardware — single GPU to multi-node | AI / ML / Agents |
| **acme** | acme — ACME protocol client library for Go — implement Let's Encrypt certificate issuance | Security & Recon |
| **act** | act — run GitHub Actions locally — test workflows without pushing to GitHub | Miscellaneous Notable Repos |
| **actix-web** | actix-web — practical and powerful Rust web framework — one of the fastest web frameworks period | Miscellaneous Notable Repos |
| **actual** | Actual Budget — local-first personal finance — end-to-end encrypted sync zero-based budgeting | Miscellaneous Notable Repos |
| **age** | age — simple file encryption tool in Rust — modern replace for PGP for file encryption | Dev Tooling & CLI |
| **age-encryption** | age — simple secure file encryption — designed to replace PGP for file encryption | Miscellaneous Notable Repos |
| **aix** | aix — AI-powered recon tool — LLM-assisted bug bounty and pentesting | AI / ML / Agents |
| **alacritty** | Alacritty — fastest terminal emulator — OpenGL GPU rendering no composite features minimal | Miscellaneous Notable Repos |
| **alloy** | Grafana Alloy — OpenTelemetry Collector distribution — batteries-included OTel pipeline | Miscellaneous Notable Repos |
| **altair** | Altair — declarative statistical visualization in Python — Vega-Lite based concise API | Miscellaneous Notable Repos |
| **alterx** | alterx — fast domain wordlist generator — mutation-based subdomain permutation for recon | Security & Recon |
| **amass** | Amass — in-depth DNS enumeration and attack surface mapping — OWASP project for recon | Security & Recon |
| **anyhow** | anyhow — flexible error handling for Rust — idiomatic error propagation with context chaining | Miscellaneous Notable Repos |
| **appsmith** | Appsmith — open-source low-code framework — build admin panels dashboards internal tools | Miscellaneous Notable Repos |
| **argo-workflows** | Argo Workflows — container-native workflow engine for Kubernetes — DAG step template jobs | Dev Tooling & CLI |
| **astro** | Astro — content-focused web framework — islands architecture partial hydration | Miscellaneous Notable Repos |
| **atuin** | Atuin — magical shell history — sync search encrypt history across machines SQLite backend | Security & Recon |
| **aws-cli** | AWS CLI — official AWS command line interface — manage all AWS services from terminal | Dev Tooling & CLI |
| **axum** | Axum — Tokio-based Rust web framework — ergonomic middleware tower-service compatible | Miscellaneous Notable Repos |
| **az** | Azure CLI — manage all Azure resources from terminal | Dev Tooling & CLI |
| **bandwhich** | bandwhich — terminal bandwidth utilization tool — shows per-process per-connection network usage | Dev Tooling & CLI |
| **base64** | base64 — base64 encoding and decoding for Rust — multiple alphabets streaming | Miscellaneous Notable Repos |
| **baserow** | Baserow — open-source no-code database — like Airtable but self-hosted Postgres-backed | Self-Hosted Apps & Platforms |
| **bat** | bat — cat with wings — syntax highlighting git integration automatic paging | Miscellaneous Notable Repos |
| **beancount** | Beancount — double-entry bookkeeping in plain text — strict syntax SQL-like queries | Storage & Databases |
| **bearer** | Bearer — code security tool — scan for sensitive data flows PII exposure API key leaks | Security & Recon |
| **beszel** | beszel — lightweight server monitoring hub — Docker container stats historical graphs alerts | Dev Tooling & CLI |
| **bind9** | BIND 9 — most widely deployed DNS server — reference implementation of DNS protocol | Networking & Infra |
| **blake3** | BLAKE3 — fastest cryptographic hash function — parallel tree hashing outperforms SHA-3 | Miscellaneous Notable Repos |
| **bleve** | bleve — modern text indexing in Go — full-text search in Go applications | Miscellaneous Notable Repos |
| **bokeh** | Bokeh — interactive web plots from Python — streaming dashboards without writing JavaScript | Miscellaneous Notable Repos |
| **bottom** | bottom — cross-platform graphical process and system monitor — like htop but better looking | Self-Hosted Apps & Platforms |
| **bpf-perf-tools-book** | bpf-perf-tools-book — BPF tools from Brendan Gregg — production performance analysis with eBPF | Miscellaneous Notable Repos |
| **brendangregg-perf** | perf-tools — Brendan Gregg's performance analysis tools — ftrace perf wrappers | Miscellaneous Notable Repos |
| **budibase** | Budibase — open-source low-code platform — build apps automate processes on your own infra | Self-Hosted Apps & Platforms |
| **buildkit** | BuildKit — next-generation Docker build — concurrent layer caching secrets cache mounts | Security & Recon |
| **buildkite** | buildkite-agent — fast CI/CD system — hybrid cloud self-hosted agents SaaS control plane | AI / ML / Agents |
| **buildpacks** | Cloud Native Buildpacks — transform source into container images — no Dockerfile heroku-style | Systems & Low-Level |
| **bytes** | Bytes — zero-copy bytes handling for Rust networking — powers Tokio Hyper and most async libs | Networking & Infra |
| **bytesize** | bytesize — human-readable byte sizes for Rust — format and parse 1.5 MB 3.2 GB naturally | Miscellaneous Notable Repos |
| **cachix** | cachix — binary cache hosting for Nix — share pre-built Nix packages avoid rebuilds | Dev Tooling & CLI |
| **cargo-audit** | cargo-audit — audit Rust dependencies for security vulnerabilities from RustSec advisory database | Security & Recon |
| **cargo-deny** | cargo-deny — lint Rust dependencies — check licenses vulnerabilities ban specific crates | Miscellaneous Notable Repos |
| **cargo-expand** | cargo-expand — show the result of macro expansion — essential for debugging derive macros | Miscellaneous Notable Repos |
| **cargo-machete** | cargo-machete — fast unused Rust dependency finder — grep-based simpler than cargo-udeps | Miscellaneous Notable Repos |
| **cargo-nextest** | cargo-nextest — next-generation test runner for Rust — parallel tests better output 3x faster | Miscellaneous Notable Repos |
| **cargo-udeps** | cargo-udeps — find unused dependencies in Rust — clean up Cargo.toml dead weight | Miscellaneous Notable Repos |
| **catboost** | CatBoost — gradient boosting by Yandex — handles categorical features natively | Miscellaneous Notable Repos |
| **certmagic** | CertMagic — automatic TLS certificate management for Go — used by Caddy internally | Miscellaneous Notable Repos |
| **cfssl** | CFSSL — Cloudflare's PKI and TLS toolkit — CA server bundler OCSP responder | Miscellaneous Notable Repos |
| **chacha20poly1305** | chacha20poly1305 — ChaCha20-Poly1305 AEAD for Rust — TLS 1.3 WireGuard cipher in pure Rust | Miscellaneous Notable Repos |
| **chaos** | chaos-client — access ProjectDiscovery Chaos dataset — all known subdomains for bug bounty programs | AI / ML / Agents |
| **checkmate** | Checkmate — self-hosted uptime and incident monitor — track server hardware response times | Self-Hosted Apps & Platforms |
| **checkmk** | Checkmk — comprehensive monitoring platform — metrics logs events single tool for everything | Dev Tooling & CLI |
| **chi** | chi — lightweight composable HTTP router in Go — idiomatic middleware chaining for Go services | Networking & Infra |
| **choose** | choose — human-friendly alternative to cut and awk — slice columns from output | Miscellaneous Notable Repos |
| **chromadb** | Chroma — open-source embedding database — store and query vectors in Python with filtering | AI / ML / Agents |
| **chrono** | chrono — date and time library for Rust — timezone-aware datetime arithmetic | Miscellaneous Notable Repos |
| **clap** | clap — command line argument parser for Rust — derive macros for CLI tools | Dev Tooling & CLI |
| **cloudflared** | cloudflared — Cloudflare Tunnel daemon — expose services without opening firewall ports | Security & Recon |
| **cloudlist** | cloudlist — multi-cloud asset discovery — enumerate all hosts IPs across AWS GCP Azure | Miscellaneous Notable Repos |
| **cluster-autoscaler** | cluster-autoscaler — Kubernetes node autoscaler — add/remove nodes based on pending pods | Dev Tooling & CLI |
| **codeql** | ,CodeQL — GitHub's semantic code analysis — queries to find security vulnerabilities in codebases | Security & Recon |
| **coder** | Coder — self-hosted cloud dev environments — provision workspaces on Kubernetes or cloud | Self-Hosted Apps & Platforms |
| **colored** | colored — coloring terminal text in Rust — simple macro-based ANSI color output | Miscellaneous Notable Repos |
| **commitlint** | commitlint — lint commit messages — enforce Conventional Commits format | Miscellaneous Notable Repos |
| **config** | config — layered configuration system for Rust — files env vars defaults merged | Miscellaneous Notable Repos |
| **console** | console — terminal manipulation library for Rust — colors styles ANSI escape codes | Miscellaneous Notable Repos |
| **coredns** | CoreDNS — CNCF DNS server — plugin-based serves Kubernetes cluster DNS service discovery | Dev Tooling & CLI |
| **corteza** | Corteza — open-source Salesforce alternative — CRM messaging automation low-code | Self-Hosted Apps & Platforms |
| **cosign** | cosign — container image signing and verification — Sigstore keyless signing for supply chain | Security & Recon |
| **cranelift** | Cranelift — fast code generator backend — used in Wasmtime for JIT compilation | Dev Tooling & CLI |
| **criterion** | criterion — statistics-driven microbenchmarking library for Rust — reliable perf measurements | Miscellaneous Notable Repos |
| **crossbeam** | crossbeam — tools for concurrent programming in Rust — channels epoch GC work-stealing deque | Miscellaneous Notable Repos |
| **ctop** | ctop — top-like interface for containers — real-time metrics per container resource usage | Systems & Low-Level |
| **cursive** | cursive — text-based UI library for Rust — dialog boxes menus from terminal applications | Miscellaneous Notable Repos |
| **cvemap** | cvemap — CLI for navigating CVE data — search filter enrich CVEs from NVD OSV Nuclei templates | Security & Recon |
| **cytoscape.js** | Cytoscape.js — graph theory library for browser and Node — network visualization analysis | Miscellaneous Notable Repos |
| **d2** | D2 — declarative diagram scripting language — modern alternative to Graphviz and Mermaid | Miscellaneous Notable Repos |
| **d3** | D3.js — data-driven documents — bind data to DOM and transform with SVG CSS JavaScript | Miscellaneous Notable Repos |
| **dagger** | Dagger — portable CI/CD engine — define pipelines in code runs locally or in CI same result | Dev Tooling & CLI |
| **dashmap** | DashMap — concurrent hashmap for Rust — sharded design high read write concurrency | Miscellaneous Notable Repos |
| **delta** | delta — better git diff — syntax highlighting side-by-side view line numbers | Miscellaneous Notable Repos |
| **detect-secrets** | detect-secrets — Yelp's tool for detecting secrets — pre-commit hook baseline file approach | Security & Recon |
| **devenv** | devenv — fast rich developer environments using Nix — per-project isolated dev shells | Dev Tooling & CLI |
| **devpod** | DevPod — codespaces but open-source — dev containers on any cloud or local machine | Miscellaneous Notable Repos |
| **devspace** | DevSpace — cloud-native development tool — develop inside Kubernetes with hot reload | Dev Tooling & CLI |
| **dialoguer** | dialoguer — interactive prompts for Rust CLI — select input confirm password from terminal | Dev Tooling & CLI |
| **diesel** | Diesel — safe extensible Rust ORM — compile-time query validation prevents SQL errors at build | Storage & Databases |
| **diffusers** | HuggingFace Diffusers — state-of-the-art diffusion models — Stable Diffusion SDXL inference | AI / ML / Agents |
| **dioxus** | Dioxus — cross-platform Rust UI library — web desktop mobile TUI from single codebase | Mobile & Flutter/Android |
| **dive** | dive — tool to explore Docker image layers — find waste optimize image size | Dev Tooling & CLI |
| **dnsdist** | dnsdist — DNS load balancer from PowerDNS — rate limiting DDoS protection frontend for DNS | Networking & Infra |
| **dnsx** | dnsx — fast DNS toolkit for running bulk queries — resolve validate bruteforce DNS records at scale | Networking & Infra |
| **dockle** | dockle — container image linter — security best practices CIS benchmark checks | Security & Recon |
| **doctl** | doctl — DigitalOcean CLI — manage droplets databases DNS load balancers from terminal | Dev Tooling & CLI |
| **docusaurus** | Docusaurus — documentation site generator by Meta — versioning i18n search React-based | Dev Tooling & CLI |
| **dolibarr** | Dolibarr — open-source ERP and CRM — SME-focused invoicing stock HR project modules | Self-Hosted Apps & Platforms |
| **drawio** | draw.io — open-source diagramming — flowcharts ERDs network diagrams offline capable | Miscellaneous Notable Repos |
| **drone** | Drone — container-native CI/CD — pipeline as code YAML Docker-native | Dev Tooling & CLI |
| **druid** | Druid — data-first Rust UI toolkit — retained-mode with reactive bindings | Miscellaneous Notable Repos |
| **duf** | duf — better df — disk usage/free utility with nice output and color coding | Miscellaneous Notable Repos |
| **dust** | dust — intuitive disk usage analyzer — visual tree of largest disk consumers | Miscellaneous Notable Repos |
| **earthly** | Earthly — reproducible builds in containers — like Makefile but container-native cacheable | Systems & Low-Level |
| **echo** | Echo — high-performance minimalist Go web framework — middleware router template engine | Miscellaneous Notable Repos |
| **ed25519-dalek** | ed25519-dalek — Ed25519 signatures for Rust — pure Rust fast constant-time implementation | Miscellaneous Notable Repos |
| **egui** | egui — easy immediate-mode GUI for Rust — runs in browser native desktop embedding | AI / ML / Agents |
| **eksctl** | eksctl — official CLI for Amazon EKS — create manage upgrade EKS clusters | Dev Tooling & CLI |
| **eleventy** | Eleventy — simpler static site generator — no client-side JS by default multi-template | Dev Tooling & CLI |
| **elysia** | Elysia — Bun-native TypeScript web framework — fast ergonomic with end-to-end type safety | Miscellaneous Notable Repos |
| **espocrm** | EspoCRM — open-source CRM — sales marketing customer support pipeline management | Self-Hosted Apps & Platforms |
| **excalidraw** | Excalidraw — virtual whiteboard — hand-drawn style diagrams collaborative self-hostable | Miscellaneous Notable Repos |
| **exllamav2** | ExLlamaV2 — fast LLM inference for GPTQ quantized models — optimized CUDA kernels | AI / ML / Agents |
| **express** | Express — minimal Node.js web framework — still the most widely deployed Node backend | Miscellaneous Notable Repos |
| **eza** | eza — modern ls replacement — git integration icons color coding tree view | Miscellaneous Notable Repos |
| **falcosidekick** | falcosidekick — fan-out Falco alerts — route security events to Slack PagerDuty JIRA etc | Security & Recon |
| **fastify** | Fastify — fast and low overhead Node.js web framework — schema validation serialization | Miscellaneous Notable Repos |
| **fd** | fd — simple fast alternative to find — respects .gitignore regex support parallel execution | Miscellaneous Notable Repos |
| **ffuf** | ffuf — fast web fuzzer in Go — directory enumeration vhost discovery API endpoint bruteforce | Miscellaneous Notable Repos |
| **fiber** | Fiber — Express-inspired Go web framework built on fasthttp — zero memory allocation in hot paths | Miscellaneous Notable Repos |
| **firefly-iii** | Firefly III — self-hosted personal finance manager — budgets categories rules recurring transactions | Self-Hosted Apps & Platforms |
| **flake** | nix flakes — experimental Nix feature — reproducible composable project-level Nix configs | Dev Tooling & CLI |
| **flamegraph** | flamegraph — easy flamegraphs for Rust programs — CPU profiling with perf and DTrace | Miscellaneous Notable Repos |
| **flume** | flume — fast multi-producer multi-consumer channel for Rust — faster than std mpsc | Miscellaneous Notable Repos |
| **focalboard** | Focalboard — open-source Trello/Notion alternative — project management kanban tables | Miscellaneous Notable Repos |
| **forgejo** | Forgejo — community-driven Gitea fork — self-hosted git with Actions CI package registry | Self-Hosted Apps & Platforms |
| **freshping** | Similar: freshping-alternative self-hosted monitoring | Self-Hosted Apps & Platforms |
| **frps** | frp — fast reverse proxy — expose local servers behind NAT via secure tunnel to public server | Networking & Infra |
| **garden** | Garden — full-stack testing and deployment tool for Kubernetes — test preview environments | Dev Tooling & CLI |
| **gatsby** | Gatsby — React static site generator — GraphQL data layer image optimization | Dev Tooling & CLI |
| **gatus** | Gatus — developer-oriented status page — YAML-defined health checks with alerting | Miscellaneous Notable Repos |
| **gau** | gau — fetch known URLs — pulls all URLs for a domain from Wayback AlienVault Common Crawl | Miscellaneous Notable Repos |
| **gcloud** | gcloud — Google Cloud SDK — manage GCP resources compute storage networking | Networking & Infra |
| **gdu** | gdu — fast disk usage analyzer with TUI — parallel scan of large directories | Miscellaneous Notable Repos |
| **gephi** | Gephi — open-source network analysis and visualization — explore large graph datasets | Miscellaneous Notable Repos |
| **gerrit** | Gerrit — code review system from Google — structured code review for large teams | Miscellaneous Notable Repos |
| **ghost** | Ghost — open-source publishing platform — headless Node.js CMS for newsletters and blogs | Self-Hosted Apps & Platforms |
| **ghostty** | Ghostty — fast feature-rich terminal emulator in Zig — native UI per platform very low latency | Self-Hosted Apps & Platforms |
| **gin** | Gin — high-performance HTTP web framework in Go — fastest Go web framework with router and middleware | Networking & Infra |
| **git-secrets** | git-secrets — AWS Labs tool to prevent secrets in commits — pre-commit hook patterns | Security & Recon |
| **gitlab-ce** | GitLab CE — self-hosted DevOps platform — Git CI/CD registry security scanning all-in-one | Security & Recon |
| **gitleaks** | gitleaks — detect secrets in git repos — scan history for API keys passwords tokens | Security & Recon |
| **gitpod** | Gitpod — cloud dev environments — ephemeral workspaces from any GitHub GitLab Bitbucket URL | Miscellaneous Notable Repos |
| **glances** | Glances — cross-platform system monitor — web UI REST API monitoring daemon | Self-Hosted Apps & Platforms |
| **glpi** | GLPI — open-source IT asset management — inventory ticketing helpdesk ITIL-compliant | Self-Hosted Apps & Platforms |
| **gnucash** | GnuCash — personal and small business financial accounting — double-entry GAAP-compliant | Payments & Fintech |
| **gogs** | Gogs — painless self-hosted git — ultra-lightweight single binary minimal resource usage | Self-Hosted Apps & Platforms |
| **golangci-lint** | golangci-lint — fast Go linters aggregator — runs 50+ linters in parallel from single binary | Go Ecosystem |
| **goldilocks** | goldilocks — Kubernetes VPA recommendation UI — right-size container resource requests | Dev Tooling & CLI |
| **gopgp** | gopgp — OpenPGP library in Go — used by ProtonMail and others for PGP operations in Go | Miscellaneous Notable Repos |
| **goreleaser** | GoReleaser — release automation for Go — build cross-platform binaries create GitHub releases | Dev Tooling & CLI |
| **gotenberg** | Gotenberg — Docker-powered API for PDF generation — Chromium LibreOffice conversion to PDF | Dev Tooling & CLI |
| **gotify** | Gotify — self-hosted push notification server — websocket delivery real-time alerts | Self-Hosted Apps & Platforms |
| **graphviz** | Graphviz — graph visualization — DOT language for dependency and relationship diagrams | Miscellaneous Notable Repos |
| **grex** | grex — generate regex from test cases — infer regular expression from examples automatically | Miscellaneous Notable Repos |
| **grocy** | Grocy — self-hosted grocery and household management — ERP for your home pantry tracking | Self-Hosted Apps & Platforms |
| **grype** | grype — vulnerability scanner for container images — fast SBOM-aware alternative to Trivy | Systems & Low-Level |
| **gtk-rs** | gtk-rs — Rust bindings for GTK4 — native Linux GUI development from Rust | Systems & Low-Level |
| **hadolint** | hadolint — Dockerfile linter — enforces best practices static analysis for Dockerfiles | Dev Tooling & CLI |
| **haproxy** | HAProxy — battle-tested L4/L7 load balancer — used at scale by GitHub Reddit Stack Overflow | Miscellaneous Notable Repos |
| **haystack** | Haystack — open-source LLM framework — build search QA RAG production pipelines | AI / ML / Agents |
| **hcloud** | hcloud — Hetzner Cloud CLI — manage Hetzner VMs networks LBs volumes programmatically | Dev Tooling & CLI |
| **heaptrack** | heaptrack — heap memory profiler — visualize all heap allocations in a program | Miscellaneous Notable Repos |
| **hex** | hex — hex encoding and decoding for Rust — encode arbitrary bytes to hex strings | Miscellaneous Notable Repos |
| **hledger** | hledger — plain text accounting tool — Ledger-compatible with web and terminal UI | Payments & Fintech |
| **home-manager** | Home Manager — manage user environment with Nix — dotfiles packages services declaratively | Dev Tooling & CLI |
| **hono** | Hono — ultrafast web framework for the edge — runs on Cloudflare Workers Deno Bun Fastly | Miscellaneous Notable Repos |
| **hotspot** | hotspot — Linux perf GUI — flamegraphs call trees for perf.data files | Systems & Low-Level |
| **httpx** | httpx — fast HTTP toolkit — probe hosts for running services technology detection status codes | Networking & Infra |
| **hugo** | Hugo — fastest static site generator — Go templates shortcodes 1000 pages per second | Dev Tooling & CLI |
| **humantime** | humantime — human-readable time formatting for Rust — parse and display durations naturally | Miscellaneous Notable Repos |
| **husky** | husky — Git hooks for Node.js projects — run scripts on commit push | Miscellaneous Notable Repos |
| **hyper** | Hyper — fast and correct HTTP implementation in Rust — low-level HTTP/1 HTTP/2 library | Networking & Infra |
| **hyperfine** | hyperfine — command-line benchmarking tool — statistical timing with warmup and comparisons | Dev Tooling & CLI |
| **iced** | iced — Elm-inspired GUI library for Rust — cross-platform reactive UI with async support | Self-Hosted Apps & Platforms |
| **icinga** | Icinga — Nagios fork with modern features — DSL for configuration REST API | Miscellaneous Notable Repos |
| **in-toto** | in-toto — software supply chain security framework — verify every step in build pipeline | Security & Recon |
| **indicatif** | indicatif — progress bars for Rust CLI apps — multi-progress spinners ETA display | Dev Tooling & CLI |
| **insta** | insta — snapshot testing library for Rust — review diffs update snapshots in one command | Miscellaneous Notable Repos |
| **interactsh** | Interactsh — OOB interaction server — detect blind SSRF XXE log4j via DNS HTTP SMTP callbacks | Networking & Infra |
| **jax** | JAX — composable transformations of Python functions — autograd XLA JIT GPU TPU | Miscellaneous Notable Repos |
| **just** | just — command runner — better make for running project-specific commands | Miscellaneous Notable Repos |
| **k9s** | k9s — terminal UI to interact with Kubernetes — navigate pods logs exec from beautiful TUI | Dev Tooling & CLI |
| **kaniko** | kaniko — build container images inside Kubernetes — no Docker daemon privileged mode needed | Dev Tooling & CLI |
| **karpenter** | Karpenter — Kubernetes node provisioning — automatically provision right-sized nodes in seconds | Dev Tooling & CLI |
| **katana** | Katana — fast web crawler — crawls JavaScript-rendered pages finds all endpoints for recon | Security & Recon |
| **keda** | KEDA — Kubernetes-based event-driven autoscaling — scale from zero based on queue depth metrics | Dev Tooling & CLI |
| **kind** | kind — Kubernetes in Docker — local k8s clusters for testing using Docker containers | Dev Tooling & CLI |
| **kitty** | kitty — GPU-based terminal emulator — graphics protocol tiling multiplexer remote kitten scripts | Miscellaneous Notable Repos |
| **knot-resolver** | Knot Resolver — fast DNSSEC-validating resolver — modular Lua-scriptable DNS resolver | Networking & Infra |
| **ko** | ko — build Go container images from source — no Dockerfile pushes directly to registry | Systems & Low-Level |
| **krew** | krew — kubectl plugin manager — discover install and manage kubectl plugins | Miscellaneous Notable Repos |
| **kroki** | Kroki — unified API for diagram generation — render Mermaid PlantUML D2 Graphviz from text | Miscellaneous Notable Repos |
| **kube-bench** | kube-bench — CIS Kubernetes benchmark tool — check cluster security configuration | Security & Recon |
| **kube-hunter** | kube-hunter — Kubernetes pentesting tool — hunt security weaknesses from inside and outside | Security & Recon |
| **kubectl-neat** | kubectl-neat — clean up kubectl output — remove clutter from kubectl get output | Miscellaneous Notable Repos |
| **kubectx** | kubectx/kubens — faster cluster and namespace switching — shell completion fzf integration | Miscellaneous Notable Repos |
| **kubescape** | kubescape — Kubernetes security posture management — NSA MITRE hardening checks | Security & Recon |
| **kustomize** | kustomize — Kubernetes config management via overlays — no templating pure YAML patches | Dev Tooling & CLI |
| **lalrpop** | LALRPOP — LR(1) parser generator for Rust — define grammars in .lalrpop generate efficient parsers | Dev Tooling & CLI |
| **langchain** | LangChain — framework for LLM applications — chains agents tools retrieval document loaders | AI / ML / Agents |
| **latex** | ,LaTeX — reference typesetting system — mathematical typesetting academic papers technical docs | Miscellaneous Notable Repos |
| **lazydocker** | lazydocker — terminal UI for Docker — manage containers images volumes from TUI | Dev Tooling & CLI |
| **leantime** | Leantime — open-source project management — goals milestones ideas timesheet strategy | Miscellaneous Notable Repos |
| **ledger** | Ledger — command-line double-entry accounting — plain text files powerful reporting | Payments & Fintech |
| **lego** | lego — ACME client in Go — request certificates from Let's Encrypt any ACME server | Security & Recon |
| **leptos** | Leptos — Rust full-stack web framework — reactive signals server-side rendering fine-grained updates | Miscellaneous Notable Repos |
| **librenms** | LibreNMS — auto-discovering network monitoring — SNMP-based for routers switches firewalls | Miscellaneous Notable Repos |
| **lightgbm** | LightGBM — gradient boosting by Microsoft — faster and lower memory than XGBoost | Miscellaneous Notable Repos |
| **lima** | Lima — Linux VMs on macOS — automatic file sharing port forwarding containerd | Systems & Low-Level |
| **linode-cli** | linode-cli — Akamai Cloud CLI — manage Linode compute networking object storage | Dev Tooling & CLI |
| **lint-staged** | lint-staged — run linters on staged git files — fast only checks changed files | Miscellaneous Notable Repos |
| **llama.cpp** | llama.cpp — LLM inference in C++ — run Llama Mistral on CPU MPS CUDA with quantization | AI / ML / Agents |
| **llamaindex** | LlamaIndex — data framework for LLM apps — ingestion indexing querying over private data | AI / ML / Agents |
| **lm-studio** | LM Studio — local LLM GUI — browse download and run models GGUF format | AI / ML / Agents |
| **loom** | loom — concurrency testing for Rust — permutation-based thread scheduling exploration | Miscellaneous Notable Repos |
| **lsof** | lsof — list open files — see what files processes have open critical for debugging | Miscellaneous Notable Repos |
| **ltrace** | ltrace — library call tracer — trace calls to shared libraries like strace but for libs | Miscellaneous Notable Repos |
| **manticore-search** | Manticore Search — easy-to-use open-source search — MySQL protocol compatible fast text search | Storage & Databases |
| **mapcidr** | mapcidr — utility for CIDR manipulation — split aggregate expand CIDR ranges for recon pipelines | Security & Recon |
| **marp** | Marp — Markdown presentation ecosystem — CLI VS Code extension themes export to PDF | Dev Tooling & CLI |
| **masscan** | masscan — fastest TCP port scanner — scan entire internet in under 6 minutes XDP-style approach | Miscellaneous Notable Repos |
| **matplotlib** | Matplotlib — comprehensive 2D plotting for Python — reference visualization library since 2003 | Miscellaneous Notable Repos |
| **mdbook** | mdBook — create books from Markdown — Rust community's documentation tool static site | Dev Tooling & CLI |
| **mealie** | Mealie — self-hosted recipe manager — meal planning shopping list import from URL | Self-Hosted Apps & Platforms |
| **meilisearch** | Meilisearch — fast typo-tolerant search engine — millisecond search REST API minimal setup | Miscellaneous Notable Repos |
| **mermaid** | Mermaid — diagram from text in Markdown — flowcharts sequence Gantt git graphs | Miscellaneous Notable Repos |
| **metrics** | metrics — ergonomic metrics facade for Rust — Prometheus StatsD backends | Miscellaneous Notable Repos |
| **milvus** | Milvus — cloud-native vector database — billion-scale similarity search distributed | Storage & Databases |
| **mime** | mime — MIME types for Rust — parse and construct content-type headers | Miscellaneous Notable Repos |
| **minikube** | minikube — local Kubernetes — start a single-node cluster for local dev | Dev Tooling & CLI |
| **miri** | Miri — undefined behavior detector for Rust — runs Rust programs in an interpreter catches UB | Miscellaneous Notable Repos |
| **mkdocs** | MkDocs — static site generator for documentation — Material theme widely used in OSS | Dev Tooling & CLI |
| **mlc-llm** | MLC LLM — machine learning compilation for LLMs — deploy on phone GPU web browser | AI / ML / Agents |
| **moka** | moka — high-performance caching library for Rust — concurrent TinyLFU eviction W-TinyLFU | Miscellaneous Notable Repos |
| **mold** | mold — fastest linker — faster than gold lld for large Rust C++ projects link time | Miscellaneous Notable Repos |
| **munin** | Munin — networked resource monitoring — graph historical resource usage across many hosts | Miscellaneous Notable Repos |
| **mupdf** | MuPDF — lightweight PDF and XPS viewer — used in embedded systems and CLI workflows | Dev Tooling & CLI |
| **naabu** | naabu — fast port scanner in Go — SYN/CONNECT scan with service detection and nmap integration | Miscellaneous Notable Repos |
| **nagios** | Nagios — reference open-source monitoring — plugin ecosystem alerting for hosts and services | Miscellaneous Notable Repos |
| **ncdu** | ncdu — NCurses-based disk usage analyzer — find what's eating your disk space interactively | Miscellaneous Notable Repos |
| **nest** | NestJS — opinionated TypeScript Node.js framework — dependency injection decorators enterprise patterns | Miscellaneous Notable Repos |
| **netbox** | NetBox — open-source network source of truth — IPAM DCIM rack management cable tracing | Miscellaneous Notable Repos |
| **netdata** | Netdata — real-time per-second system metrics — zero-config 2000+ integrations streaming | Miscellaneous Notable Repos |
| **nextra** | Nextra — Next.js-based docs framework — MDX Flexsearch dark mode built-in | Miscellaneous Notable Repos |
| **nfpm** | nfpm — simple deb rpm apk packaging in Go — create Linux packages from YAML config | Mobile & Flutter/Android |
| **nix** | Nix — purely functional package manager — reproducible builds isolated environments no conflicts | Dev Tooling & CLI |
| **nix-darwin** | nix-darwin — NixOS modules for macOS — declarative macOS configuration with Homebrew integration | Dev Tooling & CLI |
| **nixos** | NixOS — Linux distribution built on Nix — entire OS configured from single nix expression | Dev Tooling & CLI |
| **nixpkgs** | nixpkgs — largest package collection for Nix — 80000+ packages all reproducibly built | Dev Tooling & CLI |
| **nmap** | Nmap — reference port scanner and network discovery tool — used as basis for all recon tooling | Security & Recon |
| **nocodb** | NocoDB — open-source Airtable alternative — turn any database into a smart spreadsheet | Storage & Databases |
| **nom** | nom — parser combinator framework in Rust — zero-copy binary and text protocol parsers | Miscellaneous Notable Repos |
| **notify** | notify — send findings to Slack Discord Telegram from CLI tools — pipe any output to notifications | Dev Tooling & CLI |
| **nrich** | nrich — enrich IP with metadata — Shodan data for IPs offline fast for bulk enrichment | Miscellaneous Notable Repos |
| **ntfy** | ntfy — push notification service over HTTP — send notifications to any device via curl subscribe via SSE | Networking & Infra |
| **nuclei** | Nuclei — fast vulnerability scanner using community templates — YAML-defined checks at scale | Miscellaneous Notable Repos |
| **num-format** | num-format — locale-aware number formatting for Rust — thousand separators currency | Miscellaneous Notable Repos |
| **numpy** | NumPy — fundamental scientific computing in Python — N-dimensional array vectorized operations | Miscellaneous Notable Repos |
| **nushell** | Nushell — modern shell with structured data — treat command output as tables not text | Miscellaneous Notable Repos |
| **observable-plot** | Observable Plot — concise API for exploratory data visualization — built on D3 less verbose | Miscellaneous Notable Repos |
| **odoo** | Odoo — comprehensive open-source ERP — sales purchase inventory accounting HR website | Payments & Fintech |
| **okteto** | Okteto — develop applications directly in Kubernetes — replace pods with dev containers | Dev Tooling & CLI |
| **ollama** | Ollama — run LLMs locally — pull and serve models like Docker for LLMs | AI / ML / Agents |
| **oncall** | Grafana OnCall — incident management integrated with Grafana — on-call schedules alerting | Miscellaneous Notable Repos |
| **once_cell** | once_cell — single assignment cell and lazy value for Rust — standard for one-time initialization | Miscellaneous Notable Repos |
| **onnxruntime** | ONNX Runtime — cross-platform ML inference — deploy models from PyTorch TensorFlow on any hardware | AI / ML / Agents |
| **opennms** | OpenNMS — enterprise open-source network management — SNMP topology discovery fault management | Miscellaneous Notable Repos |
| **openpgp** | openpgp — Go standard library's OpenPGP implementation — message signing encryption verification | Security & Recon |
| **openproject** | OpenProject — open-source project management — Gantt charts agile boards time tracking | Miscellaneous Notable Repos |
| **opensearch** | OpenSearch — community fork of Elasticsearch — AWS-backed open governance search and analytics | Miscellaneous Notable Repos |
| **opentelemetry-operator** | OpenTelemetry Operator — auto-instrument apps in Kubernetes — inject OTel agents via annotations | Dev Tooling & CLI |
| **openvas** | OpenVAS/Greenbone — full-featured open-source vulnerability scanner — network service and web app scanning | Miscellaneous Notable Repos |
| **opnsense** | OPNsense — open-source firewall and router based on FreeBSD — pfSense fork with better UX | Security & Recon |
| **osv-scanner** | OSV Scanner — vulnerability scanning using OSV database — Google's open-source vuln scanner | Storage & Databases |
| **oxidized** | Oxidized — network device config backup — automatic versioned backup of router switch configs | Miscellaneous Notable Repos |
| **pagerduty-opensource** | Similar: PagerDuty alternatives — keep-hq/keep open-source alert management and AIOps platform | Self-Hosted Apps & Platforms |
| **pandas** | Pandas — data manipulation and analysis in Python — the standard DataFrame library | Miscellaneous Notable Repos |
| **pandoc** | Pandoc — universal document converter — Markdown to PDF DOCX HTML LaTeX and 40+ formats | Miscellaneous Notable Repos |
| **parking_lot** | parking_lot — efficient sync primitives for Rust — faster Mutex RwLock than std | Miscellaneous Notable Repos |
| **pdtm** | pdtm — ProjectDiscovery tool manager — install update all PD tools from one CLI | Dev Tooling & CLI |
| **peft** | PEFT — parameter-efficient fine-tuning — LoRA QLoRA prefix tuning without full training | AI / ML / Agents |
| **pelican** | Pelican — static site generator in Python — Jinja2 templates reStructuredText Markdown | Dev Tooling & CLI |
| **perf** | perf — Linux profiling tool — CPU cycles cache misses branch mispredictions hardware counters | Storage & Databases |
| **pest** | pest — PEG parser generator for Rust — define grammars in .pest files generate parsers | Dev Tooling & CLI |
| **pfsense** | pfSense — widely deployed open-source firewall/router — stateful packet inspection VPN IDS | Security & Recon |
| **pgvector** | pgvector — open-source vector similarity search for Postgres — IVFFlat HNSW indexing | Storage & Databases |
| **phabricator** | Phabricator (archived) — Facebook's internal code review tool — study for large-scale review design | Dev Tooling & CLI |
| **phpipam** | phpIPAM — open-source IP address management — subnet management VLAN tracking IPv4 IPv6 | Miscellaneous Notable Repos |
| **plantuml** | PlantUML — UML diagrams from text — sequence class activity state ER diagrams | Miscellaneous Notable Repos |
| **plotly** | Plotly — interactive graphing library — Python R JS charts dashboards Dash | Miscellaneous Notable Repos |
| **poem** | Poem — full-featured Rust web framework — OpenAPI spec generation macro-based routing | Miscellaneous Notable Repos |
| **polaris** | Polaris — Kubernetes best practice validation — admission webhook and audit tool | Dev Tooling & CLI |
| **polars** | Polars — fast DataFrame library in Rust with Python bindings — columnar lazy evaluation | Miscellaneous Notable Repos |
| **popeye** | popeye — Kubernetes cluster sanitizer — scans live cluster for resource misconfigs | Dev Tooling & CLI |
| **poppler** | poppler — PDF rendering library — used by most Linux PDF viewers and tools | Systems & Low-Level |
| **pre-commit** | pre-commit — framework for managing pre-commit hooks — run linters formatters scanners on commit | Miscellaneous Notable Repos |
| **prettytable-rs** | prettytable-rs — print tables in terminal from Rust — format tabular data for CLI output | Dev Tooling & CLI |
| **procs** | procs — modern replacement for ps — color output Docker integration search filter | Dev Tooling & CLI |
| **proptest** | proptest — property-based testing for Rust — auto-generate inputs to find edge cases | Miscellaneous Notable Repos |
| **prost** | prost — Protocol Buffers implementation for Rust — used by Tonic for gRPC serialization | Miscellaneous Notable Repos |
| **proxify** | proxify — Swiss army knife proxy for HTTP/HTTPS — intercept modify replay web traffic during recon | Security & Recon |
| **pytorch** | PyTorch — open-source ML framework — dynamic computation graphs used by most AI research | AI / ML / Agents |
| **qdrant** | Qdrant — vector similarity search engine — payload filtering HNSW index Rust high performance | Security & Recon |
| **quinn** | Quinn — QUIC protocol implementation in Rust — async Tokio-based high-performance QUIC | Miscellaneous Notable Repos |
| **racktables** | RackTables — datacenter asset management — racks devices cables patch panels IP management | Miscellaneous Notable Repos |
| **rand** | rand — random number generation for Rust — CSPRNG and statistical distributions | Miscellaneous Notable Repos |
| **ratatui** | ratatui — Rust library for building terminal UIs — widgets tables charts in the terminal | Miscellaneous Notable Repos |
| **rayon** | Rayon — data parallelism library for Rust — parallel iterators auto-tune thread count to cores | Miscellaneous Notable Repos |
| **regex** | regex — fast regex engine in Rust — linear time guarantees no backtracking catastrophe | Miscellaneous Notable Repos |
| **reqwest** | reqwest — ergonomic async HTTP client for Rust — Tokio-backed batteries-included | Networking & Infra |
| **retool** | Retool-alternative: open-source internal tool builder | Dev Tooling & CLI |
| **reveal.js** | reveal.js — HTML presentation framework — code syntax highlighting speaker view PDF export | Miscellaneous Notable Repos |
| **reviewdog** | reviewdog — automated code review tool — posts linter results as PR comments | Dev Tooling & CLI |
| **ring** | ring — safe fast crypto in Rust — RSA ECDSA AES GCM used in Rustls | Miscellaneous Notable Repos |
| **rio** | Rio — GPU-accelerated terminal emulator — WGPU rendering WebAssembly plugin support | Miscellaneous Notable Repos |
| **ripgrep** | ripgrep — regex search tool — respects .gitignore fastest grep in benchmarks | Dev Tooling & CLI |
| **rocket** | Rocket — type-safe web framework for Rust — request guards fairings compile-time validation | Miscellaneous Notable Repos |
| **rustls** | Rustls — modern TLS library in Rust — safe fast alternative to OpenSSL used in curl | Miscellaneous Notable Repos |
| **salvo** | Salvo — simple and powerful Rust web framework — built-in OpenAPI WebSocket multipart | Networking & Infra |
| **sccache** | sccache — shared compilation cache — ccache for Rust C C++ speeds up CI dramatically | Storage & Databases |
| **scikit-learn** | scikit-learn — machine learning library for Python — classification regression clustering pipelines | Miscellaneous Notable Repos |
| **scipy** | SciPy — scientific computing library — optimization signal processing linear algebra stats | Miscellaneous Notable Repos |
| **scorecard** | OpenSSF Scorecard — security health checks for open-source — automated security posture scoring | Security & Recon |
| **sd** | sd — intuitive find and replace CLI — sed alternative with literal strings by default | Dev Tooling & CLI |
| **sea-orm** | SeaORM — async Rust ORM — dynamic queries multi-DB Postgres MySQL SQLite | Storage & Databases |
| **seaborn** | Seaborn — statistical data visualization on Matplotlib — high-level attractive API | Miscellaneous Notable Repos |
| **semantic-release** | semantic-release — automated versioning and changelog — derives semver from commit messages | Miscellaneous Notable Repos |
| **semgrep** | Semgrep — static analysis tool — find bugs enforce code standards at scale pattern matching | Dev Tooling & CLI |
| **serde** | Serde — serialization/deserialization framework for Rust — JSON TOML YAML Bincode and more | Miscellaneous Notable Repos |
| **sha2** | sha2 — SHA-2 hash functions in pure Rust — SHA-256 SHA-384 SHA-512 | Miscellaneous Notable Repos |
| **simplehttpserver** | simplehttpserver — feature-rich alternative to Python http.server — file upload auth CORS | Security & Recon |
| **skaffold** | Skaffold — CI/CD for Kubernetes — detect changes build push deploy automatically | Dev Tooling & CLI |
| **slidev** | Slidev — presentation slides from Markdown for developers — code highlights live demos | Miscellaneous Notable Repos |
| **slint** | Slint — declarative GUI toolkit for Rust C++ and JavaScript — embedded and desktop | IoT & Embedded |
| **slsa** | ,SLSA framework — supply chain security levels — provenance attestation for build artifacts | Security & Recon |
| **snort** | Snort — open-source IDS/IPS — packet-based rule matching for intrusion detection | Miscellaneous Notable Repos |
| **solr** | Apache Solr — enterprise search platform — Lucene-based powerful faceting geospatial ranking | Geospatial & Maps |
| **sonarqube** | SonarQube — continuous code quality and security — multi-language static analysis and coverage | Security & Recon |
| **sonic** | Sonic — fast lightweight search backend — schema-less indexer query protocol in Rust | Miscellaneous Notable Repos |
| **sops** | sops — secrets encryption tool — encrypt values in YAML JSON ENV files with KMS PGP Age | Security & Recon |
| **sqlx** | sqlx — async Rust SQL toolkit — compile-time checked queries for Postgres MySQL SQLite | Storage & Databases |
| **squadcast** | Similar: openstatus/openstatus — open-source status page and uptime monitoring | Miscellaneous Notable Repos |
| **squid** | Squid — forward proxy caching server — used in enterprise networks for traffic inspection and caching | Networking & Infra |
| **starship** | Starship — minimal blazing fast shell prompt — works in bash zsh fish powershell | Miscellaneous Notable Repos |
| **statping** | Statping — open-source status page for monitoring services — beautiful UI minimal setup | Miscellaneous Notable Repos |
| **step-ca** | step-ca — open-source private CA — issue TLS certs with ACME mTLS OIDC SSHPOP | Miscellaneous Notable Repos |
| **stern** | stern — multi-pod log tailing for Kubernetes — stream logs from multiple pods simultaneously | Dev Tooling & CLI |
| **stirling-pdf** | Stirling-PDF — self-hosted PDF manipulation tool — merge split compress OCR sign all in browser | AI / ML / Agents |
| **strace** | strace — system call tracer — trace every syscall made by a process for debugging | Miscellaneous Notable Repos |
| **subfinder** | subfinder — passive subdomain discovery — aggregates from 40+ sources certificate transparency shodan | Miscellaneous Notable Repos |
| **syft** | syft — SBOM generator — generate software bill of materials from container images filesystems | Dev Tooling & CLI |
| **sysdig** | sysdig — system-level exploration and troubleshooting — capture and analyze OS events | Miscellaneous Notable Repos |
| **tabled** | tabled — pretty table formatting for Rust — derive macros to print structs as tables | Miscellaneous Notable Repos |
| **taiga** | Taiga — agile project management — Scrum Kanban epics sprints open-source alternative to JIRA | Miscellaneous Notable Repos |
| **tandoor** | Tandoor Recipes — open-source recipe manager — nutritional info shopping lists meal planning | Miscellaneous Notable Repos |
| **tantivy** | tantivy — full-text search engine in Rust — Lucene-inspired fast index build and query | Miscellaneous Notable Repos |
| **tauri** | Tauri — build desktop apps with web frontend and Rust backend — lighter than Electron | Miscellaneous Notable Repos |
| **tekton** | Tekton — Kubernetes-native CI/CD — pipelines as CRDs cloud-native build and deploy | Dev Tooling & CLI |
| **telepresence** | Telepresence — develop services locally connected to remote Kubernetes cluster | Dev Tooling & CLI |
| **tempo** | Grafana Tempo — distributed tracing backend — store traces in object storage query via Grafana | Storage & Databases |
| **text-generation-inference** | TGI — HuggingFace text generation inference — production LLM serving with continuous batching | AI / ML / Agents |
| **thiserror** | thiserror — derive macro for custom error types in Rust — ergonomic error enum definition | Miscellaneous Notable Repos |
| **tilt** | Tilt — microservice dev environment — live update containers on code change fast inner loop | Dev Tooling & CLI |
| **tlsx** | tlsx — fast TLS grabber — enumerate TLS certificates find expired weak cipher misconfigs | Miscellaneous Notable Repos |
| **tmux** | tmux — terminal multiplexer — session persistence window splits detach reattach remote workflows | Miscellaneous Notable Repos |
| **tokei** | tokei — fast code statistics — count lines of code comments in a repo by language | Miscellaneous Notable Repos |
| **tokio** | Tokio — async runtime for Rust — foundational event loop behind most Rust network services | Miscellaneous Notable Repos |
| **tonic** | Tonic — gRPC over HTTP/2 in pure Rust — code-gen from proto works with Tokio | Networking & Infra |
| **tooljet** | ToolJet — open-source low-code platform — build internal tools on databases APIs | Self-Hosted Apps & Platforms |
| **tower** | Tower — modular and reusable components for network services in Rust — middleware abstraction | Miscellaneous Notable Repos |
| **tracing** | tracing — application-level tracing for Rust — structured logging spans events for async code | Miscellaneous Notable Repos |
| **transformers** | HuggingFace Transformers — state-of-the-art NLP — BERT GPT T5 and 100000+ models | AI / ML / Agents |
| **tree-sitter** | Tree-sitter — incremental parsing library — used by Zed Neovim Helix for syntax highlighting | Miscellaneous Notable Repos |
| **triton-inference-server** | Triton Inference Server — NVIDIA's model serving — multi-framework GPU CPU inference at scale | AI / ML / Agents |
| **trivy** | Trivy — comprehensive vulnerability scanner — containers filesystems git repos IaC misconfigs | Miscellaneous Notable Repos |
| **trl** | TRL — Transformer Reinforcement Learning — SFT DPO PPO GRPO for LLM alignment | AI / ML / Agents |
| **trufflesecurity** | TruffleHog — find leaked credentials — scans git commit history S3 buckets for secrets | Security & Recon |
| **tryton** | Tryton — modular open-source ERP — double-entry accounting inventory sales server-client | Payments & Fintech |
| **typesense** | Typesense — fast typo-tolerant search engine — Algolia alternative self-hosted instant search | Self-Hosted Apps & Platforms |
| **typst** | Typst — modern markup-based typesetting system — LaTeX alternative with fast compilation | Miscellaneous Notable Repos |
| **unbound** | Unbound — validating recursive caching DNS resolver — DNSSEC resolver used in sovereign DNS stacks | Networking & Infra |
| **uncover** | uncover — quickly discover exposed hosts — Shodan Censys Fofa Hunter all in one CLI | Dev Tooling & CLI |
| **url** | url — URL parsing for Rust per WHATWG spec — percent encoding relative URL resolution | Miscellaneous Notable Repos |
| **urlfinder** | urlfinder — passive URL discovery — find all URLs for a target without active scanning | Miscellaneous Notable Repos |
| **uuid** | uuid — UUID generation and parsing for Rust — v4 v7 sortable UUIDs | Miscellaneous Notable Repos |
| **valgrind** | Valgrind — instrumentation framework — memcheck for memory errors helgrind for thread races | Miscellaneous Notable Repos |
| **varnish** | Varnish Cache — HTTP accelerator — caches HTTP responses at L7 reduces backend load dramatically | Networking & Infra |
| **vault-pki** | Vault PKI — HashiCorp Vault PKI secrets engine — issue short-lived TLS certs programmatically | Security & Recon |
| **vega** | Vega — visualization grammar — declarative JSON spec for interactive charts | Miscellaneous Notable Repos |
| **vegafusion** | VegaFusion — server-side Vega rendering in Rust — scales Vega charts to millions of rows | Miscellaneous Notable Repos |
| **vespa** | Vespa — open-source big data serving engine — real-time ranking and retrieval at scale | Miscellaneous Notable Repos |
| **vikunja** | Vikunja — self-hosted to-do and project management — tasks lists Gantt CalDAV sync | Self-Hosted Apps & Platforms |
| **vis.js** | vis.js — dynamic browser-based visualization — networks timelines graphs 3D plots | Miscellaneous Notable Repos |
| **vitepress** | VitePress — Vite-powered static site generator — Vue 3 fast HMR markdown-first | Dev Tooling & CLI |
| **vllm** | vLLM — fast LLM inference server — PagedAttention continuous batching OpenAI-compatible API | AI / ML / Agents |
| **vpa** | vertical-pod-autoscaler — automatically adjust pod resource requests — VPA for Kubernetes | Dev Tooling & CLI |
| **vultr-cli** | vultr-cli — Vultr cloud CLI — provision and manage VPS bare metal block storage | Dev Tooling & CLI |
| **warp** | warp — composable filter-based Rust web framework — tower-compatible async Hyper-backed | Miscellaneous Notable Repos |
| **wasm-bindgen** | wasm-bindgen — Rust to JavaScript interop — compile Rust to WASM call from JS and vice versa | Miscellaneous Notable Repos |
| **weasyprint** | WeasyPrint — Python HTML to PDF converter — CSS Flexbox Grid support print stylesheet | Miscellaneous Notable Repos |
| **weaviate** | Weaviate — open-source vector database — semantic search multi-modal GraphQL REST APIs | Storage & Databases |
| **wezterm** | WezTerm — GPU-accelerated terminal emulator in Rust — multiplexer built-in SSH integration | Miscellaneous Notable Repos |
| **winnow** | winnow — fork of nom parser combinator — improved ergonomics better error messages | Miscellaneous Notable Repos |
| **woodpecker** | Woodpecker CI — simple yet powerful CI/CD — Gitea/Forgejo compatible self-hosted pipelines | Self-Hosted Apps & Platforms |
| **x25519-dalek** | x25519-dalek — X25519 Diffie-Hellman for Rust — WireGuard-style key exchange in Rust | Miscellaneous Notable Repos |
| **xgboost** | XGBoost — scalable gradient boosting — dominant tabular ML model competition winner | AI / ML / Agents |
| **xh** | xh — friendly HTTPie alternative in Rust — human-readable HTTP client faster startup | Networking & Infra |
| **yazi** | yazi — fast terminal file manager in Rust — async image preview plugin system Lua scripting | Miscellaneous Notable Repos |
| **zabbix** | Zabbix — enterprise open-source monitoring — agents SNMP IPMI JMX auto-discovery | Miscellaneous Notable Repos |
| **zellij** | Zellij — terminal workspace in Rust — built-in layouts floating panes WebAssembly plugins | Miscellaneous Notable Repos |
| **zincsearch** | Zinc Search — lightweight Elasticsearch alternative — single binary Elasticsearch API compat | Miscellaneous Notable Repos |
| **zmap** | ZMap — fast single-packet network scanner — designed for internet-wide scanning research | Miscellaneous Notable Repos |
| **zola** | Zola — fast static site generator in Rust — single binary Tera templates SASS support | Dev Tooling & CLI |
| **zoxide** | zoxide — smarter cd command — frecency-based directory jumping learns your habits | Miscellaneous Notable Repos |

---

# Part 4: Corporate OSS Orgs & Foundation Directories

> Where to look when you want to know what a specific company builds in the open, or which foundation governs a project you depend on.

## Major Companies' OSS Orgs & Flagship Projects

Quick-reference of major companies' OSS orgs and their most-used flagship projects.

## Google

- Org: https://opensource.google/
- GitHub: https://github.com/google
- Top projects:
  - Kubernetes — https://github.com/kubernetes/kubernetes
  - Go — https://github.com/golang/go
  - TensorFlow — https://github.com/tensorflow/tensorflow
  - Angular — https://github.com/angular/angular
  - gRPC — https://github.com/grpc/grpc
  - Bazel — https://github.com/bazelbuild/bazel
  - Protocol Buffers — https://github.com/protocolbuffers/protobuf
  - Flutter — https://github.com/flutter/flutter
  - Chromium — https://chromium.googlesource.com/chromium/src/
  - JAX — https://github.com/google/jax
  - LevelDB — https://github.com/google/leveldb
  - Guava — https://github.com/google/guava

## Meta (Facebook)

- Org: https://opensource.fb.com/
- GitHub: https://github.com/facebook and https://github.com/facebookresearch
- Top projects:
  - React — https://github.com/facebook/react
  - PyTorch — https://github.com/pytorch/pytorch
  - React Native — https://github.com/facebook/react-native
  - RocksDB — https://github.com/facebook/rocksdb
  - GraphQL (spec, via Linux Foundation now) — https://github.com/graphql/graphql-spec
  - Folly (C++ lib) — https://github.com/facebook/folly
  - Llama models — https://github.com/meta-llama
  - Docusaurus — https://github.com/facebook/docusaurus
  - Jest — https://github.com/jestjs/jest
  - HHVM/Hack — https://github.com/facebook/hhvm

## Apple

- Org: https://opensource.apple.com/
- GitHub: https://github.com/apple
- Top projects:
  - Swift — https://github.com/apple/swift
  - Swift Package Manager — https://github.com/swiftlang/swift-package-manager
  - WebKit — https://github.com/WebKit/WebKit
  - CoreML tools — https://github.com/apple/coremltools
  - swift-nio — https://github.com/apple/swift-nio
  - FoundationDB — https://github.com/apple/foundationdb
  - ml-stable-diffusion — https://github.com/apple/ml-stable-diffusion
  - darwin-xnu (kernel sources) — https://github.com/apple-oss-distributions/xnu

## Microsoft

- Org: https://opensource.microsoft.com/
- GitHub: https://github.com/microsoft
- Top projects:
  - VS Code — https://github.com/microsoft/vscode
  - TypeScript — https://github.com/microsoft/TypeScript
  - .NET runtime — https://github.com/dotnet/runtime
  - PowerShell — https://github.com/PowerShell/PowerShell
  - WSL — https://github.com/microsoft/WSL
  - Playwright — https://github.com/microsoft/playwright
  - ONNX Runtime — https://github.com/microsoft/onnxruntime
  - Terminal — https://github.com/microsoft/terminal
  - GitHub (org, incl. Copilot CLI etc.) — https://github.com/github

## Amazon / AWS

- Org: https://aws.amazon.com/opensource/
- GitHub: https://github.com/aws and https://github.com/amzn
- Top projects:
  - Firecracker — https://github.com/firecracker-microvm/firecracker
  - Bottlerocket OS — https://github.com/bottlerocket-os/bottlerocket
  - AWS SDKs — https://github.com/aws/aws-sdk-go, https://github.com/aws/aws-sdk-js-v3
  - Amazon Corretto (OpenJDK) — https://github.com/corretto
  - s2n-tls — https://github.com/aws/s2n-tls
  - Cedar (policy language) — https://github.com/cedar-policy/cedar
  - EKS Distro — https://github.com/aws/eks-distro

## Netflix

- Org: https://netflix.github.io/
- GitHub: https://github.com/Netflix
- Top projects:
  - Hystrix (archived, historically influential) — https://github.com/Netflix/Hystrix
  - Zuul — https://github.com/Netflix/zuul
  - Eureka — https://github.com/Netflix/eureka
  - Conductor (workflow orchestration) — https://github.com/Netflix/conductor
  - Titus (container platform) — https://github.com/Netflix/titus-control-plane
  - Metaflow — https://github.com/Netflix/metaflow

## Uber

- Org: https://uber.github.io/
- GitHub: https://github.com/uber
- Top projects:
  - Jaeger (now CNCF-graduated) — https://github.com/jaegertracing/jaeger
  - Cadence (workflow engine) — https://github.com/uber/cadence
  - Kraken (P2P image distribution) — https://github.com/uber/kraken
  - go-torch / pyroscope-adjacent profiling — https://github.com/uber/go-torch
  - H3 (geospatial indexing) — https://github.com/uber/h3

## Alibaba

- Org: https://github.com/alibaba and https://github.com/aliyun
- Top projects:
  - Nacos (service discovery/config) — https://github.com/alibaba/nacos
  - Sentinel (flow control) — https://github.com/alibaba/Sentinel
  - Dubbo (donated to Apache) — https://github.com/apache/dubbo
  - Seata (distributed transactions) — https://github.com/seata/seata
  - fastjson2 — https://github.com/alibaba/fastjson2

## Tencent

- Org: https://opensource.tencent.com/
- GitHub: https://github.com/Tencent
- Top projects:
  - TARS — https://github.com/TarsCloud/Tars
  - Tencent Kona JDK — https://github.com/Tencent/TencentKona-8

## ByteDance

- GitHub: https://github.com/bytedance
- Top projects:
  - Hertz (Go HTTP framework, high-perf) — https://github.com/cloudwego/hertz
  - Kitex (Go RPC framework) — https://github.com/cloudwego/kitex
  - CloudWeGo (umbrella org) — https://github.com/cloudwego

## Databricks

- Top projects:
  - Apache Spark (donated, now ASF) — https://github.com/apache/spark
  - Delta Lake — https://github.com/delta-io/delta
  - MLflow — https://github.com/mlflow/mlflow

## Notable single-company standalone projects (not org-wide but heavily used)

- Redis (Redis Ltd / Linux Foundation as of 2025) — https://github.com/redis/redis
- HashiCorp (Terraform, Vault, Consul — now BSL-licensed, forks under OpenTofu/OpenBao) — https://github.com/hashicorp
- Docker/Moby — https://github.com/moby/moby
- Elastic (Elasticsearch, Kibana) — https://github.com/elastic

---

## Foundations, Trackers & Discovery Sites

> Foundations that host/govern OSS projects, plus sites that track who (which company) contributes to what, and curated awesome-lists for further discovery.

Foundations that host/govern OSS projects, plus sites/tools that track who (which company) contributes to what, and curated awesome-lists for discovery.

## Cloud Native Computing Foundation (CNCF)

- Landscape (full interactive map, 200+ projects): https://landscape.cncf.io/
- Graduated & Incubating list: https://www.cncf.io/projects/
- Project metrics: https://www.cncf.io/project-metrics/
- Sandbox projects: https://www.cncf.io/sandbox-projects/

**Top Graduated projects:**
- Kubernetes — https://kubernetes.io/ | https://github.com/kubernetes/kubernetes
- Prometheus — https://prometheus.io/ | https://github.com/prometheus/prometheus
- Envoy — https://www.envoyproxy.io/ | https://github.com/envoyproxy/envoy
- Helm — https://helm.sh/ | https://github.com/helm/helm
- containerd — https://containerd.io/ | https://github.com/containerd/containerd
- CoreDNS — https://coredns.io/ | https://github.com/coredns/coredns
- Argo — https://argoproj.github.io/ | https://github.com/argoproj
- Cilium (eBPF networking) — https://cilium.io/ | https://github.com/cilium/cilium
- etcd — https://etcd.io/ | https://github.com/etcd-io/etcd
- Jaeger — https://www.jaegertracing.io/ | https://github.com/jaegertracing/jaeger
- Fluentd — https://www.fluentd.org/ | https://github.com/fluent/fluentd
- Vitess (sharded MySQL) — https://vitess.io/ | https://github.com/vitessio/vitess
- gRPC — https://grpc.io/ | https://github.com/grpc/grpc
- OpenTelemetry — https://opentelemetry.io/ | https://github.com/open-telemetry
- cert-manager — https://cert-manager.io/ | https://github.com/cert-manager/cert-manager
- Dragonfly (P2P image/file distribution, graduated Jan 2026) — https://d7y.io/ | https://github.com/dragonflyoss/Dragonfly2

**Notable Incubating:**
- KEDA (event-driven autoscaling) — https://keda.sh/
- NATS (messaging) — https://nats.io/
- gRPC-Gateway, CockroachDB-adjacent tooling, Karmada (multi-cluster)

## Apache Software Foundation (ASF)

- Full projects directory: https://projects.apache.org/projects.html
- Foundation homepage: https://apache.org/
- Top-Level Projects news: https://news.apache.org/foundation/

**Flagship projects:**
- Apache Kafka — https://kafka.apache.org/ | https://github.com/apache/kafka
- Apache Spark — https://spark.apache.org/ | https://github.com/apache/spark
- Apache Airflow — https://airflow.apache.org/ | https://github.com/apache/airflow
- Apache Cassandra — https://cassandra.apache.org/
- Apache HTTP Server — https://httpd.apache.org/
- Apache Flink — https://flink.apache.org/
- Apache Iceberg — https://iceberg.apache.org/
- Apache Pulsar — https://pulsar.apache.org/
- Apache Camel — https://camel.apache.org/
- Apache Dubbo (RPC, ex-Alibaba) — https://dubbo.apache.org/
- Apache Iggy (Rust streaming, TLP as of Aug 2026) — https://iggy.apache.org/
- Apache Fluss (streaming lakehouse storage, TLP Aug 2026) — https://fluss.apache.org/
- Apache Polaris (Iceberg REST catalog) — https://polaris.apache.org/

## Linux Foundation (umbrella — hosts CNCF, PyTorch Foundation, OpenSSF, etc.)

- Projects directory: https://www.linuxfoundation.org/projects
- Top hosted projects/sub-foundations:
  - Linux kernel — https://www.kernel.org/
  - PyTorch Foundation — https://pytorch.org/foundation
  - OpenSSF (security) — https://openssf.org/
  - Hyperledger (blockchain) — https://www.hyperledger.org/
  - Automotive Grade Linux — https://www.automotivelinux.org/
  - OpenTofu (Terraform fork) — https://opentofu.org/
  - LF Edge — https://www.lfedge.org/
  - Zephyr RTOS — https://zephyrproject.org/

## Eclipse Foundation

- Projects directory: https://projects.eclipse.org/
- Top projects:
  - Eclipse IDE — https://www.eclipse.org/ide/
  - Eclipse Jakarta EE — https://jakarta.ee/
  - Eclipse Mosquitto (MQTT broker, relevant to IoT) — https://mosquitto.org/
  - Eclipse Che — https://www.eclipse.org/che/
  - Eclipse Theia — https://theia-ide.org/

## OpenJS Foundation (JavaScript ecosystem)

- Projects directory: https://openjsf.org/projects/
- Top projects:
  - Node.js — https://nodejs.org/
  - Express — https://expressjs.com/
  - webpack — https://webpack.js.org/
  - jQuery — https://jquery.com/
  - Electron — https://www.electronjs.org/

## Python Software Foundation (PSF)

- https://www.python.org/psf/
- CPython — https://github.com/python/cpython
- pip / packaging — https://github.com/pypa

## Rust Foundation

- https://rustfoundation.org/
- Rust language — https://github.com/rust-lang/rust
- Cargo — https://github.com/rust-lang/cargo

## OpenInfra Foundation (formerly OpenStack Foundation)

- https://openinfra.org/
- OpenStack — https://www.openstack.org/
- Kata Containers — https://katacontainers.io/
- Zuul CI — https://zuul-ci.org/

## FINOS (Fintech Open Source Foundation) — finance-native OSS

- Homepage: https://www.finos.org/
- Project directory: https://www.finos.org/projects
- Landscape (interactive, like CNCF's): https://landscape.finos.org/
- Top projects:
  - Legend (data platform, Goldman Sachs origin) — https://github.com/finos/legend
  - Morphir (business logic as data) — https://github.com/finos/morphir
  - Waltz (enterprise architecture) — https://github.com/finos/waltz
  - Perspective (streaming data viz, J.P. Morgan origin) — https://github.com/finos/perspective
  - Common Cloud Controls (CCC) — https://github.com/finos/common-cloud-controls

## Other finance / capital-markets-adjacent OSS bodies

- Symphony Software Foundation (merged into FINOS) — historical, now under FINOS above
- ISDA CDM (Common Domain Model, financial contracts) — https://www.isda.org/2019/07/09/isda-common-domain-model/
- Hyperledger (LF project, heavily used in fintech/blockchain) — https://www.hyperledger.org/

## OpenSSF (Open Source Security Foundation) — LF-hosted, cross-cutting

- https://openssf.org/
- Sigstore (signing/provenance) — https://www.sigstore.dev/
- Scorecard (project security scoring) — https://github.com/ossf/scorecard

## GraphQL Foundation

- https://graphql.org/foundation/

## Cloud Native Buildpacks / CDF-adjacent

- (Now under CNCF) https://buildpacks.io/

## Academy Software Foundation (media/VFX)

- https://www.aswf.io/

## LF AI & Data Foundation

- https://lfaidata.foundation/projects/
- Top projects: Milvus (vector DB), ONNX (also cross-listed w/ Microsoft), Horovod

## Presto Foundation

- https://prestodb.io/ (distributed SQL query engine, LF-hosted)

## Continuous Delivery Foundation (CDF) — merged into CNCF in 2023

- Projects (Jenkins, Spinnaker, Tekton) now tracked under CNCF landscape above

## Confidential Computing Consortium

- https://confidentialcomputing.io/

## Data & AI adjacent

- PyTorch Foundation (LF-hosted) — https://pytorch.org/foundation
- LF Edge — https://www.lfedge.org/projects/

## AOSSIE / general discovery aggregators

- Awesome Foundations meta-list — search GitHub topic "awesome-lists" for curated foundation trackers
- Open Source Initiative (license authority, not a project host) — https://opensource.org/
- Software Freedom Conservancy (fiscal host for many indie projects incl. Git, QEMU, Selenium) — https://sfconservancy.org/members/current/
- NumFOCUS (scientific Python ecosystem: NumPy, pandas, Jupyter, matplotlib) — https://numfocus.org/sponsored-projects

---

**Tip:** For a live, filterable view across ~200 CNCF projects by category (networking, storage, orchestration, observability), use the interactive landscape rather than a static list: https://landscape.cncf.io/card-mode?project=graduated

---



## OSS Contribution Trackers & Awesome-Lists

## What you're describing: company-level OSS contribution tracking

The site you're thinking of is almost certainly:

### OSCI — Open Source Contributor Index (by EPAM)
- Site: https://opensource-contributor-index.org/
- GitHub (it's itself open source): https://github.com/epam/OSCI
- What it does: ranks **commercial companies** by GitHub activity (active contributors with 10+ commits, and total community with 1+ commit). Identifies company by the committer's email domain. Lets you search a company and see their contribution volume/trend over time, and search a domain/org to see who's contributing.
- Good for: "how much does Company X actually contribute to open source" comparisons.

### Related / similar tools

- **CHAOSS (Community Health Analytics in Open Source Software)** — Linux Foundation project defining metrics + building tools (GrimoireLab, Augur) to measure project and contributor health, including per-organization breakdowns.
  - https://chaoss.community/
  - GrimoireLab: https://github.com/chaoss/grimoirelab
  - Augur: https://github.com/chaoss/augur
- **Statista's "Active GitHub contributors by employer"** chart series — periodic snapshots (GAFAM-style comparisons), not a live tool but often cited.
  - https://www.statista.com/chart/25795/active-github-contributors-by-employer/
- **Bitergia** — commercial analytics company built on GrimoireLab; sells dashboards to companies/foundations for exactly this (who's contributing what, to which project, from which org).
  - https://bitergia.com/
- **LFX Insights** (Linux Foundation's own tooling) — used by LF-hosted projects (CNCF etc.) to show contributor/org breakdowns per project (e.g., "who funds Kubernetes development").
  - https://insights.lfx.linuxfoundation.org/
  - Example: search any CNCF project here to see company-by-company commit/review share.
- **DevStats** (CNCF's own per-project stats tool, predates LFX Insights but still live for some projects) — https://k8s.devstats.cncf.io/ (Kubernetes example; swap subdomain per project)
- **OpenStack's Stackalytics** (historical, OpenStack-specific) — tracked exactly this for OpenStack: which company contributed what.
  - https://www.stackalytics.io/

### Checking a single person's or your own cross-repo OSS contributions
- **opensource-contributions-tracker** (self-hosted, generates a markdown report from GitHub API) — https://github.com/NihalJain/opensource-contributions-tracker
- GitHub's own contribution graph only shows activity, not org attribution — the tools above fill that gap.

---

## Awesome-lists (curated OSS project directories)

These are community-maintained "awesome-X" GitHub repos — the de facto standard format for curated OSS lists:

- **awesome** (meta-list of all awesome-lists) — https://github.com/sindresorhus/awesome
- **awesome-selfhosted** (huge — self-hosted alternatives to SaaS) — https://github.com/awesome-selfhosted/awesome-selfhosted
- **awesome-sysadmin** — https://github.com/awesome-foss/awesome-sysadmin
- **free-for-dev** (free tiers of dev tools/infra, many OSS) — https://github.com/ripienaar/free-for-dev
- **awesome-go** — https://github.com/avelino/awesome-go
- **awesome-rust** — https://github.com/rust-unofficial/awesome-rust
- **awesome-zig** — https://github.com/C-BJ/awesome-zig
- **awesome-cloud-native** — https://github.com/rootsongjc/awesome-cloud-native
- **awesome-kubernetes** — https://github.com/ramitsurana/awesome-kubernetes
- **awesome-sre** — https://github.com/dastergon/awesome-sre
- **awesome-distributed-systems** — https://github.com/theanalyst/awesome-distributed-systems
- **awesome-open-source-organizations** (foundations themselves, curated) — search GitHub, several maintained lists exist under this name/topic
- **CNCF Landscape** (technically the "awesome list" of cloud native, but interactive) — https://landscape.cncf.io/
- **awesome-osint / awesome-pentest** — https://github.com/jivoi/awesome-osint and https://github.com/enaqx/awesome-pentest

---

