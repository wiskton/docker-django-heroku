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
pipenv install -r requirements.txt
```

## Executa os comandos dentro do pipenv
    
``` bash
pipenv run pip freeze > requirements.txt
```

## Criação do container
    
``` bash
docker-compose up --build
```

## Rodar aplicação
    
``` bash
docker-compose up
```

## Criar migrações
    
``` bash
docker-compose run web python manage.py makemigrations
```

## Migrações

``` bash
docker-compose run web python manage.py migrate
```

## deploy heroku

``` bash
heroku login
git push heroku master # ou configurar o deploy automatico pelo github por branch
heroku run rake db:migrate
heroku restart
```