# Hi, I'm Mattéo

Master's student focused on **high-performance C++**, **GPU programming**, **real-time graphics**, **simulation**, and **low-level systems**.

I like projects where performance depends on understanding what happens below the abstraction layer: memory layout, cache behavior, parallelism, GPU execution, synchronization, resource management, and operating-system constraints.

I'm currently looking for an internship in **GPU / CUDA, HPC, simulation, graphics, or low-level C++ development**.

## Featured projects

### [fluid-simulator](https://github.com/JustARandomBadDev/fluid-simulator)

Real-time **3D SPH fluid simulator** used as a performance-engineering project across CPU and GPU implementations.

The project started from a straightforward CPU solver and was progressively optimized while keeping each step measurable:

- SPH density, pressure, viscosity and integration
- uniform-grid neighbor search over 27 surrounding cells
- Structure-of-Arrays particle storage
- OpenMP multicore parallelism
- explicit SIMD / AVX2 vectorization
- CUDA compute backend
- Vulkan real-time rendering
- reproducible benchmark suite across particle counts and thread counts
- CPU/GPU profiling and backend comparisons
- numerical and algorithmic tests
- Linux CI with sanitizers and automated validation

The main goal is not only to make the simulation faster, but to **measure where the speedup comes from and understand the bottlenecks of each implementation**.

**Tech:** C++20 · CUDA · AVX2 · OpenMP · Vulkan · GLSL · CMake

---

### [voxel-engine](https://github.com/JustARandomBadDev/voxel-engine)

#### Demo: [voxel-sandbox](https://github.com/JustARandomBadDev/voxel-sandbox)

Reusable **C++20 / Vulkan voxel engine** with a separate procedural-world demo application.

#### Engine

- chunk-based voxel world
- visible-face meshing with cross-chunk invalidation
- separate opaque and transparent geometry paths
- CPU mesh cache and explicit CPU → GPU synchronization
- paged GPU buffer suballocation
- reusable allocation ranges
- batched staging uploads
- indexed indirect drawing
- swapchain recreation and frames-in-flight synchronization
- engine API decoupled from the host windowing layer

#### Sandbox

- procedural terrain generation
- chunk streaming around the camera
- independent load/unload distances
- large static and dynamic world demonstrations
- reproducible performance scenarios

The repositories include **visual demos, architecture documentation, frame/meshing/upload measurements, CI, sanitizers, and targeted tests** for the non-graphics algorithms and resource-management code.

**Tech:** C++20 · Vulkan · GLSL · CMake · GLM

---

### Guest Wi-Fi platform

A real guest-access system deployed for a camping site, split into application and infrastructure repositories.

#### [admin-portal](https://github.com/JustARandomBadDev/admin-portal)

Go application used to manage temporary Wi-Fi access:

- temporary credential generation
- ticket lifecycle and expiration
- PostgreSQL persistence
- FreeRADIUS synchronization
- versioned migrations
- revocable administrator sessions
- thermal-printer workflow
- operational maintenance tooling

#### [guest-access-infra](https://github.com/JustARandomBadDev/guest-access-infra)

Infrastructure supporting the platform:

- OPNsense captive access
- FreeRADIUS / PostgreSQL
- UniFi network management
- reverse proxying
- Prometheus / Grafana / Loki monitoring
- SNMP and availability monitoring
- database backup / restore workflows
- Docker Compose multi-stack deployment
- scoped RADIUS clients and hardened service exposure
- public configuration sanitized from production secrets and site-specific topology

This project is interesting to me because it is not a lab-only setup: it combines **networking, authentication, observability, deployment and software used in a real environment**.

**Tech:** Go · PostgreSQL · FreeRADIUS · OPNsense · Docker · Prometheus · Grafana · Linux networking

---

### [crowd-beats-api](https://github.com/JustARandomBadDev/crowd-beats-api)

Concurrent backend for a collaborative music queue.

- transactional PostgreSQL domain model
- database-enforced invariants
- concurrent voting and queue operations
- REST + WebSocket synchronization
- bounded clients and backpressure handling
- Spotify API integration
- unit, race and integration tests
- Docker and GitHub Actions

This project is less performance-oriented than my C++ work, but it demonstrates my approach to **concurrency, correctness, testing and production-style architecture**.

**Tech:** Go · PostgreSQL · WebSocket · Docker

---

## Other low-level work

### [sOS](https://github.com/JustARandomBadDev/sOS)

x86 operating-system learning project exploring the boot path from BIOS toward a freestanding kernel.

Topics explored include:

- BIOS boot and multi-stage loading
- MBR / VBR structures
- INT 13h LBA disk access
- FAT32 internals
- A20 and GDT setup
- protected mode
- freestanding C
- VGA memory access
- custom cross-compilation and linking

**Tech:** x86 Assembly · C · QEMU · GCC cross-toolchain

## Technical focus

### Performance & parallel computing

- data-oriented C++
- cache-aware data structures
- multicore programming
- OpenMP
- SIMD / AVX2
- CUDA
- profiling and benchmarking

### Graphics & GPU

- Vulkan
- explicit GPU resource management
- synchronization
- staging and device-local memory
- indirect rendering
- GLSL
- GPU compute

### Simulation & algorithms

- SPH fluid simulation
- spatial partitioning
- uniform grids
- voxel meshing
- procedural generation
- CPU ↔ GPU execution models

### Systems

- Linux
- x86 / boot process
- networking
- containers
- observability
- PostgreSQL
- RADIUS / AAA

## Main stack

**Languages**  
C++ · C · CUDA C++ · Go · x86 Assembly · Python

**Performance / GPU**  
CUDA · Vulkan · OpenMP · AVX2 · GLSL . OpenGL

**Systems**  
Linux · Docker · PostgreSQL · FreeRADIUS · OPNsense

**Tooling**  
CMake · Git · GitHub Actions · QEMU · sanitizers · profiling tools

## Internship interests

I'm looking for opportunities involving one or more of:

- **GPU programming / CUDA**
- **HPC and parallel computing**
- **numerical or physical simulation**
- **real-time graphics / rendering**
- **performance-oriented C++**
- **engine and systems development**
- **CPU/GPU optimization and profiling**

I'm especially interested in teams working on problems where **hardware behavior, memory, parallelism and algorithmic choices have a measurable impact on performance**.
