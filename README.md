# Docker Compose para UniFi Network Application e MongoDB

Este docker-compose.yaml configura a aplicação UniFi Network juntamente com um banco de dados MongoDB, permitindo uma fácil configuração e gerenciamento da rede UniFi.

## Pré-requisitos

- Docker instalado e rodando no seu sistema.
- Docker Compose instalado no seu sistema.

## Arquivos do Projeto

Este projeto inclui os seguintes arquivos:

- `docker-compose.yaml`: Arquivo de configuração para iniciar os containers Docker necessários.
- `init-mongo.js`: Script de inicialização para configurar o usuário e as permissões do banco de dados MongoDB.

## Configuração

Antes de iniciar, você pode ajustar as variáveis de ambiente no arquivo `docker-compose.yaml` para atender às suas necessidades, como:

- `PUID` e `PGID`: Para definir o ID do usuário e grupo, respectivamente.
- `TZ`: Para definir o fuso horário, por exemplo, `America/Sao_Paulo`.
- `MONGO_USER`, `MONGO_PASS`, `MONGO_HOST`, `MONGO_PORT`, `MONGO_DBNAME`: Para configurar o acesso ao MongoDB.
- `MEM_LIMIT`, `MEM_STARTUP`: Limites de memória para a aplicação UniFi (opcional).

## Instruções de Uso

1. **Clone o Repositório (Opcional)**
   Se este setup estiver em um repositório Git, comece clonando o repositório. Se não, certifique-se de que todos os arquivos necessários estão no mesmo diretório.

2. **Inicie os Containers**
   Navegue até o diretório contendo o `docker-compose.yaml` e execute o seguinte comando para iniciar os containers:

   ```bash
   docker-compose up -d
   ```

3. **Acesso à Aplicação**
   Após os containers estarem rodando, acesse a aplicação UniFi Network através do navegador em `http://<seu-ip>:8888`.

4. **Configuração Adicional**
   Siga as instruções na tela para configurar sua rede UniFi.

## Manutenção

- **Parar os Containers**: Para parar todos os containers, utilize o comando `docker-compose down`.
- **Atualizações**: Para atualizar a aplicação ou o banco de dados, você pode atualizar a imagem no arquivo `docker-compose.yaml` e reiniciar os containers.

## Suporte

Para problemas relacionados ao Docker ou Docker Compose, consulte a documentação oficial ou fóruns de discussão. Para questões específicas da aplicação UniFi Network, o suporte da Ubiquiti pode oferecer recursos mais detalhados.
