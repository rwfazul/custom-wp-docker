# custom-wp-docker

Configuração de um WordPress personalizado utilizando Docker.

- Modificação realizada sobre o exemplo definido em <a href="https://docs.docker.com/compose/wordpress/">https://docs.docker.com/compose/wordpress/</a>

## Uso

```sh
	$ cd custom-wp-docker/
	$ docker-compose up -d
```	

Após, o acesso pode ser realizado pelo browser*: http://localhost:8000

- <a href="https://docs.docker.com/compose/wordpress/">Note</a>: The WordPress site is not immediately available on port 8000 because the containers are still being initialized and may take a couple of minutes before the first load.
