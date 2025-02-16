NSTALLATION AND CONFIGURATION
=============================

repo=https://github.com/robang74/gkrellm2-config
durl=$repo/archive/refs/heads/main.zip

sudo add-apt-repository universe
sudo apt update

sudo apt install -y $(cat thinkpad.lst) unzip wget
 XOR
sudo apt install -y $(cat pcdesktop.lst) unzip wget

mkdir -p ~/.gkrellm2
wget $durl -O ~/Downloads/gkrellm2-config-main.zip
unzip ~/Downloads/gkrellm2-config-main.zip -d ~/.gkrellm2
nohup gkrellm 2>&1 >/dev/null &
