# google-drive.service
  
[Unit]
Description=FUSE filesystem over Google Drive  
After=network.target  
[Service]  
User=jos  
Group=jos  
ExecStart=/usr/bin/google-drive-ocamlfuse -label default /home/jos/gdrive  
ExecStop=fusermount -u /home/jos/gdrive  
Restart=always  
Type=forking  
[Install]  
WantedBy=multi-user.target  
Alias=google-drive.service