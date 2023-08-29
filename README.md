# Project Setup

## Requirements

- Docker
- Docker-compose
- Linux machine (Nested virtualization enabled)

## Procedure

1. Build the Docker image using `docker-compose build`.
2. Start the provider with `docker-compose up -d`.

## Configuration

### Switching Between Mainnet and Testnet

By default, the provider starts on the testnet. You can switch to the mainnet by modifying the `Dockerfile`. Replace `--payment-network testnet` with `--payment-network mainnet` in CMD.

### Modifying Prices

Update the `presets.json` file in the `ya-provider` directory to adjust prices.

### Modifying Node Details

Modify the `globals.json` file in the `ya-provider` directory to update node details like node name, subnet, and wallet address.

### Adjusting Hardware Resources

To adjust the hardware resources, update the `hardware.json` file in the `ya-provider` directory.

### Scaling Instances

To scale instances, execute `docker-compose up -d --scale provider=3`.