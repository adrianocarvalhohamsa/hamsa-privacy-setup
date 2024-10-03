<img src="./assets/header.svg" width="100%" height="auto"/>

# Node privado - Layer 2

A Layer 2 é composta pelos ambientes privados de cada instituição, ou seja, cada instituição participante representa um Node. 

> O carregamento das imagens Docker abaixo devem ser aplicadas para implantação de cada Node.

## Arquitetura

> **Requisito mínimo:** *Máquina Virtual com ao menos 8 vCPUs/core e 16Gb de memória RAM (para ambiente de teste).*


O Node é constituído pelos microserviços abaixo:

**hamsa-msft-node:** salvar transações recebidas no pool de transações, gerenciar o ciclo de vida da transação, coordenar o fluxo de Dvp e Rollup.

**hamsa-msft-executor:** executar transações através de um EVM.  

**hamsa-msft-prover:** gera uma prova do rollup para batches de transação.


## Carregamento das imagens Docker no repositório de imagens local.

1. Faça o download das imagens abaixo:
   1. ```hamsa-msft-node:<version>.tar```
   2. ```hamsa-msft-executor:<version>.tar```
   3. ```hamsa-msft-prover:<version>.tar```

2. Após realizar o download, navegue via prompt de comando para a pasta destino dos downloads acima e execute o seguintes comandos:
     
    ```bash
    docker load -i hamsa-msft-node:<version>.tar
    ```
    
   ```bash
   docker load -i hamsa-msft-executor:<version>.tar
   ```

   ```bash
   docker load -i hamsa-msft-prover:<version>.tar
   ```



Este comando adicionará as imagens ao repositório Docker local e as disponibilizará para os próximos passos.


----

<div class="footer">
   <p><a href="./Environment_Setup.md">Configuração do ambiente Demo</a></p>
   <p><a href="./Layer1_Besu.md">Hyperledger Besu - Layer 1</a></p>
   <p><a href="./README.md">Inicio</a></p>
</div>