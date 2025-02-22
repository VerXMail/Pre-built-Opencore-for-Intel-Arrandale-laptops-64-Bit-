
# Pre-built Opencore with macOS Big Sur installer for Intel Arrandale laptops (64-Bit).

**Project Description:**

This project provides a pre-built OpenCore EFI configuration specifically tailored for Intel Arrandale-based laptops (1st Gen Intel Core i3/i5/i7 processors, e.g., Core i5-520M). It includes a ready-to-use macOS Big Sur installer, enabling users to easily install or run macOS Big Sur on compatible Arrandale laptops. The EFI folder is optimized for these systems, ensuring proper hardware compatibility, including graphics, audio, and other essential components.

**Who is it for?**
- **Hackintosh enthusiasts** who want to run macOS Big Sur on older Intel Arrandale laptops.
- **Users with limited technical expertise** who need a pre-configured OpenCore EFI to simplify the installation process.
- **Developers or testers** looking for a stable macOS environment on legacy hardware.

This project aims to make the Hackintosh process more accessible and user-friendly for Arrandale laptop owners.


# **For Legacy BIOS**

**Make the USB Drive using Windows-**

Download the source code .zip and extract the zip file. Now, insert your USB Drive and do as like as written below:
1. Run command prompt as administrator.
2. Use these commands-
`diskpart` and then `list disk` and then `select Disk 1` (replace 1 with your the disk number of your USB Drive.) and then `clean` and then `convert GPT` (if it isn't already in GPT Partitioning Scheme.)
3. Close the terminal and open Disk Management.
4. Create a FAT32 partition on your USB Drive.
5. Now, download [BOOTICE](https://www.majorgeeks.com/files/details/bootice_64_bit.html) and run it.
6. Restore MBR from the `boot0` file and PBR from the `boot1f32` file. These files are included in the `Tools` folder.
7. Copy everything from `ForLegacyBIOS` folder to the root of your USB Drive.

**Now you are ready to boot macOS from your USB Drive.**

**Make the USB Drive using macOS-**

1. Open a terminal and cd to the `Tools` folder.
2. Run command- `sudo chmod +x BootInstall_X64.tool` or `sudo chmod +x BootInstall_IA32.tool` depending on your OS architecture.
3. Run command- `sudo ./BootInstall_X64.tool` or `sudo ./BootInstall_IA32.tool` depending on your OS architecture.
4. Follow the on-screen instructions to complete installing Duet on your USB Drive.
5. Copy everything from `ForLegacyBIOS` folder to the root of your USB Drive.

**Now you are ready to boot macOS from your USB Drive.**

# **For UEFI Systems**

1. Insert your USB Drive and convert it to GPT (if it isn't already in GPT Partitioning Scheme.).
2. Create a FAT32 partition.
3. Simply copy everything from `ForUEFISystems` folder to the root of your USB Drive.

**Now you are ready to boot macOS from your USB Drive.**

# **Credits**

All credits goes to [Apple](https://www.apple.com/) and [Opencore](https://dortania.github.io/OpenCore-Install-Guide/).
