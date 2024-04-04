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
 
5.	 Na barra de pesquisa digite Azure AI Search;
 

6.	Crie um recurso Azure AI Search com as seguintes configurações:
 

 

6.1.	Assinatura: use a sua assinatura do Azure;
6.2.	Grupo de recursos: selecione ou crie um grupo de recursos com um nome exclusivo;
 

 

6.3.	Nome do serviço: um nome exclusivo;
6.4.	Localização: Selecione a região geográfica, preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros;
6.5.	Nível de preços: altere a opção padrão para Básico;
6.6.	Selecione Review + create;
 
6.7.	Aguarde a até a que seja feita validação e apareça a mensagem de Validação com Sucesso(Validation Success), depois selecione Criar(Create) e aguarde a conclusão da implantação;
 

 

Criando um recurso de serviços de IA do Azure

7.	Vamos precisar provisionar um recurso de serviços de IA do Azure que esteja no mesmo local que seu recurso do Azure AI Search. Sua solução de pesquisa usará esse recurso para enriquecer os dados no armazenamento de dados com insights gerados por IA.
8.	Acesse o portal do Azure pelo endereço https://portal.azure.com e localize a opção + Criar um recurso e clique sobre ela;
 

9.	Em seguida vá em Categorias e escolha a opção IA + Aprendizado de máquina;
 

10.	Em seguida vá até a opção Serviços de IA do Azure e escolha criar;

 

11.	 Na tela que abrirá você deverá fazer as seguintes configurações;
11.1.	Assinatura: sua assinatura do Azure;
11.2.	Grupo de recursos: selecione o mesmo grupo de recursos que foi  criado no recurso do Azure AI Search;

 
11.3.	Região: Selecione a região geográfica, preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros;
11.4.	Nome : Insira um nome exclusivo;
11.5.	Nível de preços: Padrão S0;
11.6.	Ao marcar esta caixa, confirmo que li e compreendi todos os termos abaixo: Selecionado;
11.7.	Após preencher todos os campos, deve-se clicar no botão Revise + crie .
 
11.8.	Em seguida clique em Create(Criar) e aguarde a conclusão da implantação.
 

 

Criando uma conta de armazenamento
12.	 Acesse novamente portal do Azure pelo endereço https://portal.azure.com e localize a opção + Criar um recurso e clique sobre ela;
 
13.	Procure por storage account (conta de armazenamento) e crie um recurso de conta de armazenamento e faça as seguintes configurações:
 
 

 

13.1.	Assinatura: sua assinatura do Azure;
13.2.	Grupo de recursos: Iremos escolher o mesmo grupo de recursos que usamos para criar  os recursos do Azure AI Search e dos serviços Azure AI;
13.3.	Nome da conta de armazenamento: escolha um nome exclusivo;
13.4.	Localização: Selecione a região geográfica, preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros;
 
13.5.	Desempenho: selecione Padrão(Standard);
 

13.6.	Redundância: escolha a opção Armazenamento localmente redundante (LRS). Clique em Revisar + Criar(Review + Create) e aguarde a próxima tela;
 
 
13.7.	Clique em Criar (Create) e aguarde a conclusão da implantação e vá para o recurso implantado.
 
 
 

14.	Na conta de Armazenamento do Azure que você criou, no painel de menu esquerdo, na guia Configurações selecione Configuração.
 
14.1.	Altere a configuração de Permitir acesso anônimo de Blob para Habilitado e selecione Salvar.
 

Carregando documentos para o armazenamento do Azure

15.	No menu esquerdo, selecione Containers.

 

16.	Selecione + Recipiente (+ Contêiner) e um painel do seu lado direito é aberto.
 

 

17.	Insira as seguintes configurações e clique em Criar:
17.1.	Nome: escolha um nome;
17.2.	Nível de acesso público: Container (acesso de leitura anônimo para containers e blobs);
17.3.	Avançado: sem alterações.
 

18.	Agora iremos baixar as avaliações que vamos usar no endereço https://aka.ms/mslearn-coffee-reviews.

19.	No portal do Azure, selecione o contêiner de que você criou clivando sobre o nome dele . Na tela seguinte selecione Carregar.

 

 

20.	No painel Carregar blob, selecione Selecionar um arquivo.
 
21.	Na janela do Explorer, selecione todos os arquivos na pasta de avaliações que foram baixadas, selecione Abrir e, em seguida, selecione Carregar(Upload).

 

22.	Depois que o upload for concluído, você poderá fechar o painel. Seus documentos estão agora em seu contêiner de armazenamento.
 


Indexando os documentos

Depois de armazenar os documentos, você poderá usar o Azure AI Search para extrair insights dos documentos. O portal do Azure fornece um assistente de importação de dados . Com este assistente, você pode criar automaticamente um índice e um indexador para fontes de dados suportadas. Você usará o assistente para criar um índice e importar seus documentos de pesquisa do armazenamento para o índice do Azure AI Search.
23.	No portal do Azure, navegue até o recurso Azure AI Search. Na página Visão geral, selecione Importar dados.

 

 
 

24.	Na página Importar dados na guia Conectar-se aos seus dados, em Fonte de Dados, selecione Armazenamento de blobs do azure. Preencha os detalhes do armazenamento de dados com os seguintes valores:

 
24.1.	Fonte de dados: Armazenamento de Blobs do Azure(Azure Blob Storage);


 

24.2.	Nome da fonte de dados: coffee-customer-data;
24.3.	Dados a extrair: Conteúdo e metadados;
24.4.	Modo de análise: Padrão;
24.5.	Cadeia de conexão: *Selecione Escolha uma conexão existente. Selecione sua conta de armazenamento, selecione o contêiner que você criou e clique em Selecionar;
 

 
 
24.6.	Autenticação de identidade gerenciada: Nenhuma;
24.7.	Nome do contêiner: esta configuração é preenchida automaticamente depois que você escolhe uma conexão existente;
24.8.	Pasta Blob: deixe em branco;
24.9.	Descrição: Opcional.

25.	Selecione Próximo: Adicionar habilidades cognitivas (opcional). Aguarde até finalizar a validação.
 

26.	Na secção Anexar Serviços Cognitivos, selecione o seu recurso de serviços Azure AI.
 
 
27.	Na seção Adicionar enriquecimentos:
 

27.1.	Altere o nome da qualificação; 
27.2.	Marque a caixa de seleção Habilitar OCR e o Campo de dados de origem selecione como conteúdo_mesclado (merged_content);
27.3.	Certifique-se de que o campo Dados de origem esteja configurado como merged_content e altere o nível de granularidade de enriquecimento para Páginas (blocos de 5.000 caracteres);
27.4.	Não habilite o campo Habilitar enriquecimento incremental;
 
27.5.	Selecione os seguintes campos enriquecidos:
Habilidade Cognitiva	Parâmetro	Nome do campo
Extraia nomes de locais	 	Localizações
Extraia frases-chave	 	frases chave
Detectar sentimento	 	sentimento
Gerar tags de imagens	 	imagemTags
Gere legendas de imagens	 	legenda da imagem
 
 
28.	Na seção Salvar enriquecimentos em um armazenamento de conhecimento, selecione:
 

28.1.	Projeções de imagem. Caso apareça um aviso solicitando uma cadeia de conexão de conta de armazenamento;
28.1.1.	Escolha uma conexão existente . Escolha a conta de armazenamento que você criou anteriormente;
28.1.2.	Clique em +Recipiente(+ Container) para criar um novo contêiner dando a ele um nome com o nível de privacidade definido como Privado(Private) e selecione Criar(Create);
28.1.3.	Selecione o contêiner que você acabou de criar e clique em Selecionar na parte inferior da tela;

 
 

 
 
 
 
 
28.2.	Documentos;
28.3.	Páginas;
28.4.	Frases chave;
28.5.	Entidades;
28.6.	Detalhes da imagem;
28.7.	Referências de imagem.
 

29.	Selecione projeções de blob do Azure: Documento. Uma configuração para o nome do contêiner será exibido preenchida automaticamente com  nome do contêiner que você criou. Não altere o nome do contêiner.

 
 
30.	Selecione Próximo: Personalizar índice de destino. Altere o nome do índice.
 
 

 

31.	Certifique-se de que a chave esteja configurada como metadata_storage_path. Deixe o nome do sugeridor em branco e o modo de pesquisa preenchido automaticamente.
 

32.	Revise as configurações padrão dos campos de índice. Selecione filtrável para todos os campos que já estão selecionados por padrão. Em seguida selecione Próximo: Criar um indexador.
 

 

 

33.	Altere o nome do indexador.
34.	Deixe a opção Agendar definida como Uma Vez.
35.	Expanda as opções avançadas . Certifique-se de que a opção Chaves de codificação base-64 Encode esteja selecionada, pois as chaves de codificação podem tornar o índice mais eficiente.
 
 
 
36.	Selecione Enviar para criar a fonte de dados, o conjunto de habilidades, o índice e o indexador. Aguarde a validação. 
 

37.	Volte à página de recursos do Azure AI Search. No painel esquerdo, em Gerenciamento de pesquisa, selecione Indexadores.
  
38.	Selecione o indexador recém-criado . Espere um minuto e selecione Atualizar até que o Status indique sucesso.


 

 

Consultando o índice
Use o Search Explorer para escrever e testar consultas. O explorador de pesquisa é uma ferramenta incorporada no portal do Azure que oferece uma maneira fácil de validar a qualidade do seu índice de pesquisa. Você pode usar o Search Explorer para escrever consultas e revisar resultados em JSON.

39.	Na página inicial, escolha o recursos do Azure AI Search, que você criou.
 

40.	Na página do serviço de pesquisa que você criou, selecione Explorador de pesquisa(Search explorer).
 

41.	Observe se o índice selecionado é o índice que você criou. Abaixo do índice selecionado, altere a visualização(View) para JSON view.
 

 

 

41.1.	No campo do editor de consultas JSON(JSON query editor), altere para:
{
    "search": "*",
    "count": true
}
41.2.	Selecione Pesquisar(Search). A consulta de pesquisa retorna todos os documentos no índice de pesquisa, incluindo uma contagem de todos os documentos no campo @odata.count . O índice de pesquisa deve retornar um documento JSON contendo os resultados da pesquisa.

 
 

41.3.	Agora vamos filtrar por localização. No campo do editor de consultas JSON(JSON query editor), altere para:


{
 "search": "locations:'Chicago'",
 "count": true
}
41.4.	Selecione Pesquisar(Search). A consulta pesquisa todos os documentos no índice e filtra revisões com localização em Chicago. Você deve ver 3 no campo @odata.count.
 

41.5.	Agora vamos filtrar por sentimento. No campo do editor de consultas JSON(JSON query editor), altere para:
{
 "search": "sentiment:'negative'",
 "count": true
}
41.6.	Selecione Pesquisar. A consulta pesquisa todos os documentos no índice e filtra revisões com sentimento negativo. Você deve ver 1no campo @odata.count.
 

42.	Os resultados são classificados pelo campo @search.score. Esta é a pontuação atribuída pelo mecanismo de pesquisa para mostrar o quão próximos os resultados correspondem à consulta fornecida.
Revisando o armazenamento de conhecimento
Agora vamos ver o poder do armazenamento de conhecimento em ação. Ao executar o assistente Importar dados, você também criou um armazenamento de conhecimento. Dentro do armazenamento de conhecimento, você encontrará os dados enriquecidos extraídos pelas habilidades de IA que persistem na forma de projeções e tabelas.
43.	No portal do Azure, acesse a sua conta de armazenamento.
 


44.	No painel do menu esquerdo, selecione Containers . 

 
44.1.	Selecione o contêiner privado que você criou.

 

44.2.	Selecione qualquer um dos itens e clique no arquivo objectprojection.json.
 
 
44.3.	Selecione Editar para ver o JSON produzido para um dos documentos do seu armazenamento de dados do Azure.
 
 

44.4.	Agora volte para a tela da conta de armazenamento Containers. Selecione o contêiner (nome-do-conteiner)-image-projection. 
 

44.5.	Selecione qualquer um dos itens.
 

44.6.	Selecione qualquer um dos arquivos .jpg . Selecione Editar para ver a imagem armazenada no documento. Observe como todas as imagens dos documentos são armazenadas desta forma.
 
 
 

44.7.	Agora volte para a tela da conta de armazenamento Containers. Selecione Navegador de armazenamento(Storage browser) no painel esquerdo.
 
44.8.	selecione Tabelas(Tables). Há uma tabela para cada entidade no índice. Selecione a tabela (nome-tabela)KeyPhrases.
 

 

 

44.9.	Podemos observar as frases-chave que o armazenamento de conhecimento conseguiu capturar do conteúdo das avaliações. Muitos dos campos são chaves, portanto você pode vincular as tabelas como um banco de dados relacional. O último campo mostra as frases-chave que foram extraídas pelo conjunto de habilidades.
 

45.	Observamos que a IA faz um link com uma automação e partir disso ela direciona os dados para um repositório. A partir disso podemos realizar pesquisas no próprio Explorador de pesquisa(Search explorer) usando a automação, ou desenvolver isso para usar em alguma aplicação. Essas ferramentas podem trazer resultados de forma rápida e precisa com base na pesquisa que vamos fazer.
