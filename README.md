
for our mini project by Embedded Subject.

this is algorithm-
how to Run:
python3 alpr_iot.py

To Run as Background Service (Recommended):
Create /etc/systemd/system/alpr.service:
[Unit]
Description=ALPR IoT System
After=multi-user.target

[Service]
ExecStart=/usr/bin/python3 /home/pi/alpr_iot.py
WorkingDirectory=/home/pi
StandardOutput=inherit
StandardError=inherit
Restart=always
User=pi

[Install]
WantedBy=multi-user.target


Bash:
sudo systemctl daemon-reload
sudo systemctl enable alpr.service
sudo systemctl start alpr.service
