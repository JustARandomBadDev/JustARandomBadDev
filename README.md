# Hi, I'm Mattéo 👋

I'm a Master's student in Computer Science at UBS in Vannes, France.

I'm mainly interested in **low-level programming**, **computer graphics**, **GPU computing** and **system architecture**. Most of my projects are built around understanding how things work internally, from memory management and rendering to operating systems and network infrastructure.

I'm currently looking for a **6-month internship starting in January 2027**.

## Main projects

### Voxel Engine

A modular voxel engine ecosystem written in **C++20** using **Vulkan**.

The project is split into two repositories:

* **[voxel-engine](https://github.com/JustARandomBadDev/voxel-engine)** — the reusable engine library
* **[voxel-sandbox](https://github.com/JustARandomBadDev/voxel-sandbox)** — a minimal client application used to test and demonstrate the engine

The engine currently includes:

* Explicit CPU and GPU memory management
* Vulkan rendering and synchronization
* Shaders and compute shaders
* Dynamic chunk and mesh generation
* Separation between world, engine and graphics systems
* A public API that does not expose Vulkan or GLFW types
* Integration into external projects through CMake

The long-term goal is to build a fully modular engine where features can be added through dynamically loaded `.so` modules without modifying the core engine.

### [OS From Scratch](https://github.com/JustARandomBadDev/sos)

A minimal operating system built from scratch using **C and Assembly**.

* Boot process and kernel development
* Memory management
* Interrupt handling
* Low-level hardware interaction

### [Camping Infrastructure](https://github.com/JustARandomBadDev/camping-infra)

A complete network infrastructure designed and deployed for a holiday campsite.

* Network segmentation using VLANs
* OPNsense firewall and captive portal
* FreeRADIUS and PostgreSQL authentication
* Docker-based services and monitoring
* Administration portal for Wi-Fi access management

## Technologies

* **Languages:** C++, C, Rust, Go, Python, Assembly
* **Graphics and GPU:** Vulkan, GLSL, OpenGL, Cuda
* **Systems:** Linux, memory management, multithreading
* **Infrastructure:** Docker, OPNsense, PostgreSQL, FreeRADIUS, networking

## Currently working on

* Designing the module system for my voxel engine
* Improving its architecture and performance
* Exploring GPU computing and CUDA
* Continuing the development of my operating system
* Cleaning and documenting my existing projects
