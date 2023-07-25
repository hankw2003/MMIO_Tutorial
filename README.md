MMIO_Tutorial
====
This is the tutorial for mmio nas usages.

Access via linux
----
1. Login to the account via MobaXterm
2. Access the nas drive with the mounted location /nas_data and /nas_backup
```
cd /nas_data
cd /nas_backup
```

Access via WinSCP
----
1. Donwload the application from the [website](https://winscp.net/eng/download.php "WinSCP")
2. Select SCP for file protocal, Host name: 140.112.93.195, Port number: 200
3. Enter /nas_data or /nas_backup in address line
4. Access like normal file explorer

For Sudoers
----
When NAS or the server itself got rebooted, the mount has to be redone.

```
sudo mount -t nfs 192.168.50.133:/mnt/DATA/data /nas_data
sudo mount -t nfs 192.168.50.133:/mnt/BACKUP/backup /nas_backup
```
