

Neste passo-a-passo, vamos demonstrar o uso do recurso de aprendizado de máquina automatizado no Azure Machine Learning para treinar e avaliar um modelo de aprendizado de máquina. 
1.	Primeiro vamos criar uma conta no Portal do Azure pelo endereço: https://azure.microsoft.com/pt-br/ e clique na opção Testar o Azure gratuitamente;
 
 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/601d7be6-9798-402c-bf0c-fb13c6cc41b5)

2.	Na pagina para a qual você foi direcionado clique na opção Experimente gratuitamente;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/a620a946-9cd5-46fe-a126-0bd6c24bb774)

3.	Na proxima pagina para a qual você for direcionado, será necessário criar um breve cadastro com os dados solicitados. O cadastro de um cartão de credito solicitado como forma de validação de identidade, importante excluir os dados após o uso para teste ou antes de terminar os 30 dias;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/1769656b-73ed-4994-a7ef-d40d78bab26d)

4.	Após fazer o cadastro e fazer o login, você será direcionado para a pagina inicial semelhante a essa;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/5d2771b2-a199-498c-a4cf-b7306bfe2938)

5.	Caso sua pagina seja diferente em seu primeiro acesso, outro idioma, outras cores, sem menu lateral, você poderá personalizar na opção de configurações;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/1a663126-8435-454b-85eb-d61d76ec90b3)
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/38d448d0-6393-4f86-ab09-02fa01c8e4c2)

6.	Para começar você deve criar um recurso clicando na opção Crie um recurso;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/a7229429-581e-4324-bf05-0d9624a7aeff)
 
7.	Em seguida, na tela aberta, na barra de pesquisa vamos procurar por Machine Learning;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/cad9a521-eca2-41ff-8b63-4f7b82851a48)
 
8.	Em seguida escolha a opção encontrada(Azure Machine Learning), termo traduzido na imagem;
   
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/8770765d-df85-4bb3-becc-ce99938b9291)

9.	Na tela abrir você deverá clicar na opção Criar;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/e644b83e-70d1-449e-9e77-df6d481c85a7)

10.	Na tela que abrirá você deverá fazer as seguintes configurações:

        10.1. Assinatura: sua assinatura do Azure;
        10.2. Grupo de recursos: Crie ou selecione um grupo de recursos;

![Desafio_1 Imagem_10](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/a28b95e1-89c0-4978-afba-c88cbfe333ac)

![Desafio_1 Imagem_10_1](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/3b031948-404d-4755-8f7e-1640848da067)

        10.3. Nome: Insira um nome exclusivo para seu espaço de trabalho;
        10.4. Região: Selecione a região geográfica, de preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros;
        10.5. Conta de armazenamento: observe a nova conta de armazenamento padrão que será criada para seu espaço de trabalho, geralmente será preenchido automaticamente após escolher um nome, não precisa ser alterado;
        10.6. Cofre de chaves: Observe o novo cofre de chaves padrão que será criado para seu espaço de trabalho, geralmente será preenchido automaticamente após escolher um nome, não precisa ser alterado;
        10.7. Insights de aplicativo: observe o novo recurso padrão de insights de aplicativo que será criado para seu espaço de trabalho, geralmente será preenchido automaticamente após escolher um nome, não precisa ser alterado;
        10.8. Registro de contêiner: Nenhum ( um será criado automaticamente na primeira vez que você implantar um modelo em um contêiner ).

11.	Selecione Revise e crie: Após preencher todos os campos, deve-se clicar no botão Revise + crie para que seja feita a validação. Caso Ocorra algum erro você deve comparar com esse documento para verificar se foi algum campo foi selecionado de maneira incorreta;
    
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/9c6b4db7-d4e8-480d-8458-cb1d3b36bc2d)

12.	Selecione Crie: Em seguida você deve clicar no botão Crie(Create). Isso pode levar alguns minutos. O ideal é você aguardar na tela aberta para ir acompanhando o processo;
    
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/7c1ffcd3-8191-4bfd-999e-47d663cfd634)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/8596cb23-9465-447c-ada5-d1a8a39ad363)

13.	Selecione Ir para Recurso: Após concluído a implantação do recurso você deve clicar em Ir para o recurso;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ba885c43-693a-4399-b5b4-dfd9a36ad927)

14.	Selecione Launch studio: Após clicar em ir para recurso abrirá a seguinte tela. Nessa tela você deve clicar em Launch studio. Ou vá para o endereço: https://ml.azure.com. Feche todas as mensagens, caso sejam exibidas;
    
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/68df4c4e-69ea-4765-aff5-d773aec7330e)

15.	Na página que abrir, você deverá ver seu espaço de trabalho recém-criado. Caso contrário, selecione Todos os espaços de trabalho no menu à esquerda e selecione o espaço de trabalho que você acabou de criar;
    
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/3109a5f0-a333-4dd5-863f-df82f9122219)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c207b845-f4e2-4bfb-900f-212caf74eca5)

16.	Após ter selecionado o recurso que foi criado, selecione a opção de ML automatizado;
	
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/fe036f09-4a4e-4ed2-b7de-cab8d4161435)

17.	 Agora crie um novo trabalho de ML automatizado com as seguintes configurações;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/5677ec13-bf83-4caf-8bc9-752d2d1ffa07)

        17.1. Configurações básicas:
           17.1.1. Nome do trabalho: mslearn-bike-automl;
           17.1.2. Novo nome do experimento: mslearn-bike-rental;
           17.1.3. Descrição: Aprendizado de máquina automatizado para previsão de aluguel de bicicletas;
           17.1.4. Marcas: deixe o valor padrão, não alterar;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/aa610662-3b3a-43e0-9878-1e0fa08dd6f0)
 
         17.2. Tipo de tarefa e dados:
            17.2.1. Selecione o tipo de tarefa: Regressão;
            17.2.2. Selecionar conjunto de dados: crie um novo conjunto de dados com as seguintes configurações:
  
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/e724f6f0-a986-4fa5-ad9b-b6b2a0ce3ef5)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/53ef1533-1254-4806-b6cf-b3db6b8e2eed)
 
           17.2.3 Tipo de dados:
                17.2.3.1. Nome: aluguel de bicicletas(não deixar espaços entre as palavras);
                17.2.3.2. Descrição: dados históricos de aluguel de bicicletas;
                17.2.3.3. Tipo: Tabular;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/5290a4bf-8471-4c9d-8843-0965f83cd3b6)
 











o	Fonte de dados:
	Selecione Dos arquivos da web, e clique em avançar;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/57b168c6-dbb2-4cf9-ac44-d1a8373d48ac)













o	URL da Web:
	URL da Web: use o endereço no campo URL da Web https://aka.ms/bike-rentals;
	Ignorar validação de dados: não selecionar. Em seguida clique em avançar;
 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c7a78c08-f74b-4902-a1bb-5860ed6f3c94)












o	Configurações :
	Formato de arquivo: Delimitado;
	Delimitador: Vírgula;
	Codificação: UTF-8;
	Cabeçalhos de coluna: apenas o primeiro arquivo possui cabeçalhos;
	Pular linhas: Nenhum;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/372081d4-4da1-4611-a4da-aade72248071)
 










	O conjunto de dados contém dados multilinhas: não selecione;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c2ec7bd6-96fb-41c9-934b-8b91aae1c630)
 
o	Esquema:
	Incluir todas as colunas exceto Caminho(Path);
	Revise os tipos detectados automaticamente;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/29d0157c-c015-47b6-8e51-dfd69bf4a9d5)
 

18.	Selecione Criar. Após a criação do conjunto de dados, selecione o conjunto de dados de aluguel de bicicletas para continuar a enviar o trabalho de ML automatizado.
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/cfb17f16-f59d-414f-b0a6-5618fa81a741)
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/cad875e7-a3c0-4798-972c-3ebe54a1b1f9)
 
 


19.	Em seguida selecione a tabela criada (alugueldebicicletas) e clique em avançar:
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/58011105-350b-4ea1-834c-e780445e52ca)
 















Configurações de tarefa:
•	Tipo de tarefa: Regressão;
•	Conjunto de dados: aluguel de bicicletas;
•	Coluna de destino: Aluguéis (inteiro);
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/6ccca902-7430-4a95-8bae-01e8b90700a8)
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/cbc84d01-101c-4581-bbc3-fbeba1384aaa)

 
 
•	Configurações adicionais: expandir essa opção;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/69b49b70-cd9d-4f35-8858-08ed7421eb3f)
 

o	Métrica primária: raiz do erro quadrático médio normalizado;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/04bd8b73-5934-4a0e-afb8-d66bcee1d83b)
 
o	Explique o melhor modelo: Não selecionado;
o	Usar todos os modelos suportados: Desmarcado . Você restringirá o trabalho para tentar apenas alguns algoritmos específicos;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/b5079906-9464-4a38-b63f-34e02e3d8c12)












o	Modelos permitidos: Selecione apenas RandomForest e LightGBM - normalmente você gostaria de tentar o máximo possível, mas cada modelo adicionado aumenta o tempo necessário para executar o trabalho;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/8047ec80-2eac-452e-bfe2-860fa4165e51)
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/cbf3a97d-12bd-4f94-9c1d-abcebaaade92)
 
 
	Depois clique em salvar para gravar as opções selecionadas;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/b4f98e53-5ab1-46cb-a3b7-c4b1bfc7e39f)
 














•	Limites: expanda esta seção
o	Máximo de testes: 3;
o	Máximo de testes simultâneos: 3;
o	Máximo de nós: 3;
o	Limite de pontuação da métrica: 0,085 (se um modelo atingir uma pontuação da métrica de erro quadrático médio normalizado de 0,085 ou menos, o trabalho termina);
o	Tempo limite: 15;
o	Tempo limite de iteração: 15;
o	Habilitar rescisão antecipada: selecionado;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/45da63f0-ffc2-4052-9cf8-0d11842533bc)
 








•	Validação e teste :
o	Tipo de validação: altere o campo para: divisão de validação de treinamento;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/71052a76-509f-4a7c-8fde-c5e33c5cf48d)
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/25ef122a-295d-4cc4-ab22-4d81785ec023)
 
 

o	Porcentagem de dados de validação: 10;
o	Conjunto de dados de teste: Nenhum;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c3b5d529-00c2-4904-847a-22b087c2d30c)
 













Computação:
•	Selecione o tipo de computação: sem servidor;
•	Tipo de máquina virtual: CPU;
•	Camada de máquina virtual: Dedicada;
•	Tamanho da máquina virtual: Standard_DS3_V2*;
•	Número de instâncias: 1;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/d716cb36-1488-42e0-b092-039d2032cd81)
 










20.	Envie o trabalho de treinamento. Ele inicia automaticamente.
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/9daf09e6-3f93-43bd-b873-a125ddc00256)
 

21.	Espere o trabalho terminar. Pode demorar um pouco;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/e4c2d6a4-6734-4526-a0dd-2e20614535a2)
 

22.	Quando o trabalho automatizado de aprendizado de máquina for concluído, você poderá revisar o melhor modelo treinado.
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/8912781f-95cf-42d1-aa1a-4a1e04dad0b6)
 

23.	Depois de conquido você seleciona o nome do experimento para exibir mais detalhes;
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/f1b3dbf7-5b1e-44f8-8611-80e458f4964e)
 


24.	Caso você tenha saído da tela enquanto a tarefa não tenha esteja completa, você acessar o menu lateral na opção Tarefas(Jobs);
![Uploading image.png…]()
 














•	Selecione o nome do experimento e clique sobre ele;
![Uploading image.png…]()
 
•	Clique para expandir e exibir os detalhes;
![Uploading image.png…]()
 


•	Aqui é exibido todos o histórico de como ele foi concluído;
![Uploading image.png…]()
 

•	Agora volte para a tela anterior e clique sobre o nome;
![Uploading image.png…]()
 

•	selecione o melhor modelo treinado e clique sobre ele;
![Uploading image.png…]()

 















•	Clique sobre Implatar e escolha Serviço Web;
![Uploading image.png…]()

















•	Faça as seguintes configurações:
o	Nome : prever-aluguéis
o	Descrição : Prever aluguel de bicicletas
o	Tipo de computação : Instância de Contêiner do Azure
o	Habilitar autenticação : selecionado
o	Clique em implantar
![Uploading image.png…]()

![Uploading image.png…]()
 












•	Aguarde o início da implantação – isso pode levar alguns segundos. O status de implantação(prever-alugueis) será indicado na parte principal da página como em execução;
 ![Uploading image.png…]()












•	Aguarde até que o status da implantação mude para concluído com êxito . Isso pode levar alguns minutos;
![Uploading image.png…]()
 












25.	Agora vamos testar nosso modelo. No menu lateral clique na guia Pontos de extremidade;
![Uploading image.png…]()
 	
•	Agora selecione o ponto extremidade prever-alugueis;
 ![Uploading image.png…]()



•	No menu da próxima tela selecione a opção testar;
![Uploading image.png…]()
 

•	Na próxima tela vamos substituir o modelo JSON;
![Uploading image.png…]()
 

•	Agora vamos substituir o modelo JSON pelos seguintes dados de entrada e clicar em Testar:
![Uploading image.png…]()
 















•	Os resultados deste teste, que incluem um número previsto de aluguéis com base nos recursos de entrada - semelhante a este;
![Uploading image.png…]()
 


26.	Resultado: o painel de teste pegou os dados de entrada e usou o modelo treinado para retornar o número previsto de aluguéis.


