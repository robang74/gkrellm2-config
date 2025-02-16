NSTALLATION AND CONFIGURATION
=============================

sudo add-apt-repository universe -y
sudo apt update
sudo apt install -y unzip wget

repo=https://github.com/robang74/gkrellm2-config
durl=$repo/archive/refs/heads/main.zip

mkdir -p ~/.gkrellm2
wget $durl -O ~/Downloads/gkrellm2-config-main.zip
unzip -o ~/Downloads/gkrellm2-config-main.zip -d /tmp
cp -arf /tmp/gkrellm2-config-main ~/.gkrellm2

list=$(cat ~/.gkrellm2/thinkpad.lst)
 XOR
list=$(cat ~/.gkrellm2/pcdesktop.lst)

for i in $list; do sudo apt install -y $i; done

nohup gkrellm 2>&1 >/dev/null &

