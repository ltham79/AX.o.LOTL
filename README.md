![AX.o.LOTL Splash Screen](https://github.com/ltham79/AX.o.LOTL/assets/139496887/9046e40e-0958-4afb-99f1-335dfc578510)

# AX.o.LOTL - Living Off The Land

AX.o.LOTL (Living Off The Land) is designed to assist in the exploitation and post-exploitation phases of penetration testing. AX.o.LOTL provides easy access to various living-off-the-land techniques for both Linux and Windows environments without leaving your terminal.




## Features

- **LOTL Functionality**: The `LOTL` function provides a user-friendly interface to search for and select living-off-the-land techniques for a given binary name.
- **Colorful UI**: AX.o.LOTL presents a colorful and interactive user interface.
- **Linux or Windows binaries**: Searches for Linux or Windows binaries with a simple argument change from https://gtfobins.github.io/ (for Linux Binaries) and https://lolbas-project.github.io/ (for Windows).

## Installation

1. Clone the repository to your local machine:

    ```bash
    git clone https://github.com/ltham79/AXoLOTL.git
    ```

2. Make the script executable:

    ```bash
    cd AXoLOTL
    chmod +x axolotl.sh
    ```

## Dependencies

The following dependencies are required to run AX.o.LOTL:

- **curl**: Used for making HTTP requests to retrieve data from online resources.
- **pup**: A command-line HTML parser used to extract specific elements from web pages.
- **awk**: A versatile programming language for working with structured text data.

### Installing Dependencies

You can install the dependencies on Debian/Ubuntu-based systems using the following command:

```bash
sudo apt-get install curl awk
```

For installing `pup`, you can download the binary from the [GitHub Releases page](https://github.com/ericchiang/pup/releases) and place it in your PATH.

On macOS, you can install `curl` and `awk` using Homebrew:

```bash
brew install curl gawk
```

To install `pup` on macOS, you can use Homebrew as well:

```bash
brew install pup
```

On other operating systems, please refer to the respective package manager or manual installation instructions for each dependency.

## Usage

![Screenshot](https://github.com/ltham79/AX.o.LOTL/assets/139496887/88e094e2-6810-414e-8fe2-fc5e4ea3fea3)

To run AX.o.LOTL, execute the `axolotl.sh` script with appropriate arguments:

```bash
./axolotl.sh <binary_name> <-l/-w>
```

- `<binary_name>`: The name of the binary you want to search for.
- `-l`: Search for Linux living-off-the-land techniques.
- `-w`: Search for Windows living-off-the-land techniques.

Example:

```bash
./axolotl.sh curl -l
```

## Issues
There are a few issues that I havent gotten around to fixing. Mainly in the way the script scrapes the webpages. For instance if there is more than one "exploit" for a given binary function it only displays the first one. Also when querying https://lolbas-project.github.io/ (for Windows) there can be a few problems as they do not follow the same HTML structure and I just didnt want to deal with it feel free to do so yourself. :-)

## Credits

AX.o.LOTL is maintained by [Psiber_Syn](https://github.com/ltham79). The tool is inspired by various living-off-the-land techniques and resources available online from https://gtfobins.github.io/ (for Linux Binaries) and https://lolbas-project.github.io/ (for Windows) both without whom this wouldnt be possible. Props to the creators hard work!!!

## License

This project is licensed under the [MIT License](LICENSE).
