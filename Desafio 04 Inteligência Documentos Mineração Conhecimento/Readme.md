Explorando um índice do Azure AI Search (UI)

Neste desafio vamos imaginar que você trabalha em uma rede nacional de cafés. Foi solicitado para que você ajude a criar uma solução de mineração de conhecimento que facilite a busca de insights sobre as experiências dos clientes. Você decide criar um índice do Azure AI Search usando dados extraídos de avaliações de clientes.

1.	Neste desafio precisaremos:

1.1.	Criar recursos do Azure;

1.2.	Extrair dados de uma fonte de dados;

1.3.	Enriquecer os dados com habilidades da IA;

1.4.	Utilizar o indexador do Azure no portal do Azure;

1.5.	Consultar seu índice de pesquisa;

1.6.	Revisar os resultados salvos no armazenamento de conhecimento.

Recursos do Azure necessários

2.	Para o nosso desafio vamos criar os seguintes recursos do Azure:

2.1.	Um recurso do Azure AI Search, que gerenciará a indexação e a consulta;

2.2.	Um recurso de serviços de IA do Azure, que fornece serviços de IA para habilidades que sua solução de pesquisa pode usar para enriquecer os dados na fonte de dados com insights gerados pela IA;

2.3.	Uma conta de armazenamento com contêineres de blobs, que armazenará documentos brutos e outras coleções de tabelas, objetos ou arquivos.

Criando um recurso do Azure AI Search

3.	Acesse o portal do Azure pelo endereço https://portal.azure.com;
4.	Clique sobre + Criar um recurso;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/9456c6e0-a63e-4312-9264-77953a1595dc)

5.	 Na barra de pesquisa digite Azure AI Search;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/17a07653-d053-486f-89e5-00274b92e9cd)

6.	Crie um recurso Azure AI Search com as seguintes configurações:
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/a27d4161-04c2-48f9-9fb5-47abc8834ce4)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/fd437546-f8f6-43ed-a62e-4b975803e9ee)


6.1.	Assinatura: use a sua assinatura do Azure;

6.2.	Grupo de recursos: selecione ou crie um grupo de recursos com um nome exclusivo;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/852702cf-26a3-4f4f-9122-989953e22bd2)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/5b868f2a-4471-474a-bf94-4f7dae9e2445)

6.3.	Nome do serviço: um nome exclusivo;

6.4.	Localização: Selecione a região geográfica, preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros;

6.5.	Nível de preços: altere a opção padrão para Básico;

6.6.	Selecione Review + create;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/7d888f77-d7b5-4913-a0c3-484dce64fcb7)

6.7.	Aguarde a até a que seja feita validação e apareça a mensagem de Validação com Sucesso(Validation Success), depois selecione Criar(Create) e aguarde a conclusão da implantação;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/e7daabe4-6ec1-44fa-9e01-e56e319a099c)


![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/d7553d7c-f6cb-49f6-be8d-e3d6452ea2ed)

Criando um recurso de serviços de IA do Azure

7.	Vamos precisar provisionar um recurso de serviços de IA do Azure que esteja no mesmo local que seu recurso do Azure AI Search. Sua solução de pesquisa usará esse recurso para enriquecer os dados no armazenamento de dados com insights gerados por IA.
8.	Acesse o portal do Azure pelo endereço https://portal.azure.com e localize a opção + Criar um recurso e clique sobre ela;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ded42d8e-9cfc-4a4c-a245-17a8a7771171)

9.	Em seguida vá em Categorias e escolha a opção IA + Aprendizado de máquina;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/3cb43a82-1c5e-4252-823b-dd20e52cbf1e)

10.	Em seguida vá até a opção Serviços de IA do Azure e escolha criar;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/f08ffeee-2d1f-402d-aa03-9a786d9ef60b)
 
11.	 Na tela que abrirá você deverá fazer as seguintes configurações;

11.1.	Assinatura: sua assinatura do Azure;

11.2.	Grupo de recursos: selecione o mesmo grupo de recursos que foi  criado no recurso do Azure AI Search;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/12efb524-9c4d-4279-946f-07642fdb3503)
 
11.3.	Região: Selecione a região geográfica, preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros;

11.4.	Nome: Insira um nome exclusivo;

11.5.	Nível de preços: Padrão S0;

11.6.	Ao marcar esta caixa, confirmo que li e compreendi todos os termos abaixo: Selecionado;

11.7.	Após preencher todos os campos, deve-se clicar no botão Revise + crie.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/a2cb4164-6bcf-46dc-9357-391f4233ddec)

11.8.	Em seguida clique em Create(Criar) e aguarde a conclusão da implantação.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/9e8c74a4-8c08-4739-8006-ca467b96a7e9)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/bdd94433-1159-4b81-b14f-56fa3e4194bc)

Criando uma conta de armazenamento

12.	 Acesse novamente portal do Azure pelo endereço https://portal.azure.com e localize a opção + Criar um recurso e clique sobre ela;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/d3446547-ebde-4c8a-90b3-46771ab2b07e)

13.	Procure por storage account (conta de armazenamento) e crie um recurso de conta de armazenamento e faça as seguintes configurações:
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ffd39d02-e0b5-47d8-b0a6-016c603948bf)
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/9af28615-fead-4158-8577-626aa239b70f)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/f6e4ee1f-41a7-4edd-b3ee-cbdbacdd19a3)
 
13.1.	Assinatura: sua assinatura do Azure;

13.2.	Grupo de recursos: Iremos escolher o mesmo grupo de recursos que usamos para criar  os recursos do Azure AI Search e dos serviços Azure AI;

13.3.	Nome da conta de armazenamento: escolha um nome exclusivo;

13.4.	Localização: Selecione a região geográfica, preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/6e020b0f-cfda-41fb-b53e-d124fa11ff6a)
 
13.5.	Desempenho: selecione Padrão(Standard);

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/1c92e768-e91e-4303-ab50-a4e78b42194f)
 
13.6.	Redundância: escolha a opção Armazenamento localmente redundante (LRS). Clique em Revisar + Criar(Review + Create) e aguarde a próxima tela;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/62661ec1-18ec-40ba-ac84-dda07db82d7b)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/11af0c20-9b9e-415d-9b0a-a2ae24aba285)
 
13.7.	Clique em Criar (Create) e aguarde a conclusão da implantação e vá para o recurso implantado.
 
 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/024402a8-6c6f-420c-9ac4-01cd5d9d1189)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/14276454-aa48-46c0-b54f-06c2b170b4d5)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/6899bff7-e8fb-4936-9411-a0e286b5f39e)

14.	Na conta de Armazenamento do Azure que você criou, no painel de menu esquerdo, na guia Configurações selecione Configuração.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/af9c50e3-f482-4833-a100-5d7009cce358)

14.1.	Altere a configuração de Permitir acesso anônimo de Blob para Habilitado e selecione Salvar.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/d39a67b6-1c5f-4bdf-a67f-e74b4675532a)

Carregando documentos para o armazenamento do Azure

15.	No menu esquerdo, selecione Containers.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/abf87551-87c8-4748-8fe0-257019f4599b)
 
16.	Selecione + Recipiente (+ Contêiner) e um painel do seu lado direito é aberto.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/112b653c-0d9d-45db-bada-d0e4221f98c4)

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/382230a4-492b-4a26-a05b-4594046c7f9c)

17.	Insira as seguintes configurações e clique em Criar:

17.1.	Nome: escolha um nome;

17.2.	Nível de acesso público: Container (acesso de leitura anônimo para containers e blobs);

17.3.	Avançado: sem alterações.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/67e8fcc0-fe6f-4f3f-adb1-da163f08c7cf)
 
18.	Agora iremos baixar as avaliações que vamos usar no endereço https://aka.ms/mslearn-coffee-reviews.

19.	No portal do Azure, selecione o contêiner de que você criou clivando sobre o nome dele. Na tela seguinte selecione Carregar.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/2831b828-0c4b-4cee-aabd-7bfa29275404)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/e0100357-d782-4cd9-b7b2-2845e28674ce)
 
20.	No painel Carregar blob, selecione Selecionar um arquivo.

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ed347721-af94-4a8c-8a18-edf60b382602)

21.	Na janela do Explorer, selecione todos os arquivos na pasta de avaliações que foram baixadas, selecione Abrir e, em seguida, selecione Carregar(Upload).

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/9fe87d1e-e0ff-460f-bdea-82fe7a78cd48)
 
22.	Depois que o upload for concluído, você poderá fechar o painel. Seus documentos estão agora em seu contêiner de armazenamento.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/b07fa804-c41d-49ba-aa46-c8a10e3d022b)

Indexando os documentos

Depois de armazenar os documentos, você poderá usar o Azure AI Search para extrair insights dos documentos. O portal do Azure fornece um assistente de importação de dados. Com este assistente, você pode criar automaticamente um índice e um indexador para fontes de dados suportadas. Você usará o assistente para criar um índice e importar seus documentos de pesquisa do armazenamento para o índice do Azure AI Search.
23.	No portal do Azure, navegue até o recurso Azure AI Search. Na página Visão geral, selecione Importar dados.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/4ba24f44-65ec-4f22-b4cd-2dda680e04f3)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/81a0b484-0710-4a9d-b857-193f714ccda4)
 
 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/642fdc4d-3d87-467d-ad3a-52f635215fe9)

24.	Na página Importar dados na guia Conectar-se aos seus dados, em Fonte de Dados, selecione Armazenamento de blobs do azure. Preencha os detalhes do armazenamento de dados com os seguintes valores:

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/dfcba13f-d518-4124-8c60-729941c6e7b4)
 
24.1.	Fonte de dados: Armazenamento de Blobs do Azure(Azure Blob Storage);

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/5605eda9-c194-4a41-945f-1ace23740191)

24.2.	Nome da fonte de dados: coffee-customer-data;

24.3.	Dados a extrair: Conteúdo e metadados;

24.4.	Modo de análise: Padrão;

24.5.	Cadeia de conexão: *Selecione Escolha uma conexão existente. Selecione sua conta de armazenamento, selecione o contêiner que você criou e clique em Selecionar;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/0a1ea3ab-e4c7-4ace-b256-6344de187e71)

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/84969fb6-a433-4732-986c-dd52d146000f)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/de4cf6f2-0d80-47b6-8baf-d30c222273ce)
 
24.6.	Autenticação de identidade gerenciada: Nenhuma;

24.7.	Nome do contêiner: esta configuração é preenchida automaticamente depois que você escolhe uma conexão existente;

24.8.	Pasta Blob: deixe em branco;

24.9.	Descrição: Opcional.

25.	Selecione Próximo: Adicionar habilidades cognitivas (opcional). Aguarde até finalizar a validação.

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/782c95d4-f5c8-40f1-bd21-7a588333000c)

26.	Na secção Anexar Serviços Cognitivos, selecione o seu recurso de serviços Azure AI.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ae425dab-0495-43ec-a5cf-6d74d8eecbe8)
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/892a7ecf-4d90-45c9-b7b4-004e5ca6c1d9)

27.	Na seção Adicionar enriquecimentos:
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/6b9aa9a0-64c9-4677-9b36-a48d06c3a36a)

27.1.	Altere o nome da qualificação; 

27.2.	Marque a caixa de seleção Habilitar OCR e o Campo de dados de origem selecione como conteúdo_mesclado (merged_content);

27.3.	Certifique-se de que o campo Dados de origem esteja configurado como merged_content e altere o nível de granularidade de enriquecimento para Páginas (blocos de 5.000 caracteres);

27.4.	Não habilite o campo Habilitar enriquecimento incremental;

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/6ab8edc2-1eed-48b9-b539-cc26c990aa1b)

27.5.	Selecione os seguintes campos enriquecidos:
Habilidade Cognitiva	Parâmetro	Nome do campo
Extraia nomes de locais	 	Localizações
Extraia frases-chave	 	frases chave
Detectar sentimento	 	sentimento
Gerar tags de imagens	 	imagemTags
Gere legendas de imagens	 	legenda da imagem
 
 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/1e7b9c49-a973-4fc5-8b49-eaf72758fbde)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/a53ce7a0-2ad2-4869-88a9-2819355df5ea)

28.	Na seção Salvar enriquecimentos em um armazenamento de conhecimento, selecione:

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/7fc7e55a-a176-4854-b1a7-6380ae45a56f)
 
28.1.	Projeções de imagem. Caso apareça um aviso solicitando uma cadeia de conexão de conta de armazenamento;

28.1.1.	Escolha uma conexão existente . Escolha a conta de armazenamento que você criou anteriormente;

28.1.2.	Clique em +Recipiente(+ Container) para criar um novo contêiner dando a ele um nome com o nível de privacidade definido como Privado(Private) e selecione Criar(Create);

28.1.3.	Selecione o contêiner que você acabou de criar e clique em Selecionar na parte inferior da tela;

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/36857a94-1c39-43e9-8a0b-126314e0e710)

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/81eef283-1482-4daa-8c59-ab060705a907)

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/b7c20b5d-9d77-4d85-9d45-2166c30dc7b9)

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/cae878a9-c4c0-45f9-9d91-8bed2dd8b75b)

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/12805b0d-31ed-464d-b097-c635dc1a0b3b)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/0d1a5743-bfc9-442c-bc90-3e2b6264f787)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/e60c9b6a-3033-43fa-a61f-4d24c87f7fc4)

28.2.	Documentos;

28.3.	Páginas;

28.4.	Frases chave;

28.5.	Entidades;

28.6.	Detalhes da imagem;

28.7.	Referências de imagem.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/558ae2ab-ae19-421f-886a-dabb29edf942)
 
29.	Selecione projeções de blob do Azure: Documento. Uma configuração para o nome do contêiner será exibido preenchida automaticamente com  nome do contêiner que você criou. Não altere o nome do contêiner.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/42d8383b-788a-48bb-836a-76b65dff09d0)
 
 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/a623e873-9700-484d-948c-a1a5a89d29c0)

30.	Selecione Próximo: Personalizar índice de destino. Altere o nome do índice.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/3c0d96e9-8f10-4c0d-bb8e-701f3cd0da3b)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/56df1aaa-b203-43fc-b091-a78c9436640d)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c4435dd0-821a-4b96-ba21-2bef86526cbf)

31.	Certifique-se de que a chave esteja configurada como metadata_storage_path. Deixe o nome do sugeridor em branco e o modo de pesquisa preenchido automaticamente.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/22c3b68d-e433-4c03-8670-c1a9b7c72c73)

32.	Revise as configurações padrão dos campos de índice. Selecione filtrável para todos os campos que já estão selecionados por padrão. Em seguida selecione Próximo: Criar um indexador.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/7be5bd71-dbfc-401f-a2e0-fae280004f70)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/655f5791-a1a6-49a5-975d-8867942e6a16)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ccf90e60-9331-4281-8eba-8cdd9d4347e7)
 
33.	Altere o nome do indexador.

34.	Deixe a opção Agendar definida como Uma Vez.
35.	Expanda as opções avançadas . Certifique-se de que a opção Chaves de codificação base-64 Encode esteja selecionada, pois as chaves de codificação podem tornar o índice mais eficiente.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/b32ec11e-6928-4a1a-a929-dbdba163fd27)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/e270cbe3-8502-44e8-a3a5-222786063073)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ecfe7dab-f7f5-460d-a33f-3911070c9cfd)

36.	Selecione Enviar para criar a fonte de dados, o conjunto de habilidades, o índice e o indexador. Aguarde a validação. 
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/27a9ec85-8cf8-4685-a140-d3f5ab1f389a)

37.	Volte à página de recursos do Azure AI Search. No painel esquerdo, em Gerenciamento de pesquisa, selecione Indexadores.

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/09dbb894-e09f-4004-9223-5d6f53571711)
 
38.	Selecione o indexador recém-criado . Espere um minuto e selecione Atualizar até que o Status indique sucesso.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/8be3622a-270f-453c-9999-05782ec5f59e)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/433fb820-2454-4667-a8a6-02fa7483dfbd)

Consultando o índice

Use o Search Explorer para escrever e testar consultas. O explorador de pesquisa é uma ferramenta incorporada no portal do Azure que oferece uma maneira fácil de validar a qualidade do seu índice de pesquisa. Você pode usar o Search Explorer para escrever consultas e revisar resultados em JSON.

39.	Na página inicial, escolha o recursos do Azure AI Search, que você criou.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/67b007f6-0244-4138-9715-3028f8c68028)
 
40.	Na página do serviço de pesquisa que você criou, selecione Explorador de pesquisa(Search explorer).

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ec0d2208-ba26-4c6b-bff1-fb1be776e1b6)

41.	Observe se o índice selecionado é o índice que você criou. Abaixo do índice selecionado, altere a visualização(View) para JSON view.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/14eb60c3-08fd-4ea6-968d-10c740c884e5)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/32573fcb-d44b-4f57-995a-a1a9046c6328)
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/1509de4a-22d3-4d26-be4f-9312b0d264fb)

41.1.	No campo do editor de consultas JSON(JSON query editor), altere para:

{
    "search": "*",
    "count": true
}

41.2.	Selecione Pesquisar(Search). A consulta de pesquisa retorna todos os documentos no índice de pesquisa, incluindo uma contagem de todos os documentos no campo @odata.count. O índice de pesquisa deve retornar um documento JSON contendo os resultados da pesquisa.

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/75305f2e-8d76-4c95-8025-d512772866c1)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/3095bfa7-af8c-46c9-8a4e-a031c01f8780)

41.3.	Agora vamos filtrar por localização. No campo do editor de consultas JSON(JSON query editor), altere para:

{
 "search": "locations:'Chicago'",
 "count": true
}

41.4.	Selecione Pesquisar(Search). A consulta pesquisa todos os documentos no índice e filtra revisões com localização em Chicago. Você deve ver 3 no campo @odata.count.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/fb32c7ef-eebd-40fc-98dd-29c1946e1397)

41.5.	Agora vamos filtrar por sentimento. No campo do editor de consultas JSON(JSON query editor), altere para:

{
 "search": "sentiment:'negative'",
 "count": true
}

41.6.	Selecione Pesquisar. A consulta pesquisa todos os documentos no índice e filtra revisões com sentimento negativo. Você deve ver 1no campo @odata.count.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/0bb47c9d-3908-4131-86e8-0260f5b01531)

42.	Os resultados são classificados pelo campo @search.score. Esta é a pontuação atribuída pelo mecanismo de pesquisa para mostrar o quão próximos os resultados correspondem à consulta fornecida.

Revisando o armazenamento de conhecimento

Agora vamos ver o poder do armazenamento de conhecimento em ação. Ao executar o assistente Importar dados, você também criou um armazenamento de conhecimento. Dentro do armazenamento de conhecimento, você encontrará os dados enriquecidos extraídos pelas habilidades de IA que persistem na forma de projeções e tabelas.

43.	No portal do Azure, acesse a sua conta de armazenamento.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/27cca655-1b87-4ae1-9c70-8ba63bc60f11)

44.	No painel do menu esquerdo, selecione Containers. 

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/5175b1b4-5cf8-49f0-9f60-3fd7fe4f4305)

44.1.	Selecione o contêiner privado que você criou.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/955cc357-e7a6-4471-b295-0274f7746f3e)
 
44.2.	Selecione qualquer um dos itens e clique no arquivo objectprojection.json.
 
44.3.	Selecione Editar para ver o JSON produzido para um dos documentos do seu armazenamento de dados do Azure.
 
 

44.4.	Agora volte para a tela da conta de armazenamento Containers. Selecione o contêiner (nome-do-conteiner)-image-projection. 
 

44.5.	Selecione qualquer um dos itens.
 

44.6.	Selecione qualquer um dos arquivos .jpg . Selecione Editar para ver a imagem armazenada no documento. Observe como todas as imagens dos documentos são armazenadas desta forma.
 
 
 

44.7.	Agora volte para a tela da conta de armazenamento Containers. Selecione Navegador de armazenamento(Storage browser) no painel esquerdo.
 
44.8.	selecione Tabelas(Tables). Há uma tabela para cada entidade no índice. Selecione a tabela (nome-tabela)KeyPhrases.
 

 

 

44.9.	Podemos observar as frases-chave que o armazenamento de conhecimento conseguiu capturar do conteúdo das avaliações. Muitos dos campos são chaves, portanto você pode vincular as tabelas como um banco de dados relacional. O último campo mostra as frases-chave que foram extraídas pelo conjunto de habilidades.
 

45.	Observamos que a IA faz um link com uma automação e partir disso ela direciona os dados para um repositório. A partir disso podemos realizar pesquisas no próprio Explorador de pesquisa(Search explorer) usando a automação, ou desenvolver isso para usar em alguma aplicação. Essas ferramentas podem trazer resultados de forma rápida e precisa com base na pesquisa que vamos fazer.
