### Neste passo-a-passo, vamos demonstrar o uso do recurso de aprendizado de máquina automatizado no Azure Machine Learning para treinar e avaliar um modelo de aprendizado de máquina. 
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

		17.2.3. Tipo de dados:
  		     17.2.3.1. Nome: aluguel de bicicletas(não deixar espaços entre as palavras);
	 	     17.2.3.2. Descrição: dados históricos de aluguel de bicicletas;
		     17.2.3.3. Tipo: Tabular;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/5290a4bf-8471-4c9d-8843-0965f83cd3b6)
 
 		17.2.4. Fonte de dados:
   		     17.2.4.1 Selecione Dos arquivos da web, e clique em avançar;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/57b168c6-dbb2-4cf9-ac44-d1a8373d48ac)

		17.2.5. URL da Web:
		     17.2.5.1. URL da Web: use o endereço no campo URL da Web https://aka.ms/bike-rentals;
		     17.2.5.2. Ignorar validação de dados: não selecionar. Em seguida clique em avançar;
	
 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c7a78c08-f74b-4902-a1bb-5860ed6f3c94)

		17.2.6. Configurações:
  		     17.2.6.1. Formato de arquivo: Delimitado;
  		     17.2.6.2. Delimitador: Vírgula;
	 	     17.2.6.3. Codificação: UTF-8;
		     17.2.6.4. Cabeçalhos de coluna: apenas o primeiro arquivo possui cabeçalhos;
		     17.2.6.5. Pular linhas: Nenhum;
  
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/372081d4-4da1-4611-a4da-aade72248071)
 
		     17.2.6.6. O conjunto de dados contém dados multilinhas: não selecione;
  
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c2ec7bd6-96fb-41c9-934b-8b91aae1c630)

		17.2.7. Esquema:
		     17.2.7.1.Incluir todas as colunas exceto Caminho(Path);
		     17.2.7.2. Revise os tipos detectados automaticamente;
  
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/29d0157c-c015-47b6-8e51-dfd69bf4a9d5)
 

18.	Selecione Criar. Após a criação do conjunto de dados, selecione o conjunto de dados de aluguel de bicicletas para continuar a enviar o trabalho de ML automatizado.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/cfb17f16-f59d-414f-b0a6-5618fa81a741)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/cad875e7-a3c0-4798-972c-3ebe54a1b1f9)

19.	Em seguida selecione a tabela criada (alugueldebicicletas) e clique em avançar:

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/58011105-350b-4ea1-834c-e780445e52ca)
 
	    19.1. Configurações de tarefa:
	       19.1.1. Tipo de tarefa: Regressão;
	       19.1.2. Conjunto de dados: aluguel de bicicletas;
	       19.1.3. Coluna de destino: Aluguéis (inteiro);
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/6ccca902-7430-4a95-8bae-01e8b90700a8)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/cbc84d01-101c-4581-bbc3-fbeba1384aaa)
 
	       19.1.4. Configurações adicionais: expandir essa opção;
      
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/69b49b70-cd9d-4f35-8858-08ed7421eb3f)
 
		     19.1.4.1. Métrica primária: raiz do erro quadrático médio normalizado;
  
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/04bd8b73-5934-4a0e-afb8-d66bcee1d83b)
 
		     19.1.4.2. Explique o melhor modelo: Não selecionado;
		     19.1.4.3. Usar todos os modelos suportados: Desmarcado . Você restringirá o trabalho para tentar apenas alguns algoritmos específicos;
  
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/b5079906-9464-4a38-b63f-34e02e3d8c12)

		     19.1.4.4. Modelos permitidos: Selecione apenas RandomForest e LightGBM - normalmente você gostaria de tentar o máximo possível, mas cada modelo adicionado aumenta o tempo necessário para executar o trabalho;
   
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/8047ec80-2eac-452e-bfe2-860fa4165e51)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/cbf3a97d-12bd-4f94-9c1d-abcebaaade92)
 
 		     19.1.4.5. Depois clique em salvar para gravar as opções selecionadas;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/b4f98e53-5ab1-46cb-a3b7-c4b1bfc7e39f)

	       19.1.5. Limites: expanda esta seção:
		    19.1.5.1. Máximo de testes: 3;
		    19.1.5.2. Máximo de testes simultâneos: 3;
		    19.1.5.3. Máximo de nós: 3;
		    19.1.5.4. Limite de pontuação da métrica: 0,085 (se um modelo atingir uma pontuação da métrica de erro quadrático médio normalizado de 0,085 ou menos, o trabalho termina);
		    19.1.5.5. Tempo limite: 15;
		    19.1.5.6. Tempo limite de iteração: 15;
		    19.1.5.7. Habilitar rescisão antecipada: selecionado;

![Desafio_1 Imagem_19_10](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/38077226-90d8-49e3-839a-def241685e04)

	       19.1.6. Validação e teste:
		    19.1.6.1. Tipo de validação: altere o campo para: divisão de validação de treinamento;
      
![Desafio_1 Imagem_19_11](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/a03d7b49-a910-4121-9775-9e70411e6b9e)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/17c915c3-ffbb-4b41-8fd9-1bfa9ffcdbc8)

		    19.1.6.2. Porcentagem de dados de validação: 10;
		    19.1.6.3. Conjunto de dados de teste: Nenhum;
		    19.1.6.4. Clique em avançar para prosseguir;
      
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/a748c2ba-f073-4837-b22c-e00371614bf5)

	     19.2. Computação:
		19.2.1. Selecione o tipo de computação: sem servidor;
		19.2.2. Tipo de máquina virtual: CPU;
		19.2.3. Camada de máquina virtual: Dedicada;
		19.2.4. Tamanho da máquina virtual: Standard_DS3_V2*;
		19.2.5. Número de instâncias: 1;
  		19.2.6. Clique em avançar;
  
  ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/6571702b-a966-4394-9a45-4f45ab5fc3c4)

20.	Agora clique em Enviar o trabalho de treinamento. Ele inicia automaticamente.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/0e8a71f1-cd18-43ca-b2e3-4c1ac8bac45b)
 
21.	Espere o trabalho terminar. Pode demorar um pouco;

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/9424239a-a8bb-4f11-b320-10ab4e4baa9a)

22.	Quando o trabalho automatizado de aprendizado de máquina for concluído, você poderá revisar o melhor modelo treinado.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/63a2c503-8621-46b8-9261-e83979c0bcc4)
 
23.	Depois de conquido você seleciona o nome do experimento para exibir mais detalhes;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/37d1cbef-d0ff-479a-a5e7-3851e6e27fa9)
 
24.	Caso você tenha saído da tela enquanto a tarefa não tenha esteja completa, você acessar o menu lateral na opção Tarefas(Jobs);

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/f7e4dc62-a2c4-4e3f-9cd6-83d7a26e8b91)
 
	     24.1. Selecione o nome do experimento e clique sobre ele;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/d3f93815-984f-4cf5-9dfd-88d055d9afcd)
 
	     24.2. Clique para expandir e exibir os detalhes;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/8637eaad-9032-4969-9671-26a1c9a3262c)

	     24.3. Aqui é exibido todos o histórico de como ele foi concluído;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/369c2857-1951-408c-9991-e8ca1a5b9f2a)

	     24.4. Agora volte para a tela anterior e clique sobre o nome;
     
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/16c1e0a4-88d1-41d4-9cd3-6d16bbeefd74)

	     24.5. Selecione o melhor modelo treinado e clique sobre ele;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/fb9c5d7a-3458-49e5-a30e-cfc89e3a3972)

	     24.6. Clique sobre Implatar e escolha Serviço Web;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/d071041e-5871-4802-98e6-8d8ac46f4b07)

	     24.7. Faça as seguintes configurações:
	   	24.7.1. Nome: prever-aluguéis;
	   	24.7.2. Descrição: Prever aluguel de bicicletas;
	   	24.7.3. Tipo de computação: Instância de Contêiner do Azure;
	   	24.7.4. Habilitar autenticação: selecionado;
	   	24.7.5. Clique em implantar;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/99e7ab27-c910-4b29-9cab-8f7d1ca617aa)

	     24.8. Aguarde o início da implantação – isso pode levar alguns segundos. O status de implantação(prever-alugueis) será indicado na parte principal da página como em execução;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/faeb41d4-c9cd-4c37-84ef-38914a9ffc52)

	     24.9. Aguarde até que o status da implantação mude para concluído com êxito . Isso pode levar alguns minutos;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/da27cb75-13b0-48ad-bafd-328c77cbbc54)

25.	Agora vamos testar nosso modelo. No menu lateral clique na guia Pontos de extremidade;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/0b010329-4abe-4f58-b9d6-02f1ab04e342)
 	
	     25.1. Agora selecione o ponto extremidade prever-alugueis;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/5e566656-dfd5-4c6c-b96b-ccc0db15eab8)

	     25.2. No menu da próxima tela selecione a opção testar;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/397950fd-976b-4d9a-ab4f-fa460c3de085)
 
	     25.3. Na próxima tela vamos substituir o modelo JSON sugerido;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/70848198-ae55-498e-923e-46ad4f10f073)
 

	     25.4. Agora vamos substituir o modelo JSON pelos seguintes dados de entrada e clicar em Testar:

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ea69a64d-5e2c-451d-8e64-7adf463d1daf)
 
	     25.5. Os resultados deste teste, que incluem um número previsto de aluguéis com base nos recursos de entrada - semelhante a este;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/eaa1a843-0da5-43e3-a6ca-9cf3f1ccc850)

26.	Resultado: o painel de teste pegou os dados de entrada e usou o modelo treinado para retornar o número previsto de aluguéis.

27.	O serviço web que você criou está hospedado em uma instância de contêiner do Azure . Se você não pretende usá-lo mais, é recomendado  eliminar o ponto extremidade para evitar acumular utilização desnecessária do Azure.
    
	    27.1. No estúdio Azure Machine Learning , na guia ponto extremidade, selecione o ponto de extremidade de previsão de aluguel. Em seguida, selecione Excluir e confirme que deseja excluir o ponto extremidade.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ed7df49b-c0a0-4a39-b2ff-331c1971943f)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/179bfed1-47a7-4ac6-826a-c3b26652affe)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/bb3bf4a7-bdbf-46c2-90c5-baa55473396e)

28.	Excluir sua computação garante que sua assinatura não será cobrada por recursos de computação. No entanto, será cobrada uma pequena quantia pelo armazenamento de dados, desde que o espaço de trabalho do Azure Machine Learning exista na sua assinatura. Se tiver terminado de explorar o Azure Machine Learning, poderá eliminar o espaço de trabalho Azure Machine Learning e os recursos associados.

	     28.1. Para excluir seu espaço de trabalho:
   	        28.1.1. No portal Azure(https://portal.azure.com/), na página Grupos de recursos, clique sobre o grupo de recursos que especificou ao criar o seu espaço de trabalho Azure Machine Learning.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/2a4d6635-a3bf-4939-9b2f-0a386a9ffdb1)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/65aafc09-8e61-4567-9f5a-584d2bab2a98)

		28.1.2.	Clique sobre o recurso que deseja excluir , em seguida escolha a opção delete. Para confirmar que deseja excluí-lo e selecione Excluir.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/59a5ba3d-70bd-4822-a070-40fbd7f2510f)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/dc55a21f-e03d-4fb5-b50c-08e798fa8bd9)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/623f2d50-de0d-494b-b3de-a559bdbf4eb3)

29.	Este foi o passo-a-passo, para demonstrar como eu fiz o uso do recurso de aprendizado de máquina automatizado no Azure Machine Learning e para treinar e avaliar um modelo de aprendizado de máquina. Desde a criação da conta no portal azure até o teste do modelo implantado.
