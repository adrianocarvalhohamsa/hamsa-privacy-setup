<img src="./assets/header.svg" width="100%" height="auto"/>

# Layer 1 - Node privado

## Arquitetura


> **Requisito mínimo:** *Máquina Virtual com ao menos 8 vCPUs/Cores e 16Gb de memória RAM (para ambiente de teste).*



O Node é constituído pelos microserviços abaixo:

**hamsa-privacy-node:** salvar transações recebidas no pool de transações, gerenciar o ciclo de vida da transação, coordenar o fluxo de Dvp e Rollup.

**hamsa-privacy-executor:** executar transações através de um EVM.  

**hamsa-privacy-prover:** gera uma prova do rollup para batches de transação.


## Passos de instalação

1. Faça o download das imagens abaixo:
   1. ```hamsa-privacy-node:0.0.1.tar```
   2. ```hamsa-privacy-executor:0.0.1.tar```
   3. ```hamsa-privacy-prover:0.0.1.tar```

2. Após realizar o download, navegue via prompt de comando para a pasta destino dos downloads acima e execute o seguintes comandos:
     
    ```bash
    docker load -i hamsa-privacy-node:0.0.1.tar
    ```
    
   ```bash
   docker load -i hamsa-privacy-executor:0.0.1.tar
   ```

   ```bash
   docker load -i hamsa-privacy-prover:0.0.1.tar
   ```



Este comando adicionará as imagens ao repositório Docker local e as disponibilizará para os próximos passos.


----

<div class="footer">
   <p><a href="./Environment_Setup.md">Configuração do ambiente Demo</a></p>
   <p><a href="./Layer1_Besu.md">Layer 1 - Hyperledger Besu</a></p>
   <p><a href="./README.md">Inicio</a></p>
</div>