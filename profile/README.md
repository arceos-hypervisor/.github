# ArceOS-Hypervisor 👋

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

The unified modular hypervisor based on a modular unikernel, [ArceOS](https://github.com/arceos-org/arceos)

https://arceos-hypervisor.github.io/doc/

Welcome to join our **[Discussions](https://github.com/orgs/arceos-hypervisor/discussions)**.

## Design Goal

This project originated from the [discussion/13](https://github.com/orgs/rcore-os/discussions/13) of [rCore-OS](https://github.com/rcore-os) community.

In general, this project hopes to add virtualization support crates/modules based on ArceOS unikernel, 
and build a modular hypervisor that supports multiple architectures based on the basic OS functions provided by ArceOS unikernel.

We hope to make the hypervisor as modular as possible and minimize modifications to the arceos kernel code.

## Components

ArceOS-hypervisor is mainly composed of the following independent components:

* [vmm-app](https://github.com/arceos-hypervisor/arceos-umhv/tree/master/arceos-vmm): a user app of ArceOS, acts like a VMM (Virtual Machine Monitor)
* [axvm](https://github.com/arceos-hypervisor/axvm): responsible for **resource management** within each VM
* [axvcpu](https://github.com/arceos-hypervisor/axvcpu): providing virtual CPU management
* [axdevice](https://github.com/arceos-hypervisor/axdevice): for emulated device management
* [axaddrspace](https://github.com/arceos-hypervisor/axaddrspace): for address space management
* [x86_vcpu](https://github.com/arceos-hypervisor/x86_vcpu): basic virtualization support for x86_64 architecture
* [arm_vcpu](https://github.com/arceos-hypervisor/arm_vcpu): basic virtualization support for ARM (aarch64) architecture
* [riscv_vcpu](https://github.com/arceos-hypervisor/riscv_vcpu): basic virtualization support for RISC-V architecture
* [axdevice_base](https://github.com/arceos-hypervisor/axdevice_crates/tree/main/axdevice_base): provides basic traits and structures for emulated devices
* [arm_vgic](https://github.com/arceos-hypervisor/arm_vgic): virtual GIC implementation for ARM.
  
