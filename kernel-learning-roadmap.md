# Kernel Learning Roadmap — CentOS Kernel Community Bangladesh
*A curated path from zero to first upstream patch. Link to existing resources rather than rewriting them.*

## Stage 0: Foundations (1–2 weeks)
Goal: comfortable with Linux and C basics.
- [ ] Use Linux daily (any distro) — terminal, packages, permissions
- [ ] C refresher: pointers, structs, memory management
- [ ] Git basics: clone, branch, commit, send patches via email
- [ ] Read: "Linux Kernel in a Nutshell" (free) — chapters 1–3

## Stage 1: Build your first kernel (1 week)
Goal: compile and boot a kernel you built yourself.
- [ ] Clone mainline or CentOS Stream kernel source
- [ ] Configure with `make defconfig` / `make menuconfig`
- [ ] Build with `make -j$(nproc)`, install modules, boot it in a VM
- [ ] Learn to read `dmesg` and `/proc` / `/sys`
- Milestone: screenshot of `uname -r` showing your custom kernel

## Stage 2: Kernel modules (2–3 weeks)
Goal: write, load, and debug a simple module.
- [ ] "Hello world" module: init/exit, `printk`, `insmod`/`rmmod`
- [ ] Module parameters, char device basics
- [ ] Debugging: `dmesg`, `ftrace`, `printk` levels
- [ ] Common pitfalls: locking basics, memory allocation (kmalloc vs vmalloc)
- Milestone: a GitHub repo with 2–3 small modules and a README

## Stage 3: CentOS Stream kernel (2 weeks)
Goal: understand how the distro kernel differs from mainline.
- [ ] How CentOS Stream sits between Fedora and RHEL (upstream → Stream → RHEL)
- [ ] Fetch the CentOS Stream kernel SRPM / git source
- [ ] Apply a config change, rebuild the Stream kernel package
- [ ] File layout: specs, patches, configs in the Stream kernel repo
- Milestone: successful local build of the CentOS Stream kernel package

## Stage 4: eBPF and tracing (2–3 weeks, optional but high value)
Goal: use modern kernel observability.
- [ ] eBPF concepts: programmes, maps, verifier
- [ ] Write a simple `bpftrace` one-liner and a small BCC/libbpf tool
- [ ] Trace a syscall or network event on your test VM
- Milestone: demo at a meetup

## Stage 5: First upstream contribution (ongoing)
Goal: get a patch accepted.
- [ ] Find "good first issues": kernel `TODO`, `staging` cleanups, docs fixes
- [ ] Learn `checkpatch.pl`, commit message conventions
- [ ] Submit via mailing list / GitHub (depending on subsystem)
- [ ] Review someone else's patch in the community
- Milestone: 🎉 first patch merged — we celebrate this as a community!

## How we'll run this together
- **Weekly study check-ins** in Telegram/Discord
- **Monthly workshop** per stage (recorded)
- **Patch-review circle**: bring a patch, we review it together before you send it

## Key links to curate (add your favourites)
- CentOS Stream kernel source and docs (centos.org)
- kernel.org documentation and "Linux Kernel Labs"
- eBPF.io and bpftrace guides

---
*Keep this roadmap in your GitHub org README so newcomers always know where to start.*
