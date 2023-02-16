## Sistema Web Simples de Cadastro de Vagas

Sisteminha construído por meio de uma aula do canal <a href="https://www.youtube.com/wdevoficial">WDEV</a> no youtube, usando PHP, banco de dados e implementando conceitos de PDO na aplicação.

## Tecnologias utilizadas:

- PHP
- PDO
- XAMP
- MySQL
- Composer

Necessário criar um banco de dados, segue abaixo as instruções para criar a tabela vagas:

 ```sql
  CREATE TABLE `vagas` (
  	`id` INT(11) NOT NULL AUTO_INCREMENT,
  	`titulo` VARCHAR(255) NOT NULL COLLATE 'utf8_general_ci',
  	`descricao` TEXT(65535) NOT NULL COLLATE 'utf8_general_ci',
  	`ativo` ENUM('s','n') NOT NULL COLLATE 'utf8_general_ci',
  	`data` TIMESTAMP NOT NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  	PRIMARY KEY (`id`) USING BTREE
  )
  COLLATE='utf8_general_ci'
  ENGINE=InnoDB
  AUTO_INCREMENT=1;
```

## Configuração
As credenciais do banco de dados estão no arquivo ./app/Db/Database.php e você deve alterar para as configurações do seu ambiente (HOST, NAME, USER e PASS).

## Composer
Para a aplicação funcionar, é necessário rodar o Composer para que sejam criados os arquivos responsáveis pelo autoload das classes.
