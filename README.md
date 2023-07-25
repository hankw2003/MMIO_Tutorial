MMIO_Tutorial
====
This is the tutorial for mmio nas usages.

Access via Awesun
----
1. Download the application from the [website](https://sun.aweray.com/en/ "Awesun") and finish the installation.
2. Fill in the Partner ID and passcode as below (Parnter ID: 023 052 043, Passcode: yl626)

![image](https://user-images.githubusercontent.com/117650786/216543417-04610149-20eb-41fb-a411-604e59046214.png)

3. Access file explorer, click the "data1(\\truenas)(Z:)"
![image](https://user-images.githubusercontent.com/117650786/216544102-36380b44-3819-4240-8c00-239dee0219ad.png)

4. (For first time user) Create a folder of your name. </br>
Lowercases are recommended for easier future access via command line in linux.

5. Upload your data file 

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
