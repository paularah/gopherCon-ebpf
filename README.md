# eBPF for Developers 

[Link to slides]()

## Setting up your development environment

### macOS 

eBPF is currently only fully suported in Linux, so you a Linux VM to be able to use eBPF in a non-linux environment. The easiest and preferred way on macOS is a using [Lima](https://lima-vm.io/). 

Install Lima via brew

`brew install lima`

Start a Lima VM using the config file 

`limactl start --name ubuntu lima-config.yml`

This config file essentially replicates the Linux environment for ebpf development

### Linux(ubuntu)

## Learn More

* [ebpf.io](https://ebpf.io/)
* [eBPF docs](https://docs.ebpf.io/)
* [eBPF Go](https://ebpf-go.dev/)
* [eBPF documentary](https://www.youtube.com/watch?v=Wb_vD3XZYOA)