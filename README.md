# systemd-better-tmux







josef@UbuntuVM:~$ sudo nano /etc/systemd/system/mysite.service





[Unit]
Description=My Site
After=network.target

[Service]
User=josef
WorkingDirectory=/home/josef/Anti
ExecStart=/usr/bin/python3 -m http.server 2000
Restart=always
ExecStart=/usr/bin/cloudflared tunnel --url http://localhost:2000


[Install]
WantedBy=multi-user.target


