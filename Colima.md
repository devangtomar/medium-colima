**Colima (Containers on Linux on Mac) 🐳**

**What is Colima? 🤔**

Colima is built on Lima, which generates a QEMU VM with an HVF accelerator and handles port forwarding and folder sharing. Lima has ***containerd*** and ***nerdctl***, but a Docker container runtime is necessary for a drop-in replacement, which is what Colima is for.

Colima installs the Docker container runtime in a Lima virtual machine, configures the Docker CLI on macOS, and handles port forwarding and volume mounts. Docker, like Docker Desktop, is now simply accessible on macOS without any settings.

It’s a command line program that builds on top of lima to give a more convenient and full Docker Desktop alternative, and it already shows a lot of potential. Getting started with Colima is very simple as long as you already have [brew](https://brew.sh/) and [Xcode](https://developer.apple.com/xcode/) command line tools installed.

**GitHub Repository link 🔐**

