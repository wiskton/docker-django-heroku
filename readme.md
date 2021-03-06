# Exemplo Blog - (Django, Docker, Heroku, Postgresql)

## Cria o arquivo pipfile e o ambiente
    
``` bash
pipenv --three
```

## Atualiza as dependências do projeto
    
``` bash
pipenv update
```

## Verifica se o projeto corresponde aos requisitos estabelecidos no Pipfile
        
``` bash
pipenv check
```

## Instalando os requirements no env

``` bash
pipenv install -r django/requirements.txt
```

## Executa os comandos dentro do pipenv
    
``` bash
pipenv run pip freeze > django/requirements.txt
```

## Criação do container

Lembrar de configurar os environments locais
    
``` bash
docker-compose up --build
```

## Rodar aplicação
    
``` bash
docker-compose up
```

## Criar migrações
    
``` bash
docker-compose run web python django/manage.py makemigrations
```

## Migrações

``` bash
docker-compose run web python django/manage.py migrate
```

## deploy heroku

Configurar environments no heroku

``` bash
heroku login
git push heroku master # ou configurar o deploy automatico pelo github por branch
heroku run rake db:migrate
heroku restart
```