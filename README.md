# soft-sky: Pre-Built toolchain for RISCV
Up-to-date Prebuilt RISCV GNU toolchain for painless setup. No more build from source everytime. The purpose of this effort is to save time and computer resources for users and a contribution to eco-friendly computing practices.

### Supported Environment
Prebuilt riscv64 based binaries are built on Ubuntu 22 LTS and tested on Ubuntu 23.10. 

This repository makes use of GitHub actions to build the `riscv-gnu-toolchain` from source. Just download the prebuilt binaries, add to path and use.

### Available Configurations
- [ ]   RV64 Newlib
- [ ]   RV64 Linux
- [ ]   RV32 Newlib
- [ ]   RV32 GC
- [ ]   RV64-RV32 Multi-lib Cross Compiler

If you require a custom configuration, consider building yourself or open an Issue with tag:`Enhancement`

### Installation
1- Download prebuilt binaries from GitHub Actions > Artifacts
2- Create directory for sources. Preferred `/home/usr/` to avoid the possibility of toolchain affecting any of the system files.

```
$ sudo mkdir /home/usr/riscv    # Create a new directory
```
3- Extract the downloaded file and paste in newly created directory.
```
$ sudo tar -xzf riscv-toolchain.tar.gz -C /home/usr/riscv/
```
4- Add Path to your system environment variables
```
$ nano .bashrc                  # Open bashrc
$ export PATH=/home/usr/riscv/riscv-toolchain/bin:$PATH     # Add the path at the end
```

5- Save `.bashrc` (Ctrl+O, ENTER, Ctrl+X)
6- Apply Changes
```
$ source .bashrc
```
7- Add write permissions to the source folder
```
$ sudo chmod -R +x /home/usr/riscv/riscv-toolchain/
```
### Verify installation 
Run the following Command
```
$ riscv64-unknown-elf-gcc -v
```
- You should get
```
Using built-in specs.
COLLECT_GCC=riscv64-unknown-elf-gcc
COLLECT_LTO_WRAPPER=/home/aitesam961/riscv/riscv-toolchain/bin/../libexec/gcc/riscv64-unknown-elf/13.2.0/lto-wrapper
Target: riscv64-unknown-elf
```

Congratulations! You have successfully installed the riscv-gnu-toolchain without wasting your system resources.
### License
This project is licensed under the GNU General Public License v3.0 (GPL-3.0), ensuring that it remains open source and freely accessible to all. Feel free to explore, contribute, and use this software in compliance with the terms of the GPL-3.0 license. Embrace the spirit of collaboration and freedom in software development!

### Contributions
Contributions from developers like you make open source a vibrant and innovative space. To contribute to `soft-sky-riscv-gcc-prebuilt`, please follow the guidelines outlined in the `CONTRIBUTING.md` file. Your efforts are highly valued, and together, we can continue to enhance and improve the project for the entire community.
