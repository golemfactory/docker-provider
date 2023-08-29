# Project Setup

## Requirements

-   Docker
-   Docker-compose
-   Linux machine (Nested virtualization enabled)

## Procedure

1. Build Docker image: `docker-compose build`
2. Start provider: `docker-compose up -d`

## Configuration

### Switching between mainnet / testnet

By default the provider will start on the testnet, but you can head into the `Dockerfile` and modify CMD with the parameter `--payment-network testnet` to `--payment-network mainnet`

### Pricing Modification

Edit `presets.json` within `ya-provider` directory.

### Node Details

Modify `globals.json` in `ya-provider` directory: node name, subnet, wallet address.

### Hardware Resources

Adjust `hardware.json` in `ya-provider` directory.

### Scaling Instances

Execute `docker-compose up -d --scale provider=3`
