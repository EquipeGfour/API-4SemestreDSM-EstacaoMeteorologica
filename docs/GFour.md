<br id="topo">
<h1 align = "center"> Equipe GFour Documentação</h1>
<p align = "center">

Os arquivos do projeto estão organizados em 4 repositórios, sendo: 
 

> ### 📁 <a href="https://github.com/EquipeGfour/Estacao-Metereologica-Front-end">/Estacao-Metereologica-Front-end</a>:
Contém o Front-end desenvolvido em React e TypeScript com construção em formato web tradicional

> ### 📁 <a href="https://github.com/EquipeGfour/Estacao-Metereologica-Back-end">/Estacao-Metereologica-Back-end</a>:
Contém o Back-end , implementado com uma arquitetura de MVC. 
A aplicação foi desenvolvida em torno de um conjunto de regras de negócio específico, utilizando de models para armazenar a regra de negócio. Possuindo controles que fazem a interação com o Banco de dados, Rotas - Que transitam os dados do front para o back.

> ### 📁 <a href="https://github.com/EquipeGfour/Estacao-Metereologica-Back-end-Embarcado">/Estacao-Metereologica-Back-end-Embarcado</a>:
Contém o codigo desenvolvido, ultilizando Arduino e Linguagem C como tecnologias, onde a placa ESP32 é responsável por enviar dados ao banco de dados mongodb.
 
> ### 📁 <a href="https://github.com/EquipeGfour/API-4SemestreDSM-EstacaoMeteorologica">/Documentação</a>:
Documentação da API feita no Swagger, que inclui todos os arquivos necessários para rodar a aplicação em local host.


## :railway_track: Estrutura das Branchs

<div>
  
| Nome da Branch | Representação
| ---------------------: | :--------------------- | 
| Main | Principal branch, contém associadas a ela as versões de publicação para facilitar o acesso e a busca por versões mais antigas. |
| Dev | É uma cópia da branch principal contendo algumas funcionalidades que ainda não foram publicadas. Sendo assim, é a base para o desenvolvimento de novas features. |
| Feature | Branch referente às tasks geradas a partir do epico. Nela temos a convenção do nome da segmente maneira: "nomeDoQueFez" (camelCase). |

 
 ## Swagger
   
 [Documentação com toda a parte de rotas da aplicação, no site do Swaggerhub - Versão 1.0.0](https://app.swaggerhub.com/apis-docs/VINIZEUS2002/api-tec_sus/1.0.0)

  ## Deploy 
 <details>
   <summary><b>Ansible e Aws(EC2)</b></summary>
 
 <br>
 O uso Ansible desta ferramenta em um fluxo de CI/CD é essencial para automatizar a implantação do backend da Estação Meteorológica. O playbook fornecido descreve uma série de tarefas que visam preparar o ambiente, clonar o repositório do projeto e configurar as dependências necessárias e conforme o ansible fica rodando em segundo plano com o serviço do proprio Linux.

Ao utilizar o Ansible em um fluxo de CI, é possível integrá-lo com outras ferramentas de automação e gerenciamento, como Jenkins, GitLab CI/CD. Essa integração permitirá a execução automatizada do playbook em cada estágio do pipeline de CI, garantindo uma implantação consistente e confiável do backend da Estação Meteorológica.

Além disso, a utilização do Ansible oferece vantagens como a automação de tarefas repetitivas, a reprodutibilidade do ambiente de implantação e a capacidade de versionar a configuração como código. Isso significa que qualquer alteração no playbook pode ser rastreada e revertida, facilitando a colaboração e a manutenção do projeto.

Ao realizar a execução do playbook em um estágio de CI, você pode ter confiança de que a infraestrutura será configurada corretamente, as dependências serão instaladas e o ambiente estará pronto para a execução da Estação Meteorológica. Isso contribui para a eficiência do processo de desenvolvimento, permitindo que você se concentre na implementação e nos testes do seu código, sem se preocupar com a configuração manual do ambiente.

Em suma, o uso do Ansible em seu projeto de CI/CD é uma escolha acertada, pois ele oferece automação, padronização e escalabilidade no processo de implantação do backend da Estação Meteorológica, tornando-o mais eficiente e confiável.


os arquivos do projeto para o Deploy estão, sendo:
### 📁 Api/Estacao-Metereologica-Back-end
### :lock: api-estacao-meteorologica.pem : arquivo de Token do Aws
### :lock: FATEC2.pem :arquivo de Token do Aws
### 💼 hosts : arquivo de referencia da rota do Aws 
### 💼 playbook.yml : arquivo de Tarefas do arquivo do ansible 


Comandos para rodar o deploy:

sudo ansible-playbook playbook.yml -u ubuntu --private-key api-estacao-meteorologica.pem -i hosts.yml

mysql -h localhost -u root -p password
<br>
para instalar o ansible
 <br>
sudo apt update
<br>
sudo apt install software-properties-common
<br>
sudo add-apt-repository --yes --update ppa:ansible/ansible
<br>
sudo apt-get install ansible
 <br>
# entrar na maquina
ssh -i "api-estacao-meteorologica.pem" ubuntu@ec2-35-161-181-93.us-west-2.compute.amazonaws.com
<br>
# comando para clonar os arquivos para o ec2
sudo scp -i api-estacao-meteorologica.pem hosts.yml ubuntu@ec2-34-211-225-156.us-west-2.compute.amazonaws.com:/home/ubuntu/api

</details>
 
 
 ## Padrão MVC adotado pelo time

<b>Model</b>
  
O Model será responsável por lidar com o armazenamento e processamento dos dados brutos coletados pela estação meteorológica, bem como o armazenamento dos dados tratados em um banco de dados SQL.
 
 -Banco de dados NoSQL: MongoDB;
 
 -Banco de dados SQL: MySQL.

<b>View</b>

A View será responsável pela apresentação dos dados coletados pela estação meteorológica aos usuários do sistema.
 
 -Framework para construção de interface: React;
 
 -Biblioteca de gráficos: highcharts.js.

<b>Controller</b>

O Controller será responsável pela integração entre a View e o Model, além de coordenar as ações do usuário no sistema.

  -Linguagem de programação: TypeScript;

  -Framework web: Node.js;

  -Biblioteca para conexão com HTTP:express.js;

  -Biblioteca para conexão com MongoDB: MongoDrive;

  -Biblioteca para conexão com MySQL: mysql.

### Podemos definir uma arquitetura MVC para o projeto da seguinte forma:

### Model

 - Estação meteorológica: ESP32;
 
 - Linguagem de programação: C++;
 
 - Protocolo de envio de dados: HTTP;
 
 - Banco de dados NoSQL: MongoDB;
 
 - Biblioteca de conexão HTTP: express.js;
 
 - Biblioteca para conexão com MongoDB: MongoDrive;
 
 - Biblioteca para conexão com MySQL: mysql.

### View

 - Framework para construção de interface: React;
 
 - Biblioteca de gráficos: highcharts.js.

### Controller

 - Linguagem de programação: TypeScript;
 
 - Framework web: Node.js;
 
 - Biblioteca para conexão com HTTP: express.js;
 
 - Biblioteca para conexão com MongoDB: MongoDrive;
 
 - Biblioteca para conexão com MySQL: mysql.

#### A arquitetura MVC acima descrita tem como objetivo separar as responsabilidades do sistema em três componentes principais:

 | Camadas da aplicação | Função no projeto
| ---------------------: | :--------------------- | 
| Model   | A estação meteorológica coleta dados brutos por meio de sensores e os envia por meio do protocolo HTTP. Os dados brutos são recebidos por um broker HTTP. Um script Node.js se inscreve no tópico HTTP do broker e recebe os dados brutos. |
| View    | A View é responsável pela apresentação dos dados coletados pela estação meteorológica aos usuários do sistema. Para isso, utilizaremos o React, um framework JavaScript para a construção de interfaces de usuário. O React permite criar componentes reutilizáveis e organizar a interface em uma hierarquia de componentes, o que torna a construção da interface mais simples e organizada.<br/> A biblioteca de gráficos  highcharts.js. será utilizada para exibir os dados coletados em gráficos e tabelas, de forma clara e concisa. |
| Controller    | O Controller é responsável por coordenar as ações do usuário no sistema e intermediar a comunicação entre a View e o Model. Para isso, utilizaremos o Node.js, um framework JavaScript para construção de aplicativos web.<br/> A conexão com o broker HTTP será feita por meio da biblioteca express.js. A conexão com o banco de dados NoSQL MongoDB será feita por meio da biblioteca Mongoose. Já a conexão com o banco de dados SQL MySQL será feita por meio da biblioteca mysql. <br/>O Controller receberá os dados brutos da estação meteorológica por meio da conexão MQTT e os salvará no banco de dados NoSQL MongoDB. Em seguida, o Controller realizará o tratamento dos dados e os salvará no banco de dados SQL MySQL. O Controller será responsável também por buscar os dados tratados no banco de dados SQL MySQL e enviá-los para a View, para que sejam exibidos ao usuário em forma de gráficos e tabelas, utilizando a biblioteca Chart.js. |
 


<p align="center"><a href="#topo">Voltar ao Topo</p> 
