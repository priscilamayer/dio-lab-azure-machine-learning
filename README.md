# Desafio Modelo de Previsão - Azure Machine Learning

Neste documento explico os passos realizados na execução do desafio proposto no módulo "Trabalhando com Machine Learning na Prática no Azure ML", do curso "Microsoft Azure AI Fundamentals" ministrado pela [DIO](https://web.dio.me). Neste desafio, seguimos a documentação do Microsoft Learning [Explore Automated Machine Learning in Azure Machine Learning](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html), na qual aprendemos a fazer um modelo automatizado de previsão de aluguel de bicicletas baseado em dados históricos sazonais e meteorológicos.

💡 Como meu Microsoft Azure é todo configurado em inglês, alguns botões e termos estarão escritos neste idioma.

## Primeiros Passos - Microsoft Azure
- Após fazer login na conta do Microsoft Azure, na página inicial, clicar no botão "+ Create a Resource";
- No campo de pesquisa, digitar "Machine Learning" e dentre as opções apresentadas clicar em "Azure Machine Learning";
- Clicar em "Create" e seguir os passos de preenchimento dos campos descritos na documentação;
- Clicar em "Review + create", e após validação, clicar em "Create";
- Após deployment completo, clicar em "Launch Studio", o que abrirá a página do [Azure Machine Learning Studio](https://ml.azure.com).

## Configurando Modelos e Conjuntos de Dados - Azure Machine Learning Studio
- Depois de entrar na página do Azure Machine Learning Studio, clicar no menu "Automated ML", opção "New Automated ML job" e seguir os passos de preenchimento dos campos descritos na documentação;
- Por se tratar de valores numéricos, o tipo de aprendizado de máquina escolhido é Regressão;
- Os dados que serão utilizados para a criação do modelo de previsão são fornecidos por uma URL também presente na documentação;
- Após terminar de configurar os demais campos, conforme indicado pela documentação, clicar em "Review" e em seguida em "Submit training job".

## Análise e Teste de Modelo - Azure Machine Learning Studio
- Após terminar de rodar o programa, ele nos fornece vários dados, entre eles o modelo gerado. No caso do exemplo apresentado pela professora na aula, o modelo foi gerado automaticamente. No meu caso, precisei seguir as instruções da documentação para conseguir abri-lo;
- Para isso, na aba "Overview" do experimento, selecionar o texto abaixo de "Algorithm name", para abrir o melhor modelo gerado e seguir as configurações propostas;
- Após essa configuração, deve-se ir na aba à esquerda e clicar em "Models", então em "Details" e selecionar o modelo indicado em "Registered Model";
- Então clicar em "Metrics", que apresentará, entre outros dados, dois gráficos - "predicted_true"(gráfico em linhas que mostra os valores preditos e os reais) e "residuals"(gráfico em colunas que mostra a diferença entre os valores preditos e os reais);
- Para finalizar e testar o modelo, na aba à esquerda clicar em "Endpoints" e então em "Test", colocar os dados fornecidos na documentação e clicar no botão "Test".

## Resultados encontrados
Após rodar o teste, o sistema forneceu o número float 364.78935594629985, ou seja, o modelo automatizado prevê que será necessário disponibilizar 364 bicicletas para alugar no dia determinado, com as condições meteorológicas fornecidas.

## 💻Programas Utilizados
![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white) ![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) ![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)