# Babylonchain node installation

## Setting Up a Validator Node for Babylon

### Prerequisites

1. **System Requirements**
   - Ubuntu 20.04 or later
   - At least 4 GB RAM
   - 2 CPU cores
   - 50 GB SSD
   - Go installed (version 1.18+)

2. **Install Go**
   ```bash
   sudo apt update
   sudo apt install golang-go
   ```

3. **Install Git**
   ```bash
   sudo apt install git
   ```

### Clone the Babylon Repository

1. Navigate to your working directory:
   ```bash
   cd ~
   ```

2. Clone the Babylon repository:
   ```bash
   git clone https://github.com/babylonchain/babylon.git
   cd babylon
   ```

### Build the Validator Binary

1. Build the project:
   ```bash
   make install
   ```

   This will generate a binary named `babylond` in your `$GOPATH/bin`.

### Initialize the Node

1. Initialize the node:
   ```bash
   babylond init <your_moniker>
   ```

   Replace `<your_moniker>` with a name for your validator node.

### Configure the Node

1. Edit the configuration file located at `~/.babylon/config/config.toml`:
   ```bash
   nano ~/.babylon/config/config.toml
   ```

2. Set up the persistent peers:
   ```toml
   persistent_peers = "<peer_id>@<peer_address>"
   ```

   You can find peer IDs and addresses in the Babylon documentation or community channels.

### Download Genesis File

1. Download the latest genesis file:
   ```bash
   curl -o ~/.babylon/config/genesis.json https://path_to_genesis_file
   ```

2. Update the `seeds` configuration in `~/.babylon/config/config.toml`:
   ```toml
   seeds = "<seed_node_id>@<seed_node_address>"
   ```

### Create Validator Keys

1. Generate a new keypair:
   ```bash
   babylond keys add <your_validator_key>
   ```

   Store your mnemonic securely!

### Start the Node

1. Start the Babylon validator node:
   ```bash
   babylond start
   ```

### Monitoring and Logs

- You can monitor logs by checking the console output or viewing the log file at `~/.babylon/logs`.

### Additional Commands

- To check the status of your node:
  ```bash
  babylond status
  ```

- To view your validator information:
  ```bash
  babylond q staking validator <validator_address>
  ```

### Conclusion

You now have a basic validator node running for the Babylon project. Make sure to stay updated with the Babylon community for any changes or updates.

For more detailed information, refer to the [official documentation](https://docs.babylonchain.io/docs/introduction/overview) and the [GitHub repository](https://github.com/babylonchain).

Feel free to reach out if you have any questions!

# END
You're doing great to make it all the way up here! Subscribe to my social media and stay tuned for updates!

Twitter - https://x.com/cutegina0118
Medium - https://medium.com/@sergenode
My Discord Profile - https://discord.com/users/960029203468795914
