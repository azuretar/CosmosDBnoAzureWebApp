### Aplicacao tipo To Do com Python Flask e CosmosDB usando API MongoDB para deploy em Azure WebApp

Baseado no tutorial de SARATH LAL https://codewithsarath.com/a-simple-to-do-python-flask-application-with-mongodb/

##### Requisitos

Conta gratis na Azure
https://azure.microsoft.com/pt-br/free/

Conta gratis do CosmosDB com API para MongoDB da Azure

Azure Cloud Shell



##### Instrucoes
Crie uma conta gratis na Azure seguindo as instrucoes
https://azure.microsoft.com/pt-br/free/

Crie uma conta CosmosDB com API para MongoDB da Azure

1. Na busca do portal.azure.com digite "cosmos" e clique em "Azure Cosmos DB"

2. Clique Add

3. Selecione e complete dos dados:

    Subscription: Selecione a subscription que usara oara a conta Azure Cosmos DB
    
    Resource Group: Escolhe um Resource group ou crie um novo digitando o nome

    Account Name: Escolha um nome para a sua conta Cosmos DB

    API: Selecione Cosmos DB for Mongo DB API

    Location: Selecione a localizacao geografica mais proxima de seus usuarios

    Selecione a Opcao conta gratis

4. Clique em Review and Create e aguarde a criacao da conta.

5. Apos a conta ser criada, acesse ela, clique em Connection String e selecione a PRIMARY CONNECTION STRING de mongodb:// ate /?ssl=true

6. Entre na Cloud Shell

7. Clone o codigo do git

    git clone git@github.com:frdvo/CosmosDBnoAzureWebApp.git

8. Acesse a pasta e abra o editor online

    cd CosmosDBnoAzureWebApp
    code .

9. Cole a PRIMARY CONNECTION STRING no local indicado e pressione CTRL+S para salvar

10. Teste o codigo:

    Na cloud shell digite

    python app.py
    e aperte enter

    Clique no botao WebPreview, clique em Configure
    Escreva: 5000

    Clique em Open and Browse

    Veja se a pagina abre, caso positivo aperte CTRL+C para parar e  vamos fazer o Deploy em um Azure Web App usando a AZ Cli

 11. Na Cloud Shell use comando

    az webapp up --sku F1 --name <Nome do seu Web App> --resource-group <Nome do resource group em que criou a sua conta CosmosDB>

    Aguarde o deploy

12. Na busca do Portal Azure digite App Services, clique em App Services

13. Voce vera seu WebApp listado, clique nele

14. Clique na URL para ver o seu WebApp funcionando!












##### Download/Clone source code from Github

Run app.py in Command prompt.

python app.py

Our local web server is running in the port 5000 by default.

##### Happy coding with Flask and MongoDB!!!
