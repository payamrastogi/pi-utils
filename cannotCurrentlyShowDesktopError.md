##### How to fix VNC Viewer 'Cannot Currently Show the Desktop' Error 
1. Run the following commands and reboot
```shell
sudo apt-get install --reinstall libgtk2.0-0
sudo apt-get install --reinstall lxsession
sudo reboot
```

###### References
- https://www.tomshardware.com/how-to/fix-cannot-currently-show-desktop-error-raspberry-pi