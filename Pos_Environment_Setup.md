### Completion of the demo environment setup

Configuring the `hardhat.config.js` file

1. Open the `hardhat.config.js` file in your preferred editing software and update it with the IPs/URIs:

   - server_L1_besu: IP/URI of the Hyperledger Besu (Layer 1);
   - server_L2_1: IP/URI referring to the Layer 2 Node of Bacen/SELIC;
   - server_L2_2: IP/URI referring to institution A;
   - server_L2_3: IP/URI referring to institution B;
   
   <br/>

   > <small>For this demo's testing, it's necessary to keep the port values as they are. For example: Besu: , Nodes: 8123, 8124 and 8125, as shown in the image below:</small>
   
    ![hardhat.config.js](./media/hardhat-config.png "IP Adresses  Updating")

2. For existing tests in this demo, the private keys of the Layer 1 accounts do not need to be changed. If you are using your own Layer 1 blockchain, update the file with your own keys.


---

<div class="footer">
<p><a href="./Nodes_Deployment.md">< ZK-Rollup Deployment</a></p>
<p><a href="./README.md">Home</a></p>
</div>