# Nexus Node Setup

## 📌 Prerequisites
- Ubuntu 20.04 / 22.04
- ≥ 12 CPU threads
- ≥ 16 GB RAM (recommended: 32 GB+)
- git, curl, build-essential, pkg-config, libssl-dev, protobuf-compiler

```bash
sudo apt update
sudo apt install -y build-essential pkg-config libssl-dev protobuf-compiler git curl
```

## Install Rust

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env

# Clone & Build
git clone https://github.com/username/nexus-cli.git
cd nexus-cli
cargo build --release

## Run Node
screen -S nexus1
./target/release/nexus-network start --node-id <NODE_ID> --max-threads 24 --max-difficulty EXTRA_LARGE_3 

screen -S nexus1
./target/release/nexus-network start --node-id <NODE_ID> --max-threads 24 --max-difficulty EXTRA_LARGE_4 

screen -S nexus1
./target/release/nexus-network start --node-id <NODE_ID> --max-threads 24 --max-difficulty EXTRA_LARGE_5

