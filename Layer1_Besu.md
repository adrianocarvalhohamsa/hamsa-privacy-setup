<img src="./assets/header.svg" width="100%" height="auto"/>

# <a name="layer-1---hyperledger-besu"></a> Hyperledger Besu - Layer 1

> Optional step: If Besu is already installed, proceed to the [ZK-Rollup - Layer 2](./Layer2_Nodes.md) step.
>
> **For Hyperledger Besu emulation use cases, the minimum requirement is:** \
> *A virtual machine with at least 4 vCPUs/cores and 8GB of RAM* 

<br/>

With access to the virtual machine granted, proceed with the following installation steps:

1. Download the file named [```besu-qbft-docker.zip```](https://stahamsaprivacy.blob.core.windows.net/hamsa-privacy-images/besu-qbft-docker.zip) and extract its contents to a directory of your choice.
2. Execute the following command to make the Layer 1 environment ready for the next steps.
  ```bash
  cd [extracted folder name]

  docker compose up -d
  ```
3. To check if the server is running, execute the following command and locate the term ```besu-qbft-docker```
  ```bash
  docker ps --format '\nName: {{.Names}} is running:  {{.Status}} | Image: {{.Image}}\n'
  ```

1. Make sure to save the IP address or URI of this service, as you will need it in the following steps.


## Troubleshooting

1. If during the service initialization there is a return similar to the following:
    ```bash
    validator4-1  | Supplied genesis block does not match chain data stored in /opt/besu/data.
    validator4-1  | Please specify a different data directory with --data-path, specify the original genesis file with --genesis-file or supply a testnet/mainnet option with --network.
    validator4-1  |
    validator4-1  | To display full help:
    validator4-1  | besu [COMMAND] --help
    validator4-1  | 2024-09-09 21:20:32.982+00:00 | main | ERROR | Besu | Failed to start Besu
    validator4-1  | picocli.CommandLine$ExecutionException: Supplied genesis block does not match chain data stored in /opt/besu/data.
    ```

    **Execute the following procedure using the command line:**

    ```bash
    cd [extracted folder name]

    rm -Rf ./data/validator{1,2,3,4}/*
    ```
2. Upon each data purge of this service, a new deployment of DvP Match and Rollup is mandatory. The Hash must be re-registered on the Nodes ([per Step 2 of the Smart Contract Compilation process](./Environment_Setup.md#compilação-dos-smart-contracts-implantação-do-dvp-match-e-rollup-na-layer-1)).



## Completing the setup 

To complete the Layer 1 (Hyperledger Besu) configuration, use the provided `config.toml` and `genesis.json` files. [See the Central Bank of Brazil documentation for more details](https://github.com/bacen/pilotord-kit-onboarding).

----

<div class="footer right">
  <p><a href="./Layer2_Nodes.md">ZK-Rollup - Layer 2 ></a></p>
  <p><a href="./Installation.md">< Setup</a></p>
  <p><a href="./README.md">Home</a></p>
</div>
