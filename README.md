# Template Laravel

Este é um template para iniciar um projeto Laravel utilizando Docker, PHP 8.1 e outras ferramentas necessárias para desenvolvimento. Siga os passos abaixo para configurar e iniciar o projeto:

## Configuração

1. **Baixe o Projeto:**
   - Faça o download do projeto em formato .zip.

2. **Crie o Arquivo .env:**
   - Utilize o arquivo `.env.example` como base e crie um novo arquivo `.env` no diretório raiz do projeto.

3. **Atualize as Variáveis de Ambiente:**
   - Abra o arquivo `.env` e atualize as variáveis de ambiente conforme necessário. Aqui estão algumas variáveis comuns que você pode precisar configurar:

```plaintext
APP_NAME=Laravel
APP_ENV=local
APP_KEY= "chave_aqui"
APP_DEBUG=true
APP_URL=http://localhost:8000

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=sistema_gestao
DB_USERNAME=root
DB_PASSWORD=root

MAIL_MAILER=smtp
MAIL_HOST=mailhog
MAIL_PORT=1025
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS=null
MAIL_FROM_NAME="${APP_NAME}"

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=
AWS_USE_PATH_STYLE_ENDPOINT=false

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_APP_CLUSTER=mt1

MIX_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
MIX_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}" 


```
## Docker

4. **Suba os Containers do Projeto:**
* Execute o seguinte comando para subir os containers do projeto em background:
```
docker-compose up -d
```

6. **Acesse o Container App:**
* Após subir os containers, acesse o container app para executar comandos relacionados ao Laravel:
```
docker-compose exec app bash
```

## Projeto Laravel

7. **Instale as Dependências do Projeto:**
* Dentro do container app, execute o seguinte comando para instalar as dependências do projeto Laravel:
```
composer install
```
8. **Gere a Chave do Projeto Laravel:**
* Ainda dentro do container app, gere a chave do projeto Laravel com o seguinte comando:
```
php artisan key:generate
```
e coloque nesta linha => APP_KEY= "chave_aqui"
```

Com esses passos o ambiente de desenvolvimento Laravel estará pronto para ser usado. 
Acesse o projeto em :
```
http://localhost:8000 