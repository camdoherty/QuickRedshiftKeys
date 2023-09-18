# QuickRedshiftKeys

## Overview

`QuickRedshiftKeys` is a simple one-liner that allows you to set up keyboard shortcuts for quick adjustments of color temperature and brightness using Redshift on Linux systems. This is particularly useful for media PCs where quick adjustments might be necessary.

## Prerequisites

- Linux Operating System (Tested on Mint)
- Redshift installed
- Xbindkeys installed

## Installation

1. Run the following command to append the configuration to your existing `.xbindkeysrc` file. If the file doesn't exist, it will be created.

    ```bash
    echo -e "\"redshift -P -O 1000 -b 0.1\"\n  Control+Shift + 1\n\n\"redshift -P -O 2000 -b 0.2\"\n  Control+Shift + 2\n\n\"redshift -P -O 3000 -b 0.3\"\n  Control+Shift + 3\n\n\"redshift -P -O 4000 -b 0.4\"\n  Control+Shift + 4\n\n\"redshift -P -O 5000 -b 0.5\"\n  Control+Shift + 5\n\n\"redshift -P -O 6000 -b 0.6\"\n  Control+Shift + 6\n\n\"redshift -P -O 7000 -b 0.7\"\n  Control+Shift + 7\n\n\"redshift -P -O 8000 -b 0.8\"\n  Control+Shift + 8\n\n\"redshift -P -O 9000 -b 0.9\"\n  Control+Shift + 9\n\n\"redshift -P -O 10000 -b 1.0\"\n  Control+Shift + 0\n\n\"redshift -x\"\n  Control+Shift + minus" >> ~/.xbindkeysrc
    ```

2. Reload Xbindkeys to apply the changes:

    ```bash
    killall xbindkeys; xbindkeys
    ```

## Usage

Here are the keyboard shortcuts mapped:

- `Control+Shift + 1`: Sets color temperature to 1000K and brightness to 0.1
- `Control+Shift + 2`: Sets color temperature to 2000K and brightness to 0.2
- ...
- `Control+Shift + 0`: Sets color temperature to 10000K and brightness to 1.0 (max)
- `Control+Shift + minus`: Resets all Redshift adjustments to default

## License

MIT License
