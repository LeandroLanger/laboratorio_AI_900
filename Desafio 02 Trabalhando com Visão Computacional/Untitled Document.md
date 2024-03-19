<h2 align= "center">
  <strong>
Azure AI Vision Studio
  </strong>
</h2>

1. Para começar  abra o portal do Azure em https://portal.azure.com ,
entrando com a conta da Microsoft associada à sua assinatura do Azure.
Depois você deve criar um recurso clicando na opção Crie um recurso;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/7a5abc21-5f18-427b-8c76-2c5f52ae9cf8)

2. Depois vá em Categorias e escolha a opção IA + Aprendizado de máquina;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/7cda43d8-0ed7-4c1c-97b3-0ccc8b4a1309)

3.	Em seguida vá até a opção Serviços de IA do Azure e escolha criar;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/e9f8e02b-536c-4b84-b777-c8cc8e9c4b0e)

4.	Na tela que abrirá você deverá fazer as seguintes configurações;

        4.1.	Assinatura: sua assinatura do Azure;

        4.2.	Grupo de recursos: Crie ou selecione um grupo de recursos;
  	
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/607c423f-bacc-4e42-ba7d-0bdce55f5da4)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c271f0fd-b6ff-441e-aea3-92ff01cd7161)

        4.3.  Região: Selecione a região geográfica, de preferencialmente alguma região dos EUA, pois os recurso do Brasil geralmente são mais caros;
      
        4.4.  Nome: Insira um nome exclusivo;   

        4.5.  Nível de preços: Padrão S0;
    
        4.6.  Ao marcar esta caixa, confirmo que li e compreendi todos os termos abaixo: Selecionado;
  
        4.7.  Após preencher todos os campos, deve-se clicar no botão Revise + crie . e depois Criar e aguarde a conclusão da implantação;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/f73e1214-675e-4bde-afd9-dc6737bf030d)

        4.8. E depois clique em Create(Criar) e aguarde a conclusão da implantação;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/cbeb1c63-a0b5-4f9b-9101-ba06c3c2335f)

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/866ddbea-dc97-49a1-bef8-ef20d94ac64e)

5. Após concluída a etapa anterior você deve conectar ao recurso de serviços de IA do Azure provisionado acima ao Vision Studio pelo endereço https://portal.vision.cognitive.azure.com. 

6.	Entre com sua conta e certifique-se de usar o mesmo diretório onde você criou seu recurso de serviços de IA do Azure.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ce40d62d-238b-49cf-9450-3f96a05e8a5d)

7.	Na página inicial do Vision Studio, selecione Visualizar todos os recursos.

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/e3514768-1600-4d78-90a9-cd0eaba18b86)

8. Na página Selecione um recurso para trabalhar, passe o cursor do mouse sobre o recurso que você criou
acima na lista e marque a caixa à esquerda do nome do recurso e selecione.
Selecionar como recurso padrão;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/aac0dc55-16f3-46b1-a670-3bef7b67e514)

9.	Após feito isso, feche a página de configurações
selecionando o “x” no canto superior direito da tela;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/8a7977c5-506a-4292-81b8-5dca647961f6)


<h2 align= "center">
  <strong>
Detectando rostos com Vision Studio
  </strong>
</h2>

10.	Na página inicial do Vision, selecione a guia Face; 

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c28c154c-15d2-4edd-9ad2-ba489ed4cd75)

11.	Agora selecione o bloco Detectar rostos em uma imagem;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/db86075f-9eca-4fc9-98bb-b8f7c23076fb)

12.	Você deve marcar Experimente, para aceitar a política de uso de recursos;

  ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/f77fce7e-e757-4265-85aa-cd725af9c2a9)

13.	Agora selecione uma imagem de amostra e observe os dados de detecção facial
retornados. Você pode usar as imagens disponíveis no Vision ou se preferir você pode
usar imagens próprias do seu computador ou tirar foto;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/ccb39a67-5ba5-4f1b-803e-df7b9a2a7d36)
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/31376dd2-8cfe-4a89-962f-84aea76a067d)

<h2 align= "center">
  <strong>
Extraindo texto de imagens no Vision Studio
  </strong>
</h2>

14.	Na página inicial do Vision, selecione Reconhecimento óptico de caracteres;

  ![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/b78dee5b-f79f-498d-957a-7aa0bda32f7e)

15.	Agora selecione o bloco Extrair texto de imagens;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/541104bf-e78d-43aa-9968-b8062b988827)

16.	Você deve marcar Experimente, para aceitar a política de uso de recursos;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/14a484da-d3bb-4d2e-9348-95cb4d44158c)

17.	Agora selecione um arquivo de amostra e observe os atributos detectados.
Você pode usar os arquivos disponíveis no Vision ou se preferir você pode usar
arquivos próprios do seu computador. Nas imagens, a localização do texto é
indicada por uma caixa delimitadora;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/c69e5d7c-966a-4c57-b3f7-524417936c62)
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/a1c27755-cc12-4195-8fab-d89320051e29)

<h2 align= "center">
  <strong>
Gerando legendas para uma imagem usando o Vision Studio
  </strong>
</h2>

18.	Na página inicial  do Vision, selecione a guia Análise de imagem;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/d5cc1c6a-04ed-47b3-99c4-761baa02c068)

19.	Agora selecione o bloco Adicionar legendas às imagens;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/b957666a-d1cc-46cd-81d1-eba23710f028)

20.	Você deve marcar Experimente, para aceitar a política de uso de recursos;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/344304a5-be88-407e-a9f6-586f44e9877a)

21.	Agora selecione um arquivo de amostra e observe os atributos detectados.
Você pode usar os arquivos disponíveis no Vision ou se preferir você pode usar
arquivos próprios do seu computador. Nas imagens, observe o texto da legenda gerada,
visível no painel Atributos detectados. Esta funcionalidade fornece uma única frase
que descreve o conteúdo da imagem;

![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/af741217-2432-47cd-9b4e-5ff513b8d63d)
![image](https://github.com/LeandroLanger/laboratorio_AI_900/assets/114670890/6948cac3-7e6f-4a74-89fe-26883e143062)

22.	Podemos dizer que existem inúmeras possibilidades usando essas ferramentas como
autenticação através da leitura e o rastreamento de rostos em vídeos para análise de
comportamento. Observamos que é possível usar a ferramenta para digitalização de
documentos físicos para facilitar a busca e armazenamento, bem como a extração de
dados de recibos e notas fiscais. Ainda vimos que podemos usar a ferramenta para
auxiliar na Acessibilidade para pessoas com deficiência visual, no auxílio para
descrever imagens para fins educacionais, entre tantas outras mais;

23.	Aprendemos que essa ferramenta oferece recursos para criar soluções de
reconhecimento de imagem, detecção de objetos e análise visual em diversos domínios,
como segurança, saúde, varejo e entretenimento.
