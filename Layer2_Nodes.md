<img src="./assets/header.svg" width="100%" height="auto"/>

# ZK-Rollup - Layer 2

The ZK-Rollup is architected as a microservices-based system, where each participating institution operates an independent node.

> **Minimum requirement:** *Virtual machine with at least 8 vCPUs/cores and 16GB RAM (for testing environment).*

#### Regarding components:

**hamsa-msft-node:** saves received transactions in the transaction pool, manages the transaction lifecycle, coordinates the DvP and Rollup flow.

**hamsa-msft-executor:** executes transactions through an EVM.

**hamsa-msft-prover:** generates a rollup proof for transaction batches.


### Loading Docker images into the local image repository.

1. In the folder where the base materials were extracted, ensure the following files are present:
   * ```hamsa-msft-node:<version>.tar``` 
   * ```hamsa-msft-executor:<version>.tar``` 
   * ```hamsa-msft-prover:<version>.tar```

2. For each file above, execute the following commands:
     
    ```bash
    docker load -i hamsa-msft-node:<version>.tar
    ```
    
   ```bash
   docker load -i hamsa-msft-executor:<version>.tar
   ```

   ```bash
   docker load -i hamsa-msft-prover:<version>.tar
   ```



This command will add the images to your local Docker repository, making them available for subsequent steps.


----

<div class="footer">
   <p><a href="./Environment_Setup.md">Demo environment setup and ZK-Rollup pre-configuration ></a></p>
   <p><a href="./Layer1_Besu.md">< Hyperledger Besu  - Layer 1</a></p>
   <p><a href="./README.md">Home</a></p>
</div>