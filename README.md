# FakeProdutoAPI

Simula o comportamento de uma API responsável por gerenciar dados de produtos.

Esta API oferece diversos endpoints que possibilitam a listagem de dados de todos os produtos, a recuperação de informações de um produto específico (por meio de seu ID) e a atualização do estoque de forma individual ou em lote.

Além disso, a API simula um comportamento em que, de tempos em tempos, alguns produtos são selecionados aleatoriamente e têm seus estoques e preços modificados. Isso reproduz ações que eventualmente podem ocorrer em cenários reais, onde uma API pode ser consumida por vários sistemas simultaneamente, resultando em dados de vendas eventualmente datados.

## Instruções de Execução

### Usando binários

- Clone ou faça o download do repositório.
- Execute o arquivo binário correspondente ao seu sistema operacional.
- Na mesma pasta do arquivo, será criado um arquivo chamado "produto.db", responsável por armazenar os dados dos produtos da API.
- Acesse `http://localhost:3000/swagger` em seu navegador para explorar a documentação interativa da API, que contém informações sobre os endpoints existentes e descrições breves de seus comportamentos.

Observações:
- Ao baixar o executável, verifique as propriedades do arquivo para garantir permissão de execução. Caso não tenha permissão, utilize `chmod +x nome_do_arquivo` para MacOS e Linux.
- O arquivo `produto.db` pode ser deletado para assegurar um banco de dados "limpo" entre as execuções da API.


### Usando Docker

A API também está disponível no Dockerhub em `julianoctsvr/fakeprodutoapi`, podendo tanto ser executada com `docker run -p 3000:3000 julianoctsvr/fakeprodutoapi` ou mesmo através do `docker-compose.yml` encontrado nesse repositório.

## IMPORTANTE

Apesar de a API gerar um arquivo de banco de dados SQLite, é **obrigatório** acessar e modificar dados de produtos exclusivamente por meio de requisições HTTP conforme documentado no Swagger do projeto. Projetos que realizarem acesso direto ao banco de dados SQLite serão desconsiderados.
