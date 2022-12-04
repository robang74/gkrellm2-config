sudo add-apt-repository universe
sudo apt update
sudo apt install -y $(cat packages.list)
mkdir -p ~/.gkrellm2
tar xvzf gkrellm2-config.tar.gz -C ~/.gkrellm2
nohup gkrellm &
