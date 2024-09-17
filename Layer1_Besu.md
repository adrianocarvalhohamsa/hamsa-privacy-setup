<img src="./assets/header.svg" width="100%" height="auto"/>

# <a name="layer-1---hyperledger-besu"></a> Layer 1 - Hyperledger Besu

1. Faça o download do arquivo ```besu-qbft-docker.zip``` e extraia seu conteúdo.
2. Execute o comando abaixo para que o ambiente de Layer 1 esteja já disponível para os próximos passos.
  ```bash
  cd [nome da pasta extraida]

  docker compose up -d
  ```
1. Para conferir se o servidor está rodando execute o comando abaixo e localize o termo ```besu-qbft-docker```
  ```bash
  docker ps --format 'Image: {{.Image}} | Name: {{.Names}} | Image:  {{.Image}}'
  ```

![listagem do serviços de Layer 1](./media/Screenshot%202024-09-16%20at%2010.37.30.png "Listagem do serviços de Layer 1")



----

<link href="./assets/style.css" rel="stylesheet"/>

<div class="footer">
  <a href="./README.md">Inicio</a>
  <a href="./Installation.md">Instalação</a>
  <a href="./Layer2_Nodes.md">Layer 2 - Rollup node</a>
</div>