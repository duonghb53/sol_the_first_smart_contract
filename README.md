# The First Smartcontract in Solana
## What you will learn
- How to program a basic Solana program in Rust
- How to build and deploy a Solana Rust program

## Requirement
### Install Rust and Cargo
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
### Install solana program and Solana CLI
```
cargo add solana-program
sh -c "$(curl -sSfL https://release.solana.com/stable/install)"
```

### Set config
```
solana config set --url https://api.devnet.solana.com
```
Example output config
```
Config File: /Users/duonghb53/.config/solana/cli/config.yml
RPC URL: https://api.devnet.solana.com
WebSocket URL: wss://api.devnet.solana.com/ (computed)
Keypair Path: /Users/duonghb53/.config/solana/id.json
Commitment: confirmed
```

### Create Keygen & get SOL
```
solana-keygen new
Or
solana-keygen new --outfile ~/my-solana-wallet/my-keypair.json
```
A keypair will be create in `~/.config/solana/id.json` or `~/my-solana-wallet/my-keypair.json`

Get SOL
```
solana airdrop 1 <WALLET_ADDRESS> --url https://api.devnet.solana.com
```
Check balance
```
solana balance <WALLET_ADDRESS> --url https://api.devnet.solana.com
```

### Build program
```
cargo build-bpf
```

### Deploy your Solana program
```
solana program deploy ./target/deploy/sol_first_smart_contract.so
```

```yaml
# example output
Program Id: EFH95fWg49vkFNbAdw9vy75tM7sWZ2hQbTTUmuACGip3
```

**Congratulations**!

You have successfully setup, built, and deployed a Solana program using the Rust language.
