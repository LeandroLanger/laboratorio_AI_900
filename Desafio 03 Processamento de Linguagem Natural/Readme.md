Nesse desafio vamos explorar o Estúdio de Fala e o Estúdio de Liguagem.

Explorando o Estúdio de Fala
1.	O serviço Azure AI Speech transcreve a fala em texto e o texto em fala audível. Você pode usar o AI Speech para criar um aplicativo que possa transcrever notas de reuniões ou gerar texto a partir da gravação de entrevistas.
Criando um recurso de fala do Azure AI

2.	Podemos usar o serviço de Fala criando um recurso de Fala ou um recurso de serviços de IA do Azure . Vamos criar um recurso AI Speech, a menos que já tenha um recurso que possa usar.
3.	Abra o endereço https://speech.microsoft.com/portal, e entre em sua conta.
 

4.	Selecione a opção Configurações.

 
5.	Em seguida Crie um recurso. 

 

6.	Agora faça as seguintes configurações:

        6.1.	Nome do novo recurso: Insira um nome exclusivo;
        6.2.	Assinatura: sua assinatura do Azure;
        6.3.	Região: Selecione a região geográfica, de preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros;
        6.4.	Tipo de preço:  selecione Padrão S0;
        6.5.	Grupo de recursos: Selecione ou crie um grupo de recursos com um nome exclusivo;
        6.6.	Selecione Criar recurso e aguarde até que o recurso seja criado .
 
7.	Na tela será exibido o recurso criado. Selecione o recurso que acabou de ser criado. E em seguida selecione Usar recurso . A página Introdução à Fala é exibida.
 

8.	Na página Introdução à fala, navegue até a opção Conversão de fala em texto, localize Conversão de fala em texto em tempo real . Usaremos a opção Experimente a Conversão de fala em texto em tempo real.
 
 

9.	Vamos escolher o idioma do audio que queremos converter em texto. Em seguida vá em Escolher arquivos de áudio , selecione Procurar arquivos e navegue até a pasta onde você salvou o arquivo ou escolha a opção gravar áudio com um microfone.
 
 

 
10.	O serviço Speech transcreve e exibe o texto em tempo real. Se você tiver áudio em seu computador, poderá ouvir a gravação enquanto o texto é transcrito.
11.	Neste exemplo foi criado um recurso AI Speech no Speech Studio. Em seguida, usamos o serviço de fala em texto em tempo real para transcrever uma gravação de áudio.

Analisando texto com o Estúdio de Linguagem

12.	Agora vamos explorar os recursos da linguagem Azure AI analisando alguns exemplos de avaliações de hotéis. Vamos usar o Language Studio para entender se as avaliações são em sua maioria positivas ou negativas.
O Azure AI Language Service inclui análise de texto e recursos de Processamento de Linguagem Natural (PNL). Isso inclui a identificação de frases-chave no texto e a classificação do texto com base no sentimento.

13.	Para começar vamos criar recurso de idioma. O Azure AI Language possui muitos recursos, para o nosso exemplo utilizaremos um recurso Linguagem. Abra o portal do Azure em https://portal.azure.com e clique no botão ＋ Crie um recurso.
 
14.	Em Categorias, escolha a opção IA + aprendizado de máquina e depois em serviço de idiomas clique em Criar.
 

15.	Em seguida você será levado a uma página para selecionar recursos adicionais . Mantenha a seleção padrão e clique em Continue a criar seu recurso .
 

16.	Na página Criar Idioma , faça as seguintes configurações:
    16.1.	Assinatura: sua assinatura do Azure .
    16.2.	Grupo de recursos: selecione ou crie um grupo de recursos com um nome exclusivo .
 

 
            16.3.	Região: Selecione a região geográfica, preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros.
            16.4.	Nome: Insira um nome exclusivo.
            16.5.	Nível de preços: F0 grátis ou S se F0 grátis não estiver disponível
            16.6.	Ao marcar esta caixa, confirmo que li e compreendi todos os termos abaixo: Selecionada .
            16.7.	Selecione Revise + crie e depois em Criar e aguarde a conclusão da implantação.

 

 

 

17.	Após concluida a implantação vamos configurar o nosso recurso no Azure AI Language Studio, para isso acesse o Language Studio endereço https://language.cognitive.azure.com e acesse sua conta.
 

18.	Em seguida Selecione um recurso do azure fazendo as seguintes configurações:
 
        18.1.	Diretório do Azure : diretório padrão, o diretório que você está usando.
        18.2.	Assinatura do Azure : selecione a assinatura que você está usando.
 
        18.3.	Tipo de recurso: linguagem.
        18.4.	Nome do recurso : selecione o recurso de serviço de idioma que você acabou de criar no portal https://portal.azure.com.
        18.5.	Em seguida, selecione Concluir(Feito). Caso tenha ocorra algum erro no momento da escolha das opções, tente fazer sem traduzir a página.

 

19.	Na página Bem-vindo ao Estudio de Idiomas(Language Studio), selecione a guia Classificar texto. 
 


20.	Em seguida, selecione o bloco Analise o sentimento e extraia opiniões .
 
21.	Em Selecionar idioma do texto , selecione o idioma do texto que quer analisar.
22.	Em Selecione seu recurso do Azure , selecione seu recurso.
 

23.	No campo Insira o texto aqui digite seu próprio texto ou carregue um arquivo.
  

24.	Primeiro exemplo, fizemos a escolha do idioma, escolhemos o recurso que criamos e colamos o texto. 
 
        24.1.	Selecionamos o caixa de texto para confirmar que a demonstração incorrerá em uso do recurso e poderá incorrer em custos e clicamos em Executar(Run)
 

        24.2.	O resultado da analise considerou que 81% da senteça tem valor positivo, 1% é neutro e 18% é negativo.
 
 
25.	Nesse segundo exemplo, fizemos as configurações e executamos.
        
        25.1.	O resultado da analise considerou que 43% da senteça tem valor positivo, 0% é neutro e 57% é negativo.
 


 
26.	Observação: usamos a página sem a tradução em alguns momentos, pois a tradução fazia com ocorressem alguns erros, não permitindo a correta configuração ou erros na tradução das sentenças.

27.	Podemos observar que essa tecnologia pode ajudar a melhorar os serviços ou produtos que as empresas fornecem, através de opinões e percepções de seus usuários e que muitas vezes as soluções podem não ser de dificil solução. As empresas podem usar avaliações positivas a seu favor para atrair novos clientes.

