# Linux-Service-Python3
Linux service for a Python3 application/scripts.

1. Go to cd /etc/systemd/system/
2. Create a file sudo nano myscript.service (yourapp is your name on the new service)
3. Add this to the file:
```
[Unit]
Description=My Python Script
After=network.target

[Service]
ExecStart=/usr/bin/python3 /path/to/your/script.py
WorkingDirectory=/path/to/your/script/directory

[Install]
WantedBy=default.target
```

4. After creating the service file, reload the Systemd daemon to ensure it recognizes the new service:
   
```sudo systemctl daemon-reload```

6. Enable the service to start on boot:
   
```sudo systemctl enable myscript```

7. Manage the service
Now that the service is configured, you can start, stop, restart, and check the status of your Node.js app.

6.1 To start the service:

```sudo systemctl start myscript```

6.2 To stop the service:

```sudo systemctl stop myscript```

6.3 To restart the service:

```sudo systemctl restart myscript```

6.4 To check the status of the service:

```sudo systemctl status myscript```
