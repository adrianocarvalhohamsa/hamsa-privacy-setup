### Atualizando as configurações do ambiente demo

Configuração do arquivo hardhat.config.js

1. Abra o arquivo hardhat.config.js em seu software de edição de preferência e atualize-o com os IPs/URI:
   1. server_L1_besu: IP/URI do Hyperledger Besu (Layer 1);
   2. server_L2_1: IP/URI referente ao Node Layer 2 do Bacen/SELIC;
   3. server_L2_2: IP/URI referente à instituição A;
   4. server_L2_3: IP/URI referente à instituição B;
   
   <br/>

   > <small>Para os testes desta demo é necessário manter os valores referentes às portas. Exemplo: Besu:8545, Nodes: 8123, 8124 e 8125, imagem abaixo:</small>
   
    ![hardhat.config.js](./media/hardhat-config.png "Atualização dos IPs")

2. Para testes já existentes nesta demo, as chaves privadas das contas na Layer 1 não precisam ser modificadas. Caso você esteja usando sua própria blockchain Layer 1, atualize o arquivo com as sua próprias chaves.


---

<div class="footer">
<p><a href="./Nodes_Deployment.md">< Implantação de ZK-Rollup</a></p>
<p><a href="./README.md">Inicio</a></p>
</div>