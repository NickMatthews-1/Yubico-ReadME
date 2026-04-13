# Install and Usage Instructions for Linux

### Basic usage
To run Yubico Authenticator, execute the authenticator binary by double clicking or running it from command line:

    ./authenticator

## Debain based systems (Debian, Ubuntu, Pop_OS!, Mint, Tails) 

You will need to have the software package PCSCD installed in order for it to function as intended.
PCSCD can be obtained from the package manager with the following command

    sudo apt install pcscd

Once PCSCD is installed you will need to enable it to get full functionality. This is done with

    sudo systemctl enable pcscd.service


Note that the QR scanning feature requires gnome-screenshot when using Wayland.

    sudo apt install gnome-screenshot

### Intstallation on the operating system
Execute following command to istall Yubico Authenticator to your computer:

    ./desktop_integration.sh --install

## Arch Based Systems

In order for the software to work as intended you will need to install the software packages,
PCSCLITE and CCID. This is done with the following command.

    sudo pacman -S pcsclite ccid

Once PCSCLITE and CCID have been installed you will need to start and enable PCSCD with the following commands

    sudo systemctl enable pcscd.service

    sudo systemctl start pcscd.service

In order to check to see if it is loaded you will need to run the following command

    sudo systemctl status pcscd.service

When running this command it will return a "inactive" status, this is expected as until you are using the Yubico Authenticator software the interface software will not be running at all.
When running the Yubico Authenticator software it will return an active status. This is the intended behaviour.

In order to install the software you will need to run

    ./desktop_integration.sh --install

From where you have extracted the tar package.
