# Akshat Rawat

[![Linux Kernel](https://img.shields.io/badge/Linux_Kernel-v7.4--rc1-222222?style=flat-square&logo=linux&logoColor=white)](https://github.com/torvalds/linux)
[![Mainline](https://img.shields.io/badge/Mainline_Status-Merged_by_Linus-success?style=flat-square&logo=git&logoColor=white)](https://github.com/torvalds/linux/commit/9b6f2eabc8372659cb4526d152c92e92c46f1406)
[![C](https://img.shields.io/badge/C-C99%2FC11-00599C?style=flat-square&logo=c&logoColor=white)](https://kernel.org)
[![Lore Archive](https://img.shields.io/badge/LKML-Public_Archive-orange?style=flat-square)](https://lore.kernel.org/all/?q=Akshat+Rawat)

Undergraduate Computer Science & Engineering student focusing on Linux kernel internals, device drivers, and low-level systems programming in C.

---

### Upstream Linux Kernel ([`torvalds/linux`](https://github.com/torvalds/linux))

| Subsystem | Driver / File | Change | Upstream Status |
| :--- | :--- | :--- | :--- |
| **RTC** | `drivers/rtc/rtc-rv3028.c` | Buffer safety: `sprintf()` → `sysfs_emit()` | **Merged by Linus Torvalds** ([`55bb5877494d`](https://github.com/torvalds/linux/commit/55bb5877494d6c99898b959aa593663ce4676f4e)) · `v7.4-rc1` |
| **LEDs** | `drivers/leds/led-class-flash.c` | Buffer safety: `sprintf()` → `sysfs_emit()` | **In Review** ([Mailing List](https://lore.kernel.org/linux-leds/20261101033427.442-1-akshatrawat095@gmail.com/)) · Passed Sashiko CI |

#### Details

- **Micro Crystal RV-3028 RTC Driver Modernization**  
  * Replaced legacy `sprintf()` calls with buffer-safe `sysfs_emit()` in sysfs attribute callbacks (`timestamp0_show`, `timestamp0_count_show`) to enforce `PAGE_SIZE` boundary checking per `Documentation/filesystems/sysfs.rst`.
  * Reviewed and applied by RTC maintainer Alexandre Belloni, prompting a subsequent subsystem-wide cleanup sweep across 10 sibling RTC drivers. Merged into mainline for **Linux 7.4-rc1** by **Linus Torvalds** ([Merge Commit `9b6f2eabc837`](https://github.com/torvalds/linux/commit/9b6f2eabc8372659cb4526d152c92e92c46f1406)).

- **LED Flash Class Subsystem Modernization**  
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
