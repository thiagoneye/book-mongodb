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

- **db.collectionName.insert(*documentName*)** - Insere dados em uma coleção.

### Queries de dados

- **db.collectionName.find()** - Exibe todos os documentos adicionados.
- **db.collectionName.find({*key: value*})** - Exibe os documentos que atendem ao filtro determinado.

### Utilizando a notação com ponto

- **db.collectionName.find({*key.subkey: value*})** - Exibe os documentos que atendem ao filtro determinado, mais detalhado.

### Usando as funções sort, limit e skip

- **db.collectionName.find().sort({*key*: 1})** - Ordena os resultados retornados por uma query. Os resultados podem ser ordenados de forma crescente ou decrescente usando 1 ou -1.
- **db.collectionName.find().limit(*number*)** - Limita o número máximo de resultados retornados.
- **db.collectionName.find().skip(*number*)** - Ignora os primeiros *number* documentos de uma coleção.

### Trabalhando com capped collections, ordem natural e $natural

- **db.createCollection("*collectionName*", {capped: true, size: *sizeBytes*})** - Cria uma *capped collection* (coleção limitada), ou seja, uma coleção de seu banco de dados em que se garante que a ordem natural seja a ordem em que os documentos foram inseridos.
- **db.collectionName.find().sort({$natural: -1})** - Ordena os resultados retornados por uma query, para uma coleção limitada.

### Obtendo um único documento

- **db.collectionName.findOne()** - Exibe um único documento.

### Usando comandos de agregação

- **db.collectionName.count()** - Retorna a quantidade de documentos na coleção especificada. Observe que a função *count()* ignora um parâmetro *skip()* ou *limit()* por padrão. Para garantir que sua query não irá ignorar esses parâmetros e que o seu contador resultante corresponderá aos parâmetros *limit* e/ou *skip*, utilize *count(true)*.
- **db.collectionName.distinct(*key*)** - Retorna somente valores únicos.
- **db.collectionName.group({key: {*keyName*: *value*}, initial: {Total: *number*}, reduce: function (*argument1*, *argument2*) {*operation*}})** - Agrupa documentos em uma coleção por especificar chaves (*key*, *initial*, *reduce*).

### Trabalhando com operadores condicionais

- **$gt** - Operador maior que (*greater than*).
- **$gte** - Operador maior ou igual que (*greater than or equal to*).
- **$lt** - Operador menor que (*less than*).
- **$lte** - Operador menor ou igual que (*less than or equal to*).
- **$ne** - Operador diferente de (*not equals*).
- **$in** - Operador em (*in*).
- **$nin** - Operador não está em (*not in*).
- **$all** - Operador todos (*all*).
- **$or** - Operador ou (*or*).