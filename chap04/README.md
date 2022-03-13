# Trabalhando com Dados

## Comandos

### Inicializando software

- **mongo** - Inicializa o software.

### Navegando pelos seus bancos de dados

- **use *databaseName*** - Muda para um banco de dados existente ou criar um novo.

### Visualizando os bancos de dados e as coleções disponíveis

- **show dbs** - Lista de todos os bancos de dados disponíveis.
- **db** - Mostra o banco de dados em que você está trabalhando.
- **show collections** - Lista de todas as coleções disponíveis.

### Inserindo dados em coleções

- **db.media.insert(*documentName*)** - Insere dados em uma coleção.

### Queries de dados

- **db.media.find()** - Exibe todos os documentos adicionados.
- **db.media.find( { *key: value* } )** - Exibe os documentos que atendem ao filtro determinado.

### Utilizando a notação com ponto

- **db.media.find( { *key.subkey: value* } )** - Exibe os documentos que atendem ao filtro determinado, mais detalhado.

### Usando as funções sort, limit e skip
