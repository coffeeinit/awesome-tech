
# Awesome Systems Engineering Checklist

A practical, broad checklist for learning systems engineering from digital logic and hardware to operating systems, networking, distributed systems, infrastructure, security, reliability, and engineering practice.

> **Scope:** This is a learning map, not a claim that every engineer must master every topic. Choose the pillars that match your role and goals.

## What is included

- **61 pillars** across hardware, software, infrastructure, distributed systems, security, and engineering practice.
- A topic-level self-evaluation using **G / Y / R**: Green = can build, debug, and explain it; Yellow = understand the term but need references; Red = not yet understood.
- A scorecard to find knowledge gaps and select the next learning target.
- A reusable AI coaching prompt to help turn the checklist into a personal roadmap.

## How to use this checklist

1. Choose a target role or project. Do not try to study all pillars at once.
2. Mark each topic: `G` (can build/debug/teach), `Y` (need documentation), or `R` (new topic).
3. Count each status in the scorecard at the end.
4. Start with the lowest-scoring core pillar. Convert knowledge into evidence by building, debugging, measuring, or documenting a real system.
5. Revisit the scorecard every four weeks.

## Contribution rules

- Keep topics specific and useful for practice.
- Prefer primary documentation, standards, papers, and maintained project docs when adding references.
- Avoid duplicate topics. Link overlapping topics when this is clearer than repeating them.
- Do not mark a tool or project as recommended only because it is popular. Explain the use case and trade-offs.
- If a topic or reference may be outdated, mark it for review rather than presenting it as current fact.
- Small corrections and focused pull requests are welcome.

## Important note

The checklist is intentionally broad. It is not a certification, a hiring rubric, or a guarantee of expertise. Use practical projects and observable results to confirm progress.

---

# Master Checklist

The following checklist is included as the project's core reference. Its topic coverage and scorecard are retained from the source document.

# Systems Engineering: Master Self-Evaluation Checklist

61 pillars, 1180 topics. Silicon up to global scale, plus practice and theory.

## Quick start: use this file with an AI

1. Copy this whole file into a chat with any AI (Claude, ChatGPT, Gemini, a local model).
2. Paste the prompt below **above** it, then send.
3. Answer the AI's questions, grade the tables (G/Y/R), and send your counts back.

\`\`\`text
You are a senior systems engineer and learning coach. Below is a master checklist of systems engineering topics (61 pillars, ~1180 topics) that is common to all systems engineers. Use it as the shared base map.

STEP 1: INTAKE. Before anything else, ask me these questions in ONE message and wait:
- Which field do I want to specialize in? (e.g. backend/distributed, OS/kernel, embedded/firmware, networking, storage/databases, security, SRE/infra, HPC/GPU, compilers, space/safety-critical, or "not sure")
- What is my goal? (job role, startup, research, certification, personal project) and the timeline.
- Current level and background (years of experience, languages, what I already build).
- Hours per week I can study.
- What I need most: depth in fewer areas, or breadth across many?
- Anything I must avoid or already know.

STEP 2: EVALUATE. After my answers, tell me which pillars to grade first (max 5) and wait for my G/Y/R counts. G = can build, debug and teach it. Y = know the term, need docs. R = blank.

STEP 3: PERSONALIZE. Using my field, goal and grades, produce:
1. Pillar triage: Core (must master), Supporting (needed alongside), Skip-for-now (not needed for my field). One line of reasoning each.
2. Overlap groups: pillars that are needed alike or overlap, so I can study them together instead of separately (e.g. cache hierarchy + memory management + performance engineering).
3. Deep expansion: for my Core pillars only, expand the topics into three tiers (Core, Advanced, Specialist) with new topics the base list lacks.
4. One proof task per Core pillar (something I build or debug that proves G, not self-judged).
5. A week-by-week roadmap that fits my hours, ordered by dependency, starting from my lowest-G Core pillar. Each week: topics, one build task, one reading source (kernel docs, RFC, paper, book chapter).
6. Re-grade checkpoints every 4 weeks.

RULES: Be concise and specific. No filler. Do not expand pillars outside my field unless I ask. Where you are unsure a fact is current, say so. End every reply with one concrete next step.

Start with STEP 1 now.
\`\`\`

---

## How to use

1. Mark one box per row: **G** = can build, debug and teach it now. **Y** = know the term, need docs to apply. **R** = blank spot. Replace `☐` with `☒`.
2. Count G/Y/R per pillar and fill the [scorecard](#scorecard).
3. Any pillar under 50% G is a gap. Lowest-G pillar is the first study target.
4. Convert Y to G by building something; convert R to Y by reading one primary source.

## Contents

- [P1. Digital Logic & Silicon Fundamentals](#p1-digital-logic--silicon-fundamentals)
- [P2. CPU Microarchitecture](#p2-cpu-microarchitecture)
- [P3. Cache & Memory Hierarchy](#p3-cache--memory-hierarchy)
- [P4. Main Memory, Buses & Interconnects](#p4-main-memory-buses--interconnects)
- [P5. Accelerators: GPU, TPU, FPGA, ASIC](#p5-accelerators-gpu-tpu-fpga-asic)
- [P6. Firmware, Boot & BIOS/UEFI](#p6-firmware-boot--biosuefi)
- [P7. Embedded Systems & Microcontrollers](#p7-embedded-systems--microcontrollers)
- [P8. Hardware Buses & Peripheral Interfaces](#p8-hardware-buses--peripheral-interfaces)
- [P9. OS: Processes, Threads & Scheduling](#p9-os-processes-threads--scheduling)
- [P10. OS: Memory Management](#p10-os-memory-management)
- [P11. OS: Concurrency & Synchronization](#p11-os-concurrency--synchronization)
- [P12. OS: I/O Subsystem & Virtual File System](#p12-os-io-subsystem--virtual-file-system)
- [P13. OS: Interrupts, Drivers & Kernel Development](#p13-os-interrupts-drivers--kernel-development)
- [P14. Operating System Families & Platform Differences](#p14-operating-system-families--platform-differences)
- [P15. Storage Hardware](#p15-storage-hardware)
- [P16. File Systems & Volume Management](#p16-file-systems--volume-management)
- [P17. Networking: Linux Stack & Packet Path](#p17-networking-linux-stack--packet-path)
- [P18. Networking: Transport Layer](#p18-networking-transport-layer)
- [P19. Networking: L2/L3, Routing & Switching](#p19-networking-l2l3-routing--switching)
- [P20. Networking: Application Protocols, DNS & TLS](#p20-networking-application-protocols-dns--tls)
- [P21. Networking: High-Performance, Datacenter & Edge](#p21-networking-high-performance-datacenter--edge)
- [P22. Wireless, IoT & Telecom Protocols](#p22-wireless-iot--telecom-protocols)
- [P23. Compilers & Program Translation](#p23-compilers--program-translation)
- [P24. Linking, Loading & ABI](#p24-linking-loading--abi)
- [P25. Programming Languages & Runtimes](#p25-programming-languages--runtimes)
- [P26. Build Systems, Packaging & Toolchains](#p26-build-systems-packaging--toolchains)
- [P27. Data Structures](#p27-data-structures)
- [P28. Algorithms](#p28-algorithms)
- [P29. Performance Math & Queueing Theory](#p29-performance-math--queueing-theory)
- [P30. Databases: Single-Node Engines](#p30-databases-single-node-engines)
- [P31. Distributed Databases, Messaging & Caching](#p31-distributed-databases-messaging--caching)
- [P32. Distributed Systems Theory](#p32-distributed-systems-theory)
- [P33. Distributed Systems Patterns & Resilience](#p33-distributed-systems-patterns--resilience)
- [P34. Virtualization & Hypervisors](#p34-virtualization--hypervisors)
- [P35. Containers & Runtimes](#p35-containers--runtimes)
- [P36. Kubernetes & Orchestration](#p36-kubernetes--orchestration)
- [P37. Cloud Platforms & Infrastructure as Code](#p37-cloud-platforms--infrastructure-as-code)
- [P38. Observability & Monitoring](#p38-observability--monitoring)
- [P39. Debugging, Tracing & Diagnostics](#p39-debugging-tracing--diagnostics)
- [P40. Performance Engineering](#p40-performance-engineering)
- [P41. Reliability, SRE & Operations](#p41-reliability-sre--operations)
- [P42. CI/CD & Release Engineering](#p42-cicd--release-engineering)
- [P43. Security: OS, Application & Memory Safety](#p43-security-os-application--memory-safety)
- [P44. Cryptography, PKI & Identity](#p44-cryptography-pki--identity)
- [P45. Network & Infrastructure Security](#p45-network--infrastructure-security)
- [P46. Testing, Correctness & Formal Methods](#p46-testing-correctness--formal-methods)
- [P47. Architecture, API & Protocol Design](#p47-architecture-api--protocol-design)
- [P48. Software Engineering Fundamentals & Design](#p48-software-engineering-fundamentals--design)
- [P49. Backend & Web Application Development](#p49-backend--web-application-development)
- [P50. Frontend & Browser Internals](#p50-frontend--browser-internals)
- [P51. Mobile & Desktop Applications](#p51-mobile--desktop-applications)
- [P52. Graphics, Audio, Video & Game Systems](#p52-graphics-audio-video--game-systems)
- [P53. Application Security & Privacy Engineering](#p53-application-security--privacy-engineering)
- [P54. Domain Application Systems & Product Patterns](#p54-domain-application-systems--product-patterns)
- [P55. Software Process, Product & Team Engineering](#p55-software-process-product--team-engineering)
- [P56. Data Engineering, ML Systems & AI Infrastructure](#p56-data-engineering-ml-systems--ai-infrastructure)
- [P57. Specialized & Safety-Critical Domains](#p57-specialized--safety-critical-domains)
- [P58. Mathematics & CS Theory Foundations](#p58-mathematics--cs-theory-foundations)
- [P59. Linux Administration, Shell & Daily Tooling](#p59-linux-administration-shell--daily-tooling)
- [P60. Time, Text, Encoding & Data Formats](#p60-time-text-encoding--data-formats)
- [P61. Engineering Practice, Communication & Career](#p61-engineering-practice-communication--career)
- [Scorecard](#scorecard)

---

## P1. Digital Logic & Silicon Fundamentals

### 1.1 Logic & circuits

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 1.1.1 | Boolean algebra | ☐ | ☐ | ☐ |
| 1.1.2 | Combinational vs sequential logic | ☐ | ☐ | ☐ |
| 1.1.3 | Gates, CMOS, transistor basics | ☐ | ☐ | ☐ |
| 1.1.4 | Flip-flops, latches, registers | ☐ | ☐ | ☐ |
| 1.1.5 | Clock, setup/hold time, clock domains, metastability | ☐ | ☐ | ☐ |
| 1.1.6 | Clock domain crossing, synchronizers | ☐ | ☐ | ☐ |
| 1.1.7 | Finite state machines | ☐ | ☐ | ☐ |
| 1.1.8 | ALU, adders (ripple, carry-lookahead), multipliers | ☐ | ☐ | ☐ |
| 1.1.9 | Floating point (IEEE 754), denormals, rounding modes | ☐ | ☐ | ☐ |
| 1.1.10 | Fixed point, two's complement, endianness | ☐ | ☐ | ☐ |

### 1.2 Silicon & manufacturing

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 1.2.1 | Process nodes, FinFET, GAA | ☐ | ☐ | ☐ |
| 1.2.2 | Die, wafer, yield, binning | ☐ | ☐ | ☐ |
| 1.2.3 | Chiplets, 2.5D/3D packaging, interposers | ☐ | ☐ | ☐ |
| 1.2.4 | Power: dynamic vs leakage, DVFS, power gating | ☐ | ☐ | ☐ |
| 1.2.5 | Thermal design, TDP, throttling | ☐ | ☐ | ☐ |
| 1.2.6 | HDL basics: Verilog/VHDL/SystemVerilog | ☐ | ☐ | ☐ |
| 1.2.7 | FPGA synthesis, place & route, timing closure | ☐ | ☐ | ☐ |
| 1.2.8 | Simulation, verification, formal equivalence | ☐ | ☐ | ☐ |

## P2. CPU Microarchitecture

### 2.1 ISA

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 2.1.1 | x86-64 vs ARM64 vs RISC-V | ☐ | ☐ | ☐ |
| 2.1.2 | CISC vs RISC, micro-ops, microcode | ☐ | ☐ | ☐ |
| 2.1.3 | Privilege levels, rings, exception levels | ☐ | ☐ | ☐ |
| 2.1.4 | Addressing modes, calling conventions at ISA level | ☐ | ☐ | ☐ |
| 2.1.5 | Vector ISAs: SSE, AVX2, AVX-512, NEON, SVE, RVV | ☐ | ☐ | ☐ |
| 2.1.6 | Atomic and ordering instructions (LOCK, LL/SC, LSE) | ☐ | ☐ | ☐ |
| 2.1.7 | Crypto/CRC/AES-NI instructions | ☐ | ☐ | ☐ |

### 2.2 Pipeline & execution

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 2.2.1 | Pipeline stages | ☐ | ☐ | ☐ |
| 2.2.2 | Structural, data (RAW/WAR/WAW), control hazards | ☐ | ☐ | ☐ |
| 2.2.3 | Forwarding/bypassing, stalls, bubbles | ☐ | ☐ | ☐ |
| 2.2.4 | Superscalar, VLIW, EPIC | ☐ | ☐ | ☐ |
| 2.2.5 | Out-of-order: reservation stations, ROB, register renaming, Tomasulo | ☐ | ☐ | ☐ |
| 2.2.6 | Load/store queues, store-to-load forwarding, memory disambiguation | ☐ | ☐ | ☐ |
| 2.2.7 | Micro-op cache, decoders, loop stream detector | ☐ | ☐ | ☐ |
| 2.2.8 | Execution ports, throughput vs latency per instruction | ☐ | ☐ | ☐ |
| 2.2.9 | Branch prediction: BTB, RSB, TAGE, perceptron, indirect predictors | ☐ | ☐ | ☐ |
| 2.2.10 | Speculative execution | ☐ | ☐ | ☐ |
| 2.2.11 | SMT / Hyper-Threading | ☐ | ☐ | ☐ |
| 2.2.12 | Heterogeneous cores: P/E, big.LITTLE, scheduling implications | ☐ | ☐ | ☐ |

### 2.3 Vulnerabilities & mitigations

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 2.3.1 | Spectre v1/v2, Meltdown | ☐ | ☐ | ☐ |
| 2.3.2 | MDS, TAA, L1TF, Retbleed, Downfall | ☐ | ☐ | ☐ |
| 2.3.3 | Mitigations: retpoline, IBRS/STIBP, KPTI, microcode | ☐ | ☐ | ☐ |
| 2.3.4 | Side channels: cache timing, Prime+Probe, Flush+Reload | ☐ | ☐ | ☐ |
| 2.3.5 | Rowhammer, cold boot | ☐ | ☐ | ☐ |
| 2.3.6 | Performance cost of mitigations | ☐ | ☐ | ☐ |

### 2.4 Performance counters

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 2.4.1 | PMU / PMC events | ☐ | ☐ | ☐ |
| 2.4.2 | IPC, CPI, top-down microarchitecture analysis | ☐ | ☐ | ☐ |
| 2.4.3 | Frontend vs backend bound, bad speculation | ☐ | ☐ | ☐ |
| 2.4.4 | Intel VTune, perf, AMD uProf basics | ☐ | ☐ | ☐ |

## P3. Cache & Memory Hierarchy

### 3.1 Cache design

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 3.1.1 | L1i/L1d/L2/L3 roles and sizes | ☐ | ☐ | ☐ |
| 3.1.2 | Inclusive, exclusive, non-inclusive | ☐ | ☐ | ☐ |
| 3.1.3 | Direct-mapped, fully associative, set-associative | ☐ | ☐ | ☐ |
| 3.1.4 | Replacement: LRU, pLRU, LFU, FIFO, random, RRIP | ☐ | ☐ | ☐ |
| 3.1.5 | Write-through vs write-back; write-allocate vs no-write-allocate | ☐ | ☐ | ☐ |
| 3.1.6 | Cache line (64B), sectors | ☐ | ☐ | ☐ |
| 3.1.7 | Tag/index/offset breakdown | ☐ | ☐ | ☐ |
| 3.1.8 | Victim cache, stacked cache (3D V-Cache) | ☐ | ☐ | ☐ |
| 3.1.9 | Hardware prefetchers, software prefetch | ☐ | ☐ | ☐ |
| 3.1.10 | Non-temporal stores, cache bypass, CLFLUSH/CLWB | ☐ | ☐ | ☐ |

### 3.2 Coherency & ordering

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 3.2.1 | MESI, MOESI, MESIF | ☐ | ☐ | ☐ |
| 3.2.2 | Snooping vs directory protocols | ☐ | ☐ | ☐ |
| 3.2.3 | False sharing, true sharing, cache-line bouncing | ☐ | ☐ | ☐ |
| 3.2.4 | Padding, alignment, cache-line-aware layout | ☐ | ☐ | ☐ |
| 3.2.5 | Memory consistency: sequential, TSO, weak, release/acquire | ☐ | ☐ | ☐ |
| 3.2.6 | Fences: MFENCE, LFENCE, SFENCE, DMB, DSB | ☐ | ☐ | ☐ |
| 3.2.7 | Store buffers, write combining | ☐ | ☐ | ☐ |
| 3.2.8 | C11/C++/Rust atomics orderings | ☐ | ☐ | ☐ |

### 3.3 Locality & layout

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 3.3.1 | Spatial and temporal locality | ☐ | ☐ | ☐ |
| 3.3.2 | Working set, cache miss types (compulsory, capacity, conflict) | ☐ | ☐ | ☐ |
| 3.3.3 | Data-oriented design, SoA vs AoS | ☐ | ☐ | ☐ |
| 3.3.4 | Cache-blocking / tiling | ☐ | ☐ | ☐ |
| 3.3.5 | Cache-oblivious algorithms | ☐ | ☐ | ☐ |
| 3.3.6 | Pointer chasing cost, linked-list pitfalls | ☐ | ☐ | ☐ |
| 3.3.7 | TLB reach and huge-page effects | ☐ | ☐ | ☐ |
| 3.3.8 | NUMA locality, first-touch policy | ☐ | ☐ | ☐ |

## P4. Main Memory, Buses & Interconnects

### 4.1 DRAM

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 4.1.1 | DRAM cell, refresh, rows/banks/ranks/channels | ☐ | ☐ | ☐ |
| 4.1.2 | DDR4 vs DDR5, LPDDR, GDDR, HBM | ☐ | ☐ | ☐ |
| 4.1.3 | ECC, chipkill, scrubbing | ☐ | ☐ | ☐ |
| 4.1.4 | Registered/unbuffered/LR DIMMs | ☐ | ☐ | ☐ |
| 4.1.5 | Memory timings (CL, tRCD, tRP), bandwidth vs latency | ☐ | ☐ | ☐ |
| 4.1.6 | Rowhammer and TRR | ☐ | ☐ | ☐ |
| 4.1.7 | Persistent memory, Optane history, CXL.mem | ☐ | ☐ | ☐ |
| 4.1.8 | Memory training at boot | ☐ | ☐ | ☐ |

### 4.2 Interconnects

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 4.2.1 | UMA vs NUMA, NUMA distance, SNC/NPS modes | ☐ | ☐ | ☐ |
| 4.2.2 | Intel UPI, AMD Infinity Fabric, ARM CMN | ☐ | ☐ | ☐ |
| 4.2.3 | CXL types 1/2/3, memory pooling | ☐ | ☐ | ☐ |
| 4.2.4 | Ring vs mesh on-die interconnect | ☐ | ☐ | ☐ |
| 4.2.5 | PCIe generations, lanes, bifurcation, switches | ☐ | ☐ | ☐ |
| 4.2.6 | PCIe config space, BAR, MSI/MSI-X, ACS, ATS | ☐ | ☐ | ☐ |
| 4.2.7 | Thunderbolt/USB4 | ☐ | ☐ | ☐ |
| 4.2.8 | NVLink, NVSwitch, Infiniband topology | ☐ | ☐ | ☐ |

### 4.3 DMA & IOMMU

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 4.3.1 | DMA, scatter-gather, bus mastering | ☐ | ☐ | ☐ |
| 4.3.2 | IOMMU, VT-d, AMD-Vi, DMA remapping | ☐ | ☐ | ☐ |
| 4.3.3 | Bounce buffers, DMA-coherent vs streaming mappings | ☐ | ☐ | ☐ |
| 4.3.4 | P2P DMA, GPUDirect, RDMA | ☐ | ☐ | ☐ |
| 4.3.5 | Cache coherence with DMA devices | ☐ | ☐ | ☐ |
| 4.3.6 | Interrupt remapping | ☐ | ☐ | ☐ |

## P5. Accelerators: GPU, TPU, FPGA, ASIC

### 5.1 GPU

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 5.1.1 | SIMT, warps/wavefronts, SMs, occupancy | ☐ | ☐ | ☐ |
| 5.1.2 | GPU memory hierarchy: global, shared, registers, L2 | ☐ | ☐ | ☐ |
| 5.1.3 | CUDA, ROCm, OpenCL, Vulkan compute, SYCL | ☐ | ☐ | ☐ |
| 5.1.4 | Kernel launch overhead, streams, async copies | ☐ | ☐ | ☐ |
| 5.1.5 | Warp divergence, memory coalescing, bank conflicts | ☐ | ☐ | ☐ |
| 5.1.6 | Tensor cores, mixed precision | ☐ | ☐ | ☐ |
| 5.1.7 | Unified memory, pinned memory, PCIe transfer cost | ☐ | ☐ | ☐ |
| 5.1.8 | NCCL, collective communication | ☐ | ☐ | ☐ |
| 5.1.9 | GPU virtualization: MIG, SR-IOV, vGPU | ☐ | ☐ | ☐ |

### 5.2 Other accelerators

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 5.2.1 | TPU systolic arrays | ☐ | ☐ | ☐ |
| 5.2.2 | NPUs, DSPs, neuromorphic chips | ☐ | ☐ | ☐ |
| 5.2.3 | FPGA: LUTs, DSP slices, BRAM, HLS | ☐ | ☐ | ☐ |
| 5.2.4 | SmartNIC, DPU, IPU (BlueField, Pensando) | ☐ | ☐ | ☐ |
| 5.2.5 | Intel QuickAssist, compression/crypto offload | ☐ | ☐ | ☐ |
| 5.2.6 | ASIC design flow basics | ☐ | ☐ | ☐ |
| 5.2.7 | Roofline model for accelerators | ☐ | ☐ | ☐ |

## P6. Firmware, Boot & BIOS/UEFI

### 6.1 Boot chain

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 6.1.1 | Reset vector, boot ROM | ☐ | ☐ | ☐ |
| 6.1.2 | First-stage and second-stage bootloaders | ☐ | ☐ | ☐ |
| 6.1.3 | BIOS vs UEFI, PEI/DXE/BDS phases | ☐ | ☐ | ☐ |
| 6.1.4 | coreboot, U-Boot, GRUB, systemd-boot, EDK II | ☐ | ☐ | ☐ |
| 6.1.5 | Device tree, ACPI tables, SMBIOS | ☐ | ☐ | ☐ |
| 6.1.6 | Kernel handoff, initramfs, early userspace | ☐ | ☐ | ☐ |
| 6.1.7 | init systems: systemd, OpenRC, runit | ☐ | ☐ | ☐ |
| 6.1.8 | PXE, iPXE, netboot, HTTP boot | ☐ | ☐ | ☐ |

### 6.2 Platform security & management

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 6.2.1 | Secure Boot, key hierarchy, db/dbx, shim | ☐ | ☐ | ☐ |
| 6.2.2 | Measured boot, TPM PCRs, remote attestation | ☐ | ☐ | ☐ |
| 6.2.3 | Intel ME, AMD PSP, SMM | ☐ | ☐ | ☐ |
| 6.2.4 | BMC, IPMI, Redfish, OpenBMC | ☐ | ☐ | ☐ |
| 6.2.5 | Firmware updates, fwupd, capsule updates | ☐ | ☐ | ☐ |
| 6.2.6 | Rollback protection, anti-rollback counters | ☐ | ☐ | ☐ |
| 6.2.7 | Trusted Firmware-A, OP-TEE, TrustZone | ☐ | ☐ | ☐ |
| 6.2.8 | Coreboot/LinuxBoot, Heads | ☐ | ☐ | ☐ |

## P7. Embedded Systems & Microcontrollers

### 7.1 MCU fundamentals

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 7.1.1 | ARM Cortex-M, RISC-V MCUs, ESP32, AVR, STM32 | ☐ | ☐ | ☐ |
| 7.1.2 | Memory map, flash/SRAM, memory-mapped I/O | ☐ | ☐ | ☐ |
| 7.1.3 | Interrupts, NVIC, priorities, nesting | ☐ | ☐ | ☐ |
| 7.1.4 | Timers, PWM, input capture | ☐ | ☐ | ☐ |
| 7.1.5 | ADC/DAC, sampling theory, oversampling | ☐ | ☐ | ☐ |
| 7.1.6 | GPIO, pull-ups, debouncing | ☐ | ☐ | ☐ |
| 7.1.7 | DMA on MCUs | ☐ | ☐ | ☐ |
| 7.1.8 | Watchdogs, brown-out, reset causes | ☐ | ☐ | ☐ |
| 7.1.9 | Low-power modes, wake sources, power budgeting | ☐ | ☐ | ☐ |
| 7.1.10 | Clock trees, PLL, crystals | ☐ | ☐ | ☐ |

### 7.2 Bare-metal & RTOS

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 7.2.1 | Linker scripts, startup code, vector tables | ☐ | ☐ | ☐ |
| 7.2.2 | Stack/heap sizing on MCU | ☐ | ☐ | ☐ |
| 7.2.3 | FreeRTOS, Zephyr, RTEMS, ThreadX | ☐ | ☐ | ☐ |
| 7.2.4 | Real-time scheduling: RMS, EDF, WCET | ☐ | ☐ | ☐ |
| 7.2.5 | Priority inversion, priority ceiling | ☐ | ☐ | ☐ |
| 7.2.6 | ISR-to-task communication patterns | ☐ | ☐ | ☐ |
| 7.2.7 | Static vs dynamic allocation in embedded | ☐ | ☐ | ☐ |
| 7.2.8 | Embedded Rust, Zig, no_std/freestanding | ☐ | ☐ | ☐ |
| 7.2.9 | Bootloaders, OTA with A/B partitions, delta updates | ☐ | ☐ | ☐ |

### 7.3 Hardware debug & bring-up

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 7.3.1 | JTAG, SWD, OpenOCD, GDB remote | ☐ | ☐ | ☐ |
| 7.3.2 | Logic analyzer, oscilloscope, protocol decoders | ☐ | ☐ | ☐ |
| 7.3.3 | Multimeter, bench PSU, current profiling | ☐ | ☐ | ☐ |
| 7.3.4 | Reading schematics and datasheets | ☐ | ☐ | ☐ |
| 7.3.5 | PCB basics, layout, EMI/EMC, grounding, decoupling | ☐ | ☐ | ☐ |
| 7.3.6 | Signal integrity, termination, impedance | ☐ | ☐ | ☐ |
| 7.3.7 | Flash programming, fuse bits, secure elements | ☐ | ☐ | ☐ |
| 7.3.8 | Manufacturing test, provisioning, factory flashing | ☐ | ☐ | ☐ |

## P8. Hardware Buses & Peripheral Interfaces

### 8.1 Serial & board-level buses

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 8.1.1 | UART/RS-232/RS-485 | ☐ | ☐ | ☐ |
| 8.1.2 | SPI, QSPI, OSPI | ☐ | ☐ | ☐ |
| 8.1.3 | I2C, SMBus, PMBus | ☐ | ☐ | ☐ |
| 8.1.4 | CAN, CAN-FD, LIN | ☐ | ☐ | ☐ |
| 8.1.5 | 1-Wire | ☐ | ☐ | ☐ |
| 8.1.6 | I2S, PDM audio | ☐ | ☐ | ☐ |
| 8.1.7 | MIPI CSI/DSI | ☐ | ☐ | ☐ |
| 8.1.8 | SDIO, eMMC, SD | ☐ | ☐ | ☐ |
| 8.1.9 | USB: descriptors, enumeration, classes, host vs device | ☐ | ☐ | ☐ |
| 8.1.10 | Ethernet PHY/MAC, MII/RGMII, PoE | ☐ | ☐ | ☐ |
| 8.1.11 | Modbus, Profibus, EtherCAT, OPC UA | ☐ | ☐ | ☐ |
| 8.1.12 | GPIB, PXI basics | ☐ | ☐ | ☐ |

### 8.2 Sensors & actuators

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 8.2.1 | Sensor types, calibration, noise, filtering (Kalman, complementary) | ☐ | ☐ | ☐ |
| 8.2.2 | Motor drivers, stepper, BLDC, FOC basics | ☐ | ☐ | ☐ |
| 8.2.3 | PID control | ☐ | ☐ | ☐ |
| 8.2.4 | Power electronics basics: buck/boost, LDO | ☐ | ☐ | ☐ |
| 8.2.5 | Batteries, BMS, charging | ☐ | ☐ | ☐ |
| 8.2.6 | Level shifting, isolation, optocouplers | ☐ | ☐ | ☐ |

## P9. OS: Processes, Threads & Scheduling

### 9.1 Execution model

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 9.1.1 | User vs kernel space, rings | ☐ | ☐ | ☐ |
| 9.1.2 | System calls, syscall/sysenter, vDSO, syscall tables | ☐ | ☐ | ☐ |
| 9.1.3 | ELF layout: text/data/BSS, heap, stack, auxv | ☐ | ☐ | ☐ |
| 9.1.4 | fork, exec, clone, vfork, posix_spawn | ☐ | ☐ | ☐ |
| 9.1.5 | Copy-on-write fork, zombies, orphans, reaping | ☐ | ☐ | ☐ |
| 9.1.6 | Signals: delivery, masks, async-signal-safety | ☐ | ☐ | ☐ |
| 9.1.7 | Process groups, sessions, controlling terminal, daemons | ☐ | ☐ | ☐ |
| 9.1.8 | Threads: 1:1, N:1, M:N; TLS | ☐ | ☐ | ☐ |
| 9.1.9 | Thread-local storage mechanics | ☐ | ☐ | ☐ |
| 9.1.10 | Credentials: uid/gid, setuid, capabilities | ☐ | ☐ | ☐ |

### 9.2 Scheduling

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 9.2.1 | CFS, EEVDF, vruntime | ☐ | ☐ | ☐ |
| 9.2.2 | RT classes: SCHED_FIFO, SCHED_RR, SCHED_DEADLINE | ☐ | ☐ | ☐ |
| 9.2.3 | Nice values, cgroup CPU shares/quota | ☐ | ☐ | ☐ |
| 9.2.4 | CPU affinity, taskset, numactl, isolcpus, nohz_full | ☐ | ☐ | ☐ |
| 9.2.5 | Load balancing, scheduling domains, wake-up placement | ☐ | ☐ | ☐ |
| 9.2.6 | Context switch cost: registers, TLB, cache | ☐ | ☐ | ☐ |
| 9.2.7 | Preemption models: voluntary, full, PREEMPT_RT | ☐ | ☐ | ☐ |
| 9.2.8 | CPU throttling in containers (CFS bandwidth) | ☐ | ☐ | ☐ |
| 9.2.9 | Priority inversion and inheritance | ☐ | ☐ | ☐ |
| 9.2.10 | Scheduler tracing: sched_switch, schedstat, perf sched | ☐ | ☐ | ☐ |

## P10. OS: Memory Management

### 10.1 Virtual memory

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 10.1.1 | Virtual vs physical addresses, MMU | ☐ | ☐ | ☐ |
| 10.1.2 | Multi-level page tables, 4/5-level paging | ☐ | ☐ | ☐ |
| 10.1.3 | PTE flags: present, dirty, accessed, NX, user | ☐ | ☐ | ☐ |
| 10.1.4 | TLB, TLB shootdowns, ASID/PCID | ☐ | ☐ | ☐ |
| 10.1.5 | Page faults: minor, major, COW, demand paging | ☐ | ☐ | ☐ |
| 10.1.6 | mmap: file-backed, anonymous, shared, private | ☐ | ☐ | ☐ |
| 10.1.7 | Address space layout, ASLR, KASLR, guard pages | ☐ | ☐ | ☐ |
| 10.1.8 | Huge pages: THP vs hugetlbfs, 2MB/1GB | ☐ | ☐ | ☐ |
| 10.1.9 | Memory overcommit, vm.overcommit_memory | ☐ | ☐ | ☐ |
| 10.1.10 | mlock, madvise, mremap, userfaultfd | ☐ | ☐ | ☐ |

### 10.2 Allocators & reclaim

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 10.2.1 | brk/sbrk vs mmap | ☐ | ☐ | ☐ |
| 10.2.2 | glibc ptmalloc arenas, fragmentation | ☐ | ☐ | ☐ |
| 10.2.3 | jemalloc, tcmalloc, mimalloc | ☐ | ☐ | ☐ |
| 10.2.4 | Kernel: buddy allocator, slab/SLUB, vmalloc, kmalloc | ☐ | ☐ | ☐ |
| 10.2.5 | Page cache vs anonymous memory, LRU lists, active/inactive | ☐ | ☐ | ☐ |
| 10.2.6 | kswapd, direct reclaim, watermarks | ☐ | ☐ | ☐ |
| 10.2.7 | Swap, zswap, zram, swappiness | ☐ | ☐ | ☐ |
| 10.2.8 | OOM killer, oom_score_adj, memory cgroups OOM | ☐ | ☐ | ☐ |
| 10.2.9 | PSI (pressure stall information) | ☐ | ☐ | ☐ |
| 10.2.10 | KSM, memory compaction, NUMA balancing | ☐ | ☐ | ☐ |
| 10.2.11 | Memory leak hunting: valgrind, heaptrack, ASan, bpf memleak | ☐ | ☐ | ☐ |

## P11. OS: Concurrency & Synchronization

### 11.1 Primitives

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 11.1.1 | Atomics: CAS, TAS, FAA, LL/SC | ☐ | ☐ | ☐ |
| 11.1.2 | Mutex, semaphore, spinlock, rwlock, seqlock | ☐ | ☐ | ☐ |
| 11.1.3 | Futex internals | ☐ | ☐ | ☐ |
| 11.1.4 | Condition variables, barriers | ☐ | ☐ | ☐ |
| 11.1.5 | RCU: grace periods, read-side critical sections | ☐ | ☐ | ☐ |
| 11.1.6 | Lock-free and wait-free queues/stacks | ☐ | ☐ | ☐ |
| 11.1.7 | Hazard pointers, epoch-based reclamation | ☐ | ☐ | ☐ |
| 11.1.8 | Memory ordering in lock-free code | ☐ | ☐ | ☐ |
| 11.1.9 | Per-CPU data, sharding to avoid contention | ☐ | ☐ | ☐ |
| 11.1.10 | Transactional memory (HTM/TSX) | ☐ | ☐ | ☐ |

### 11.2 Bugs & models

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 11.2.1 | Deadlock: conditions, lock ordering, detection | ☐ | ☐ | ☐ |
| 11.2.2 | Livelock, starvation, convoys | ☐ | ☐ | ☐ |
| 11.2.3 | Data races vs race conditions | ☐ | ☐ | ☐ |
| 11.2.4 | ABA problem | ☐ | ☐ | ☐ |
| 11.2.5 | Priority inversion | ☐ | ☐ | ☐ |
| 11.2.6 | Thundering herd | ☐ | ☐ | ☐ |
| 11.2.7 | Actor model, CSP, message passing | ☐ | ☐ | ☐ |
| 11.2.8 | Async/await, coroutines, green threads, work stealing | ☐ | ☐ | ☐ |
| 11.2.9 | Structured concurrency | ☐ | ☐ | ☐ |
| 11.2.10 | Tools: TSan, helgrind, lockdep, rr | ☐ | ☐ | ☐ |

## P12. OS: I/O Subsystem & Virtual File System

### 12.1 VFS & files

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 12.1.1 | File descriptors, open file table, inodes, dentries, superblock | ☐ | ☐ | ☐ |
| 12.1.2 | ulimit, fd exhaustion, epoll fd semantics | ☐ | ☐ | ☐ |
| 12.1.3 | Page cache, dirty writeback, flusher threads, readahead | ☐ | ☐ | ☐ |
| 12.1.4 | O_DIRECT, O_SYNC, fsync, fdatasync, sync_file_range | ☐ | ☐ | ☐ |
| 12.1.5 | File locking: flock, fcntl, leases | ☐ | ☐ | ☐ |
| 12.1.6 | inotify, fanotify | ☐ | ☐ | ☐ |
| 12.1.7 | Mount namespaces, bind mounts, overlay mounts | ☐ | ☐ | ☐ |
| 12.1.8 | procfs, sysfs, debugfs, tmpfs, cgroupfs | ☐ | ☐ | ☐ |
| 12.1.9 | Extended attributes, ACLs | ☐ | ☐ | ☐ |
| 12.1.10 | Sparse files, fallocate, reflinks | ☐ | ☐ | ☐ |

### 12.2 I/O models

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 12.2.1 | Blocking, non-blocking, async | ☐ | ☐ | ☐ |
| 12.2.2 | select, poll, epoll (level vs edge) | ☐ | ☐ | ☐ |
| 12.2.3 | io_uring: SQ/CQ, registered buffers, fixed files | ☐ | ☐ | ☐ |
| 12.2.4 | POSIX AIO, libaio, kernel AIO | ☐ | ☐ | ☐ |
| 12.2.5 | Zero-copy: sendfile, splice, tee, MSG_ZEROCOPY | ☐ | ☐ | ☐ |
| 12.2.6 | mmap vs read/write tradeoffs | ☐ | ☐ | ☐ |
| 12.2.7 | Reactor vs proactor patterns | ☐ | ☐ | ☐ |
| 12.2.8 | Block layer: bio, request queues, I/O schedulers (mq-deadline, kyber, bfq, none) | ☐ | ☐ | ☐ |
| 12.2.9 | IPC: pipes, FIFOs, UNIX sockets, shm, POSIX mq, eventfd, signalfd, memfd, pidfd | ☐ | ☐ | ☐ |

## P13. OS: Interrupts, Drivers & Kernel Development

### 13.1 Interrupts & drivers

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 13.1.1 | Hard IRQ, softirq, tasklet, workqueue, threaded IRQ | ☐ | ☐ | ☐ |
| 13.1.2 | APIC, IOAPIC, GIC, IRQ affinity, irqbalance | ☐ | ☐ | ☐ |
| 13.1.3 | NMI, MCE | ☐ | ☐ | ☐ |
| 13.1.4 | Character, block, network drivers | ☐ | ☐ | ☐ |
| 13.1.5 | Platform drivers, device tree bindings | ☐ | ☐ | ☐ |
| 13.1.6 | PCI driver model, probe/remove | ☐ | ☐ | ☐ |
| 13.1.7 | DMA API in drivers | ☐ | ☐ | ☐ |
| 13.1.8 | Kernel modules, insmod/modprobe, DKMS | ☐ | ☐ | ☐ |
| 13.1.9 | Module signing, lockdown | ☐ | ☐ | ☐ |
| 13.1.10 | Hotplug, udev, devtmpfs | ☐ | ☐ | ☐ |

### 13.2 Kernel dev practice

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 13.2.1 | Kernel build: Kconfig, Kbuild, defconfig | ☐ | ☐ | ☐ |
| 13.2.2 | Kernel coding style, kernel API (list_head, kref, RCU APIs) | ☐ | ☐ | ☐ |
| 13.2.3 | Memory contexts: atomic vs process context | ☐ | ☐ | ☐ |
| 13.2.4 | Debugging: printk, dynamic debug, ftrace, kgdb, KASAN, KCSAN, KMSAN, UBSAN, lockdep | ☐ | ☐ | ☐ |
| 13.2.5 | kdump, crash, oops/panic reading | ☐ | ☐ | ☐ |
| 13.2.6 | Patch workflow, git send-email, mailing lists, maintainers | ☐ | ☐ | ☐ |
| 13.2.7 | Rust-for-Linux basics | ☐ | ☐ | ☐ |
| 13.2.8 | Livepatch, kexec | ☐ | ☐ | ☐ |

## P14. Operating System Families & Platform Differences

### 14.1 Other OSes

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 14.1.1 | Windows internals: NT kernel, object manager, handles, WDM/WDF | ☐ | ☐ | ☐ |
| 14.1.2 | Windows: Win32 vs NT API, registry, ETW, WinDbg | ☐ | ☐ | ☐ |
| 14.1.3 | macOS/XNU: Mach, BSD layer, launchd, Endpoint Security | ☐ | ☐ | ☐ |
| 14.1.4 | FreeBSD: jails, kqueue, pf, ZFS, bhyve | ☐ | ☐ | ☐ |
| 14.1.5 | OpenBSD: pledge, unveil, security philosophy | ☐ | ☐ | ☐ |
| 14.1.6 | Android: Binder, ART, SELinux, Treble | ☐ | ☐ | ☐ |
| 14.1.7 | RTOS vs general-purpose OS | ☐ | ☐ | ☐ |
| 14.1.8 | Unikernels, library OSes | ☐ | ☐ | ☐ |
| 14.1.9 | Microkernels: seL4, QNX, Fuchsia | ☐ | ☐ | ☐ |
| 14.1.10 | WASI and WASM as an OS abstraction | ☐ | ☐ | ☐ |

## P15. Storage Hardware

### 15.1 Disks & flash

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 15.1.1 | HDD mechanics: seek, rotation, zones, SMR vs CMR | ☐ | ☐ | ☐ |
| 15.1.2 | NCQ, TCQ, SATA vs SAS | ☐ | ☐ | ☐ |
| 15.1.3 | NAND: SLC/MLC/TLC/QLC, pages, blocks, erase | ☐ | ☐ | ☐ |
| 15.1.4 | FTL, garbage collection, wear leveling | ☐ | ☐ | ☐ |
| 15.1.5 | Write amplification, over-provisioning, TRIM/discard | ☐ | ☐ | ☐ |
| 15.1.6 | Power-loss protection, capacitors | ☐ | ☐ | ☐ |
| 15.1.7 | SSD latency spikes, steady-state performance | ☐ | ☐ | ☐ |
| 15.1.8 | NVMe: queues, namespaces, doorbells, MSI-X | ☐ | ☐ | ☐ |
| 15.1.9 | NVMe-oF (RDMA/TCP/FC), ZNS, FDP | ☐ | ☐ | ☐ |
| 15.1.10 | SMART, health telemetry, firmware updates | ☐ | ☐ | ☐ |
| 15.1.11 | Tape, optical, archival media | ☐ | ☐ | ☐ |

## P16. File Systems & Volume Management

### 16.1 File systems

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 16.1.1 | Ext4: extents, journaling modes, delayed allocation | ☐ | ☐ | ☐ |
| 16.1.2 | XFS: allocation groups, B+trees, reflink | ☐ | ☐ | ☐ |
| 16.1.3 | Btrfs: COW, subvolumes, snapshots, send/receive | ☐ | ☐ | ☐ |
| 16.1.4 | ZFS: ARC, L2ARC, ZIL/SLOG, vdevs, scrubs, zvols | ☐ | ☐ | ☐ |
| 16.1.5 | F2FS, NILFS, log-structured file systems | ☐ | ☐ | ☐ |
| 16.1.6 | FAT/exFAT/NTFS basics | ☐ | ☐ | ☐ |
| 16.1.7 | Crash consistency, journaling vs COW, torn writes | ☐ | ☐ | ☐ |
| 16.1.8 | fsck, repair tools | ☐ | ☐ | ☐ |
| 16.1.9 | Checksums, bit rot, scrubbing | ☐ | ☐ | ☐ |
| 16.1.10 | Quotas, project quotas | ☐ | ☐ | ☐ |
| 16.1.11 | FUSE, virtiofs, 9p | ☐ | ☐ | ☐ |

### 16.2 Volumes & distributed storage

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 16.2.1 | RAID 0/1/5/6/10, write hole | ☐ | ☐ | ☐ |
| 16.2.2 | Erasure coding, Reed-Solomon | ☐ | ☐ | ☐ |
| 16.2.3 | LVM: PV/VG/LV, thin provisioning, snapshots | ☐ | ☐ | ☐ |
| 16.2.4 | dm-crypt/LUKS, dm-verity, dm-integrity | ☐ | ☐ | ☐ |
| 16.2.5 | bcache, dm-cache | ☐ | ☐ | ☐ |
| 16.2.6 | mdadm | ☐ | ☐ | ☐ |
| 16.2.7 | NFS, SMB/CIFS, iSCSI, FC | ☐ | ☐ | ☐ |
| 16.2.8 | Ceph (RADOS, CRUSH), GlusterFS, Lustre, BeeGFS | ☐ | ☐ | ☐ |
| 16.2.9 | HDFS, object storage, S3 semantics, MinIO | ☐ | ☐ | ☐ |
| 16.2.10 | Backup: snapshots, incremental, dedup, restic/borg, 3-2-1 | ☐ | ☐ | ☐ |

## P17. Networking: Linux Stack & Packet Path

### 17.1 Ingress/egress

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 17.1.1 | NIC rings, DMA, IRQ moderation | ☐ | ☐ | ☐ |
| 17.1.2 | NAPI, GRO, LRO, RSS, RPS, RFS, XPS | ☐ | ☐ | ☐ |
| 17.1.3 | sk_buff structure and lifecycle | ☐ | ☐ | ☐ |
| 17.1.4 | Qdiscs: fq, fq_codel, pfifo_fast, mq, tc | ☐ | ☐ | ☐ |
| 17.1.5 | TSO/GSO/GRO offloads, checksum offload | ☐ | ☐ | ☐ |
| 17.1.6 | Socket buffers, autotuning, backlog, SO_REUSEPORT, SO_REUSEADDR | ☐ | ☐ | ☐ |
| 17.1.7 | Netfilter hooks, iptables, nftables, conntrack | ☐ | ☐ | ☐ |
| 17.1.8 | Routing tables, policy routing, ip rule | ☐ | ☐ | ☐ |
| 17.1.9 | XDP, AF_XDP, tc-bpf, eBPF networking | ☐ | ☐ | ☐ |
| 17.1.10 | DPDK, VPP, netmap | ☐ | ☐ | ☐ |
| 17.1.11 | Packet capture: tcpdump, Wireshark, pcap filters, tshark | ☐ | ☐ | ☐ |
| 17.1.12 | Network namespaces, veth, macvlan, ipvlan | ☐ | ☐ | ☐ |

## P18. Networking: Transport Layer

### 18.1 TCP

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 18.1.1 | 3-way handshake, 4-way close, RST | ☐ | ☐ | ☐ |
| 18.1.2 | State machine, TIME_WAIT, CLOSE_WAIT, FIN_WAIT | ☐ | ☐ | ☐ |
| 18.1.3 | SYN flood, SYN cookies, accept queues | ☐ | ☐ | ☐ |
| 18.1.4 | Sliding window, flow control, zero-window | ☐ | ☐ | ☐ |
| 18.1.5 | Retransmission: RTO, fast retransmit, SACK, DSACK, TLP | ☐ | ☐ | ☐ |
| 18.1.6 | Congestion control: Reno, Cubic, BBR, Vegas | ☐ | ☐ | ☐ |
| 18.1.7 | ECN, DCTCP | ☐ | ☐ | ☐ |
| 18.1.8 | Nagle, delayed ACK, TCP_NODELAY, cork | ☐ | ☐ | ☐ |
| 18.1.9 | TCP Fast Open, MPTCP | ☐ | ☐ | ☐ |
| 18.1.10 | Keepalives, user timeout | ☐ | ☐ | ☐ |
| 18.1.11 | MSS, MTU, PMTUD, MTU black holes | ☐ | ☐ | ☐ |
| 18.1.12 | Bufferbloat | ☐ | ☐ | ☐ |

### 18.2 UDP, QUIC & others

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 18.2.1 | UDP semantics, checksum, fragmentation | ☐ | ☐ | ☐ |
| 18.2.2 | QUIC: connection IDs, streams, 0-RTT, loss recovery, migration | ☐ | ☐ | ☐ |
| 18.2.3 | SCTP, DCCP | ☐ | ☐ | ☐ |
| 18.2.4 | RTP/RTCP, SRT | ☐ | ☐ | ☐ |
| 18.2.5 | Multicast, IGMP, PIM | ☐ | ☐ | ☐ |
| 18.2.6 | Reliable UDP designs | ☐ | ☐ | ☐ |

## P19. Networking: L2/L3, Routing & Switching

### 19.1 Layer 2

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 19.1.1 | Ethernet frames, MAC, ARP, NDP | ☐ | ☐ | ☐ |
| 19.1.2 | VLAN 802.1Q, QinQ | ☐ | ☐ | ☐ |
| 19.1.3 | STP/RSTP/MSTP, LACP, bonding | ☐ | ☐ | ☐ |
| 19.1.4 | VXLAN, GENEVE, GRE, EVPN | ☐ | ☐ | ☐ |
| 19.1.5 | Linux bridges, OVS, OVN | ☐ | ☐ | ☐ |
| 19.1.6 | 802.1X, MACsec, port security | ☐ | ☐ | ☐ |
| 19.1.7 | Switch ASICs, TCAM, cut-through vs store-and-forward | ☐ | ☐ | ☐ |

### 19.2 Layer 3

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 19.2.1 | IPv4 addressing, CIDR, subnetting, NAT, CGNAT | ☐ | ☐ | ☐ |
| 19.2.2 | IPv6 addressing, SLAAC, extension headers, transition | ☐ | ☐ | ☐ |
| 19.2.3 | ICMP, traceroute, MTU discovery | ☐ | ☐ | ☐ |
| 19.2.4 | Static routing, OSPF, IS-IS | ☐ | ☐ | ☐ |
| 19.2.5 | BGP: eBGP/iBGP, path selection, communities, RPKI, route leaks | ☐ | ☐ | ☐ |
| 19.2.6 | ECMP, anycast | ☐ | ☐ | ☐ |
| 19.2.7 | MPLS, segment routing | ☐ | ☐ | ☐ |
| 19.2.8 | Datacenter fabrics: Clos, leaf-spine | ☐ | ☐ | ☐ |
| 19.2.9 | VRF, policy-based routing | ☐ | ☐ | ☐ |
| 19.2.10 | DDoS: amplification, scrubbing, BGP flowspec | ☐ | ☐ | ☐ |

## P20. Networking: Application Protocols, DNS & TLS

### 20.1 Web & app protocols

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 20.1.1 | HTTP/1.1, HTTP/2, HTTP/3, head-of-line blocking | ☐ | ☐ | ☐ |
| 20.1.2 | HTTP caching, ETags, CDN cache keys | ☐ | ☐ | ☐ |
| 20.1.3 | WebSockets, SSE, long polling | ☐ | ☐ | ☐ |
| 20.1.4 | gRPC, Thrift, GraphQL transport | ☐ | ☐ | ☐ |
| 20.1.5 | MQTT, CoAP, AMQP, NATS, Kafka protocol | ☐ | ☐ | ☐ |
| 20.1.6 | SMTP, IMAP, SPF, DKIM, DMARC | ☐ | ☐ | ☐ |
| 20.1.7 | SSH internals, port forwarding, certificates | ☐ | ☐ | ☐ |
| 20.1.8 | FTP/SFTP, rsync, NTP, PTP | ☐ | ☐ | ☐ |
| 20.1.9 | SIP/WebRTC basics, ICE, STUN, TURN | ☐ | ☐ | ☐ |
| 20.1.10 | OAuth2, OIDC, SAML, JWT | ☐ | ☐ | ☐ |

### 20.2 DNS & TLS

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 20.2.1 | Recursive vs authoritative, caching, TTL | ☐ | ☐ | ☐ |
| 20.2.2 | Record types, CNAME flattening, SRV | ☐ | ☐ | ☐ |
| 20.2.3 | EDNS, DNSSEC, DoH, DoT, DoQ | ☐ | ☐ | ☐ |
| 20.2.4 | Anycast DNS, GeoDNS, split horizon | ☐ | ☐ | ☐ |
| 20.2.5 | DNS failure modes, negative caching, resolver behavior | ☐ | ☐ | ☐ |
| 20.2.6 | TLS 1.2 vs 1.3 handshake, session resumption, 0-RTT | ☐ | ☐ | ☐ |
| 20.2.7 | ALPN, SNI, ECH, OCSP stapling | ☐ | ☐ | ☐ |
| 20.2.8 | Cipher suites, forward secrecy | ☐ | ☐ | ☐ |
| 20.2.9 | Certificate chains, CT logs, ACME | ☐ | ☐ | ☐ |
| 20.2.10 | mTLS, SPIFFE/SPIRE | ☐ | ☐ | ☐ |

## P21. Networking: High-Performance, Datacenter & Edge

### 21.1 High performance

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 21.1.1 | Kernel bypass: DPDK, RDMA verbs, io_uring networking | ☐ | ☐ | ☐ |
| 21.1.2 | RoCE v2, Infiniband, iWARP, PFC/ECN tuning | ☐ | ☐ | ☐ |
| 21.1.3 | SmartNIC/DPU offload, SR-IOV, virtio-net, vhost | ☐ | ☐ | ☐ |
| 21.1.4 | Packet processing pipelines, P4 | ☐ | ☐ | ☐ |
| 21.1.5 | Hardware timestamping, PTP, White Rabbit | ☐ | ☐ | ☐ |
| 21.1.6 | 100/400/800G optics, PAM4, cabling, transceivers | ☐ | ☐ | ☐ |
| 21.1.7 | Load balancing L4/L7: Maglev, IPVS, Envoy, HAProxy, Nginx | ☐ | ☐ | ☐ |
| 21.1.8 | Consistent-hash LB, connection draining | ☐ | ☐ | ☐ |
| 21.1.9 | Reverse proxies, TLS termination, connection pooling | ☐ | ☐ | ☐ |

### 21.2 Edge & global

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 21.2.1 | CDN architecture, tiered caching, origin shield | ☐ | ☐ | ☐ |
| 21.2.2 | Edge compute: Workers, WASM at the edge | ☐ | ☐ | ☐ |
| 21.2.3 | GSLB, geo-routing, latency-based routing | ☐ | ☐ | ☐ |
| 21.2.4 | Peering, IXPs, transit, Tier-1 relationships | ☐ | ☐ | ☐ |
| 21.2.5 | WAN optimization, SD-WAN | ☐ | ☐ | ☐ |
| 21.2.6 | VPNs: WireGuard, IPsec, OpenVPN, Tailscale-style overlays | ☐ | ☐ | ☐ |
| 21.2.7 | NAT traversal, hole punching | ☐ | ☐ | ☐ |
| 21.2.8 | Mesh networks, Tor, I2P | ☐ | ☐ | ☐ |

## P22. Wireless, IoT & Telecom Protocols

### 22.1 Wireless

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 22.1.1 | 802.11 a/b/g/n/ac/ax/be, channels, MIMO, roaming | ☐ | ☐ | ☐ |
| 22.1.2 | Bluetooth Classic/LE, GATT, mesh | ☐ | ☐ | ☐ |
| 22.1.3 | Zigbee, Thread, Matter, Z-Wave | ☐ | ☐ | ☐ |
| 22.1.4 | LoRa/LoRaWAN, Sigfox, NB-IoT, LTE-M | ☐ | ☐ | ☐ |
| 22.1.5 | Cellular: 4G/5G NR, core network, slicing, SIM/eSIM | ☐ | ☐ | ☐ |
| 22.1.6 | GNSS/GPS, RTK, timing | ☐ | ☐ | ☐ |
| 22.1.7 | RF basics: dBm, link budget, antenna, modulation (QAM, OFDM) | ☐ | ☐ | ☐ |
| 22.1.8 | Satellite links: LEO/GEO, latency, Doppler | ☐ | ☐ | ☐ |

### 22.2 IoT systems

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 22.2.1 | Device provisioning, identity, certificates | ☐ | ☐ | ☐ |
| 22.2.2 | OTA update frameworks (Mender, RAUC, SWUpdate) | ☐ | ☐ | ☐ |
| 22.2.3 | Device shadow/twin patterns | ☐ | ☐ | ☐ |
| 22.2.4 | Edge gateways, protocol translation | ☐ | ☐ | ☐ |
| 22.2.5 | Telemetry pipelines, batching, store-and-forward | ☐ | ☐ | ☐ |
| 22.2.6 | Power/duty-cycle tradeoffs | ☐ | ☐ | ☐ |
| 22.2.7 | Fleet management, remote diagnostics | ☐ | ☐ | ☐ |

## P23. Compilers & Program Translation

### 23.1 Compiler pipeline

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 23.1.1 | Lexing, parsing, grammars (LL, LR, PEG) | ☐ | ☐ | ☐ |
| 23.1.2 | AST, symbol tables, type checking, inference | ☐ | ☐ | ☐ |
| 23.1.3 | Intermediate representations: SSA, CFG, LLVM IR, MIR | ☐ | ☐ | ☐ |
| 23.1.4 | Optimization passes: inlining, DCE, CSE, LICM, loop unrolling, vectorization | ☐ | ☐ | ☐ |
| 23.1.5 | Escape analysis, devirtualization | ☐ | ☐ | ☐ |
| 23.1.6 | Register allocation, instruction selection, scheduling | ☐ | ☐ | ☐ |
| 23.1.7 | Codegen, target backends | ☐ | ☐ | ☐ |
| 23.1.8 | Link-time optimization, ThinLTO | ☐ | ☐ | ☐ |
| 23.1.9 | PGO, AutoFDO, BOLT | ☐ | ☐ | ☐ |
| 23.1.10 | Undefined behavior and compiler exploitation of it | ☐ | ☐ | ☐ |
| 23.1.11 | Compiler flags: -O2/-O3/-Os/-march/-mtune/-fno-omit-frame-pointer | ☐ | ☐ | ☐ |
| 23.1.12 | Sanitizers: ASan, TSan, UBSan, MSan, HWASan | ☐ | ☐ | ☐ |

### 23.2 JIT & interpreters

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 23.2.1 | Bytecode VMs, stack vs register machines | ☐ | ☐ | ☐ |
| 23.2.2 | JIT tiers, inline caches, hidden classes | ☐ | ☐ | ☐ |
| 23.2.3 | Tracing vs method JIT | ☐ | ☐ | ☐ |
| 23.2.4 | Garbage collector integration | ☐ | ☐ | ☐ |
| 23.2.5 | WebAssembly: modules, linear memory, WASI, component model | ☐ | ☐ | ☐ |
| 23.2.6 | Interpreter design: dispatch techniques | ☐ | ☐ | ☐ |
| 23.2.7 | Cross-compilation, cross toolchains, sysroots | ☐ | ☐ | ☐ |
| 23.2.8 | Decompilation, disassembly, binary lifting | ☐ | ☐ | ☐ |

## P24. Linking, Loading & ABI

### 24.1 Binary format & loader

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 24.1.1 | ELF sections vs segments, program headers | ☐ | ☐ | ☐ |
| 24.1.2 | Symbol resolution, visibility, weak symbols | ☐ | ☐ | ☐ |
| 24.1.3 | Static vs dynamic linking, shared libraries .so/.dll/.dylib | ☐ | ☐ | ☐ |
| 24.1.4 | PLT/GOT, lazy binding, RELRO, BIND_NOW | ☐ | ☐ | ☐ |
| 24.1.5 | Dynamic loader ld.so, LD_PRELOAD, rpath, RUNPATH | ☐ | ☐ | ☐ |
| 24.1.6 | PIE, ASLR, relocations | ☐ | ☐ | ☐ |
| 24.1.7 | Symbol versioning, ABI stability, soname | ☐ | ☐ | ☐ |
| 24.1.8 | Name mangling, C++ ABI, vtables | ☐ | ☐ | ☐ |
| 24.1.9 | Calling conventions: SysV, Win64, AAPCS | ☐ | ☐ | ☐ |
| 24.1.10 | FFI: C ABI, cgo costs, bindgen | ☐ | ☐ | ☐ |
| 24.1.11 | musl vs glibc, static binaries | ☐ | ☐ | ☐ |
| 24.1.12 | Core file format, debug info (DWARF), stripping, separate debug info | ☐ | ☐ | ☐ |

## P25. Programming Languages & Runtimes

### 25.1 Systems languages

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 25.1.1 | C: undefined behavior, strict aliasing, volatile, restrict | ☐ | ☐ | ☐ |
| 25.1.2 | C++: RAII, move semantics, templates, constexpr, ABI pitfalls | ☐ | ☐ | ☐ |
| 25.1.3 | Rust: ownership, borrowing, lifetimes, unsafe, Send/Sync, async | ☐ | ☐ | ☐ |
| 25.1.4 | Zig: comptime, allocators, error unions, build system | ☐ | ☐ | ☐ |
| 25.1.5 | Go: goroutines, GMP scheduler, channels, GC, escape analysis, pprof | ☐ | ☐ | ☐ |
| 25.1.6 | Assembly reading/writing for x86-64 and ARM64 | ☐ | ☐ | ☐ |
| 25.1.7 | Inline asm, intrinsics | ☐ | ☐ | ☐ |
| 25.1.8 | Memory-safe vs unsafe languages tradeoffs | ☐ | ☐ | ☐ |

### 25.2 Managed & scripting runtimes

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 25.2.1 | JVM: classloading, JIT, GC (G1, ZGC, Shenandoah), JFR | ☐ | ☐ | ☐ |
| 25.2.2 | CLR/.NET runtime | ☐ | ☐ | ☐ |
| 25.2.3 | V8/Node: event loop, libuv, JIT, GC | ☐ | ☐ | ☐ |
| 25.2.4 | CPython: GIL, refcounting, C extensions | ☐ | ☐ | ☐ |
| 25.2.5 | Python performance: numpy, cython, PyPy | ☐ | ☐ | ☐ |
| 25.2.6 | Lua/LuaJIT, eBPF VM | ☐ | ☐ | ☐ |
| 25.2.7 | Garbage collection: tracing, generational, concurrent, region-based | ☐ | ☐ | ☐ |
| 25.2.8 | Reference counting, cycle collection, arenas | ☐ | ☐ | ☐ |
| 25.2.9 | Green threads and async runtimes: tokio, Go scheduler, libuv | ☐ | ☐ | ☐ |
| 25.2.10 | Shell scripting robustness: bash, POSIX sh, set -euo pipefail | ☐ | ☐ | ☐ |

## P26. Build Systems, Packaging & Toolchains

### 26.1 Build

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 26.1.1 | Make, CMake, Ninja, Meson | ☐ | ☐ | ☐ |
| 26.1.2 | Bazel, Buck, Pants hermetic builds | ☐ | ☐ | ☐ |
| 26.1.3 | Cargo, go build/modules, zig build, npm/pnpm | ☐ | ☐ | ☐ |
| 26.1.4 | Nix, Guix, reproducible and hermetic builds | ☐ | ☐ | ☐ |
| 26.1.5 | Incremental builds, caching, remote execution (sccache, ccache, RBE) | ☐ | ☐ | ☐ |
| 26.1.6 | Cross-compilation | ☐ | ☐ | ☐ |
| 26.1.7 | Dependency resolution, lockfiles, vendoring | ☐ | ☐ | ☐ |
| 26.1.8 | Semantic versioning, ABI vs API compatibility | ☐ | ☐ | ☐ |

### 26.2 Packaging & distribution

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 26.2.1 | deb, rpm, apk, pacman, nixpkgs | ☐ | ☐ | ☐ |
| 26.2.2 | Container images as packages, distroless, scratch | ☐ | ☐ | ☐ |
| 26.2.3 | AppImage, Flatpak, Snap | ☐ | ☐ | ☐ |
| 26.2.4 | Package signing, repositories, mirrors | ☐ | ☐ | ☐ |
| 26.2.5 | SBOM, SPDX, CycloneDX | ☐ | ☐ | ☐ |
| 26.2.6 | Provenance: SLSA, in-toto, sigstore | ☐ | ☐ | ☐ |
| 26.2.7 | Debuginfod, symbol servers | ☐ | ☐ | ☐ |
| 26.2.8 | Licensing: GPL, LGPL, MIT, Apache, AGPL, compliance | ☐ | ☐ | ☐ |

## P27. Data Structures

### 27.1 Core & in-memory

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 27.1.1 | Arrays, dynamic arrays, ring buffers, deques | ☐ | ☐ | ☐ |
| 27.1.2 | Linked lists, intrusive lists, XOR lists | ☐ | ☐ | ☐ |
| 27.1.3 | Hash tables: chaining, open addressing, robin hood, cuckoo, swiss tables | ☐ | ☐ | ☐ |
| 27.1.4 | Heaps, priority queues, d-ary heaps, pairing heaps | ☐ | ☐ | ☐ |
| 27.1.5 | Binary search trees, AVL, red-black, treaps, splay | ☐ | ☐ | ☐ |
| 27.1.6 | Tries, radix trees, ART, HAT-trie | ☐ | ☐ | ☐ |
| 27.1.7 | Skip lists | ☐ | ☐ | ☐ |
| 27.1.8 | Union-find | ☐ | ☐ | ☐ |
| 27.1.9 | Segment trees, Fenwick trees, interval trees | ☐ | ☐ | ☐ |
| 27.1.10 | Rope, gap buffer, piece table | ☐ | ☐ | ☐ |
| 27.1.11 | Arenas, slabs, object pools, free lists | ☐ | ☐ | ☐ |
| 27.1.12 | Bitsets, bitmaps, roaring bitmaps, succinct structures | ☐ | ☐ | ☐ |

### 27.2 Disk, concurrent & probabilistic

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 27.2.1 | B-tree, B+tree, B-epsilon trees | ☐ | ☐ | ☐ |
| 27.2.2 | LSM-tree, SSTable, memtable | ☐ | ☐ | ☐ |
| 27.2.3 | Fractal trees | ☐ | ☐ | ☐ |
| 27.2.4 | Persistent/immutable structures, HAMT, finger trees | ☐ | ☐ | ☐ |
| 27.2.5 | Concurrent hash maps, lock-free queues, MPMC/SPSC rings | ☐ | ☐ | ☐ |
| 27.2.6 | Disruptor pattern | ☐ | ☐ | ☐ |
| 27.2.7 | Bloom, counting Bloom, cuckoo, xor filters | ☐ | ☐ | ☐ |
| 27.2.8 | HyperLogLog, count-min sketch, t-digest, reservoir sampling | ☐ | ☐ | ☐ |
| 27.2.9 | Merkle trees, Merkle DAGs | ☐ | ☐ | ☐ |
| 27.2.10 | Graph representations: adjacency list/matrix, CSR | ☐ | ☐ | ☐ |
| 27.2.11 | Spatial: R-tree, k-d tree, quadtree, geohash, H3, S2 | ☐ | ☐ | ☐ |
| 27.2.12 | Vector indexes: HNSW, IVF, PQ | ☐ | ☐ | ☐ |

## P28. Algorithms

### 28.1 Classical

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 28.1.1 | Big-O, amortized analysis, cache-aware complexity | ☐ | ☐ | ☐ |
| 28.1.2 | Sorting: quicksort, mergesort, radix, introsort, timsort | ☐ | ☐ | ☐ |
| 28.1.3 | Searching, binary search variants | ☐ | ☐ | ☐ |
| 28.1.4 | Graph: BFS, DFS, Dijkstra, A*, Bellman-Ford, Floyd-Warshall | ☐ | ☐ | ☐ |
| 28.1.5 | MST: Kruskal, Prim | ☐ | ☐ | ☐ |
| 28.1.6 | Max flow, matching | ☐ | ☐ | ☐ |
| 28.1.7 | Topological sort, SCC | ☐ | ☐ | ☐ |
| 28.1.8 | Dynamic programming, greedy, divide and conquer | ☐ | ☐ | ☐ |
| 28.1.9 | String algorithms: KMP, Rabin-Karp, suffix arrays, Aho-Corasick | ☐ | ☐ | ☐ |
| 28.1.10 | Hashing: universal, consistent, rendezvous, locality-sensitive | ☐ | ☐ | ☐ |
| 28.1.11 | Randomized algorithms | ☐ | ☐ | ☐ |
| 28.1.12 | NP-hardness, approximation, heuristics | ☐ | ☐ | ☐ |

### 28.2 Systems-flavored

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 28.2.1 | Compression: LZ77, LZ4, zstd, Huffman, ANS, BWT | ☐ | ☐ | ☐ |
| 28.2.2 | Checksums and ECC: CRC, Hamming, Reed-Solomon, LDPC | ☐ | ☐ | ☐ |
| 28.2.3 | Scheduling algorithms: FIFO, RR, MLFQ, fair queuing | ☐ | ☐ | ☐ |
| 28.2.4 | Rate limiting: token bucket, leaky bucket, GCRA | ☐ | ☐ | ☐ |
| 28.2.5 | Load balancing algorithms: P2C, least-conn, weighted | ☐ | ☐ | ☐ |
| 28.2.6 | Cache eviction: LRU, LFU, ARC, TinyLFU, CLOCK, S3-FIFO | ☐ | ☐ | ☐ |
| 28.2.7 | Diff/merge: Myers, 3-way merge, CRDT merges | ☐ | ☐ | ☐ |
| 28.2.8 | Serialization, parsing, tokenization | ☐ | ☐ | ☐ |
| 28.2.9 | Numeric methods, FFT, linear algebra basics | ☐ | ☐ | ☐ |
| 28.2.10 | Streaming and online algorithms | ☐ | ☐ | ☐ |

## P29. Performance Math & Queueing Theory

### 29.1 Models

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 29.1.1 | Little's Law | ☐ | ☐ | ☐ |
| 29.1.2 | M/M/1, M/M/c, M/G/1 queues | ☐ | ☐ | ☐ |
| 29.1.3 | Utilization vs latency hockey stick | ☐ | ☐ | ☐ |
| 29.1.4 | Amdahl's Law, Gustafson's Law | ☐ | ☐ | ☐ |
| 29.1.5 | Universal Scalability Law (Gunther) | ☐ | ☐ | ☐ |
| 29.1.6 | Roofline model | ☐ | ☐ | ☐ |
| 29.1.7 | Tail latency amplification, fan-out | ☐ | ☐ | ☐ |
| 29.1.8 | Coordinated omission | ☐ | ☐ | ☐ |
| 29.1.9 | Percentiles, histograms (HDR), why averages lie | ☐ | ☐ | ☐ |
| 29.1.10 | Statistical significance, confidence intervals, bootstrapping | ☐ | ☐ | ☐ |
| 29.1.11 | Power laws, Zipf distributions, hot keys | ☐ | ☐ | ☐ |
| 29.1.12 | Back-of-envelope estimation: latency numbers, throughput, storage | ☐ | ☐ | ☐ |

## P30. Databases: Single-Node Engines

### 30.1 Storage engine

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 30.1.1 | B-tree engines (InnoDB, Postgres heap, SQLite) | ☐ | ☐ | ☐ |
| 30.1.2 | LSM engines (RocksDB, LevelDB, Pebble) | ☐ | ☐ | ☐ |
| 30.1.3 | WAL, checkpoints, recovery (ARIES) | ☐ | ☐ | ☐ |
| 30.1.4 | Memtable, SSTables, compaction (size-tiered, leveled, FIFO, universal) | ☐ | ☐ | ☐ |
| 30.1.5 | Write/read/space amplification | ☐ | ☐ | ☐ |
| 30.1.6 | Buffer pool, page layout, slotted pages | ☐ | ☐ | ☐ |
| 30.1.7 | Bloom filters, block cache, prefix seek | ☐ | ☐ | ☐ |
| 30.1.8 | Columnar storage: Parquet, ORC, Arrow, vectorized execution | ☐ | ☐ | ☐ |
| 30.1.9 | Embedded DBs: SQLite internals, DuckDB, LMDB | ☐ | ☐ | ☐ |

### 30.2 Transactions & query

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 30.2.1 | ACID, isolation levels RU/RC/RR/Serializable | ☐ | ☐ | ☐ |
| 30.2.2 | Snapshot isolation, write skew, phantoms, SSI | ☐ | ☐ | ☐ |
| 30.2.3 | MVCC implementations, vacuum/GC, bloat | ☐ | ☐ | ☐ |
| 30.2.4 | 2PL, OCC, timestamp ordering | ☐ | ☐ | ☐ |
| 30.2.5 | Deadlock detection in DBs | ☐ | ☐ | ☐ |
| 30.2.6 | Query parsing, planner, cost model, statistics | ☐ | ☐ | ☐ |
| 30.2.7 | Join algorithms: nested loop, hash, merge | ☐ | ☐ | ☐ |
| 30.2.8 | Index types: B-tree, hash, GIN, GiST, BRIN, covering, partial | ☐ | ☐ | ☐ |
| 30.2.9 | EXPLAIN / EXPLAIN ANALYZE reading | ☐ | ☐ | ☐ |
| 30.2.10 | Schema design, normalization, denormalization | ☐ | ☐ | ☐ |
| 30.2.11 | Migrations, online schema change | ☐ | ☐ | ☐ |
| 30.2.12 | Postgres internals, MySQL internals, replication lag | ☐ | ☐ | ☐ |

### 30.3 Specialized stores

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 30.3.1 | Key-value stores | ☐ | ☐ | ☐ |
| 30.3.2 | Document stores (MongoDB) | ☐ | ☐ | ☐ |
| 30.3.3 | Wide-column (Cassandra, HBase, Bigtable) | ☐ | ☐ | ☐ |
| 30.3.4 | Graph DBs | ☐ | ☐ | ☐ |
| 30.3.5 | Time-series DBs (InfluxDB, TimescaleDB, VictoriaMetrics) | ☐ | ☐ | ☐ |
| 30.3.6 | Search engines: Lucene, Elasticsearch, inverted indexes, BM25 | ☐ | ☐ | ☐ |
| 30.3.7 | Vector databases | ☐ | ☐ | ☐ |
| 30.3.8 | OLAP: ClickHouse, Druid, Pinot | ☐ | ☐ | ☐ |
| 30.3.9 | In-memory DBs: Redis data structures, persistence (RDB/AOF) | ☐ | ☐ | ☐ |

## P31. Distributed Databases, Messaging & Caching

### 31.1 Distributed databases

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 31.1.1 | Spanner, TrueTime, external consistency | ☐ | ☐ | ☐ |
| 31.1.2 | CockroachDB, TiDB, YugabyteDB, FoundationDB | ☐ | ☐ | ☐ |
| 31.1.3 | Dynamo, Cassandra: tunable consistency, hinted handoff, anti-entropy | ☐ | ☐ | ☐ |
| 31.1.4 | Replication: statement, WAL shipping, logical, physical | ☐ | ☐ | ☐ |
| 31.1.5 | Multi-region topologies, geo-partitioning | ☐ | ☐ | ☐ |
| 31.1.6 | CDC: Debezium, logical decoding | ☐ | ☐ | ☐ |
| 31.1.7 | Read replicas, replication lag handling | ☐ | ☐ | ☐ |
| 31.1.8 | Online resharding, rebalancing | ☐ | ☐ | ☐ |
| 31.1.9 | Backup/PITR, restore testing | ☐ | ☐ | ☐ |

### 31.2 Messaging & streaming

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 31.2.1 | Kafka internals: log segments, partitions, ISR, controller (KRaft) | ☐ | ☐ | ☐ |
| 31.2.2 | Consumer groups, offsets, rebalancing | ☐ | ☐ | ☐ |
| 31.2.3 | Delivery semantics: at-most/at-least/exactly-once | ☐ | ☐ | ☐ |
| 31.2.4 | Transactional outbox, idempotent consumers | ☐ | ☐ | ☐ |
| 31.2.5 | RabbitMQ, NATS/JetStream, Pulsar, SQS/SNS | ☐ | ☐ | ☐ |
| 31.2.6 | Stream processing: Flink, Kafka Streams, windowing, watermarks | ☐ | ☐ | ☐ |
| 31.2.7 | Event sourcing, CQRS | ☐ | ☐ | ☐ |
| 31.2.8 | Dead-letter queues, retries, poison messages | ☐ | ☐ | ☐ |
| 31.2.9 | Backpressure in pipelines | ☐ | ☐ | ☐ |

### 31.3 Caching

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 31.3.1 | Cache-aside, read-through, write-through, write-back | ☐ | ☐ | ☐ |
| 31.3.2 | Cache stampede, dogpile, request coalescing | ☐ | ☐ | ☐ |
| 31.3.3 | Cache invalidation strategies, TTL, versioned keys | ☐ | ☐ | ☐ |
| 31.3.4 | Redis Cluster, Memcached, client-side caching | ☐ | ☐ | ☐ |
| 31.3.5 | Eviction policies, memory fragmentation | ☐ | ☐ | ☐ |
| 31.3.6 | Hot key and big key handling | ☐ | ☐ | ☐ |
| 31.3.7 | CDN and browser caching layers | ☐ | ☐ | ☐ |
| 31.3.8 | Negative caching | ☐ | ☐ | ☐ |

## P32. Distributed Systems Theory

### 32.1 Foundations

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 32.1.1 | Fallacies of distributed computing | ☐ | ☐ | ☐ |
| 32.1.2 | CAP, PACELC, FLP impossibility | ☐ | ☐ | ☐ |
| 32.1.3 | Failure models: crash, omission, Byzantine | ☐ | ☐ | ☐ |
| 32.1.4 | System models: synchronous, partially synchronous, async | ☐ | ☐ | ☐ |
| 32.1.5 | Safety vs liveness | ☐ | ☐ | ☐ |
| 32.1.6 | Linearizability, sequential, causal, eventual consistency | ☐ | ☐ | ☐ |
| 32.1.7 | Session guarantees: read-your-writes, monotonic reads | ☐ | ☐ | ☐ |
| 32.1.8 | CRDTs, operational transforms | ☐ | ☐ | ☐ |
| 32.1.9 | Lamport clocks, vector clocks, HLC, TrueTime, PTP | ☐ | ☐ | ☐ |
| 32.1.10 | Happens-before | ☐ | ☐ | ☐ |
| 32.1.11 | Two Generals, quorum intersection | ☐ | ☐ | ☐ |

### 32.2 Consensus & coordination

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 32.2.1 | Paxos, Multi-Paxos, Fast Paxos | ☐ | ☐ | ☐ |
| 32.2.2 | Raft: election, log replication, membership change, snapshots | ☐ | ☐ | ☐ |
| 32.2.3 | Viewstamped Replication, ZAB | ☐ | ☐ | ☐ |
| 32.2.4 | PBFT, Tendermint, HotStuff, blockchain consensus | ☐ | ☐ | ☐ |
| 32.2.5 | Leader leases, fencing tokens | ☐ | ☐ | ☐ |
| 32.2.6 | ZooKeeper, etcd, Consul semantics | ☐ | ☐ | ☐ |
| 32.2.7 | Distributed locks, why Redlock is debated | ☐ | ☐ | ☐ |
| 32.2.8 | Gossip, SWIM, phi-accrual failure detection | ☐ | ☐ | ☐ |
| 32.2.9 | Membership and service discovery | ☐ | ☐ | ☐ |
| 32.2.10 | Atomic broadcast, total order | ☐ | ☐ | ☐ |
| 32.2.11 | Distributed snapshots (Chandy-Lamport) | ☐ | ☐ | ☐ |

## P33. Distributed Systems Patterns & Resilience

### 33.1 Patterns

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 33.1.1 | Sharding: range, hash, consistent hashing, vnodes, rendezvous | ☐ | ☐ | ☐ |
| 33.1.2 | Hotspot mitigation, split/merge | ☐ | ☐ | ☐ |
| 33.1.3 | Replication topologies: leader-follower, multi-leader, leaderless | ☐ | ☐ | ☐ |
| 33.1.4 | 2PC, 3PC, sagas, TCC | ☐ | ☐ | ☐ |
| 33.1.5 | Idempotency keys, deduplication | ☐ | ☐ | ☐ |
| 33.1.6 | Outbox, inbox patterns | ☐ | ☐ | ☐ |
| 33.1.7 | Leader election patterns | ☐ | ☐ | ☐ |
| 33.1.8 | Service discovery, client-side vs server-side LB | ☐ | ☐ | ☐ |
| 33.1.9 | Sidecar, ambassador, adapter patterns | ☐ | ☐ | ☐ |
| 33.1.10 | API gateway, BFF | ☐ | ☐ | ☐ |
| 33.1.11 | Control plane vs data plane separation | ☐ | ☐ | ☐ |
| 33.1.12 | Cell-based architecture, shuffle sharding | ☐ | ☐ | ☐ |

### 33.2 Resilience

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 33.2.1 | Timeouts, deadline propagation | ☐ | ☐ | ☐ |
| 33.2.2 | Retries with exponential backoff and jitter, retry budgets | ☐ | ☐ | ☐ |
| 33.2.3 | Circuit breakers, bulkheads | ☐ | ☐ | ☐ |
| 33.2.4 | Load shedding, admission control, priority queues | ☐ | ☐ | ☐ |
| 33.2.5 | Backpressure, flow control, queue sizing | ☐ | ☐ | ☐ |
| 33.2.6 | Hedged requests, tail-at-scale techniques | ☐ | ☐ | ☐ |
| 33.2.7 | Graceful degradation, fallbacks | ☐ | ☐ | ☐ |
| 33.2.8 | Rate limiting, quotas, fairness | ☐ | ☐ | ☐ |
| 33.2.9 | Metastable failures, retry storms, cascading failures | ☐ | ☐ | ☐ |
| 33.2.10 | Idempotent operations and exactly-once illusions | ☐ | ☐ | ☐ |
| 33.2.11 | Chaos engineering, fault injection | ☐ | ☐ | ☐ |
| 33.2.12 | Deterministic simulation testing, Jepsen | ☐ | ☐ | ☐ |

## P34. Virtualization & Hypervisors

### 34.1 Hypervisors

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 34.1.1 | Type-1 vs Type-2 | ☐ | ☐ | ☐ |
| 34.1.2 | VT-x/AMD-V, EPT/NPT, VMCS, VM exits | ☐ | ☐ | ☐ |
| 34.1.3 | KVM, QEMU, libvirt, Xen, Hyper-V, bhyve | ☐ | ☐ | ☐ |
| 34.1.4 | virtio, vhost, vhost-user, vDPA | ☐ | ☐ | ☐ |
| 34.1.5 | Device passthrough, VFIO, SR-IOV | ☐ | ☐ | ☐ |
| 34.1.6 | Paravirtualization vs full vs hardware assist | ☐ | ☐ | ☐ |
| 34.1.7 | Live migration, dirty page tracking | ☐ | ☐ | ☐ |
| 34.1.8 | Memory ballooning, overcommit, KSM | ☐ | ☐ | ☐ |
| 34.1.9 | Nested virtualization | ☐ | ☐ | ☐ |
| 34.1.10 | VM sizing, CPU pinning, NUMA topology for guests | ☐ | ☐ | ☐ |
| 34.1.11 | Confidential VMs: SEV-SNP, TDX, SGX | ☐ | ☐ | ☐ |

### 34.2 MicroVMs & sandboxes

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 34.2.1 | Firecracker, Cloud Hypervisor, crosvm | ☐ | ☐ | ☐ |
| 34.2.2 | gVisor, Kata Containers | ☐ | ☐ | ☐ |
| 34.2.3 | Snapshot/restore for fast boot | ☐ | ☐ | ☐ |
| 34.2.4 | Jailer, seccomp, cgroup confinement of VMMs | ☐ | ☐ | ☐ |
| 34.2.5 | VMM attack surface, virtio device emulation risks | ☐ | ☐ | ☐ |
| 34.2.6 | Unikernel-based isolation | ☐ | ☐ | ☐ |
| 34.2.7 | WASM sandboxes, V8 isolates | ☐ | ☐ | ☐ |

## P35. Containers & Runtimes

### 35.1 Isolation primitives

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 35.1.1 | Namespaces: pid, net, mnt, ipc, uts, user, cgroup, time | ☐ | ☐ | ☐ |
| 35.1.2 | cgroups v1 vs v2: cpu, memory, io, pids, cpuset | ☐ | ☐ | ☐ |
| 35.1.3 | Capabilities, seccomp, AppArmor/SELinux in containers | ☐ | ☐ | ☐ |
| 35.1.4 | Rootless containers, user namespace mapping | ☐ | ☐ | ☐ |
| 35.1.5 | OverlayFS, layers, copy-up, snapshotters | ☐ | ☐ | ☐ |
| 35.1.6 | OCI image and runtime specs | ☐ | ☐ | ☐ |
| 35.1.7 | runc, crun, containerd, CRI-O, Podman, Docker daemon | ☐ | ☐ | ☐ |
| 35.1.8 | Image building: Dockerfile, BuildKit, multi-stage, distroless | ☐ | ☐ | ☐ |
| 35.1.9 | Registries, content addressing, image signing | ☐ | ☐ | ☐ |
| 35.1.10 | Container networking: bridge, host, macvlan, CNI | ☐ | ☐ | ☐ |
| 35.1.11 | Resource limits pitfalls: CPU throttling, memory accounting, OOM | ☐ | ☐ | ☐ |
| 35.1.12 | Container escapes and hardening | ☐ | ☐ | ☐ |

## P36. Kubernetes & Orchestration

### 36.1 Control plane & data plane

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 36.1.1 | kube-apiserver, etcd, watch semantics, resourceVersion | ☐ | ☐ | ☐ |
| 36.1.2 | Scheduler: filter, score, preemption, affinity, taints, topology spread | ☐ | ☐ | ☐ |
| 36.1.3 | Controller manager, reconciliation loops | ☐ | ☐ | ☐ |
| 36.1.4 | Kubelet, CRI, CNI, CSI | ☐ | ☐ | ☐ |
| 36.1.5 | kube-proxy: iptables vs IPVS vs eBPF | ☐ | ☐ | ☐ |
| 36.1.6 | CoreDNS, ndots, DNS performance | ☐ | ☐ | ☐ |
| 36.1.7 | Operators, CRDs, admission webhooks, finalizers | ☐ | ☐ | ☐ |
| 36.1.8 | Workloads: Deployment, StatefulSet, DaemonSet, Job, CronJob | ☐ | ☐ | ☐ |
| 36.1.9 | HPA, VPA, KEDA, cluster autoscaler, Karpenter | ☐ | ☐ | ☐ |
| 36.1.10 | PodDisruptionBudgets, probes, graceful termination | ☐ | ☐ | ☐ |
| 36.1.11 | RBAC, ServiceAccounts, PSA, network policies | ☐ | ☐ | ☐ |
| 36.1.12 | Cilium, Calico, service mesh (Istio, Linkerd, ambient) | ☐ | ☐ | ☐ |
| 36.1.13 | Gateway API, ingress controllers | ☐ | ☐ | ☐ |
| 36.1.14 | Storage: PV/PVC, StorageClass, snapshots | ☐ | ☐ | ☐ |
| 36.1.15 | Multi-cluster, federation, upgrades, etcd backup/restore | ☐ | ☐ | ☐ |
| 36.1.16 | Alternatives: Nomad, Swarm, Mesos, systemd-based orchestration | ☐ | ☐ | ☐ |

## P37. Cloud Platforms & Infrastructure as Code

### 37.1 Cloud

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 37.1.1 | IaaS/PaaS/SaaS, serverless, FaaS cold starts | ☐ | ☐ | ☐ |
| 37.1.2 | Compute: instances, spot, bare metal, Graviton/ARM | ☐ | ☐ | ☐ |
| 37.1.3 | Storage: block, object, file; durability and consistency models | ☐ | ☐ | ☐ |
| 37.1.4 | Networking: VPC, subnets, peering, transit gateways, private link | ☐ | ☐ | ☐ |
| 37.1.5 | IAM models: roles, policies, least privilege, workload identity | ☐ | ☐ | ☐ |
| 37.1.6 | Managed databases and their hidden limits | ☐ | ☐ | ☐ |
| 37.1.7 | Load balancers, autoscaling groups | ☐ | ☐ | ☐ |
| 37.1.8 | Multi-cloud, hybrid, on-prem tradeoffs | ☐ | ☐ | ☐ |
| 37.1.9 | Region/AZ failure domains | ☐ | ☐ | ☐ |
| 37.1.10 | Cost models, egress, reserved/spot, FinOps | ☐ | ☐ | ☐ |
| 37.1.11 | Sovereignty, data residency, compliance (SOC2, ISO 27001, GDPR, DPDP) | ☐ | ☐ | ☐ |

### 37.2 IaC & config management

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 37.2.1 | Terraform/OpenTofu state, modules, drift | ☐ | ☐ | ☐ |
| 37.2.2 | Pulumi, CDK | ☐ | ☐ | ☐ |
| 37.2.3 | Ansible, Salt, Puppet, Chef, idempotency | ☐ | ☐ | ☐ |
| 37.2.4 | NixOS, declarative systems, flakes | ☐ | ☐ | ☐ |
| 37.2.5 | Packer, golden images, immutable infra | ☐ | ☐ | ☐ |
| 37.2.6 | GitOps: Argo CD, Flux | ☐ | ☐ | ☐ |
| 37.2.7 | Secrets: Vault, SOPS, sealed secrets, KMS | ☐ | ☐ | ☐ |
| 37.2.8 | Policy as code: OPA, Kyverno | ☐ | ☐ | ☐ |
| 37.2.9 | Self-hosted platforms: Forgejo, Gitea, Woodpecker, Harbor | ☐ | ☐ | ☐ |
| 37.2.10 | Bare-metal provisioning: MAAS, Tinkerbell, Ironic, PXE | ☐ | ☐ | ☐ |

## P38. Observability & Monitoring

### 38.1 Signals & stacks

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 38.1.1 | Metrics, logs, traces, profiles, events | ☐ | ☐ | ☐ |
| 38.1.2 | OpenTelemetry: SDK, collector, semantic conventions | ☐ | ☐ | ☐ |
| 38.1.3 | Prometheus: scraping, PromQL, recording rules, federation, remote write | ☐ | ☐ | ☐ |
| 38.1.4 | Grafana, Loki, Tempo, Mimir, Jaeger, Elastic stack | ☐ | ☐ | ☐ |
| 38.1.5 | Metric types: counter, gauge, histogram, summary | ☐ | ☐ | ☐ |
| 38.1.6 | Cardinality explosion and cost | ☐ | ☐ | ☐ |
| 38.1.7 | Sampling: head vs tail | ☐ | ☐ | ☐ |
| 38.1.8 | Structured logging, log levels, correlation IDs | ☐ | ☐ | ☐ |
| 38.1.9 | Alerting: symptom vs cause, burn rate, noise reduction | ☐ | ☐ | ☐ |
| 38.1.10 | USE method, RED method, golden signals | ☐ | ☐ | ☐ |
| 38.1.11 | Synthetic monitoring, blackbox probes | ☐ | ☐ | ☐ |
| 38.1.12 | Continuous profiling: Parca, Pyroscope | ☐ | ☐ | ☐ |
| 38.1.13 | Dashboards that answer questions | ☐ | ☐ | ☐ |
| 38.1.14 | Audit and security telemetry | ☐ | ☐ | ☐ |

## P39. Debugging, Tracing & Diagnostics

### 39.1 Kernel & userspace tracing

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 39.1.1 | kprobes, kretprobes, uprobes, tracepoints, USDT | ☐ | ☐ | ☐ |
| 39.1.2 | ftrace, trace-cmd, perf trace, perf record/report/stat/annotate | ☐ | ☐ | ☐ |
| 39.1.3 | eBPF: verifier, maps, helpers, CO-RE, libbpf, BTF | ☐ | ☐ | ☐ |
| 39.1.4 | bpftrace, BCC tools, Cilium Tetragon, Falco | ☐ | ☐ | ☐ |
| 39.1.5 | Flame graphs: on-CPU, off-CPU, memory, differential | ☐ | ☐ | ☐ |
| 39.1.6 | strace, ltrace, gdb, lldb, rr, delve, pwndbg | ☐ | ☐ | ☐ |
| 39.1.7 | Core dumps, minidumps, symbolization | ☐ | ☐ | ☐ |
| 39.1.8 | Heap profilers, leak detectors | ☐ | ☐ | ☐ |
| 39.1.9 | Network debugging: tcpdump, ss, ip, ethtool, mtr, nmap | ☐ | ☐ | ☐ |
| 39.1.10 | Disk debugging: iostat, iotop, blktrace, fio | ☐ | ☐ | ☐ |
| 39.1.11 | Memory debugging: vmstat, free, pmap, /proc/meminfo, smem | ☐ | ☐ | ☐ |
| 39.1.12 | CPU debugging: top, htop, pidstat, mpstat, turbostat | ☐ | ☐ | ☐ |

### 39.2 Debugging method

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 39.2.1 | Reproduce, minimize, bisect (git bisect) | ☐ | ☐ | ☐ |
| 39.2.2 | Hypothesis-driven debugging, one variable at a time | ☐ | ☐ | ☐ |
| 39.2.3 | Building tight feedback loops before theorizing | ☐ | ☐ | ☐ |
| 39.2.4 | Log vs trace vs debugger tradeoffs | ☐ | ☐ | ☐ |
| 39.2.5 | Debugging heisenbugs and timing bugs | ☐ | ☐ | ☐ |
| 39.2.6 | Debugging in production safely | ☐ | ☐ | ☐ |
| 39.2.7 | Reading kernel oops/panic and stack traces | ☐ | ☐ | ☐ |
| 39.2.8 | Postmortem debugging from artifacts | ☐ | ☐ | ☐ |
| 39.2.9 | Rubber-duck, writing the bug report | ☐ | ☐ | ☐ |
| 39.2.10 | Knowing when it is hardware (ECC, thermal, flaky cable) | ☐ | ☐ | ☐ |

## P40. Performance Engineering

### 40.1 Method & measurement

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 40.1.1 | Measure first, establish baselines | ☐ | ☐ | ☐ |
| 40.1.2 | Latency vs throughput vs utilization | ☐ | ☐ | ☐ |
| 40.1.3 | Tail latency p99/p999, jitter | ☐ | ☐ | ☐ |
| 40.1.4 | Microbenchmarks: warmup, variance, dead-code elimination, pitfalls | ☐ | ☐ | ☐ |
| 40.1.5 | Macrobenchmarks, realistic workloads, replay | ☐ | ☐ | ☐ |
| 40.1.6 | Load testing: stress, soak, spike, open vs closed loop (wrk2, k6, vegeta, fio, iperf3) | ☐ | ☐ | ☐ |
| 40.1.7 | A/B performance testing, regression detection in CI | ☐ | ☐ | ☐ |
| 40.1.8 | Profiling-guided optimization | ☐ | ☐ | ☐ |
| 40.1.9 | Performance budgets | ☐ | ☐ | ☐ |
| 40.1.10 | Capacity planning, saturation, headroom | ☐ | ☐ | ☐ |

### 40.2 Tuning

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 40.2.1 | sysctl tuning: net.*, vm.*, fs.* | ☐ | ☐ | ☐ |
| 40.2.2 | IRQ affinity, RPS/XPS, busy polling | ☐ | ☐ | ☐ |
| 40.2.3 | CPU governors, C-state tuning, turbo, isolcpus | ☐ | ☐ | ☐ |
| 40.2.4 | NUMA tuning, huge pages | ☐ | ☐ | ☐ |
| 40.2.5 | Lock contention analysis | ☐ | ☐ | ☐ |
| 40.2.6 | Allocator tuning | ☐ | ☐ | ☐ |
| 40.2.7 | GC tuning | ☐ | ☐ | ☐ |
| 40.2.8 | Batching, pipelining, coalescing | ☐ | ☐ | ☐ |
| 40.2.9 | Zero-copy design, avoiding syscalls | ☐ | ☐ | ☐ |
| 40.2.10 | Vectorization, SIMD tuning | ☐ | ☐ | ☐ |
| 40.2.11 | Compression vs CPU tradeoffs | ☐ | ☐ | ☐ |
| 40.2.12 | Storage tuning: queue depth, scheduler, mount options | ☐ | ☐ | ☐ |

## P41. Reliability, SRE & Operations

### 41.1 SRE practice

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 41.1.1 | SLI, SLO, SLA, error budgets, burn-rate alerting | ☐ | ☐ | ☐ |
| 41.1.2 | On-call design, rotation, escalation | ☐ | ☐ | ☐ |
| 41.1.3 | Incident command, severity, comms, status pages | ☐ | ☐ | ☐ |
| 41.1.4 | Runbooks and playbooks | ☐ | ☐ | ☐ |
| 41.1.5 | Blameless postmortems, RCA, 5 whys, contributing factors | ☐ | ☐ | ☐ |
| 41.1.6 | Change management, change freezes | ☐ | ☐ | ☐ |
| 41.1.7 | Deployment: blue-green, canary, rolling, feature flags, auto-rollback | ☐ | ☐ | ☐ |
| 41.1.8 | Progressive delivery, dark launches | ☐ | ☐ | ☐ |
| 41.1.9 | Toil measurement and elimination | ☐ | ☐ | ☐ |
| 41.1.10 | Capacity reviews, launch readiness reviews | ☐ | ☐ | ☐ |
| 41.1.11 | Cost engineering, FinOps | ☐ | ☐ | ☐ |

### 41.2 DR & resilience

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 41.2.1 | RTO, RPO, backup strategies, restore drills | ☐ | ☐ | ☐ |
| 41.2.2 | Multi-region active-active vs active-passive | ☐ | ☐ | ☐ |
| 41.2.3 | Failover testing, game days | ☐ | ☐ | ☐ |
| 41.2.4 | Data corruption recovery, point-in-time recovery | ☐ | ☐ | ☐ |
| 41.2.5 | Dependency mapping, blast radius | ☐ | ☐ | ☐ |
| 41.2.6 | Disaster scenarios: DNS, cert expiry, clock skew, credential leak | ☐ | ☐ | ☐ |
| 41.2.7 | Business continuity planning | ☐ | ☐ | ☐ |
| 41.2.8 | Fleet ops: patching, kernel live patching, rolling reboots | ☐ | ☐ | ☐ |
| 41.2.9 | Hardware lifecycle, spares, RMA | ☐ | ☐ | ☐ |
| 41.2.10 | Data center basics: power, cooling, racks, PDUs, UPS | ☐ | ☐ | ☐ |

## P42. CI/CD & Release Engineering

### 42.1 Pipelines

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 42.1.1 | CI design: fast feedback, caching, parallelism, flaky tests | ☐ | ☐ | ☐ |
| 42.1.2 | Runners: self-hosted, ephemeral, autoscaled | ☐ | ☐ | ☐ |
| 42.1.3 | Static analysis: linters, SAST, type checkers | ☐ | ☐ | ☐ |
| 42.1.4 | Dependency scanning, license checks | ☐ | ☐ | ☐ |
| 42.1.5 | Artifact registries, promotion across environments | ☐ | ☐ | ☐ |
| 42.1.6 | Release trains, trunk-based development, monorepo vs polyrepo | ☐ | ☐ | ☐ |
| 42.1.7 | Branching strategies, code review practice | ☐ | ☐ | ☐ |
| 42.1.8 | Database migration in pipelines | ☐ | ☐ | ☐ |
| 42.1.9 | Rollback and roll-forward policy | ☐ | ☐ | ☐ |
| 42.1.10 | Versioning, changelogs, release notes | ☐ | ☐ | ☐ |
| 42.1.11 | Reproducible builds and verification | ☐ | ☐ | ☐ |
| 42.1.12 | Developer environments: devcontainers, Nix shells | ☐ | ☐ | ☐ |

## P43. Security: OS, Application & Memory Safety

### 43.1 Isolation & hardening

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 43.1.1 | Linux capabilities, seccomp-bpf, Landlock | ☐ | ☐ | ☐ |
| 43.1.2 | SELinux, AppArmor, SMACK | ☐ | ☐ | ☐ |
| 43.1.3 | User namespaces, rootless, sandboxing (bubblewrap, firejail) | ☐ | ☐ | ☐ |
| 43.1.4 | Kernel hardening: KASLR, SMEP/SMAP, CFI, lockdown | ☐ | ☐ | ☐ |
| 43.1.5 | Auditd, eBPF-based runtime security | ☐ | ☐ | ☐ |
| 43.1.6 | SSH hardening, bastions, certificates | ☐ | ☐ | ☐ |
| 43.1.7 | Least privilege, privilege separation | ☐ | ☐ | ☐ |
| 43.1.8 | Secrets handling: env vars, files, memory scrubbing | ☐ | ☐ | ☐ |
| 43.1.9 | Patch management and CVE triage | ☐ | ☐ | ☐ |
| 43.1.10 | CIS benchmarks, STIG | ☐ | ☐ | ☐ |
| 43.1.11 | Immutable and minimal OS images | ☐ | ☐ | ☐ |

### 43.2 Memory safety & exploitation

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 43.2.1 | Stack overflow, heap overflow, use-after-free, double free | ☐ | ☐ | ☐ |
| 43.2.2 | Integer overflow, format strings, type confusion | ☐ | ☐ | ☐ |
| 43.2.3 | ROP, JOP, stack canaries, CFI, shadow stacks, W^X | ☐ | ☐ | ☐ |
| 43.2.4 | ASLR bypasses, info leaks | ☐ | ☐ | ☐ |
| 43.2.5 | Fuzzing: AFL++, libFuzzer, honggfuzz, syzkaller | ☐ | ☐ | ☐ |
| 43.2.6 | Reverse engineering: Ghidra, IDA, radare2 | ☐ | ☐ | ☐ |
| 43.2.7 | Malware analysis basics | ☐ | ☐ | ☐ |
| 43.2.8 | Web: XSS, CSRF, SQLi, SSRF, deserialization, path traversal | ☐ | ☐ | ☐ |
| 43.2.9 | OWASP Top 10, ASVS | ☐ | ☐ | ☐ |
| 43.2.10 | Race-condition exploits, TOCTOU | ☐ | ☐ | ☐ |
| 43.2.11 | Side channels in software, constant-time coding | ☐ | ☐ | ☐ |

## P44. Cryptography, PKI & Identity

### 44.1 Cryptography

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 44.1.1 | Symmetric: AES modes (GCM, CTR, XTS), ChaCha20-Poly1305 | ☐ | ☐ | ☐ |
| 44.1.2 | Hashes: SHA-2, SHA-3, BLAKE2/3 | ☐ | ☐ | ☐ |
| 44.1.3 | MACs, HMAC, AEAD | ☐ | ☐ | ☐ |
| 44.1.4 | KDFs: HKDF, PBKDF2, scrypt, Argon2 | ☐ | ☐ | ☐ |
| 44.1.5 | Asymmetric: RSA, ECC, Curve25519, Ed25519, ECDSA | ☐ | ☐ | ☐ |
| 44.1.6 | Key exchange: DH, ECDH, X25519 | ☐ | ☐ | ☐ |
| 44.1.7 | Post-quantum: ML-KEM, ML-DSA, hybrid schemes | ☐ | ☐ | ☐ |
| 44.1.8 | Randomness: CSPRNG, entropy sources, /dev/urandom, getrandom | ☐ | ☐ | ☐ |
| 44.1.9 | Nonce reuse, padding oracles, timing attacks | ☐ | ☐ | ☐ |
| 44.1.10 | Zero-knowledge proofs, MPC, homomorphic encryption basics | ☐ | ☐ | ☐ |
| 44.1.11 | Protocols: Noise, Signal, WireGuard handshake | ☐ | ☐ | ☐ |
| 44.1.12 | Crypto API misuse and safe libraries (libsodium, ring) | ☐ | ☐ | ☐ |

### 44.2 PKI & identity

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 44.2.1 | X.509, CA hierarchy, chain validation, revocation | ☐ | ☐ | ☐ |
| 44.2.2 | ACME, Let's Encrypt, cert rotation automation | ☐ | ☐ | ☐ |
| 44.2.3 | HSM, KMS, PKCS#11, YubiHSM | ☐ | ☐ | ☐ |
| 44.2.4 | TPM 2.0, key attestation | ☐ | ☐ | ☐ |
| 44.2.5 | SSH certificates, SPIFFE/SPIRE | ☐ | ☐ | ☐ |
| 44.2.6 | OAuth2/OIDC flows, PKCE, token binding | ☐ | ☐ | ☐ |
| 44.2.7 | Passkeys, WebAuthn, FIDO2 | ☐ | ☐ | ☐ |
| 44.2.8 | Kerberos, LDAP, Active Directory basics | ☐ | ☐ | ☐ |
| 44.2.9 | Zero trust architecture | ☐ | ☐ | ☐ |
| 44.2.10 | Secrets rotation, short-lived credentials | ☐ | ☐ | ☐ |

## P45. Network & Infrastructure Security

### 45.1 Defense

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 45.1.1 | Firewalls: stateful, nftables, security groups | ☐ | ☐ | ☐ |
| 45.1.2 | IDS/IPS: Suricata, Snort, Zeek | ☐ | ☐ | ☐ |
| 45.1.3 | WAF, bot mitigation, rate limiting | ☐ | ☐ | ☐ |
| 45.1.4 | VPN, bastion, jump host design | ☐ | ☐ | ☐ |
| 45.1.5 | Network segmentation, microsegmentation | ☐ | ☐ | ☐ |
| 45.1.6 | DDoS defense | ☐ | ☐ | ☐ |
| 45.1.7 | DNS security, sinkholing | ☐ | ☐ | ☐ |
| 45.1.8 | Email security | ☐ | ☐ | ☐ |
| 45.1.9 | Log integrity, SIEM, detection engineering | ☐ | ☐ | ☐ |
| 45.1.10 | Threat modeling: STRIDE, attack trees | ☐ | ☐ | ☐ |
| 45.1.11 | Honeypots, deception | ☐ | ☐ | ☐ |
| 45.1.12 | Incident response and forensics: disk, memory, network | ☐ | ☐ | ☐ |

### 45.2 Offense & disclosure

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 45.2.1 | Recon: nmap, masscan, OSINT | ☐ | ☐ | ☐ |
| 45.2.2 | Exploitation frameworks, privilege escalation | ☐ | ☐ | ☐ |
| 45.2.3 | Web app pentesting: Burp, ZAP | ☐ | ☐ | ☐ |
| 45.2.4 | Active Directory attack paths | ☐ | ☐ | ☐ |
| 45.2.5 | Cloud misconfigurations | ☐ | ☐ | ☐ |
| 45.2.6 | Wireless attacks, evil twin | ☐ | ☐ | ☐ |
| 45.2.7 | Physical security, hardware implants | ☐ | ☐ | ☐ |
| 45.2.8 | Red/blue/purple team operations | ☐ | ☐ | ☐ |
| 45.2.9 | VAPT reporting, CVSS, severity | ☐ | ☐ | ☐ |
| 45.2.10 | Responsible disclosure, CVE process, bug bounty (HackerOne), CERT-In | ☐ | ☐ | ☐ |

## P46. Testing, Correctness & Formal Methods

### 46.1 Testing

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 46.1.1 | Unit, integration, end-to-end, contract tests | ☐ | ☐ | ☐ |
| 46.1.2 | Test pyramid and its limits | ☐ | ☐ | ☐ |
| 46.1.3 | Property-based testing: QuickCheck, Hypothesis, proptest | ☐ | ☐ | ☐ |
| 46.1.4 | Fuzzing, differential testing, metamorphic testing | ☐ | ☐ | ☐ |
| 46.1.5 | Mutation testing | ☐ | ☐ | ☐ |
| 46.1.6 | Fault injection, chaos testing | ☐ | ☐ | ☐ |
| 46.1.7 | Deterministic simulation, record/replay | ☐ | ☐ | ☐ |
| 46.1.8 | Flaky test diagnosis | ☐ | ☐ | ☐ |
| 46.1.9 | Test seams, mocks vs fakes, dependency injection | ☐ | ☐ | ☐ |
| 46.1.10 | TDD red-green-refactor, tight feedback loops | ☐ | ☐ | ☐ |
| 46.1.11 | Coverage and its limits | ☐ | ☐ | ☐ |
| 46.1.12 | Hardware-in-the-loop, emulation (QEMU, Renode) | ☐ | ☐ | ☐ |
| 46.1.13 | Performance and soak tests | ☐ | ☐ | ☐ |

### 46.2 Formal methods

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 46.2.1 | Invariants, pre/postconditions, refinement | ☐ | ☐ | ☐ |
| 46.2.2 | TLA+, PlusCal, Alloy | ☐ | ☐ | ☐ |
| 46.2.3 | Model checking: SPIN, CBMC, Kani | ☐ | ☐ | ☐ |
| 46.2.4 | Theorem provers: Coq, Lean, Isabelle | ☐ | ☐ | ☐ |
| 46.2.5 | Verified systems: seL4, CompCert, CakeML | ☐ | ☐ | ☐ |
| 46.2.6 | Static analysis, abstract interpretation | ☐ | ☐ | ☐ |
| 46.2.7 | Type systems as proofs, session types | ☐ | ☐ | ☐ |
| 46.2.8 | Concurrency verification: loom, shuttle | ☐ | ☐ | ☐ |
| 46.2.9 | Contracts and specification languages | ☐ | ☐ | ☐ |
| 46.2.10 | Proving protocols (Raft, Paxos) correct | ☐ | ☐ | ☐ |

## P47. Architecture, API & Protocol Design

### 47.1 Design

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 47.1.1 | Requirements, constraints, non-goals, tradeoff analysis | ☐ | ☐ | ☐ |
| 47.1.2 | ADRs, design docs, RFCs | ☐ | ☐ | ☐ |
| 47.1.3 | Monolith vs modular monolith vs microservices | ☐ | ☐ | ☐ |
| 47.1.4 | Domain-driven design, bounded contexts | ☐ | ☐ | ☐ |
| 47.1.5 | Event-driven, CQRS, event sourcing, actor model | ☐ | ☐ | ☐ |
| 47.1.6 | Layering, ports and adapters, hexagonal | ☐ | ☐ | ☐ |
| 47.1.7 | API design: REST, gRPC, GraphQL, versioning, pagination, errors | ☐ | ☐ | ☐ |
| 47.1.8 | Serialization: Protobuf, FlatBuffers, Cap'n Proto, MessagePack, CBOR, JSON, Avro | ☐ | ☐ | ☐ |
| 47.1.9 | Schema evolution, compatibility rules | ☐ | ☐ | ☐ |
| 47.1.10 | Binary protocol design: framing, versioning, length prefixes, endianness | ☐ | ☐ | ☐ |
| 47.1.11 | Idempotency, ordering, delivery guarantees | ☐ | ☐ | ☐ |
| 47.1.12 | Multi-tenancy, isolation models | ☐ | ☐ | ☐ |
| 47.1.13 | Plugin and extension architectures | ☐ | ☐ | ☐ |
| 47.1.14 | Configuration design, feature flags | ☐ | ☐ | ☐ |
| 47.1.15 | Backward compatibility, deprecation policy | ☐ | ☐ | ☐ |
| 47.1.16 | Data modeling and ownership | ☐ | ☐ | ☐ |
| 47.1.17 | Build vs buy vs adopt open source | ☐ | ☐ | ☐ |

## P48. Software Engineering Fundamentals & Design

### 48.1 Paradigms & design

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 48.1.1 | Procedural, OOP, functional, logic, dataflow, reactive paradigms | ☐ | ☐ | ☐ |
| 48.1.2 | OOP: encapsulation, inheritance, polymorphism, composition over inheritance | ☐ | ☐ | ☐ |
| 48.1.3 | SOLID principles, DRY, KISS, YAGNI, Law of Demeter | ☐ | ☐ | ☐ |
| 48.1.4 | Design patterns: creational, structural, behavioral (GoF) | ☐ | ☐ | ☐ |
| 48.1.5 | Concurrency patterns: producer-consumer, thread pool, pub/sub, reactor | ☐ | ☐ | ☐ |
| 48.1.6 | Functional programming: pure functions, immutability, higher-order functions, monads, algebraic data types | ☐ | ☐ | ☐ |
| 48.1.7 | Type systems: static vs dynamic, generics, traits/interfaces, variance, null safety | ☐ | ☐ | ☐ |
| 48.1.8 | Error handling models: exceptions, Result/Option, error codes, panics | ☐ | ☐ | ☐ |
| 48.1.9 | State management and side-effect isolation | ☐ | ☐ | ☐ |
| 48.1.10 | Dependency injection, inversion of control | ☐ | ☐ | ☐ |
| 48.1.11 | Domain modeling, value objects, entities, aggregates | ☐ | ☐ | ☐ |

### 48.2 Code quality & maintenance

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 48.2.1 | Naming, readability, small functions, cohesion and coupling | ☐ | ☐ | ☐ |
| 48.2.2 | Refactoring techniques and code smells | ☐ | ☐ | ☐ |
| 48.2.3 | Technical debt: identifying, measuring, paying down | ☐ | ☐ | ☐ |
| 48.2.4 | Static analysis, linters, formatters, type checkers | ☐ | ☐ | ☐ |
| 48.2.5 | Code review practice and review checklists | ☐ | ☐ | ☐ |
| 48.2.6 | Dependency management, upgrades, deprecation handling | ☐ | ☐ | ☐ |
| 48.2.7 | Logging, configuration, and feature-flag design in code | ☐ | ☐ | ☐ |
| 48.2.8 | Legacy code: characterization tests, strangler pattern | ☐ | ☐ | ☐ |
| 48.2.9 | Documentation in code: comments, docstrings, examples | ☐ | ☐ | ☐ |
| 48.2.10 | API ergonomics and library design for other developers | ☐ | ☐ | ☐ |
| 48.2.11 | Monorepo vs polyrepo code organization, module boundaries | ☐ | ☐ | ☐ |
| 48.2.12 | Memory/resource management at app level: RAII, defer, using, closing handles | ☐ | ☐ | ☐ |

## P49. Backend & Web Application Development

### 49.1 Server-side fundamentals

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 49.1.1 | HTTP server internals: accept loop, thread/event models, keep-alive | ☐ | ☐ | ☐ |
| 49.1.2 | Routing, middleware chains, request/response lifecycle | ☐ | ☐ | ☐ |
| 49.1.3 | Frameworks: Express/Fastify, Django/Flask/FastAPI, Spring, Rails, Laravel, Gin/Echo/Fiber, Axum/Actix | ☐ | ☐ | ☐ |
| 49.1.4 | Request validation, serialization, error responses | ☐ | ☐ | ☐ |
| 49.1.5 | Sessions, cookies, JWT, refresh tokens, CSRF defenses | ☐ | ☐ | ☐ |
| 49.1.6 | Authentication flows: password, magic link, OAuth2/OIDC, SSO, MFA | ☐ | ☐ | ☐ |
| 49.1.7 | Authorization models: RBAC, ABAC, ReBAC, policy engines | ☐ | ☐ | ☐ |
| 49.1.8 | File uploads, multipart, streaming, presigned URLs | ☐ | ☐ | ☐ |
| 49.1.9 | Pagination: offset, cursor, keyset | ☐ | ☐ | ☐ |
| 49.1.10 | Background jobs, task queues, schedulers, cron, retries (Sidekiq, Celery, Temporal, BullMQ) | ☐ | ☐ | ☐ |
| 49.1.11 | WebSockets, SSE, real-time fan-out | ☐ | ☐ | ☐ |
| 49.1.12 | Webhooks: signing, retries, idempotency | ☐ | ☐ | ☐ |
| 49.1.13 | Email/SMS/push integration, deliverability | ☐ | ☐ | ☐ |
| 49.1.14 | Templating, server-side rendering | ☐ | ☐ | ☐ |
| 49.1.15 | Graceful shutdown, health checks, readiness, 12-factor apps | ☐ | ☐ | ☐ |
| 49.1.16 | API versioning, OpenAPI/Swagger, SDK generation, contract testing | ☐ | ☐ | ☐ |
| 49.1.17 | Rate limiting, quotas, abuse prevention at app level | ☐ | ☐ | ☐ |

### 49.2 App data layer & integration

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 49.2.1 | ORMs vs query builders vs raw SQL, N+1 queries | ☐ | ☐ | ☐ |
| 49.2.2 | Migrations, zero-downtime schema changes, expand/contract | ☐ | ☐ | ☐ |
| 49.2.3 | Connection pooling, pool sizing, pgbouncer | ☐ | ☐ | ☐ |
| 49.2.4 | Transactions in app code, isolation pitfalls, optimistic locking | ☐ | ☐ | ☐ |
| 49.2.5 | Soft deletes, audit trails, history tables | ☐ | ☐ | ☐ |
| 49.2.6 | Multi-tenancy: shared schema, schema-per-tenant, DB-per-tenant | ☐ | ☐ | ☐ |
| 49.2.7 | Caching at app level: memoization, HTTP caching, fragment caching | ☐ | ☐ | ☐ |
| 49.2.8 | Search integration: Elasticsearch/Meilisearch/Postgres FTS | ☐ | ☐ | ☐ |
| 49.2.9 | Payment gateway integration, idempotency, reconciliation | ☐ | ☐ | ☐ |
| 49.2.10 | Third-party API clients: timeouts, retries, circuit breaking, quotas | ☐ | ☐ | ☐ |
| 49.2.11 | Object storage integration, CDN, image processing pipelines | ☐ | ☐ | ☐ |
| 49.2.12 | Internationalization and localization, time zones, currencies | ☐ | ☐ | ☐ |
| 49.2.13 | Config and secrets in apps, environment parity | ☐ | ☐ | ☐ |
| 49.2.14 | Error tracking, structured logs, tracing in app code (Sentry, OpenTelemetry) | ☐ | ☐ | ☐ |

## P50. Frontend & Browser Internals

### 50.1 Browser platform

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 50.1.1 | HTML, semantic markup, forms, accessibility tree | ☐ | ☐ | ☐ |
| 50.1.2 | CSS: cascade, specificity, box model, flexbox, grid, container queries, custom properties | ☐ | ☐ | ☐ |
| 50.1.3 | JavaScript: event loop, microtasks, closures, prototypes, modules, promises, async/await | ☐ | ☐ | ☐ |
| 50.1.4 | DOM and CSSOM, style recalculation, layout, paint, compositing, layers | ☐ | ☐ | ☐ |
| 50.1.5 | Rendering pipeline and jank: reflow, repaint, GPU compositing, frame budget | ☐ | ☐ | ☐ |
| 50.1.6 | Web APIs: fetch, storage, IndexedDB, Cache API, WebSockets, WebRTC, Web Workers, Service Workers | ☐ | ☐ | ☐ |
| 50.1.7 | Progressive web apps, offline-first, installability, push | ☐ | ☐ | ☐ |
| 50.1.8 | WebAssembly, WebGL, WebGPU, canvas | ☐ | ☐ | ☐ |
| 50.1.9 | Browser security: same-origin policy, CORS, CSP, cookies SameSite, sandboxing, Trusted Types | ☐ | ☐ | ☐ |
| 50.1.10 | Browser engines: Blink, Gecko, WebKit; process model, site isolation | ☐ | ☐ | ☐ |
| 50.1.11 | Web performance: Core Web Vitals (LCP, INP, CLS), critical rendering path, resource hints, lazy loading | ☐ | ☐ | ☐ |
| 50.1.12 | DevTools: network, performance, memory, coverage profiling | ☐ | ☐ | ☐ |

### 50.2 Frameworks & tooling

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 50.2.1 | TypeScript: structural typing, generics, narrowing, declaration files | ☐ | ☐ | ☐ |
| 50.2.2 | React: components, hooks, reconciliation, concurrent rendering, state patterns | ☐ | ☐ | ☐ |
| 50.2.3 | Vue, Svelte, Solid, Angular: reactivity models compared | ☐ | ☐ | ☐ |
| 50.2.4 | State management: Redux, Zustand, signals, server state (TanStack Query) | ☐ | ☐ | ☐ |
| 50.2.5 | Routing, SSR, SSG, ISR, islands, streaming, hydration (Next, Nuxt, Astro, Remix, SvelteKit) | ☐ | ☐ | ☐ |
| 50.2.6 | Bundlers: Vite, webpack, esbuild, Rollup; tree shaking, code splitting | ☐ | ☐ | ☐ |
| 50.2.7 | Styling: CSS modules, Tailwind, CSS-in-JS tradeoffs, design tokens | ☐ | ☐ | ☐ |
| 50.2.8 | Component libraries and design systems | ☐ | ☐ | ☐ |
| 50.2.9 | Forms, validation, optimistic updates | ☐ | ☐ | ☐ |
| 50.2.10 | Accessibility: ARIA, keyboard navigation, focus management, WCAG | ☐ | ☐ | ☐ |
| 50.2.11 | Frontend testing: unit, component, e2e (Playwright, Cypress), visual regression | ☐ | ☐ | ☐ |
| 50.2.12 | Frontend security: XSS, dependency risks, supply chain, CSP | ☐ | ☐ | ☐ |
| 50.2.13 | Micro-frontends, module federation | ☐ | ☐ | ☐ |
| 50.2.14 | Frontend observability: RUM, error tracking, session replay | ☐ | ☐ | ☐ |

## P51. Mobile & Desktop Applications

### 51.1 Mobile

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 51.1.1 | Android: activities, fragments, lifecycle, intents, services, Binder, permissions | ☐ | ☐ | ☐ |
| 51.1.2 | Android UI: Jetpack Compose, Views, ViewModel, Room, WorkManager, Kotlin coroutines | ☐ | ☐ | ☐ |
| 51.1.3 | iOS: UIKit, SwiftUI, app lifecycle, Swift concurrency, Core Data, entitlements | ☐ | ☐ | ☐ |
| 51.1.4 | Background execution limits, battery, doze, push notifications (FCM, APNs) | ☐ | ☐ | ☐ |
| 51.1.5 | Cross-platform: Flutter, React Native, Kotlin Multiplatform, Capacitor tradeoffs | ☐ | ☐ | ☐ |
| 51.1.6 | Offline-first design, local DB, sync, conflict resolution | ☐ | ☐ | ☐ |
| 51.1.7 | Mobile networking: flaky links, retries, caching, binary protocols | ☐ | ☐ | ☐ |
| 51.1.8 | App signing, store review, release tracks, staged rollouts, deep links | ☐ | ☐ | ☐ |
| 51.1.9 | Mobile security: keystore/keychain, certificate pinning, jailbreak/root detection, obfuscation | ☐ | ☐ | ☐ |
| 51.1.10 | Mobile performance: startup time, memory, jank, app size | ☐ | ☐ | ☐ |
| 51.1.11 | Sensors, camera, location, BLE from apps | ☐ | ☐ | ☐ |
| 51.1.12 | Crash reporting, analytics, remote config, A/B testing | ☐ | ☐ | ☐ |

### 51.2 Desktop & GUI

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 51.2.1 | GUI event loops, widgets, layout engines, retained vs immediate mode | ☐ | ☐ | ☐ |
| 51.2.2 | Electron, Tauri, Qt, GTK, WinUI/WPF, Cocoa, Dear ImGui | ☐ | ☐ | ☐ |
| 51.2.3 | Native vs web-view tradeoffs, memory and startup cost | ☐ | ☐ | ☐ |
| 51.2.4 | Windowing and input: Wayland, X11, Win32 messages, IME, high-DPI | ☐ | ☐ | ☐ |
| 51.2.5 | Auto-update, installers, code signing, notarization | ☐ | ☐ | ☐ |
| 51.2.6 | Packaging: MSI, DMG, deb/rpm, Flatpak, AppImage | ☐ | ☐ | ☐ |
| 51.2.7 | Accessibility APIs: AT-SPI, UIA, NSAccessibility | ☐ | ☐ | ☐ |
| 51.2.8 | Plugin architectures and scripting embedding | ☐ | ☐ | ☐ |
| 51.2.9 | Crash dumps and telemetry for desktop apps | ☐ | ☐ | ☐ |
| 51.2.10 | CLI and TUI design: argument parsing, exit codes, pipes, ncurses, ratatui | ☐ | ☐ | ☐ |

## P52. Graphics, Audio, Video & Game Systems

### 52.1 Graphics & display

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 52.1.1 | Rasterization vs ray tracing, graphics pipeline stages | ☐ | ☐ | ☐ |
| 52.1.2 | Shaders: vertex, fragment, compute; GLSL, HLSL, WGSL, SPIR-V | ☐ | ☐ | ☐ |
| 52.1.3 | Vulkan, Metal, DirectX 12, OpenGL, WebGPU concepts | ☐ | ☐ | ☐ |
| 52.1.4 | Textures, mipmaps, framebuffers, depth/stencil, MSAA | ☐ | ☐ | ☐ |
| 52.1.5 | Color spaces, gamma, HDR, ICC | ☐ | ☐ | ☐ |
| 52.1.6 | Linux display stack: DRM/KMS, GBM, Mesa, Wayland compositors, X11 | ☐ | ☐ | ☐ |
| 52.1.7 | Font rendering: glyphs, shaping (HarfBuzz), hinting, subpixel | ☐ | ☐ | ☐ |
| 52.1.8 | Image formats: PNG, JPEG, WebP, AVIF, decoding costs | ☐ | ☐ | ☐ |
| 52.1.9 | 2D vector graphics, SVG, Skia, Cairo | ☐ | ☐ | ☐ |
| 52.1.10 | GPU debugging: RenderDoc, Nsight | ☐ | ☐ | ☐ |

### 52.2 Audio, video & games

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 52.2.1 | Audio fundamentals: PCM, sample rate, bit depth, latency, buffers, xruns | ☐ | ☐ | ☐ |
| 52.2.2 | Audio stacks: ALSA, PulseAudio, PipeWire, JACK, CoreAudio, WASAPI | ☐ | ☐ | ☐ |
| 52.2.3 | Codecs: Opus, AAC, FLAC, MP3 | ☐ | ☐ | ☐ |
| 52.2.4 | Video fundamentals: frames, GOP, I/P/B frames, bitrate control | ☐ | ☐ | ☐ |
| 52.2.5 | Codecs: H.264, H.265, VP9, AV1; hardware decode/encode (VAAPI, NVENC) | ☐ | ☐ | ☐ |
| 52.2.6 | Containers: MP4, MKV, WebM, MPEG-TS | ☐ | ☐ | ☐ |
| 52.2.7 | Streaming: HLS, DASH, RTMP, SRT, WebRTC, adaptive bitrate | ☐ | ☐ | ☐ |
| 52.2.8 | FFmpeg and GStreamer pipelines | ☐ | ☐ | ☐ |
| 52.2.9 | Game loop, fixed vs variable timestep, ECS, scene graphs | ☐ | ☐ | ☐ |
| 52.2.10 | Physics engines, collision detection | ☐ | ☐ | ☐ |
| 52.2.11 | Game networking: client prediction, lag compensation, rollback netcode | ☐ | ☐ | ☐ |
| 52.2.12 | Game engines: Unity, Unreal, Godot, Bevy | ☐ | ☐ | ☐ |

## P53. Application Security & Privacy Engineering

### 53.1 Secure application design

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 53.1.1 | Authentication vs authorization separation, session management pitfalls | ☐ | ☐ | ☐ |
| 53.1.2 | Password storage, credential stuffing defenses, account recovery flows | ☐ | ☐ | ☐ |
| 53.1.3 | Secure headers: CSP, HSTS, X-Frame-Options, Referrer-Policy | ☐ | ☐ | ☐ |
| 53.1.4 | Input validation, output encoding, parameterized queries | ☐ | ☐ | ☐ |
| 53.1.5 | Insecure direct object references, broken access control, mass assignment | ☐ | ☐ | ☐ |
| 53.1.6 | SSRF, XXE, deserialization, prototype pollution, template injection | ☐ | ☐ | ☐ |
| 53.1.7 | API security: auth schemes, scopes, token leakage, GraphQL abuse | ☐ | ☐ | ☐ |
| 53.1.8 | Tenant isolation and data segregation | ☐ | ☐ | ☐ |
| 53.1.9 | Secrets in code, CI, and logs | ☐ | ☐ | ☐ |
| 53.1.10 | Dependency and supply-chain risk in app ecosystems (npm, PyPI, crates) | ☐ | ☐ | ☐ |
| 53.1.11 | Secure SDLC: threat modeling, security reviews, SAST/DAST in pipeline | ☐ | ☐ | ☐ |
| 53.1.12 | Audit logging for sensitive actions | ☐ | ☐ | ☐ |

### 53.2 Privacy & compliance

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 53.2.1 | PII classification, data minimization, retention, deletion | ☐ | ☐ | ☐ |
| 53.2.2 | GDPR, India DPDP Act, CCPA concepts | ☐ | ☐ | ☐ |
| 53.2.3 | Consent management, cookie law basics | ☐ | ☐ | ☐ |
| 53.2.4 | Encryption at rest and in transit, field-level encryption, tokenization | ☐ | ☐ | ☐ |
| 53.2.5 | PCI DSS basics for payment handling | ☐ | ☐ | ☐ |
| 53.2.6 | Data subject requests, export and erase flows | ☐ | ☐ | ☐ |
| 53.2.7 | Anonymization, pseudonymization, differential privacy basics | ☐ | ☐ | ☐ |
| 53.2.8 | Compliance frameworks: SOC 2, ISO 27001, HIPAA basics | ☐ | ☐ | ☐ |
| 53.2.9 | Breach response and notification obligations | ☐ | ☐ | ☐ |

## P54. Domain Application Systems & Product Patterns

### 54.1 Common product systems

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 54.1.1 | Payments and ledgers: double-entry accounting, idempotency, settlement, reconciliation, UPI/card/wallet flows | ☐ | ☐ | ☐ |
| 54.1.2 | E-commerce: catalog, cart, inventory reservation, orders, fulfillment, returns | ☐ | ☐ | ☐ |
| 54.1.3 | Marketplaces and multi-vendor platforms: commissions, payouts, disputes | ☐ | ☐ | ☐ |
| 54.1.4 | Ride-hailing and dispatch: geospatial indexing, matching, ETA, surge pricing | ☐ | ☐ | ☐ |
| 54.1.5 | Messaging and chat: presence, fan-out, delivery receipts, ordering, end-to-end encryption | ☐ | ☐ | ☐ |
| 54.1.6 | Social feeds: fan-out on write vs read, ranking, timelines | ☐ | ☐ | ☐ |
| 54.1.7 | Notifications: channels, preferences, batching, dedup | ☐ | ☐ | ☐ |
| 54.1.8 | Real-time collaboration: CRDTs, operational transforms, presence | ☐ | ☐ | ☐ |
| 54.1.9 | Search and recommendation systems: indexing, ranking, personalization | ☐ | ☐ | ☐ |
| 54.1.10 | Media platforms: upload, transcoding, CDN delivery, DRM | ☐ | ☐ | ☐ |
| 54.1.11 | SaaS: multi-tenancy, subscriptions, metering, billing, entitlements | ☐ | ☐ | ☐ |
| 54.1.12 | Booking and scheduling systems: availability, double-booking prevention | ☐ | ☐ | ☐ |
| 54.1.13 | Workflow and approval engines, state machines, BPMN | ☐ | ☐ | ☐ |
| 54.1.14 | ERP/CRM/HRMS fundamentals, accounting basics | ☐ | ☐ | ☐ |
| 54.1.15 | Healthcare and gov systems: HL7/FHIR, e-KYC, Aadhaar-style identity flows | ☐ | ☐ | ☐ |
| 54.1.16 | Maps and GIS: tiles, routing, geocoding, spatial queries | ☐ | ☐ | ☐ |
| 54.1.17 | Analytics products: event tracking, funnels, cohorts, dashboards | ☐ | ☐ | ☐ |

## P55. Software Process, Product & Team Engineering

### 55.1 Process

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 55.1.1 | SDLC models: waterfall, iterative, Agile, Scrum, Kanban, Shape Up | ☐ | ☐ | ☐ |
| 55.1.2 | Requirements: user stories, acceptance criteria, specs, PRDs | ☐ | ☐ | ☐ |
| 55.1.3 | Estimation, roadmapping, scope control, MVP definition | ☐ | ☐ | ☐ |
| 55.1.4 | Prioritization frameworks, tradeoffs between speed and quality | ☐ | ☐ | ☐ |
| 55.1.5 | Release management, versioning, changelogs, deprecation communication | ☐ | ☐ | ☐ |
| 55.1.6 | DORA metrics, engineering metrics and their misuse | ☐ | ☐ | ☐ |
| 55.1.7 | Documentation strategy: READMEs, API docs, ADRs, runbooks | ☐ | ☐ | ☐ |
| 55.1.8 | Onboarding, knowledge sharing, bus factor | ☐ | ☐ | ☐ |
| 55.1.9 | Hiring, interviewing, and team structure basics | ☐ | ☐ | ☐ |
| 55.1.10 | Product thinking: users, metrics, experiments, A/B testing | ☐ | ☐ | ☐ |
| 55.1.11 | Contracts, SLAs, and scoping for client work | ☐ | ☐ | ☐ |
| 55.1.12 | Open-source project management: issues, releases, governance | ☐ | ☐ | ☐ |

### 55.2 Automation & integration

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 55.2.1 | CLI tool design, scripting, task automation | ☐ | ☐ | ☐ |
| 55.2.2 | API integration glue: webhooks, polling, ETL scripts | ☐ | ☐ | ☐ |
| 55.2.3 | Browser automation: Playwright, Puppeteer, Selenium | ☐ | ☐ | ☐ |
| 55.2.4 | Scraping, robots.txt, legal and ethical limits | ☐ | ☐ | ☐ |
| 55.2.5 | Low-code/no-code and workflow tools (n8n, Zapier-style) | ☐ | ☐ | ☐ |
| 55.2.6 | RPA basics, desktop automation | ☐ | ☐ | ☐ |
| 55.2.7 | Cron, schedulers, workflow orchestration | ☐ | ☐ | ☐ |
| 55.2.8 | ChatOps, bots, Slack/Discord/Telegram integrations | ☐ | ☐ | ☐ |

## P56. Data Engineering, ML Systems & AI Infrastructure

### 56.1 Data platforms

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 56.1.1 | ETL/ELT, batch vs stream | ☐ | ☐ | ☐ |
| 56.1.2 | Lakehouse: Parquet, Iceberg, Delta, Hudi | ☐ | ☐ | ☐ |
| 56.1.3 | Spark, Flink, Beam, Trino | ☐ | ☐ | ☐ |
| 56.1.4 | Orchestration: Airflow, Dagster, Temporal | ☐ | ☐ | ☐ |
| 56.1.5 | Data quality, lineage, schema registry | ☐ | ☐ | ☐ |
| 56.1.6 | Warehouses: BigQuery, Snowflake, ClickHouse | ☐ | ☐ | ☐ |
| 56.1.7 | Feature stores | ☐ | ☐ | ☐ |

### 56.2 ML/AI systems

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 56.2.1 | Training loop, backprop, optimizers, mixed precision | ☐ | ☐ | ☐ |
| 56.2.2 | Distributed training: data/tensor/pipeline parallelism, ZeRO, FSDP | ☐ | ☐ | ☐ |
| 56.2.3 | Inference serving: batching, KV cache, paged attention, quantization (INT8/4), speculative decoding | ☐ | ☐ | ☐ |
| 56.2.4 | Inference engines: vLLM, llama.cpp, TensorRT, ONNX Runtime, GGUF | ☐ | ☐ | ☐ |
| 56.2.5 | Model formats and tokenizers | ☐ | ☐ | ☐ |
| 56.2.6 | Fine-tuning: LoRA, QLoRA, PEFT | ☐ | ☐ | ☐ |
| 56.2.7 | RAG architecture, embeddings, vector search, reranking | ☐ | ☐ | ☐ |
| 56.2.8 | Evaluation, benchmarks, regression suites | ☐ | ☐ | ☐ |
| 56.2.9 | GPU cluster ops, scheduling, failure handling | ☐ | ☐ | ☐ |
| 56.2.10 | Edge inference on small devices, memory budgets | ☐ | ☐ | ☐ |
| 56.2.11 | MLOps: registry, versioning, drift monitoring | ☐ | ☐ | ☐ |
| 56.2.12 | Safety, guardrails, prompt injection defenses | ☐ | ☐ | ☐ |

## P57. Specialized & Safety-Critical Domains

### 57.1 Real-time & critical

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 57.1.1 | Hard vs soft real-time, determinism, jitter budgets | ☐ | ☐ | ☐ |
| 57.1.2 | PREEMPT_RT, Xenomai, bare-metal control loops | ☐ | ☐ | ☐ |
| 57.1.3 | DO-178C, ISO 26262, IEC 61508, MISRA C | ☐ | ☐ | ☐ |
| 57.1.4 | Fault tolerance: TMR, lockstep cores, watchdog design | ☐ | ☐ | ☐ |
| 57.1.5 | Radiation effects, SEU, ECC and scrubbing, rad-hard parts | ☐ | ☐ | ☐ |
| 57.1.6 | Avionics/space buses: MIL-STD-1553, SpaceWire, CCSDS | ☐ | ☐ | ☐ |
| 57.1.7 | Automotive: AUTOSAR, CAN, OTA, functional safety | ☐ | ☐ | ☐ |
| 57.1.8 | Medical device software constraints | ☐ | ☐ | ☐ |
| 57.1.9 | Industrial control: PLC, SCADA, IEC 61131 | ☐ | ☐ | ☐ |

### 57.2 HPC & scientific

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 57.2.1 | MPI, OpenMP, SLURM, job scheduling | ☐ | ☐ | ☐ |
| 57.2.2 | Parallel file systems, burst buffers | ☐ | ☐ | ☐ |
| 57.2.3 | Numerical stability, BLAS/LAPACK | ☐ | ☐ | ☐ |
| 57.2.4 | Interconnect topologies, collective communication | ☐ | ☐ | ☐ |
| 57.2.5 | Checkpoint/restart | ☐ | ☐ | ☐ |
| 57.2.6 | Quantum computing basics: qubits, gates, noise, Qiskit | ☐ | ☐ | ☐ |
| 57.2.7 | Neuromorphic and brain-inspired computing basics | ☐ | ☐ | ☐ |

## P58. Mathematics & CS Theory Foundations

### 58.1 Math

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 58.1.1 | Discrete math, logic, proofs, induction | ☐ | ☐ | ☐ |
| 58.1.2 | Combinatorics, probability, expectation, variance | ☐ | ☐ | ☐ |
| 58.1.3 | Statistics: distributions, hypothesis testing, Bayesian reasoning | ☐ | ☐ | ☐ |
| 58.1.4 | Linear algebra: matrices, eigenvectors, SVD | ☐ | ☐ | ☐ |
| 58.1.5 | Calculus, gradients, optimization | ☐ | ☐ | ☐ |
| 58.1.6 | Information theory: entropy, mutual information, coding theorems | ☐ | ☐ | ☐ |
| 58.1.7 | Number theory, modular arithmetic, finite fields | ☐ | ☐ | ☐ |
| 58.1.8 | Graph theory | ☐ | ☐ | ☐ |
| 58.1.9 | Queueing and Markov chains | ☐ | ☐ | ☐ |
| 58.1.10 | Control theory basics, stability, feedback | ☐ | ☐ | ☐ |

### 58.2 CS theory

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 58.2.1 | Automata, regular languages, context-free grammars | ☐ | ☐ | ☐ |
| 58.2.2 | Computability, halting problem | ☐ | ☐ | ☐ |
| 58.2.3 | Complexity classes: P, NP, PSPACE | ☐ | ☐ | ☐ |
| 58.2.4 | Lambda calculus, type theory | ☐ | ☐ | ☐ |
| 58.2.5 | Distributed computing theory | ☐ | ☐ | ☐ |
| 58.2.6 | Cryptographic assumptions | ☐ | ☐ | ☐ |
| 58.2.7 | Algorithmic game theory basics | ☐ | ☐ | ☐ |

## P59. Linux Administration, Shell & Daily Tooling

### 59.1 Administration

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 59.1.1 | systemd units, timers, journald, cgroups integration | ☐ | ☐ | ☐ |
| 59.1.2 | Package managers and repositories | ☐ | ☐ | ☐ |
| 59.1.3 | User/group management, PAM, sudo | ☐ | ☐ | ☐ |
| 59.1.4 | Networking config: NetworkManager, systemd-networkd, netplan, nmcli | ☐ | ☐ | ☐ |
| 59.1.5 | Disks: fdisk, parted, mkfs, mount, fstab, LVM tasks | ☐ | ☐ | ☐ |
| 59.1.6 | Cron, at, scheduled jobs | ☐ | ☐ | ☐ |
| 59.1.7 | Logging: rsyslog, journald, logrotate | ☐ | ☐ | ☐ |
| 59.1.8 | Time sync: chrony, ntpd | ☐ | ☐ | ☐ |
| 59.1.9 | Kernel parameters, modules, boot parameters | ☐ | ☐ | ☐ |
| 59.1.10 | Performance triage checklist (60-second analysis) | ☐ | ☐ | ☐ |
| 59.1.11 | Backup and restore tools | ☐ | ☐ | ☐ |
| 59.1.12 | Remote administration, tmux/screen, ssh config, mosh | ☐ | ☐ | ☐ |

### 59.2 Shell & tools

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 59.2.1 | Bash/Zsh scripting, quoting rules, traps | ☐ | ☐ | ☐ |
| 59.2.2 | coreutils, find, xargs, sed, awk, grep, jq, yq | ☐ | ☐ | ☐ |
| 59.2.3 | Pipes, redirections, process substitution | ☐ | ☐ | ☐ |
| 59.2.4 | Git: internals, rebase, bisect, worktrees, hooks, submodules | ☐ | ☐ | ☐ |
| 59.2.5 | Vim/Neovim/Emacs or equivalent proficiency | ☐ | ☐ | ☐ |
| 59.2.6 | Makefiles, task runners | ☐ | ☐ | ☐ |
| 59.2.7 | Regex, PCRE vs RE2 | ☐ | ☐ | ☐ |
| 59.2.8 | Terminal multiplexing, dotfiles | ☐ | ☐ | ☐ |
| 59.2.9 | Python/Go/Rust for glue tooling | ☐ | ☐ | ☐ |
| 59.2.10 | Reading man pages, RFCs, datasheets, kernel docs | ☐ | ☐ | ☐ |

## P60. Time, Text, Encoding & Data Formats

### 60.1 Fundamentals

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 60.1.1 | Clocks: monotonic vs realtime, TSC, HPET, vDSO clock_gettime | ☐ | ☐ | ☐ |
| 60.1.2 | NTP, PTP, leap seconds, clock skew handling | ☐ | ☐ | ☐ |
| 60.1.3 | Time zones, DST, tzdata, calendars | ☐ | ☐ | ☐ |
| 60.1.4 | Unicode, UTF-8/16/32, normalization, grapheme clusters | ☐ | ☐ | ☐ |
| 60.1.5 | Text collation, locale pitfalls, case folding | ☐ | ☐ | ☐ |
| 60.1.6 | Floating-point money pitfalls, decimal types | ☐ | ☐ | ☐ |
| 60.1.7 | Binary formats and hex reading skills | ☐ | ☐ | ☐ |
| 60.1.8 | Endianness, alignment, padding, packed structs | ☐ | ☐ | ☐ |
| 60.1.9 | Regex engines and ReDoS | ☐ | ☐ | ☐ |
| 60.1.10 | Date/time and numeric edge cases in serialization | ☐ | ☐ | ☐ |

## P61. Engineering Practice, Communication & Career

### 61.1 Practice

| # | Topic | G | Y | R |
|---|---|:-:|:-:|:-:|
| 61.1.1 | Reading large codebases and OSS source | ☐ | ☐ | ☐ |
| 61.1.2 | Writing design docs, RFCs, ADRs, runbooks | ☐ | ☐ | ☐ |
| 61.1.3 | Technical writing and documentation | ☐ | ☐ | ☐ |
| 61.1.4 | Estimation, planning, scoping, risk | ☐ | ☐ | ☐ |
| 61.1.5 | Code review craft | ☐ | ☐ | ☐ |
| 61.1.6 | Mentoring and teaching | ☐ | ☐ | ☐ |
| 61.1.7 | Open-source contribution workflow, maintainership | ☐ | ☐ | ☐ |
| 61.1.8 | Licensing and IP basics | ☐ | ☐ | ☐ |
| 61.1.9 | Vendor evaluation, build-vs-buy analysis | ☐ | ☐ | ☐ |
| 61.1.10 | Technical due diligence, consulting engagement scoping | ☐ | ☐ | ☐ |
| 61.1.11 | Working with non-engineers, translating tradeoffs | ☐ | ☐ | ☐ |
| 61.1.12 | Operating independently: contracts, SLAs with clients, pricing | ☐ | ☐ | ☐ |
| 61.1.13 | Public technical presence: blogs, talks, videos | ☐ | ☐ | ☐ |

## Scorecard

| Pillar | Topics | G | Y | R | % G |
|---|:-:|:-:|:-:|:-:|:-:|
| P1. Digital Logic & Silicon Fundamentals | 18 |  |  |  |  |
| P2. CPU Microarchitecture | 29 |  |  |  |  |
| P3. Cache & Memory Hierarchy | 26 |  |  |  |  |
| P4. Main Memory, Buses & Interconnects | 22 |  |  |  |  |
| P5. Accelerators: GPU, TPU, FPGA, ASIC | 16 |  |  |  |  |
| P6. Firmware, Boot & BIOS/UEFI | 16 |  |  |  |  |
| P7. Embedded Systems & Microcontrollers | 27 |  |  |  |  |
| P8. Hardware Buses & Peripheral Interfaces | 18 |  |  |  |  |
| P9. OS: Processes, Threads & Scheduling | 20 |  |  |  |  |
| P10. OS: Memory Management | 21 |  |  |  |  |
| P11. OS: Concurrency & Synchronization | 20 |  |  |  |  |
| P12. OS: I/O Subsystem & Virtual File System | 19 |  |  |  |  |
| P13. OS: Interrupts, Drivers & Kernel Development | 18 |  |  |  |  |
| P14. Operating System Families & Platform Differences | 10 |  |  |  |  |
| P15. Storage Hardware | 11 |  |  |  |  |
| P16. File Systems & Volume Management | 21 |  |  |  |  |
| P17. Networking: Linux Stack & Packet Path | 12 |  |  |  |  |
| P18. Networking: Transport Layer | 18 |  |  |  |  |
| P19. Networking: L2/L3, Routing & Switching | 17 |  |  |  |  |
| P20. Networking: Application Protocols, DNS & TLS | 20 |  |  |  |  |
| P21. Networking: High-Performance, Datacenter & Edge | 17 |  |  |  |  |
| P22. Wireless, IoT & Telecom Protocols | 15 |  |  |  |  |
| P23. Compilers & Program Translation | 20 |  |  |  |  |
| P24. Linking, Loading & ABI | 12 |  |  |  |  |
| P25. Programming Languages & Runtimes | 18 |  |  |  |  |
| P26. Build Systems, Packaging & Toolchains | 16 |  |  |  |  |
| P27. Data Structures | 24 |  |  |  |  |
| P28. Algorithms | 22 |  |  |  |  |
| P29. Performance Math & Queueing Theory | 12 |  |  |  |  |
| P30. Databases: Single-Node Engines | 30 |  |  |  |  |
| P31. Distributed Databases, Messaging & Caching | 26 |  |  |  |  |
| P32. Distributed Systems Theory | 22 |  |  |  |  |
| P33. Distributed Systems Patterns & Resilience | 24 |  |  |  |  |
| P34. Virtualization & Hypervisors | 18 |  |  |  |  |
| P35. Containers & Runtimes | 12 |  |  |  |  |
| P36. Kubernetes & Orchestration | 16 |  |  |  |  |
| P37. Cloud Platforms & Infrastructure as Code | 21 |  |  |  |  |
| P38. Observability & Monitoring | 14 |  |  |  |  |
| P39. Debugging, Tracing & Diagnostics | 22 |  |  |  |  |
| P40. Performance Engineering | 22 |  |  |  |  |
| P41. Reliability, SRE & Operations | 21 |  |  |  |  |
| P42. CI/CD & Release Engineering | 12 |  |  |  |  |
| P43. Security: OS, Application & Memory Safety | 22 |  |  |  |  |
| P44. Cryptography, PKI & Identity | 22 |  |  |  |  |
| P45. Network & Infrastructure Security | 22 |  |  |  |  |
| P46. Testing, Correctness & Formal Methods | 23 |  |  |  |  |
| P47. Architecture, API & Protocol Design | 17 |  |  |  |  |
| P48. Software Engineering Fundamentals & Design | 23 |  |  |  |  |
| P49. Backend & Web Application Development | 31 |  |  |  |  |
| P50. Frontend & Browser Internals | 26 |  |  |  |  |
| P51. Mobile & Desktop Applications | 22 |  |  |  |  |
| P52. Graphics, Audio, Video & Game Systems | 22 |  |  |  |  |
| P53. Application Security & Privacy Engineering | 21 |  |  |  |  |
| P54. Domain Application Systems & Product Patterns | 17 |  |  |  |  |
| P55. Software Process, Product & Team Engineering | 20 |  |  |  |  |
| P56. Data Engineering, ML Systems & AI Infrastructure | 19 |  |  |  |  |
| P57. Specialized & Safety-Critical Domains | 16 |  |  |  |  |
| P58. Mathematics & CS Theory Foundations | 17 |  |  |  |  |
| P59. Linux Administration, Shell & Daily Tooling | 22 |  |  |  |  |
| P60. Time, Text, Encoding & Data Formats | 10 |  |  |  |  |
| P61. Engineering Practice, Communication & Career | 13 |  |  |  |  |
| **Total** | **1180** |  |  |  |  |

