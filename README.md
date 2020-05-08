### Aplicação tipo To Do com Python Flask e CosmosDB usando API MongoDB para deploy em Azure WebApp

Baseado no tutorial de SARATH LAL https://codewithsarath.com/a-simple-to-do-python-flask-application-with-mongodb/

##### Requisitos

Conta grátis na Azure
https://azure.microsoft.com/pt-br/free/

Conta grátis do CosmosDB com API para MongoDB da Azure

Azure Cloud Shell


##### Instruções
Crie uma conta grátis na Azure seguindo as instruções
https://azure.microsoft.com/pt-br/free/

Crie uma conta CosmosDB com API para MongoDB da Azure

1. Na busca do portal.azure.com digite "cosmos" e clique em "Azure Cosmos DB"

2. Clique Add

3. Selecione e complete dos dados

    Subscription: Selecione a subscription que usara para a conta Azure Cosmos DB, deve se chamar "Avaliação Gratuita" caso esteja usando Azure em Português
    
    Resource Group: Escolhe um Resource group ou crie um novo digitando o nome

    Account Name: Escolha um nome para a sua conta Cosmos DB

    API: Selecione Cosmos DB for Mongo DB API

    Notebooks: Selecione Off

    Apply Free Tier Discount: Selecione Apply, isso lhe permitira usufruir o CosmosDB gratis.

    Location: Selecione a localizacao geografica mais proxima de seus usuarios - (South America) Brazil South

    Version: Selecione 3.6

    Geo-Redundancy: Selecione Disable

    Multi-region Writes: Selecione Disable

4. Clique em Review and Create, aguarde a validação então clique em Create e aguarde a criação da conta.

5. Apos a conta ser criada, acesse ela, clique em Connection String e selecione a PRIMARY CONNECTION STRING desde mongodb:// até /?ssl=true e copie

6. Entre na Cloud Shell

7. Clone o codigo do github com o comando

    git clone https://github.com/frdvo/CosmosDBnoAzureWebApp.git

8. Instale os pacotes necessarios com comando

    pip install -r requirements.txt

9. Acesse a pasta e abra o editor online

    cd CosmosDBnoAzureWebApp
    code .

10. Abra o arquivo app.py e cole a PRIMARY CONNECTION STRING no local indicado e pressione CTRL+S para salvar

11. Teste o codigo

    Na cloud shell digite

    python app.py
    e aperte enter

    Clique no botao WebPreview, clique em Configure
    Escreva: 5000

    Clique em Open and Browse

    Veja se a pagina abre, caso positivo aperte CTRL+C para parar e  vamos fazer o Deploy em um Azure Web App usando a AZ Cli

 12. Na Cloud Shell use comando

    az webapp up --sku F1 --name <Nome do seu Web App> --resource-group <Nome do resource group em que criou a sua conta CosmosDB>

    Aguarde o deploy

13. Na busca do Portal Azure digite App Services, clique em App Services

14. Voce vera seu WebApp listado, clique nele

15. Clique na URL para ver o seu WebApp funcionando!

16. Para apagar digite resources na busca do Portal Azure, e clique em Resource Groups, clique no Resource Group onde esta a conta do CosmosDB e o WebApp, clique em Delete resource group, escreva o nome do resource group e clique em delete.

