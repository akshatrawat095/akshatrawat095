# Akshat Rawat

Undergraduate Computer Science & Engineering student with a focus on operating systems, low-level C programming, and Linux kernel internals.

---

### Upstream Contributions

#### Linux Kernel ([`torvalds/linux`](https://github.com/torvalds/linux))

- **Micro Crystal RV-3028 RTC Driver Modernization**  
  [`55bb5877494d`](https://github.com/torvalds/linux/commit/55bb5877494d) · [`git.kernel.org`](https://git.kernel.org/pub/scm/linux/kernel/git/abelloni/linux.git/commit/?id=55bb5877494d)  
  * Replaced legacy `sprintf()` calls with `sysfs_emit()` in sysfs attribute callbacks to enforce `PAGE_SIZE` boundary checking as recommended in `Documentation/filesystems/sysfs.rst`.
  * Preserved full userspace ABI compatibility. Reviewed and accepted by RTC subsystem maintainer Alexandre Belloni.

- **Micro Crystal RV-3029 RTC Driver Modernization**  
  [Mailing List Thread](https://lore.kernel.org/linux-rtc/20261030105118.426-1-akshatrawat095@gmail.com/)  
  * Follow-up modernization replacing `sprintf()` in the hardware monitoring and update interval sysfs handlers with `sysfs_emit()`. Passed kernel static analysis (`checkpatch.pl`, `sashiko-bot`).

---

### Focus & Technical Interests

- **Systems Programming**: C, Linux Kernel Architecture, Device Drivers
- **Kernel Subsystems**: Real-Time Clocks (RTC), Sysfs API, Driver Frameworks
- **Tooling**: Git (`git send-email`, `checkpatch.pl`), WSL2/Linux, Bash

---

### Contact & Links

- **Email**: akshatrawat095@gmail.com
- **Public Archive**: [lore.kernel.org/all/?q=Akshat+Rawat](https://lore.kernel.org/all/?q=Akshat+Rawat)
