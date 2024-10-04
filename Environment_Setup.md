<img src="./assets/header.svg" width="100%" height="auto"/>

# Demo environment setup and ZK-Rollup pre-configuration.

1. Extract the compressed file:
   
   ```hamsa-msft-demo.zip```

2. Access the directory via command line:
    ```bash
    cd hamsa-msft-demo
    ```

3. Open the `hardhat.config.js` file in your preferred editor and update the Hyperledger Besu address:
   
   - server_L1_besu: \<IP or URI do Hyperledger Besu (Layer 1)>:\<PORT>;

   
   ![](./media/server_L1_besu%20address.png)


### Smart contract compilation and deployment of DVP-Match and Rollup on Layer 1

1. Run the following commands to install dependencies and compile smart contracts:
    
    > Install dependencies:
     ```bash
    npm i
    ```

    > Compile smart contracts:
    ```bash
    npx hardhat compile
    ```

### Deploying DVP-Match on Hyperledger Besu

1. To deploy DVP-Match, run the following command:

    ```bash
    npm run deploy-dvp-match-server-L1
    ```

    The expected output will be similar to the following:

    ![L1MatchScAddress output](./media/L1MatchScAddress_deployed.png "Deployment result of DVP-Match and Rollup")

2. An `L1MatchScAddress` will be generated. You will need to update the existing `.env` file in each Node (institution).
   - Locate the environment variable `DVP_L1MATCHSCADDRESS` in the file `./server/node{1,2 or 3}/.envs`.
   - Update the existing value with the generated `L1MatchScAddress`.
  
  ![.env DvP Match value](./media/env_DVP_Server_address.png ".env DvP Match value")


### Rollup Verifier Deployment on Hyperledger Besu

1. To deploy the Rollup verifier, execute the command below:

    ```bash
    npm run deploy-rollup-server-L1
    ```

    ![Deploy Rollup Server Output](./media/rollup-server_deploy-output.png)
    ![.env file Rollup verify config deploy](./media/rollup_verify_config.png)

    - Locate the environment variable `ROLLUP_VERIFYCONFIG_VERIFYCONTRACT` in the file `./server/node{1,2 or 3}/.env;` update the existing value with the value highlighted above.

2. In the same file `./server/node{1,2 or 3}/.env` of the Node, locate the variable L1_URL and update it with the IP address/URI of the Layer 1 server (Hyperledger Besu that you using).
    
    ![./server/node{1,2 ou 3}/.env file](./media/L1_server_address.png)


----


<div class="footer">
<p><a href="./Nodes_Deployment.md">ZK-Rollup Deployment ></a></p>
<p><a href="./Layer2_Nodes.md">< ZK-Rollup - Layer 2</a></p>
<p><a href="./README.md">Inicio</a></p>
</div>


