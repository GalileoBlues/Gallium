# How to use this ![Kanata](https://github.com/jtroo/kanata) config
1. Download the ![Kanata release](https://github.com/jtroo/kanata/releases) binary for your system and rename it to "kanata".
2. Grab Gallium.cfg and uncomment the version of Gallium you want the config to use.
3. Test the config here with the release binary: `./kanata -c Gallium.cfg`.

## To install layout as a systemd service (Linux):

1. Place the Kanata binary in `/usr/bin/` or wherever your system stores binaries (if different edit the service).
2. Create a "kanata" folder in your `/home/$USER/.config/` directory if it doesn't exist and place both `Gallium.cfg` and `kanata.service` there.
3. Copy `kanata.service` to `/etc/systemd/system/` to allow the system to access the service.
4. Run the command `sudo systemctl enable kanata.service` to enable this service on startup.
