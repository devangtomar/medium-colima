**Colima (Containers on Linux on Mac) 🐳**

**What is Colima? 🤔**

Colima is built on Lima, which generates a QEMU VM with an HVF accelerator and handles port forwarding and folder sharing. Lima has ***containerd*** and ***nerdctl***, but a Docker container runtime is necessary for a drop-in replacement, which is what Colima is for.

Colima installs the Docker container runtime in a Lima virtual machine, configures the Docker CLI on macOS, and handles port forwarding and volume mounts. Docker, like Docker Desktop, is now simply accessible on macOS without any settings.

It’s a command line program that builds on top of lima to give a more convenient and full Docker Desktop alternative, and it already shows a lot of potential. Getting started with Colima is very simple as long as you already have [brew](https://brew.sh/) and [Xcode](https://developer.apple.com/xcode/) command line tools installed.

**GitHub Repository link 🔐**

<https://github.com/abiosoft/colima>

**Intro GIF 📌**

**Installation and Setup ⚙️**

Installation is easy and can be done through Homebrew:

brew install colima

To start the VM we run:

colima start


It will start the docker daemon in the VM and configure the docker CLI on the host. The usage in macOS is no different from Docker Desktop, and all docker commands should work as before.

**Features 💯**

- Intel and M1 Macs support
- Simple CLI interface
- Docker and Containerd support
- Port Forwarding
- Volume mounts
- Kubernetes

**Changing VM size 🛐**

The default VM may be on a tiny side, especially if you opt to run Kubernetes as well.

To give your VM greater resources, use

colima stop

followed by

colima start — cpu 6 — memory 6.

This will provide your **Colima VM 6 CPU cores and 6GB of RAM**. You can get a full list of options by simply running colima and pressing enter.

*More about that here : [https://github.com/abiosoft/colima#customizing-the-vm*](https://github.com/abiosoft/colima#customizing-the-vm)*

**Kubernetes ☸️**

**kubectl** is required for Kubernetes. Installable with

brew install kubectl

To enable Kubernetes, start Colima with --with-kubernetes flag.

colima start --with-kubernetes

**More Usage options 📜**

colima --help

