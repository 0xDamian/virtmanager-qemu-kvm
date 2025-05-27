# QEMU/KVM and Virt-Manager Notes

This repository contains concise documentation, command references, and configurations related to virtualisation using QEMU/KVM and virt-manager on Linux.

## Contents

- Installation steps
- VM creation and management
- Bridged networking setup
- Tips for GPU passthrough
- Troubleshooting common issues 
- CLI and GUI usage notes 


## Tools Covered

- QEMU
- KVM
- virt-manager
- virsh

## System Requirements

- Linux with KVM support (`/dev/kvm` accessible)
- `libvirt`, `qemu`, `virt-manager` installed
- Systemd-based distro (e.g., Ubuntu, Linux Mint)

> **Note:**
> This documentation would work for anybody; however, Linux systems that are not systemd-based (eg, rc-service) name some packages differently. Simply find the alternative names and install them to follow along.

## License

MIT License
