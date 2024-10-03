<img src="./assets/header.svg" width="100%" height="auto"/>

# Configuração do ambiente Demo e pré-configuração do ZK-Rollup e pré-configuração do ZK-Rollup

1. Realize a extração do aquivo abaixo:
   
   ```hamsa-msft-demo.zip```

2. Através de linha de comando, acesse o diretório:
    ```bash
    cd hamsa-msft-demo
    ```

3. Abra o arquivo hardhat.config.js em seu software de edição de preferência e atualize o endereço do Hyperledger Besu:
   
   - server_L1_besu: \<IP/URI do Hyperledger Besu (Layer 1)>:PORTA;

   
   ![](./media/server_L1_besu%20address.png)


### Compilação dos smart contracts, Implantação do DVP-Match e Rollup na Layer 1

1. Execute os seguintes comandos para realizar instalação das dependências e compilar os smart contracts
    
    > instalação das dependências
     ```bash
    npm i
    ```

    > compilação dos smart contracts
    ```bash
    npx hardhat compile
    ```

### Implantação do DvP Match em Hyperledger Besu
   
2. Implantação DVP-Match, execute o comando abaixo:

    ```bash
    npm run deploy-dvp-match-server-L1
    ```

    O resultado esperado será seguindo o seguindo o exemplo abaixo:

    ![L1MatchScAddress output](./media/L1MatchScAddress_deployed.png "Resultado da implantação do DVP-Match e Rollup")

4. Um endereço `L1MatchScAddress` será gerado e será necessário atualizar o arquivo `.env` existente em cada Node (instituição).
   - Localize no arquivo `./server/node{1,2 ou 3}/.env` a variável de ambiente: `DVP_L1MATCHSCADDRESS`;
   - Atualize o valor existente pelo valor de `L1MatchScAddress`, destacado acima;
  
  ![.env DvP Match value](./media/env_DVP_Server_address.png ".env DvP Match value")


### Implantação Verificador Rollup em Hyperledger Besu

1. Implantação do servidor de Rollup, execute o comando abaixo:
    ```bash
    npm run deploy-rollup-server-L1
    ```

    ![Deploy Rollup Server Output](./media/rollup-server_deploy-output.png)
    ![.env file Rollup verify config deploy](./media/rollup_verify_config.png)

    - Localize no arquivo `./server/node{1,2 ou 3}/.env` a variável de ambiente: `ROLLUP_VERIFYCONFIG_VERIFYCONTRACT`;
    - Atualize o valor existente pelo valor destacado acima;

6. No mesmo arquivo `./server/node{1,2 ou 3}/.env` do Node, localize a variável `L1_URL` e atualize com o endereço de IP/URI do servidor Layer 1 (Hyperledger Besu utlizado).
    
    ![./server/node{1,2 ou 3}/.env file](./media/L1_server_address.png)


----


<div class="footer">
<p><a href="./Nodes_Deployment.md">Implantação de ZK-Rollup</a></p>
<p><a href="./Layer2_Nodes.md">ZK-Rollup - Camada 2</a></p>
<p><a href="./README.md">Inicio</a></p>
</div>


