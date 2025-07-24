# INEX Pop32 Setup

> [!IMPORTANT]
> linux is the only priority right now, feel free to submit pr
>

## Linux
### VSCode setup
wip

### libusb error
While uploading the code you might get an error that looks something like this:
`libusb: error [get_usbfs_fd] libusb couldn't open USB device XXX/XX XXXXXXXXXXXXXXXXXX`

Fix:
```shell
cd /etc/udev/rules.d/
sudo wget https://raw.githubusercontent.com/namooTH/setup-pop32/refs/heads/main/70-stm32.rules
sudo udevadm control --reload-rules
sudo udevadm trigger
```
