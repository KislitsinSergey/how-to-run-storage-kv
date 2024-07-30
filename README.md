# how-to-run-storage-kv

![0g-storage-bg](https://github.com/user-attachments/assets/031d050a-8eda-4173-92a5-e771c6b892e0)

## Hardware Requirement
```bash
- Memory: 16 GB RAM
- CPU: 4 cores
- Disk: 500GB / 1T NVME SSD
- Bandwidth: 500 MBps for Download / Upload
```

## Download The source code
```bash
git clone -b v1.1.0-testnet https://github.com/0glabs/0g-storage-kv.git
```

## Build the source code
```bash
cd 0g-storage-kv
git submodule update --init
cargo build --release
```

## Copy the config_example.toml to config.toml
```toml
rpc_listen_address = ""

zgs_node_urls = "http://ip1:port1,http://ip2:port2,..."

blockchain_rpc_endpoint = ""

log_contract_address = ""

log_sync_start_block_number = ""

zgs_node_urls = ""
```

## Run the kv service
```bash
cd run

# consider using tmux in order to run in background
../target/release/zgs_kv --config config.toml
```

# END
You're doing great to make it all the way up here! Subscribe to my social media and stay tuned for updates!

Twitter - https://x.com/cutegina0118
Medium - https://medium.com/@sergenode
My Discord Profile - https://discord.com/users/960029203468795914
