# 🛠️ fridaDownloader

fridaDownloader is a command-line tool that streamlines downloading the Frida Gadget or Server for Android, enabling developers and security researchers to quickly access the components needed for dynamic instrumentation.

## Features

- **Download Options**: Easily download either the Frida Gadget or Server for Android.
- **Latest Version**: Use the `--last-version` option to download the most recent version of Frida.
- **Specific Version**: Specify a particular version of Frida to download using the `--version VERSION` option.
- **Target Selection**: Choose the target for download with the `--target` option, allowing you to select either `gadget` or `server`.
- **Architecture Support**: Select the appropriate Android architecture with the `--architecture` option. Supported architectures include:
  - `arm`
  - `arm64`
  - `x86`
  - `x86_64`
- **Custom Output Directory**: Use the `--output` option to specify a directory for saving the downloaded file, with a default location of `~/Downloads`.

## Installation

### Manual:

1. Clone the repository:

```bash
git clone https://github.com/mateofumis/fridaDownloader.git
cd fridaDownloader
```

2. Set up a virtual environment (optional but recommended):

```bash
python3 -m venv env
source env/bin/activate  # On Windows use `.\env\Scripts\activate`
```

3. Install dependencies:

```bash
pip3 install -r requirements.txt
```

### Using pip (or pipx) install

- Install fridaDownloader with pip3

```bash
pip3 install fridaDownloader 
```
- Install fridaDownloader with pipx

```bash
pipx install fridaDownloader 
```

See this project on PyPi: [https://pypi.org/project/fridaDownloader/](https://pypi.org/project/fridaDownloader/) 

## Usage

```bash
$: fridaDownloader -h

*********************************************
*  Welcome to the Frida Downloader          *
*                           by hackermater  *
*********************************************

usage: fridaDownloader.py [-h] [--last-version] [--version VERSION] --target {gadget,server} [--architecture ARCHITECTURE]
                          [--output OUTPUT]

Download Frida Gadget or Server for Android

options:
  -h, --help            show this help message and exit
  --last-version        Download the latest version of Frida
  --version VERSION     Download a specific version of Frida
  --target {gadget,server}
                        Specify the target to download: gadget or server
  --architecture ARCHITECTURE
                        Android architecture (default: arm). Options: arm, arm64, x86, x86_64
  --output OUTPUT       Directory to save the downloaded file (default: ~/Downloads)
```

## Examples

- Download the last version of Frida Server for x86 architecture:

```bash
python3 fridaDownloader.py --target server --architecture x86 --last-version
```

- Download a specific version of Frida Gadget for arm64 architecture with specific output:

```bash
python3 fridaDownloader.py --target gadget --architecture arm64 --version 15.2.0 --output ~/Frida/Gadget/frida-gadget-arm64
```

## License

This project is licensed under the Apache License 2.0 - see the LICENSE file for details.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue.

## 🧡 Support me with a virtual Coffee! 🧡

[![Ko-Fi](https://storage.ko-fi.com/cdn/brandasset/kofi_button_stroke.png)](https://ko-fi.com/hackermater)
