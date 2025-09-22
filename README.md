# DeepErase

**DeepErase** is an open-source graphical tool for Linux to securely wipe entire storage devices.  
It is built with Lazarus/FPC and aims to provide a simple and reliable user interface for secure erasure.

---

## Features (planned / in progress)

- Securely wipe entire block devices (HDDs / SSDs / NVMe).
- Support for multiple erasure methods:
  - Zero pass
  - Random pass
  - Multi-pass standards (e.g. DoD, GOST)
- Awareness of SSDs/NVMe:
  - Integration with `hdparm` (ATA Secure Erase)
  - Integration with `nvme-cli` (Sanitize / Format)
- Optional free-space wiping.
- Simulation mode (dry-run) using `/dev/null` or RAM-based targets.
- Progress display and log output.
- Open Source, extensible architecture.

---

## Project Goals

DeepErase is intended to be the **Linux equivalent of Eraser for Windows**, with a strong focus on:

- **Simplicity:** easy-to-use graphical interface.  
- **Reliability:** based on well-known Linux tools (`dd`, `hdparm`, `nvme-cli`).  
- **Transparency:** clear reporting and open source code.  
- **Modern storage awareness:** proper handling of SSDs/NVMe drives, not just HDDs.  

---

## Status

- Current stage: **early prototype (v0)**  
- Implemented: Lazarus GUI, integration with `dd` (dry-run support, output parsing).  
- Next steps: progress bar improvements, wipe profiles, device detection.

---

## License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

## Contributing

Contributions are welcome! Planned areas include:
- Adding more wipe profiles.
- Improving device detection and safety checks.
- Expanding the GUI with settings and logs.
- Writing documentation and tutorials.

---

## Roadmap

- **v0** – Lazarus GUI + `dd` backend + dry-run simulation.  
- **v1** – Add wipe profiles (DoD, GOST, etc.) + free-space wipe.  
- **v2** – Device type detection (HDD/SSD/NVMe) + integration with `hdparm` / `nvme-cli`.  
- **v3** – Verification mode + reporting system + packaging.  

---

## Disclaimer

DeepErase is a tool that can **irreversibly destroy data**.  
Always test with the *simulation mode* before using it on real hardware.  
Use at your own risk.
