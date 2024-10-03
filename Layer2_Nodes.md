<img src="./assets/header.svg" width="100%" height="auto"/>

# ZK-Rollup - Camada 2

A ZK-Rollup é composta por microsserviços e componentes, ou seja, cada instituição participante terá seu próprio nó.

> **Requisito mínimo:** *Máquina Virtual com ao menos 8 vCPUs/core e 16Gb de memória RAM (para ambiente de teste).*

#### Sobre os componentes:

**hamsa-msft-node:** salvar transações recebidas no pool de transações, gerenciar o ciclo de vida da transação, coordenar o fluxo de DvP e Rollup.

**hamsa-msft-executor:** executar transações através de um EVM.  

**hamsa-msft-prover:** gera uma prova do rollup para batches de transação.


### Carregamento das imagens Docker no repositório de imagens local.

1. Na pasta onde foram extraídos os materiais base, certifique-se de que os arquivos abaixo estão presentes:
   1. ```hamsa-msft-node:<version>.tar``` 
   2. ```hamsa-msft-executor:<version>.tar``` 
   3. ```hamsa-msft-prover:<version>.tar```

2. Para cada arquivo acima execute o seguintes comandos:
     
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
   <p><a href="./Environment_Setup.md">Configuração do ambiente Demo e pré-configuração do ZK-Rollup</a></p>
   <p><a href="./Layer1_Besu.md">Hyperledger Besu  - Camada 1</a></p>
   <p><a href="./README.md">Inicio</a></p>
</div>