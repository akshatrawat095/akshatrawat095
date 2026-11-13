# Akshat Rawat

[![Linux Kernel](https://img.shields.io/badge/Linux_Kernel-v7.4--rc1-222222?style=flat-square&logo=linux&logoColor=white)](https://github.com/torvalds/linux)
[![Mainline](https://img.shields.io/badge/Mainline_Status-Merged_by_Linus-success?style=flat-square&logo=git&logoColor=white)](https://github.com/torvalds/linux/commit/9b6f2eabc8371dea951c244f4aa9e013f36de9f8)
[![C](https://img.shields.io/badge/C-C99%2FC11-00599C?style=flat-square&logo=c&logoColor=white)](https://kernel.org)
[![Lore Archive](https://img.shields.io/badge/LKML-Public_Archive-orange?style=flat-square)](https://lore.kernel.org/all/?q=Akshat+Rawat)
[![GPG](https://img.shields.io/badge/GPG-F88A3F0F0733C500-green?style=flat-square&logo=gnu-privacy-guard&logoColor=white)](https://keys.openpgp.org/search?q=78D1E2AEE452FAD1DCFA313AF88A3F0F0733C500)

Undergraduate Computer Science & Engineering student focusing on Linux kernel internals, device drivers, and low-level systems programming in C.

---

### Upstream Linux Kernel ([`torvalds/linux`](https://github.com/torvalds/linux))

| Subsystem | Driver / File | Change | Upstream Status |
| :--- | :--- | :--- | :--- |
| **RTC** | `drivers/rtc/rtc-rv3028.c` | Buffer safety: `sprintf()` → `sysfs_emit()` | **Merged by Linus Torvalds** ([`55bb5877494d`](https://github.com/torvalds/linux/commit/55bb5877494d6c99898b959aa593663ce4676f4e)) · `v7.4-rc1` |
| **LEDs** | `drivers/leds/led-class-flash.c` | Buffer safety: `sprintf()` → `sysfs_emit()` (5 attributes) | **Applied by Lee Jones** ([`d9357f26370b`](https://git.kernel.org/pub/scm/linux/kernel/git/lee/leds.git/commit/?h=for-leds-next&id=d9357f26370b374cd18df38141600c80f5711c5e)) · `for-leds-next` (`v7.5`) |

#### Details

- **Micro Crystal RV-3028 RTC Driver Modernization**  
  * Replaced legacy `sprintf()` calls with buffer-safe `sysfs_emit()` in sysfs attribute callbacks (`timestamp0_show`, `timestamp0_count_show`) to enforce `PAGE_SIZE` boundary checking per `Documentation/filesystems/sysfs.rst`.
  * Reviewed and applied by RTC maintainer Alexandre Belloni, prompting a subsequent subsystem-wide cleanup sweep across 10 sibling RTC drivers. Merged into mainline for **Linux 7.4-rc1** by **Linus Torvalds** ([Merge Commit `9b6f2eabc837`](https://github.com/torvalds/linux/commit/9b6f2eabc8371dea951c244f4aa9e013f36de9f8)).

- **LED Flash Class Sysfs Modernization**  
  * Migrated 5 sysfs show callbacks (`flash_brightness_show`, `max_flash_brightness_show`, `flash_strobe_show`, `flash_timeout_show`, and `max_flash_timeout_show`) from `sprintf()` to `sysfs_emit()` to guarantee `PAGE_SIZE` buffer safety.
  * Reviewed and applied by LED subsystem maintainer Lee Jones into [`for-leds-next`](https://git.kernel.org/pub/scm/linux/kernel/git/lee/leds.git/commit/?h=for-leds-next&id=d9357f26370b374cd18df38141600c80f5711c5e) ([Commit `d9357f26370b`](https://git.kernel.org/pub/scm/linux/kernel/git/lee/leds.git/commit/?h=for-leds-next&id=d9357f26370b374cd18df38141600c80f5711c5e)) queued for the upcoming **Linux 7.5** merge window.

---

### Technical Focus

- **Systems & Languages**: C (Linux Kernel Style), POSIX APIs, Bash, Python
- **Kernel Subsystems**: Real-Time Clocks (RTC), LED Subsystem, Sysfs & Driver Infrastructure
- **Upstream Workflow**: Git (`git send-email`, `git format-patch`), LKML / Subsystem Mailing Lists (`vger.kernel.org`), `checkpatch.pl`

---

### Links & Verification

- **Upstream Patch Archive**: [lore.kernel.org/all/?q=Akshat+Rawat](https://lore.kernel.org/all/?q=Akshat+Rawat)
- **PGP Key Fingerprint**: [`78D1 E2AE E452 FAD1 DCFA  313A F88A 3F0F 0733 C500`](https://keys.openpgp.org/search?q=78D1E2AEE452FAD1DCFA313AF88A3F0F0733C500)
- **Email**: akshatrawat095@gmail.com
