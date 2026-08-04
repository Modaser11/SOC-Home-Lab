## First Step:
we need to setup windows [windows_setup_video](https://youtu.be/-85D8WIKaCc?si=4aGH4dgU1PHMGgKH).\
<img width="805" height="503" alt="image" src="https://github.com/user-attachments/assets/c14ccf00-4be1-4646-a5c7-888e43a94751" />\
Then we need to setup Kali [kali_setup_video](https://youtu.be/4huDEcXFVQc?si=U36KC35MJssduXbd).\
<img width="586" height="538" alt="image" src="https://github.com/user-attachments/assets/0bdefb5f-0419-496e-863a-c4429541205b" /> \
Finally to finish setting the core components of the lab as operating systems without anything else we finally finish setting up ubuntu through this video [ubuntu_server_setup](https://youtu.be/8ZV0ZQFsDJY?si=bRmCHPkqklShiU1D).\
<img width="607" height="257" alt="image" src="https://github.com/user-attachments/assets/5fa2232e-b10f-4fd5-954d-7edf758062b4" /> 
***

## Second Step:
we need to download every needed tool at every machine so we'll star with Splunk we'll download it on the ubuntu server. \
All you need is to follow these commands:
```bash
sudo apt update && sudo apt upgrade -y
```
after updating and upgrading you can go to splunk website to create an account and get a free trial of splunk enterprise\
<img width="1165" height="286" alt="image" src="https://github.com/user-attachments/assets/1ed1e918-9788-46bd-9e12-afeff913dffc" /> \
as You see in image I have selected linux because of ubuntu and you should copy the wget link of the .deb package because ubuntu based on debian \
you will get a command like this:
```bash
wget -O splunk-10.4.2-33c3bf42cd73-linux-amd64.deb "https://download.splunk.com/products/splunk/releases/10.4.2/linux/splunk-10.4.2-33c3bf42cd73-linux-amd64.deb"
```
just paste it in the terminal. \
after you confirm that the file has downloaded successfully as the following image \
<img width="345" height="44" alt="image" src="https://github.com/user-attachments/assets/12914abd-f00f-46b7-bce2-d4ba5ad91481" /> \
use the following command to install the package: 
```bash
sudo dpkg -i splunk-10.4.2-33c3bf42cd73-linux-amd64.deb
```
Then start splunk and accept license: 
```bash
sudo /opt/splunk/bin/splunk start --accept-license
```
we can do a good step which is enabling Splunk at Boot (optional):
```bash
sudo /opt/splunk/bin/splunk enable boot-start
```
