# eBPF for Go Developers

GopherCon 2025

[Link to slides](https://docs.google.com/presentation/d/1_cyzyGsLsq5P_1zcEJ_ZX9EDmHWyHsGThsw6ijcK8Rg/edit?usp=sharing)

## Setting up your development environment

### Linux(ubuntu)

Install these dependencies. If you're using a distro that is not debian based, you most likely might different dependencies from the ones listed here. A quick google search should point you in the right direction.

```
sudo apt install -y clang llvm libbpf-dev linux-headers-$(uname -r)

# Debian/Ubuntu quirk: ensure asm headers are reachable
sudo ln -sf /usr/include/asm-generic /usr/include/asm

```

### macOS

eBPF is currently only fully suported in Linux, so you need a Linux VM to be able to use eBPF in a non-linux environment. The easiest and preferred way on macOS is a using [Lima](https://lima-vm.io/).

Install Lima via brew

`brew install lima`

Start a Lima VM using the config file

`limactl start --name ubuntu lima-config.yml`

This config file essentially replicates the ubuntu environment for ebpf development in a VM


## Compile and run the ebpf code & userspace Go code

List the interfaces on your pc using `ip -br a`, then change the `ifname` variable to a active interface. THe eBPF program is now attaced this interface.

`go generate && go build && sudo ./gophercon-ebpf`

## Learn More

* [ebpf.io](https://ebpf.io/)
* [eBPF docs](https://docs.ebpf.io/)
* [eBPF Go](https://ebpf-go.dev/)
* [eBPF documentary](https://www.youtube.com/watch?v=Wb_vD3XZYOA)
