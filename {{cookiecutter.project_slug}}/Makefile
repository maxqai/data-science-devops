help:
	@cat Makefile

notebook:
	docker-compose up -d

bash: notebook
	docker-compose run jupyter bash

ipython: notebook
	docker-compose run jupyter ipython

test: notebook
	docker-compose run jupyter python tests/test.py
