<h1 align= "center">
  <strong>
Azure AI Speech Studio e Language Studio
  </strong>
</h1>

<h3>
  <strong>
 Nesse desafio vamos explorar o Estúdio de Fala e o Estúdio de Liguagem.
  </strong>
</h3>

<h2 align= "center">
  <strong>
 Explorando o Estúdio de Fala
  </strong>
</h2>

1.	O serviço Azure AI Speech transcreve a fala em texto e o texto em fala audível. Você pode usar o AI Speech para criar um aplicativo que possa transcrever notas de reuniões ou gerar texto a partir da gravação de entrevistas.

  <strong>
 Criando um recurso de fala do Azure AI
  </strong>


2.	Podemos usar o serviço de Fala criando um recurso de Fala ou um recurso de serviços de IA do Azure. Vamos criar um recurso AI Speech, a menos que já tenha um recurso que possa usar.

3.	Abra o endereço https://speech.microsoft.com/portal, e entre em sua conta.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/1366c0fc-63c1-4d28-afb1-015eed342641)

4.	Selecione a opção Configurações.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/6e8a1f04-2157-46e4-9d70-96abc32e506f)
 
5.	Em seguida Crie um recurso. 

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/3db3cce0-f343-4528-bad4-fc97a5205aea)
 

6.	Agora faça as seguintes configurações:

        6.1.	Nome do novo recurso: Insira um nome exclusivo;
  	
        6.2.	Assinatura: sua assinatura do Azure;
  	
        6.3.	Região: Selecione a região geográfica, de preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros;
  	
        6.4.	Tipo de preço:  selecione Padrão S0;
  	
        6.5.	Grupo de recursos: Selecione ou crie um grupo de recursos com um nome exclusivo;
  	
        6.6.	Selecione Criar recurso e aguarde até que o recurso seja criado.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/4b38c91a-2ddf-4a05-b661-ed3a4b518199)
 
7.	Na tela será exibido o recurso criado. Selecione o recurso que acabou de ser criado. E em seguida selecione Usar recurso. A página Introdução à Fala é exibida.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c394852a-1915-4fed-a0da-9f451a383ba2)

8.	Na página Introdução à fala, navegue até a opção Conversão de fala em texto, localize Conversão de fala em texto em tempo real. Usaremos a opção Experimente a Conversão de fala em texto em tempo real.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/fbddd07c-7a3e-4b2a-b3ad-5e9b330f3777)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/e0dca656-2794-4338-976f-c6d61295f250)

9.	Vamos escolher o idioma do audio que queremos converter em texto. Em seguida vá em Escolher arquivos de áudio, selecione Procurar arquivos e navegue até a pasta onde você salvou o arquivo ou escolha a opção gravar áudio com um microfone.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c85c10bd-ba9a-4a79-9918-59e4ab119184)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/a93c2050-c29b-455a-83ab-d1951b4e9d8d)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/be8ba137-6417-4a09-a89b-84eb4dd29887)

10.	O serviço Speech transcreve e exibe o texto em tempo real. Se você tiver áudio em seu computador, poderá ouvir a gravação enquanto o texto é transcrito.

11.	Neste exemplo foi criado um recurso AI Speech no Speech Studio. Em seguida, usamos o serviço de fala em texto em tempo real para transcrever uma gravação de áudio.

<h2 align= "center">
  <strong>
 Analisando texto com o Estúdio de Linguagem
  </strong>
</h2>


12.	Agora vamos explorar os recursos da linguagem Azure AI analisando alguns exemplos de avaliações de hotéis. Vamos usar o Language Studio para entender se as avaliações são em sua maioria positivas ou negativas. O Azure AI Language Service inclui análise de texto e recursos de Processamento de Linguagem Natural (PNL). Isso inclui a identificação de frases-chave no texto e a classificação do texto com base no sentimento.

13.	Para começar vamos criar recurso de idioma. O Azure AI Language possui muitos recursos, para o nosso exemplo utilizaremos um recurso Linguagem. Abra o portal do Azure em https://portal.azure.com e clique no botão ＋ Crie um recurso.

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/88a4a6b3-84cc-4bdf-92ef-86ffcfb76fc2)

14.	Em Categorias, escolha a opção IA + aprendizado de máquina e depois em serviço de idiomas clique em Criar.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/185c9dc7-0a84-4dd0-819d-da1664ecd7fe)

15.	Em seguida você será levado a uma página para selecionar recursos adicionais. Mantenha a seleção padrão e clique em Continue a criar seu recurso.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/9b55c024-b7e4-41d0-ab27-dd835b156ef9)

16.	Na página Criar Idioma, faça as seguintes configurações:

        16.1. Assinatura: sua assinatura do Azure;
   	
        16.2. Grupo de recursos: selecione ou crie um grupo de recursos com um nome exclusivo;
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/feaceb57-5f93-47db-b8c2-dbd661a486cc)

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/b0d72a82-7d03-466a-92d9-828dd2da9e73)

        16.3. Região: Selecione a região geográfica, preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros;
            
        16.4. Nome: Insira um nome exclusivo;
            
        16.5. Nível de preços: F0 grátis ou S se F0 grátis não estiver disponível;
            
        16.6. Ao marcar esta caixa, confirmo que li e compreendi todos os termos abaixo: Selecionada;
            
        16.7. Selecione Revise + crie e depois em Criar e aguarde a conclusão da implantação.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c9fe1780-5346-4325-8080-3a5685e03c20)
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/96965e30-07d1-4e52-8a8e-226ed61f2ad1)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/3dee363c-f6ad-4f85-ac2d-99b01d1495c3)

 

17.	Após concluída a implantação vamos configurar o nosso recurso no Azure AI Language Studio, para isso acesse o Language Studio endereço https://language.cognitive.azure.com e acesse sua conta.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/feb7891d-f81c-4d88-9127-1f73cab1da77)

18.	Em seguida Selecione um recurso do azure fazendo as seguintes configurações:

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/abe80118-73fe-40bd-a0a7-d1be8df76b00)

        18.1. Diretório do Azure: diretório padrão, o diretório que você está usando;
        
        18.2. Assinatura do Azure: selecione a assinatura que você está usando;

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/e82d8eb9-b403-48c0-b7c3-11b01a20fe2c)

        18.3. Tipo de recurso: linguagem;
        
        18.4. Nome do recurso: selecione o recurso de serviço de idioma que você acabou de criar no portal https://portal.azure.com;
        
        18.5. Em seguida, selecione Concluir(Feito). Caso tenha ocorra algum erro no momento da escolha das opções, tente fazer sem traduzir a página.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/09f4eb7a-9c2a-4c50-932a-b531112adbf0)
 
19.	Na página Bem-vindo ao Estudio de Idiomas(Language Studio), selecione a guia Classificar texto. 
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/4e7e61d0-c886-4962-b7b2-3ec4b8983937)


20.	Em seguida, selecione o bloco Analise o sentimento e extraia opiniões.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/fc28a9e0-040b-47c3-811f-eaf245e660f6)

21.	Em Selecionar idioma do texto, selecione o idioma do texto que quer analisar.

22.	Em Selecione seu recurso do Azure, selecione seu recurso.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/50624431-5921-43c0-bfe7-7537fe815df9)

23.	No campo Insira o texto aqui digite seu próprio texto ou carregue um arquivo.
  
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/fb019a90-eeec-4b2d-b5f9-db09f7ba64c3)

24.	Primeiro exemplo, fizemos a escolha do idioma, escolhemos o recurso que criamos e colamos o texto. 

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c84c1947-966c-4f90-b45c-c7384a0f6ba1)

        24.1. Selecionamos o caixa de texto para confirmar que a demonstração incorrerá em uso do recurso e poderá incorrer em custos e clicamos em Executar(Run);
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/9651c34e-3649-40bc-a51e-6756bf0b2722)

        24.2. O resultado da analise considerou que 81% da senteça tem valor positivo, 1% é neutro e 18% é negativo.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/12b54c78-b4c4-46a5-899c-9219a0c1b5c0)

 ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/d41eb7f2-c409-42e8-8b57-56118626f1c1)

25.	Nesse segundo exemplo, fizemos as configurações e executamos.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/55e40f38-806c-4887-b3ce-701e79cffb68)

        25.1. O resultado da analise considerou que 43% da senteça tem valor positivo, 0% é neutro e 57% é negativo.
 
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/da3ee877-efdd-46f8-9ae2-d45a73705954)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/09abbcf5-32cc-4c16-97b5-5dd45cc9e611)

 
26.	Observação: usamos a página sem a tradução em alguns momentos, pois a tradução fazia com ocorressem alguns erros, não permitindo a correta configuração ou erros na tradução das sentenças.

27.	Podemos observar que essa tecnologia pode ajudar a melhorar os serviços ou produtos que as empresas fornecem, através de opinões e percepções de seus usuários e que muitas vezes as soluções podem não ser de dificil solução. As empresas podem usar avaliações positivas a seu favor para atrair novos clientes.

