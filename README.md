# Akshat Rawat

Undergraduate Computer Science & Engineering student focusing on Linux kernel internals, device drivers, and low-level systems programming in C.

---

### Upstream Linux Kernel ([`torvalds/linux`](https://github.com/torvalds/linux))

- **`rtc: rv3028: use sysfs_emit() instead of sprintf()`**  
  **Mainline Commit**: [`55bb5877494d`](https://github.com/torvalds/linux/commit/55bb5877494d6c99898b959aa593663ce4676f4e) · [`git.kernel.org`](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=55bb5877494d6c99898b959aa593663ce4676f4e)  
  **Merged by**: **Linus Torvalds** into `master` ([Commit `9b6f2eabc837`](https://github.com/torvalds/linux/commit/9b6f2eabc8372659cb4526d152c92e92c46f1406)) · **Tag**: `v7.4-rc1`  
  * Replaced legacy `sprintf()` calls with `sysfs_emit()` in sysfs attribute callbacks (`timestamp0_show`, `timestamp0_count_show`) to enforce `PAGE_SIZE` buffer boundary safety per `Documentation/filesystems/sysfs.rst`.
  * Reviewed and accepted by RTC subsystem maintainer Alexandre Belloni, prompting a subsequent subsystem-wide cleanup sweep across 10 sibling RTC drivers.

- **`leds: class-flash: use sysfs_emit() instead of sprintf()`**  
  **Submission**: [Mailing List Thread](https://lore.kernel.org/linux-leds/20261101033427.442-1-akshatrawat095@gmail.com/) · [Sashiko CI Review](https://sashiko.dev/#/patchset/20261101033427.442-1-akshatrawat095@gmail.com?part=1)  
  **Status**: Under review by LED subsystem maintainers Lee Jones & Pavel Machek for Linux 7.5.  
  * Completed the sysfs modernization of `drivers/leds/led-class-flash.c` by migrating remaining `_show()` attributes (`flash_brightness`, `max_flash_brightness`, `flash_strobe`, `flash_timeout`, `max_flash_timeout`) to buffer-safe `sysfs_emit()`.
  * Verified 0 errors and 0 warnings with `checkpatch.pl`; passed automated kernel test bots with no issues found.

---

### Technical Focus

- **Systems & Languages**: C (Linux Kernel Style), POSIX APIs, Bash, Python
- **Kernel Subsystems**: Real-Time Clocks (RTC), LED Subsystem, Sysfs Architecture, Character & Platform Devices
- **Upstream Workflow**: Git (`git send-email`, `git format-patch`), LKML / Subsystem Mailing Lists (`vger.kernel.org`), `checkpatch.pl`

---

### Links & Verification

- **Upstream Patch Archive**: [lore.kernel.org/all/?q=Akshat+Rawat](https://lore.kernel.org/all/?q=Akshat+Rawat)
- **Email**: akshatrawat095@gmail.com
- **LinkedIn**: [linkedin.com/in/akshat-rawat](https://www.linkedin.com/in/akshat-rawat/)
