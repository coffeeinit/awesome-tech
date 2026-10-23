# Awesome Containers & Orchestration [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A systems-level index of container engineering, Kubernetes, microVMs, and the surrounding supply chain. Organized by **layer of the stack**, not by vendor or popularity.

**Last Updated: 2026-10-04**

[![Layers](https://img.shields.io/badge/Layers-18-blue?style=for-the-badge)](#-table-of-contents)
[![Tools](https://img.shields.io/badge/Tools-250%2B-green?style=for-the-badge)](#-table-of-contents)
[![Updated](https://img.shields.io/badge/Updated-2026--10--04-orange?style=for-the-badge)](#)

---

## Table of Contents

1. [Base Images](#1-base-images)
2. [Build Tools](#2-build-tools)
3. [Image Security](#3-image-security)
4. [Signing, SBOM & Supply Chain](#4-signing-sbom--supply-chain)
5. [Registries](#5-registries)
6. [Container Runtimes & CRI](#6-container-runtimes--cri)
7. [MicroVMs & Sandboxing](#7-microvms--sandboxing)
8. [Networking & CNI](#8-networking--cni)
9. [Storage](#9-storage)
10. [Service Mesh & Proxies](#10-service-mesh--proxies)
11. [Serverless Containers](#11-serverless-containers)
12. [WASM & Hybrid Runtimes](#12-wasm--hybrid-runtimes)
13. [Observability & Runtime Security](#13-observability--runtime-security)
14. [Rootless & Daemonless](#14-rootless--daemonless)
15. [Multi-Arch & Cross-Platform](#15-multi-arch--cross-platform)
16. [Self-Hosted Container Management Platforms](#16-self-hosted-container-management-platforms)
17. [Self-Hosted Kubernetes Distributions](#17-self-hosted-kubernetes-distributions)
18. [KVM / VMM / Virtualization Management](#18-kvm--vmm--virtualization-management)
19. [Reference Architectures](#19-reference-architectures)

---

## 1. Base Images

*The foundation layer. What you inherit determines your CVE baseline.*

### Minimalist & Distroless

| Image | Base | Shell | Package Manager | CVE Posture | Notes |
|---|---|---|---|---|---|
| **[Scratch](https://hub.docker.com/_/scratch)** | None | ❌ | ❌ | 0 | Empty layer. For static binaries only. |
| **[Distroless](https://github.com/GoogleContainerTools/distroless)** | Debian | ❌ | ❌ | Low | Google's reference distroless. Built with Bazel. |
| **[Chainguard](https://www.chainguard.dev/)** | Wolfi | ❌ | ❌ | 0 (at build) | Built with apko. Zero known CVEs at build time.  |
| **[Wolfi](https://github.com/wolfi-dev)** | Wolfi | ✅ (dev) | apk | Low | The undistro behind Chainguard. glibc-based.  |
| **[Alpine](https://hub.docker.com/_/alpine)** | Alpine | ✅ | apk | Very low | musl libc. 5 MB base. |
| **[Debian Slim](https://hub.docker.com/_/debian)** | Debian | ✅ | apt | Low | glibc. Familiar territory. |
| **[UBI Micro](https://developers.redhat.com/products/rhel/ubi)** | RHEL | ❌ | ❌ | Low | Red Hat's minimal base. |
| **[Photon OS](https://github.com/vmware/photon)** | Photon | ✅ | tdnf | Low | VMware's minimal Linux. |

**Key decision:** Distroless and Chainguard images have **no shell and no package manager** by default. This is a security feature, not a bug. Use `-dev` variants for builder stages, then copy artifacts into the distroless runtime stage. 

### Language-Specific Bases

| Language | Recommended Base | Why |
|---|---|---|
| **Go** | `scratch` or `distroless/static` | Static binary. No libc needed. |
| **Rust** | `scratch` or `distroless/cc` | musl or glibc static. |
| **Java** | `distroless/java` or `chainguard/jre` | JRE only, no shell. Use Jib or Ko. |
| **Python** | `chainguard/python` or `distroless/python3` | Venv + distroless. |
| **Node** | `chainguard/node` or `distroless/nodejs` | Bundle to single JS file with esbuild. |
| **.NET** | `dotnet/runtime-deps` | Native AOT or self-contained. |

### Base Image Comparison: CVE Reality

A 2026 benchmark found **Chainguard Images and Google's distroless** lead on zero-CVE posture. Wolfi-base is 13 MB with 0 CVEs; Ubuntu takes significantly longer to reach that state. 

> **Rule of thumb:** If your base image has a shell, you have an attack surface. If it has a package manager, you have a supply chain risk. Distroless solves both.

---

## 2. Build Tools

*How the image is composed. The build layer determines reproducibility, cache efficiency, and rootless capability.*

### Dockerfile-Based

| Tool | Rootless | Daemonless | Cache | Notes |
|---|---|---|---|---|
| **[Docker BuildKit](https://docs.docker.com/build/buildkit/)** | ✅ | ❌ | ✅ | The modern backend for `docker build`. Multi-stage, cache mounts, secrets. |
| **[Buildah](https://buildah.io/)** | ✅ | ✅ | ✅ | Red Hat's daemonless builder. OCI-compliant. |
| **[Kaniko](https://github.com/GoogleContainerTools/kaniko)** | ✅ | ✅ | ✅ | Builds inside Kubernetes without privileged mode. **Archived.**  |
| **[img](https://github.com/genuinetools/img)** | ✅ | ✅ | ✅ | Standalone, daemonless, rootless. |
| **[Buildpacks](https://buildpacks.io/)** | ✅ | ✅ | ✅ | CNCF. Auto-detects language. No Dockerfile. |

### Declarative & Nix-Based

| Tool | Approach | Reproducible | Notes |
|---|---|---|---|
| **[Nix](https://nixos.org/)** | Pure functional | ✅ | `dockerTools.buildImage`. Full system reproducibility. |
| **[Earthly](https://earthly.dev/)** | Containerized Makefile | ✅ | Dockerfile + Makefile hybrid. |
| **[Dagger](https://dagger.io/)** | Programmable pipelines | ✅ | SDKs in Go, Python, TypeScript. |

### Language-Native Builders

| Tool | Language | Output | Notes |
|---|---|---|---|
| **[Jib](https://github.com/GoogleContainerTools/jib)** | Java | OCI image | No Docker daemon. Maven/Gradle plugin. |
| **[Ko](https://github.com/ko-build/ko)** | Go | OCI image | Builds and pushes from `go build`. |
| **[Jib](https://github.com/GoogleContainerTools/jib)** | Java | OCI | No Dockerfile. |
| **[Spring Boot Buildpacks](https://spring.io/guides/gs/spring-boot-docker/)** | Java | OCI | Auto-detects. |

### Build Optimization

| Technique | Tools | Impact |
|---|---|---|
| **Multi-stage builds** | Docker, BuildKit | Removes build tools from runtime. |
| **Cache mounts** | BuildKit `--mount=type=cache` | Speeds rebuilds. |
| **Layer ordering** | Dockerfile best practices | Least-changed layers first. |
| **Squashing** | `docker-squash`, BuildKit `--squash` | Reduces layer count. |
| **Compression** | zstd, estargz, nydus | Faster pulls. |

> **2026 reality:** Kaniko is archived. BuildKit + Buildah is the modern path. Rootless is no longer optional.

---

## 3. Image Security

*Scanning, linting, and vulnerability detection. What you find before it runs.*

### Vulnerability Scanners

| Scanner | Speed | Ecosystem | Notes |
|---|---|---|---|
| **[Trivy](https://trivy.dev/)** | Fast | Broadest | Scans OS packages, language deps, IaC, secrets. **The default.**  |
| **[Grype](https://github.com/anchore/grype)** | Fast | Broad | Anchore's scanner. Pairs with Syft for SBOM. |
| **[Snyk Container](https://snyk.io/product/container-vulnerability-management/)** | Medium | Commercial | IDE integration. |
| **[Docker Scout](https://docs.docker.com/scout/)** | Medium | Docker-native | Built into Docker Desktop. |
| **[Clair](https://github.com/quay/clair)** | Medium | CoreOS | The original. Used by Quay. |

### Dockerfile Linters

| Tool | Rules | Notes |
|---|---|---|
| **[Hadolint](https://github.com/hadolint/hadolint)** | 50+ | Shellcheck inside Dockerfile. The standard. |
| **[Dockerlint](https://github.com/projectatomic/dockerfile_lint)** | Basic | Red Hat's linter. |
| **[Checkov](https://www.checkov.io/)** | IaC | Also scans Dockerfiles. |

### Runtime Security

| Tool | Mechanism | Notes |
|---|---|---|
| **[Falco](https://falco.org/)** | eBPF + syscall | CNCF. Runtime threat detection. |
| **[Tetragon](https://tetragon.io/)** | eBPF | Cilium's runtime security. |
| **[Tracee](https://aquasecurity.github.io/tracee/)** | eBPF | Aqua Security's runtime tracer. |
| **[Sysdig](https://sysdig.com/)** | eBPF + kernel | Commercial. |

> **The highest-leverage control is admission:** An admission rule that rejects unsigned images converts every other verification from advisory finding into precondition. 

---

## 4. Signing, SBOM & Supply Chain

*Provenance, attestation, and verifiability. How you know the image is what you built.*

### Signing & Attestation

| Tool | Mechanism | Notes |
|---|---|---|
| **[Cosign](https://github.com/sigstore/cosign)** | Keyless (OIDC) or key-based | The standard. Stores signatures in OCI registry.  |
| **[Sigstore](https://www.sigstore.dev/)** | Fulcio + Rekor | Root CA + transparency log. |
| **[Notation](https://notaryproject.dev/)** | OCI-native | CNCF. Notary v2. |
| **[in-toto](https://in-toto.io/)** | Attestation framework | SLSA provenance. |

### SBOM Generation

| Tool | Format | Notes |
|---|---|---|
| **[Syft](https://github.com/anchore/syft)** | SPDX, CycloneDX | Anchore's SBOM generator. |
| **[Trivy](https://trivy.dev/)** | SPDX, CycloneDX | `trivy image --format cyclonedx`. |
| **[cdxgen](https://github.com/CycloneDX/cdxgen)** | CycloneDX | Multi-language. |
| **[Tern](https://github.com/tern-tools/tern)** | SPDX | Container-focused. |

### SLSA & Provenance

| Level | Requirements | Tooling |
|---|---|---|
| **SLSA 1** | Documented build process | Any |
| **SLSA 2** | Hosted build, signed provenance | GitHub Actions + Cosign |
| **SLSA 3** | Hardened build, non-falsifiable | Tekton, Google Cloud Build |
| **SLSA 4** | Two-party review, hermetic | Rare |

### Policy Enforcement

| Tool | Engine | Notes |
|---|---|---|
| **[OPA Gatekeeper](https://open-policy-agent.github.io/gatekeeper/)** | Rego | Admission control. |
| **[Kyverno](https://kyverno.io/)** | YAML | Kubernetes-native policy. |
| **[Sigstore Policy Controller](https://docs.sigstore.dev/policy-controller/overview/)** | Sigstore | Reject unsigned images. |
| **[Connaisseur](https://github.com/sse-secure-systems/connaisseur)** | Cosign, Notary | Admission controller. |

> **The five-surface model:** Build, registry, admission, runtime, observation. Each surface has distinct controls the others cannot substitute for. 

---

## 5. Registries

*Where images live. The registry determines pull performance, policy enforcement, and air-gap capability.*

### Self-Hosted

| Registry | Complexity | OCI 1.1 | UI | Scanning | Notes |
|---|---|---|---|---|---|
| **[Distribution](https://github.com/distribution/distribution)** | Low | Partial | ❌ | ❌ | The `registry:2` baseline.  |
| **[Zot](https://zotregistry.dev/)** | Low | Full | ✅ | Optional | Single Go binary. CNCF.  |
| **[Harbor](https://goharbor.io/)** | High | Full | ✅ | Trivy built-in | Full platform. CNCF.  |
| **[Quay](https://quay.io/)** | Medium | Full | ✅ | Clair | Red Hat. |
| **[GitLab Registry](https://docs.gitlab.com/ee/user/packages/container_registry/)** | Medium | Full | ✅ | ✅ | Bundled with GitLab. |
| **[Nexus](https://www.sonatype.com/products/repository-oss)** | Medium | Partial | ✅ | ✅ | Also Maven, npm, etc. |
| **[Artifactory](https://jfrog.com/artifactory/)** | High | Full | ✅ | ✅ | Universal artifact repo. |

### Cloud-Managed

| Registry | Provider | OCI 1.1 | Notes |
|---|---|---|---|
| **[ECR](https://aws.amazon.com/ecr/)** | AWS | Full | IAM integration. |
| **[GCR / Artifact Registry](https://cloud.google.com/artifact-registry)** | Google | Full | GCP-native. |
| **[ACR](https://azure.microsoft.com/products/container-registry)** | Azure | Full | Azure-native. |
| **[GHCR](https://ghcr.io/)** | GitHub | Full | Free for public images. |

**2026 recommendation:** Start with **Zot** for homelab and small teams. Use **Distribution** for a throwaway internal cache. Use **Harbor** only when you need multi-tenant policy and will maintain it. 

---

## 6. Container Runtimes & CRI

*The execution layer. What actually runs the container.*

### Low-Level Runtimes (OCI)

| Runtime | Language | Notes |
|---|---|---|
| **[runc](https://github.com/opencontainers/runc)** | Go | The reference OCI runtime. |
| **[crun](https://github.com/containers/crun)** | C | Faster than runc. Used by Podman. |
| **[youki](https://github.com/containers/youki)** | Rust | Memory-safe runc alternative. |
| **[runsc (gVisor)](https://gvisor.dev/)** | Go | User-space kernel. Sandboxed. |

### High-Level Runtimes (CRI)

Kubernetes supports any implementation of the **Container Runtime Interface (CRI)**. The two serious contenders are containerd and CRI-O. 

| Runtime | Origin | Attack Surface | Notes |
|---|---|---|---|
| **[containerd](https://containerd.io/)** | Docker → CNCF | Medium | General-purpose. Used by Docker, GKE, EKS. |
| **[CRI-O](https://cri-o.io/)** | Red Hat | Small | Built **only** for Kubernetes. No Docker baggage.  |
| **[Docker Engine](https://docs.docker.com/engine/)** | Docker | Large | **Deprecated** as a CRI runtime. |

**CRI-O vs containerd:** CRI-O was built specifically to implement the CRI and nothing else. containerd started as a general-purpose runtime and added CRI later. For hardened clusters, CRI-O's smaller attack surface matters. 

### Runtime Comparison

| Criterion | containerd | CRI-O |
|---|---|---|
| **Scope** | General-purpose | Kubernetes-only |
| **Attack surface** | Larger | Smaller |
| **OCI runtime** | runc, crun | crun, runc |
| **Image building** | ✅ (BuildKit) | ❌ |
| **Docker compat** | ✅ | ❌ |

---

## 7. MicroVMs & Sandboxing

*Stronger isolation than runc, less overhead than a full VM. The layer between containers and VMs.*

### MicroVM Comparison (2026)

| Runtime | Boot Time | Memory Overhead | Security Boundary | Best For |
|---|---|---|---|---|
| **[Firecracker](https://firecracker-microvm.github.io/)** | **110–140 ms** | **5 MB** | KVM + minimal device model | Serverless, FaaS, multi-tenant |
| **[Cloud Hypervisor](https://www.cloudhypervisor.org/)** | 180–240 ms | 8 MB | KVM + broader device model | Modern cloud workloads |
| **[Kata Containers](https://katacontainers.io/)** | 200–350 ms | 30–50 MB | Orchestration shim + VMM | Unmodified OCI workloads |

**Firecracker** presents the narrowest attack surface: ~50,000 lines of Rust, no PCI, no USB, no GPU passthrough. Fewer than 10 CVEs in its lifetime. 

**Kata Containers** is an orchestration shim that runs OCI workloads inside a microVM. The security boundary is whichever hypervisor you pair it with — Firecracker, Cloud Hypervisor, or QEMU. 

### Sandboxing

| Tool | Mechanism | Isolation Level | Notes |
|---|---|---|---|
| **[gVisor](https://gvisor.dev/)** | User-space kernel | High | Intercepts syscalls. runsc runtime. |
| **[Firecracker](https://firecracker-microvm.github.io/)** | KVM microVM | Very high | Hardware virtualization. |
| **[Kata Containers](https://katacontainers.io/)** | VM + agent | Very high | OCI-compatible. |
| **[Nabla Containers](https://github.com/nabla-containers)** | Unikernel | Very high | Library OS. |
| **[Unikraft](https://unikraft.org/)** | Unikernel | Very high | POSIX-compatible unikernel. |

### When to Use What

| Workload | Recommendation |
|---|---|
| **Serverless / FaaS** | Firecracker |
| **Multi-tenant SaaS** | Firecracker or Kata |
| **Untrusted code execution** | gVisor or Firecracker |
| **Standard Kubernetes** | containerd or CRI-O with runc |
| **Hardened multi-tenant K8s** | Kata Containers with Firecracker backend |

> **The 2026 rule:** If you are building a function-as-a-service or sandbox-as-a-service product, Firecracker pays off because the small attack surface lets you defend it credibly to customers. 

---

## 8. Networking & CNI

*Pod-to-pod communication, network policy, and service discovery.*

### CNI Plugins

| Plugin | Dataplane | L7 Policy | Performance | Notes |
|---|---|---|---|---|
| **[Cilium](https://cilium.io/)** | eBPF | ✅ | **8.9K Mbps** @ 1000 rules | Bypasses iptables. Kernel-level.  |
| **[Calico](https://www.tigera.io/project-calico/)** | iptables, eBPF | ❌ | High | BGP routing. Windows support.  |
| **[Flannel](https://github.com/flannel-io/flannel)** | VXLAN | ❌ | Medium | Simple. No policy. |
| **[Canal](https://projectcalico.docs.tigera.io/getting-started/kubernetes/flannel/)** | Calico + Flannel | ❌ | Medium | Calico policy + Flannel networking. |
| **[Antrea](https://antrea.io/)** | OVS | ✅ | High | VMware. Open vSwitch. |
| **[Kube-router](https://www.kube-router.io/)** | BGP | ❌ | High | All-in-one. |

**Cilium vs Calico:** Cilium is eBPF-native, offering L7 policy, DNS-aware controls, and sidecarless service mesh. Calico is iptables-based (or eBPF), with BGP for hybrid/multi-cloud and strong Windows support. 

### Service Mesh Integration

| Mesh | Dataplane | Sidecar | Notes |
|---|---|---|---|
| **[Istio](https://istio.io/)** | Envoy | ✅ | The standard. Ambient mode (sidecarless). |
| **[Linkerd](https://linkerd.io/)** | Rust micro-proxy | ✅ | Lightweight. |
| **[Cilium Service Mesh](https://cilium.io/use-cases/service-mesh/)** | eBPF | ❌ | Sidecarless. |
| **[Consul Connect](https://developer.hashicorp.com/consul/docs/connect)** | Envoy | ✅ | HashiCorp. |

### Ingress & Gateway

| Tool | Layer | Notes |
|---|---|---|
| **[Envoy Gateway](https://gateway.envoyproxy.io/)** | L7 | Kubernetes Gateway API. |
| **[Traefik](https://traefik.io/)** | L7 | Automatic HTTPS. |
| **[Nginx Ingress](https://kubernetes.github.io/ingress-nginx/)** | L7 | The old standard. |
| **[Contour](https://projectcontour.io/)** | L7 | Envoy-based. |

---

## 9. Storage

*Persistent volumes, CSI drivers, and storage backends.*

### CSI Drivers

| Driver | Backend | Notes |
|---|---|---|
| **[Rook](https://rook.io/)** | Ceph | The standard. Block, file, object. |
| **[Longhorn](https://longhorn.io/)** | Built-in | Rancher. Lightweight. |
| **[OpenEBS](https://openebs.io/)** | Various | Container-attached storage. |
| **[Portworx](https://portworx.com/)** | Various | Enterprise. |
| **[JuiceFS](https://juicefs.com/)** | Object storage | POSIX over S3. |

### Storage Patterns

| Pattern | Use Case | Tools |
|---|---|---|
| **Ephemeral** | Scratch space | `emptyDir` |
| **Block** | Databases | Rook, Longhorn |
| **File** | Shared config | NFS, CephFS |
| **Object** | Artifacts, backups | MinIO, Ceph RGW |
| **CSI** | Kubernetes-native | Any CSI driver |

---

## 10. Service Mesh & Proxies

*L7 traffic management, mTLS, and observability.*

### Sidecar-Based

| Mesh | Proxy | Language | Notes |
|---|---|---|---|
| **[Istio](https://istio.io/)** | Envoy | C++ | The standard. Ambient mode. |
| **[Linkerd](https://linkerd.io/)** | Rust micro-proxy | Rust | Lightweight. Fast. |
| **[Consul Connect](https://developer.hashicorp.com/consul/docs/connect)** | Envoy | C++ | HashiCorp ecosystem. |
| **[Kuma](https://kuma.io/)** | Envoy | C++ | CNCF. Multi-zone. |

### Sidecarless / Ambient

| Mesh | Mechanism | Notes |
|---|---|---|
| **[Istio Ambient](https://istio.io/latest/docs/ambient/)** | ztunnel + waypoint | No sidecar. L4 + L7 separation. |
| **[Cilium Service Mesh](https://cilium.io/use-cases/service-mesh/)** | eBPF | Kernel-level. |
| **[Ambient Mesh](https://github.com/istio/istio/tree/master/ambient)** | ztunnel | Istio's sidecarless mode. |

### Proxies

| Proxy | Language | Use Case | Notes |
|---|---|---|---|
| **[Envoy](https://www.envoyproxy.io/)** | C++ | Service mesh, edge | The standard. |
| **[HAProxy](https://www.haproxy.org/)** | C | Load balancing | Battle-tested. |
| **[Traefik](https://traefik.io/)** | Go | Edge, Kubernetes | Automatic HTTPS. |
| **[Nginx](https://nginx.org/)** | C | Edge, reverse proxy | Ubiquitous. |
| **[Caddy](https://caddyserver.com/)** | Go | Edge, HTTPS | Automatic TLS. |

---

## 11. Serverless Containers

*Run containers without managing nodes.*

| Platform | Isolation | Cold Start | Notes |
|---|---|---|---|
| **[AWS Fargate](https://aws.amazon.com/fargate/)** | Firecracker | ~1s | ECS/EKS-native. |
| **[Google Cloud Run](https://cloud.google.com/run)** | gVisor | ~500ms | GCP-native. |
| **[Azure Container Apps](https://azure.microsoft.com/products/container-apps)** | Hyper-V | ~1s | Azure-native. |
| **[Knative](https://knative.dev/)** | Kubernetes | ~2s | Self-hosted. |
| **[OpenFaaS](https://www.openfaas.com/)** | Kubernetes | ~1s | Self-hosted. |
| **[Nuclio](https://nuclio.io/)** | Kubernetes | ~500ms | High-performance. |
| **[Fly.io](https://fly.io/)** | Firecracker | ~300ms | Global. |
| **[Cloudflare Containers](https://developers.cloudflare.com/containers/)** | Firecracker | ~500ms | Edge. |

---

## 12. WASM & Hybrid Runtimes

*The bridge between containers and WebAssembly.*

| Runtime | WASI | Container Compat | Notes |
|---|---|---|---|
| **[Wasmtime](https://wasmtime.dev/)** | ✅ | OCI (experimental) | Bytecode Alliance. |
| **[Wasmer](https://wasmer.io/)** | ✅ | OCI | Universal runtime. |
| **[WasmEdge](https://wasmedge.org/)** | ✅ | OCI | CNCF. Edge-focused. |
| **[Spin](https://github.com/fermyon/spin)** | ✅ | ❌ | Fermyon. Serverless WASM. |
| **[WasmCloud](https://wasmcloud.com/)** | ✅ | ❌ | CNCF. Actor model. |
| **[Extism](https://extism.org/)** | ✅ | ❌ | Plugin system. |

### Container-to-WASM Tooling

| Tool | Direction | Notes |
|---|---|---|
| **[wasm-to-oci](https://github.com/engineerd/wasm-to-oci)** | WASM → OCI | Push WASM as OCI artifact. |
| **[crun-wasm](https://github.com/containers/crun)** | OCI → WASM | Run WASM via crun. |
| **[youki-wasm](https://github.com/containers/youki)** | OCI → WASM | WASM runtime for youki. |

---

## 13. Observability & Runtime Security

*What runs inside the container, and how you see it.*

### Runtime Security

| Tool | Mechanism | Notes |
|---|---|---|
| **[Falco](https://falco.org/)** | eBPF + syscall | CNCF. The standard. |
| **[Tetragon](https://tetragon.io/)** | eBPF | Cilium. Kernel-level. |
| **[Tracee](https://aquasecurity.github.io/tracee/)** | eBPF | Aqua. |
| **[Sysdig](https://sysdig.com/)** | eBPF + kernel | Commercial. |

### Observability

| Pillar | Tools | Notes |
|---|---|---|
| **Metrics** | Prometheus, VictoriaMetrics, Mimir | CNCF. |
| **Logs** | Loki, Fluent Bit, Vector | CNCF. |
| **Traces** | Tempo, Jaeger, OpenTelemetry | CNCF. |
| **Profiles** | Pyroscope, Parca | Continuous profiling. |
| **eBPF** | Cilium Hubble, Pixie | Network observability. |

---

## 14. Rootless & Daemonless

*Running containers without root and without a daemon.*

| Tool | Rootless | Daemonless | Notes |
|---|---|---|---|
| **[Podman](https://podman.io/)** | ✅ | ✅ | Docker-compatible CLI. |
| **[Buildah](https://buildah.io/)** | ✅ | ✅ | Build images without daemon. |
| **[Skopeo](https://github.com/containers/skopeo)** | ✅ | ✅ | Copy images between registries. |
| **[Kaniko](https://github.com/GoogleContainerTools/kaniko)** | ✅ | ✅ | Build in Kubernetes. **Archived.** |
| **[img](https://github.com/genuinetools/img)** | ✅ | ✅ | Standalone builder. |
| **[nerdctl](https://github.com/containerd/nerdctl)** | ✅ | ✅ | containerd CLI. |

**Why rootless matters:** A rootless container runs as a non-root user on the host. If the container escapes, the attacker has no host root. This is the default in Podman and Buildah.

---

## 15. Multi-Arch & Cross-Platform

*Build once, run anywhere.*

| Tool | Mechanism | Notes |
|---|---|---|
| **[Buildx](https://docs.docker.com/build/buildx/)** | QEMU + BuildKit | Docker's multi-arch builder. |
| **[Docker BuildKit](https://docs.docker.com/build/buildkit/)** | Native + QEMU | `--platform` flag. |
| **[buildah](https://buildah.io/)** | `--arch` | Multi-arch manifests. |
| **[manifest-tool](https://github.com/estesp/manifest-tool)** | OCI manifests | Create multi-arch manifests. |
| **[regctl](https://github.com/regclient/regclient)** | OCI manifests | Registry client. |

### Platforms to Target

| Platform | Architecture | Notes |
|---|---|---|
| **linux/amd64** | x86_64 | The default. |
| **linux/arm64** | aarch64 | Apple Silicon, Graviton, Raspberry Pi. |
| **linux/arm/v7** | armv7 | Older Raspberry Pi. |
| **linux/riscv64** | riscv64 | Emerging. |
| **windows/amd64** | x86_64 | Windows containers. |

---

## 16. Self-Hosted Container Management Platforms

*Web UIs and PaaS control planes for managing Docker, Podman, and container fleets on your own infrastructure.*

| Tool | Type | Runtime Support | Notable Features | GitHub / Source |
|---|---|---|---|---|
| **[Portainer](https://www.portainer.io/)** | Web UI | Docker, Swarm, Kubernetes | The de facto standard. Stack deployment, RBAC, registry management, edge agent. | `portainer/portainer` |
| **[Coolify](https://coolify.io/)** | PaaS / Control Plane | Docker, Compose, Nixpacks | Self-hosted Heroku/Vercel alternative. Git-driven deploys, databases, SSL. | `coollabsio/coolify` |
| **[Dokploy](https://dokploy.com/)** | PaaS / Control Plane | Docker, Compose | Open-source Vercel/Netlify alternative. Multi-server, monitoring, backups. | `Dokploy/dokploy` |
| **[Easypanel](https://easypanel.io/)** | PaaS / Control Plane | Docker | Server control panel with visual builder. One-click apps, templates. | `easypanel-io/easypanel` |
| **[CapRover](https://caprover.com/)** | PaaS / Control Plane | Docker, Swarm | Scalable PaaS. One-click apps, CLI, web UI, Nginx reverse proxy. | `caprover/caprover` |
| **[Cowbox](https://pypi.org/project/cowbox/)** | PaaS / Control Plane | Docker | Self-hosted PaaS alternative to Dokploy, Coolify, Easypanel. Open-source. | `pypi.org/project/cowbox` |
| **[Surek](https://pypi.org/project/surek/)** | Compose Orchestrator | Docker Compose | Caddy reverse proxy + automatic HTTPS, S3 backups, Portainer + Netdata. | `pypi.org/project/surek` |
| **[Containly](https://hub.docker.com/r/amslertec/containly)** | Web UI | Docker | Modern, secure Docker management UI with file-based Compose stacks. | `amslertec/containly` |
| **[D4S (D-Force)](https://pkg.go.dev/github.com/jr-k/d4s)** | TUI | Docker | K9s-inspired terminal UI for local Docker management. | `github.com/jr-k/d4s` |
| **[Usulnet](https://github.com/fran-olivares/usulnet)** | Web UI / Platform | Docker | All-in-one: containers, security, DNS, VPN, monitoring, backups, multi-node. | `fran-olivares/usulnet` |
| **[DD-UI](https://hub.docker.com/r/prplanit/dd-ui)** | Orchestration Engine | Docker | Declarative, security-first Docker orchestration. AGPL-3.0. | `prplanit/dd-ui` |
| **[Helling](https://pkg.go.dev/helling)** | Platform | Incus, Podman | Single-node, Debian-first system container and VM management. Web UI + API + CLI. | `pkg.go.dev/helling` |
| **[Gubernator](https://hub.docker.com/r/marioezquerro/gubernator)** | Orchestrator | Docker Swarm | "Goldilocks" orchestrator combining Docker Swarm simplicity with robust management. | `marioezquerro/gubernator` |
| **[Podling](https://pkg.go.dev/podling)** | Orchestrator | Docker | Lightweight, educational container orchestrator built from scratch in Go. | `pkg.go.dev/podling` |
| **[Warren](https://pkg.go.dev/warren)** | Orchestrator | Docker | Edge-focused container orchestration. Single binary, built-in HA, secrets, metrics. | `pkg.go.dev/warren` |
| **[SimpleOrch](https://hub.docker.com/r/simpleorch/control-plane)** | Orchestrator | Docker Swarm | On-premises orchestration for Windows & Linux without Kubernetes complexity. | `simpleorch/control-plane` |
| **[Cyber Container Platform](https://github.com/alott2223/cyber-container-platform)** | Web UI | Docker | Modern container management with cyberpunk aesthetics. Go + React. | `alott2223/cyber-container-platform` |
| **[Janus](https://www.osti.gov/biblio/3003095)** | Orchestrator | Containers | Lightweight container management for high-performance data movement. | `osti.gov/biblio/3003095` |

**When to choose what:**

| Need | Recommendation |
|---|---|
| **General Docker management** | Portainer |
| **Self-hosted PaaS (Heroku-like)** | Coolify, Dokploy, or Easypanel |
| **Docker Compose orchestration** | Surek or CapRover |
| **Terminal-based management** | D4S |
| **Lightweight, single-binary PaaS** | Cowbox |
| **Edge/on-prem without K8s** | Warren or SimpleOrch |

---

## 17. Self-Hosted Kubernetes Distributions

*Run Kubernetes on your own infrastructure. Choose based on footprint, complexity, and use case.*

| Distribution | Min RAM | Installation | Best For | Notes |
|---|---|---|---|---|
| **[K3s](https://k3s.io/)** | **512 MB** | 1 command | Edge, IoT, CI/CD | CNCF certified. Single binary < 100 MB.  |
| **[K0s](https://k0sproject.io/)** | ~1 GB | Single binary | Single-node, edge | Zero friction. Fully self-contained.  |
| **[MicroK8s](https://microk8s.io/)** | ~1 GB | Snap install | Developer workstations | Built-in addons. Lightweight.  |
| **[RKE2](https://docs.rke2.io/)** | 2 GB | Script / installer | On-prem, security-focused | Rancher/SUSE. Hardened by default.  |
| **[kubeadm](https://kubernetes.io/docs/reference/setup-tools/kubeadm/)** | 2 GB | Manual | On-premise production | Upstream reference. Community support.  |
| **[Kubespray](https://kubespray.io/)** | 2 GB | Ansible | On-prem, multi-cloud | Production-grade. Ansible-based.  |
| **[OpenShift](https://www.redhat.com/en/technologies/cloud-computing/openshift)** | 8 GB+ | Installer | Enterprise production | Red Hat. Full platform. |
| **[Minikube](https://minikube.sigs.k8s.io/)** | 2 GB | 1 command | Local development | Single-node. For testing.  |
| **[Kind](https://kind.sigs.k8s.io/)** | 2 GB | 1 command | CI/CD, ephemeral clusters | Kubernetes in Docker.  |
| **[SIGHUP Distribution](https://pkg.go.dev/github.com/sighupio/fury-distribution)** | 2 GB | Manual | On-premise production | CNCF certified. Based purely on upstream K8s.  |

**Comparison:** K3s and MicroK8s are suitable for lightweight deployments and resource-constrained environments. K0s is ideal for single-node environments. K8s (vanilla) is well suited for large-scale environments.  For on-prem, RKE2, OpenShift, k0s, kubeadm/Kubespray, and K3s are the top choices, each suited to different team sizes and security postures. 

**Quick decision guide:**

| Scenario | Pick |
|---|---|
| **Edge / IoT / Raspberry Pi** | K3s |
| **Single-node production** | K0s or RKE2 |
| **Developer laptop** | MicroK8s or Minikube |
| **CI/CD ephemeral clusters** | Kind |
| **Enterprise on-prem** | RKE2 or OpenShift |
| **Ansible-managed fleet** | Kubespray |

---

## 18. KVM / VMM / Virtualization Management

*Manage virtual machines, hypervisors, and mixed container/VM workloads from self-hosted control planes.*

| Tool | Type | Backends | Notable Features | Source |
|---|---|---|---|---|
| **[Proxmox VE](https://www.proxmox.com/)** | Hypervisor Platform | KVM, LXC | The de facto open-source virtualization platform. Web UI, HA, backups, Ceph. | `proxmox.com` |
| **[oVirt](https://www.ovirt.org/)** | Virtualization Manager | KVM | Enterprise-grade. Centralized management of VMs, storage, networking. Self-hosted engine. | `ovirt.org` |
| **[WebVirtCloud](https://github.com/retspen/webvirtcloud)** | Web UI | QEMU/KVM | Virtualization web interface for admins and users. | `retspen/webvirtcloud` |
| **[WebKVM](https://github.com/Slaker19/webkvm)** | Web UI | QEMU/KVM, Incus | Single ~14 MB binary. ~15 MB idle RAM. Unified VM + container view. | `Slaker19/webkvm` |
| **[CoreVM](https://github.com/corevm-team/corevm)** | VMM / Hypervisor | KVM (x86) | Pure-software x86 VMM in Rust + NASM. Web UI, cluster orchestration, DRS, HA. | `corevm-team/corevm` |
| **[OneClickVirt](https://github.com/oneclickvirt/oneclickvirt)** | Universal Platform | LXD, Incus, Docker, Podman, Containerd, Proxmox VE, QEMU/KVM, KubeVirt | Extensible universal virtualization management platform. Vue 3 web console. | `oneclickvirt/oneclickvirt` |
| **[Corral](https://github.com/tuna-os/corral)** | VM Manager | QEMU/KVM, KubeVirt, Incus, libvirt, Proxmox VE | Proxmox-style web UI. Tailscale integration. Cross-backend VM migration. | `tuna-os/corral` |
| **[MFCloud Console](https://hub.docker.com/r/mfconsole/kvm-manager)** | KVM Manager | KVM | Enterprise KVM hypervisor manager. Live migration, Ceph/LINSTOR/ZFS, OVN networking. | `mfconsole/kvm-manager` |
| **[Flint](https://github.com/flint-kvm/flint)** | KVM Manager | KVM | Single <11 MB binary. Modern Web UI, CLI, API. Zero bloat. | `flint-kvm/flint` |
| **[VirtUI Manager](https://pypi.org/project/virtui-manager/)** | TUI | QEMU/KVM | Terminal UI for managing VMs via libvirt Python API. Auto-install for major distros. | `pypi.org/project/virtui-manager` |
| **[aqemu](https://packages.debian.org/aqemu)** | GUI | QEMU/KVM | Qt5 frontend for QEMU and KVM. User-friendly interface. | `packages.debian.org/aqemu` |
| **[virt-manager](https://virt-manager.org/)** | GUI | KVM, Xen, LXC | Lightweight GUI for managing VMs and containers via libvirt. | `virt-manager.org` |
| **[Kimchi](https://github.com/kimchi-project/kimchi)** | Web UI | KVM | HTML5-based KVM management. Modern web interface. | `kimchi-project/kimchi` |
| **[Sylve](https://pkg.go.dev/sylve)** | Platform | Bhyve, Jails, ZFS | FreeBSD-native infrastructure management. VMs, jails, ZFS, networking, backups. | `pkg.go.dev/sylve` |
| **[Pabawi](https://hub.docker.com/r/example42/pabawi)** | Web Frontend | Proxmox, AWS, Azure | Manage classic infrastructure — physical servers, VMs, and tools. | `example42/pabawi` |
| **[PVMSS](https://hub.docker.com/r/jhmmt/pvmss)** | Self-Service Portal | Proxmox VE | Allow users to create/manage VMs without direct Proxmox access. | `jhmmt/pvmss` |
| **[Corsinvest cv4pve-admin](https://github.com/Corsinvest/cv4pve-admin)** | Admin Console | Proxmox VE | Multi-cluster management. Health Score. Self-service portal. | `Corsinvest/cv4pve-admin` |
| **[Web Appliance Dashboard](https://github.com/alflewerken/web-appliance-dashboard)** | Dashboard | VMs, Docker | Homelab management. SSH/VNC/RDP access, real-time monitoring. | `alflewerken/web-appliance-dashboard` |

**KVM management comparison:**

| Tool | Install Footprint | Idle RAM | Host Preservation | Best For |
|---|---|---|---|---|
| **WebKVM** | Single binary (~14 MB) | **~15 MB** | 100% untouched | Lightweight, single-server |
| **Proxmox VE** | Entire ISO / OS takeover | 1.2–2.5 GB | Requires custom Debian fork | Full platform, clusters |
| **virt-manager** | Desktop GTK app | N/A (client) | Untouched | Desktop management |
| **Cockpit (Machines)** | System daemon + modules | ~80 MB | Untouched | General server admin |

**When to choose what:**

| Need | Recommendation |
|---|---|
| **Full virtualization platform** | Proxmox VE |
| **Lightweight KVM web UI** | WebKVM or Flint |
| **Terminal-based KVM management** | VirtUI Manager |
| **Mixed VM + container management** | OneClickVirt or Corral |
| **Enterprise KVM with HA** | oVirt or MFCloud Console |
| **FreeBSD infrastructure** | Sylve |

---

## 19. Reference Architectures

*How these layers fit together in production.*

### The Golden Path (2026)

```
┌─────────────────────────────────────────────────────────────┐
│  BUILD                                                       │
│  BuildKit + multi-stage + distroless runtime                 │
│  Hadolint + Trivy + Syft SBOM                               │
├─────────────────────────────────────────────────────────────┤
│  SIGN                                                        │
│  Cosign (keyless) + SLSA provenance                         │
├─────────────────────────────────────────────────────────────┤
│  STORE                                                       │
│  Zot or Harbor + retention policies                         │
├─────────────────────────────────────────────────────────────┤
│  ADMIT                                                       │
│  OPA Gatekeeper / Kyverno / Sigstore Policy Controller      │
├─────────────────────────────────────────────────────────────┤
│  RUN                                                         │
│  containerd or CRI-O + runc                                  │
│  (or Firecracker / Kata for stronger isolation)             │
├─────────────────────────────────────────────────────────────┤
│  NETWORK                                                     │
│  Cilium (eBPF) + Gateway API                                │
├─────────────────────────────────────────────────────────────┤
│  OBSERVE                                                     │
│  Falco + Prometheus + OpenTelemetry                         │
└─────────────────────────────────────────────────────────────┘
```

### When to Use What

| Scenario | Base Image | Build | Runtime | Isolation |
|---|---|---|---|---|
| **Standard web app** | distroless | BuildKit | containerd | runc |
| **Multi-tenant SaaS** | distroless | BuildKit | CRI-O | Kata + Firecracker |
| **Serverless / FaaS** | scratch | BuildKit | Firecracker | Firecracker |
| **Untrusted code** | scratch | BuildKit | gVisor | gVisor |
| **Edge / IoT** | Alpine | Buildah | containerd | runc |
| **Windows workloads** | nanoserver | BuildKit | containerd | Hyper-V |

---

## 🤝 Contributing

Contributions are welcome! To add a tool or project, please use the issue template.

## 📚 Source Links

*Direct GitHub and source links for tools referenced in the search results.*

- Cowbox: `pypi.org/project/cowbox`
- Surek: `pypi.org/project/surek`
- Containly: `amslertec/containly`
- D4S (D-Force): `github.com/jr-k/d4s`
- Usulnet: `fran-olivares/usulnet`
- Helling: `pkg.go.dev/helling`
- DD-UI: `prplanit/dd-ui`
- Cyber Container Platform: `alott2223/cyber-container-platform`
- CoreVM: `corevm-team/corevm`
- WebKVM: `Slaker19/webkvm`
- OneClickVirt: `oneclickvirt/oneclickvirt`
- Corral: `tuna-os/corral`
- MFCloud Console: `mfconsole/kvm-manager`
- Flint: `flint-kvm/flint`
- VirtUI Manager: `pypi.org/project/virtui-manager`
- aqemu: `packages.debian.org/aqemu`
- virt-manager: `virt-manager.org`
- Kimchi: `kimchi-project/kimchi`
- Sylve: `pkg.go.dev/sylve`
- Pabawi: `example42/pabawi`
- PVMSS: `jhmmt/pvmss`
- Corsinvest cv4pve-admin: `Corsinvest/cv4pve-admin`
- Web Appliance Dashboard: `alflewerken/web-appliance-dashboard`
- Podling: `pkg.go.dev/podling`
- Warren: `pkg.go.dev/warren`
- Gubernator: `marioezquerro/gubernator`
- SimpleOrch: `simpleorch/control-plane`
- Janus: `osti.gov/biblio/3003095`
- SIGHUP Distribution: `pkg.go.dev/github.com/sighupio/fury-distribution`
