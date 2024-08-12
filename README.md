<p align="center">
  <img src="assets/Sherlock.png" alt="SherlockElf" width="104" height="171"/>
  <img src="assets/Font.png" alt="SherlockElf" width="233" height="60"/>
</p>

**SherlockElf** мощный инструмент, предназначенный как для статического, так и для динамического анализа двоичных файлов Android ELF и динамического анализа двоичных файлов iOS Macho-O (экспериментальный). Он помогает исследователям безопасности, разработчикам и реверс-инженерам получить представление о двоичных файлах ELF (Executable and Linkable Format), используемых в приложениях Android, и двоичных файлах Mach-O (Mach Object), используемых в приложениях iOS.
<br>
<p align="center">
  <img src="assets/Emu.gif" alt="Emu"/>
</p>

## Features ✨

- **Static Analysis**: Extracts and analyzes metadata, headers, and sections from ELF binaries.
- **Dynamic Analysis**: Executes and monitors ELF and Mach-O (experimental) binaries to observe runtime behavior and identify potential vulnerabilities.
- **User-friendly Interface**: Intuitive command-line interface for easy interaction.
- **Comprehensive Reports**: Generates detailed analysis reports for further inspection.
- **Cross-platform Support**: Works seamlessly on multiple platforms including Windows, macOS, and Linux.

## Installation 🛠️

To get started with SherlockElf, follow these steps:

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/iamtorsten/SherlockElf.git
    cd SherlockElf
    ```

2. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Setup Environment**:
- Magisk or [KernelSU](https://github.com/tiann/KernelSU) rooted Android Phone or Tablet
- Jailbroken iOS Device (experimental)
- Running Frida Server on Phone or Tablet
- Installed Frida Tools on PC

## Usage 🚀

Using SherlockElf is straightforward. Below are some common commands and their descriptions:

- **Static Analysis**:
    ```bash
    python emulate.py
    ```
    This command performs a static analysis on the specified ELF binary and outputs the results.
<br><br>
- **Dynamic Analysis**:
    ```python
    with open("hook/mem.js") as f:
        script_code = f.read()

    device, session = Inject(target=target).attach()
    script = session.create_script(script_code)
    script.on('message', on_message)
    script.load()
    ```
    This command executes the ELF binary and monitors its memory behavior.

## Contributing 🤝

We welcome contributions from the community! If you'd like to contribute to SherlockElf, please follow these steps:

1. **Fork the Repository**: Click the "Fork" button at the top right of this page.
2. **Clone Your Fork**:
    ```bash
    git clone https://github.com/iamtorsten/SherlockElf.git
    ```
3. **Create a Branch**:
    ```bash
    git checkout -b feature-branch
    ```
4. **Make Your Changes** and **Commit**:
    ```bash
    git commit -am 'Add new feature'
    ```
5. **Push to Your Fork**:
    ```bash
    git push origin feature-branch
    ```
6. **Create a Pull Request**: Navigate to the original repository and submit a pull request.

## License 📜

SherlockElf is licensed under the MIT License. See the [LICENSE](https://github.com/iamtorsten/SherlockElf/blob/main/LICENSE) file for more information.

## Contact 📬

For any questions or feedback, please reach out via email at [torsten.klinger@googlemail.com](mailto:torsten.klinger@googlemail.com).

## Disclaimer ⚖️

This Project is just for personal educational purposed only. You can modify it for your personal used. But i do not take any resonsibility for issues caused by any modification of this project. All processes illustrated in the project serve only as examples. <br><br>**Use of this code must comply with applicable laws.**

## Thanks 🙏

- [Frida](https://github.com/frida/frida)
- [Capstone](https://www.capstone-engine.org)
- [Keystone](https://docs.openstack.org/keystone/latest/#top)
- [Unicorn](https://www.unicorn-engine.org/)
- [ExAndroidNativeEmu](https://github.com/maiyao1988/ExAndroidNativeEmu)

