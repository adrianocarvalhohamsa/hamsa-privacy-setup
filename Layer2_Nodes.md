<div class="header">
  <h1>Hamsa Privacy</h1>
  <img class="equation" src="./media/logo_partnership.png" />
</div>

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

<link href="./assets/style.css" rel="stylesheet"/>

<div class="footer">
<a href="./README.md">Inicio</a>
<a href="./Layer1_Besu.md">Layer 1 - Hyperledger Besu Emulation (Opcional)</a>
<a href="./Environment_Setup.md">Configuração do ambiente Demo</a>
</div>