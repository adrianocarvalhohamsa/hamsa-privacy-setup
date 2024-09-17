<img src="./assets/header.svg" width="100%" height="auto"/>

# Layer 2 - Docker images dos nodes privados

1. Faça o download das imagens abaixo:
   1. ```hamsa-privacy-executor:0.0.1.tar```
   2. ```hamsa-privacy-node:0.0.1.tar```
2. Após realizar o download, navegue via prompt de comando para a pasta destino dos downloads acima e execute o seguintes comandos:
     
    ```bash
    docker load -i hamsa-privacy-node:0.0.1.tar
    ```
    
   ```bash
   docker load -i hamsa-privacy-executor:0.0.1.tar
   ```

   Este comando adicionará as imagens ao repositório Docker local e as disponibilizará para os próximos passos.


----

<div class="footer">
   <p><a href="./Environment_Setup.md">Configuração do ambiente Demo</a></p>
   <p><a href="./Layer1_Besu.md">Layer 1 - Hyperledger Besu Emulation (Opcional)</a></p>
   <p><a href="./README.md">Inicio</a></p>
</div>