# custom-wp-docker

Configuração de um WordPress customizado utilizando Docker.

- Modificação realizada sobre o exemplo definido em <a href="https://docs.docker.com/compose/wordpress/" target="_blank">https://docs.docker.com/compose/wordpress/</a>

- Pela estrutura do WordPress, o conteúdo dos websites fica localizado em:
	+ diretório /wp-content (conteúdos estáticos tais como plugins, temas, imagens);
	+ banco de dados MySQL.

- Dessa forma, as customizações foram realizadas através do mapeamento de volumes. O contéudo para exemplo (tema da página, imagens, <em>dump</em> do banco, etc.) foi extraído de um <a href="http://coral.ufsm.br/pet-si/" target="_blank">site</a> que já utiliza WordPress.

- <a href="https://hub.docker.com/_/mysql" target="_blank">Nota</a>: quando o serviço do MySQL inicia, seu <em>script</em> de <em>entrypoint</em> executa automaticamente o <a href="https://github.com/rwfazul/custom-wp-docker/blob/master/docker-compose.yml#L11" target="_blank">SQL</a> (arquivo de <em>dump</em>) mapeado para dentro do diretório <em>docker-entrypoint-initdb.d</em>.

## Uso

```sh
	$ cd custom-wp-docker/
	$ docker-compose up -d
```	

Após, o acesso pode ser realizado pelo browser* em http://localhost:8000

\* <a href="https://docs.docker.com/compose/wordpress/" target="_blank">Nota</a>: The WordPress site is not immediately available on port 8000 because the containers are still being initialized and may take a couple of minutes before the first load.
