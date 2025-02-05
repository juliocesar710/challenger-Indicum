Segue o conteúdo em formato Markdown:


# Projeto EDA e Precificação de Imóveis

Este projeto realiza uma análise exploratória dos dados (EDA) de anúncios de imóveis, gera visualizações, analisa características textuais e constrói um modelo preditivo (regressão linear) para estimar o preço dos imóveis.

## Requisitos

- Python 3.7 ou superior
- Acesso ao arquivo de dados `teste_indicium_precificacao.csv` (deve estar localizado na pasta `/data/raw_data/teste_indicum_precificacao.csv` ou ajustar o caminho conforme necessário)

## Dependências

O projeto utiliza as seguintes bibliotecas Python:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `joblib`
- `nltk`
- `wordcloud`

## Instalação

1. **Crie e ative um ambiente virtual (opcional, mas recomendado):**

   ```bash
   python -m venv venv
   # No Windows:
   venv\Scripts\activate
   # No Linux/macOS:
   source venv/bin/activate
   ```

2. **Instale as dependências:**

   Execute o seguinte comando:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn joblib nltk wordcloud
   ```

    Também pode executar diretamente pelo os arquivo `requeriments.txt`
   ```
   pip install -r requirements.txt
   ```

3. **Configuração do NLTK:**

   O script realiza o download dos *stopwords* do NLTK automaticamente. Caso prefira fazer o download manualmente, execute:

   ```python
   import nltk
   nltk.download('stopwords')
   ```

## Execução do Projeto

1. **Verifique o local do arquivo CSV:**

   O script lê o dataset a partir do caminho `/content/teste_indicium_precificacao.csv`. Caso o arquivo esteja em outro diretório, ajuste o caminho no script.(recomendo sempre conferir o caminho)

2. **Executando o script:**

   Se estiver utilizando um Jupyter Notebook ou Google Colab, basta executar as células sequencialmente. Para executar como script Python, utilize:

   ```bash
   python eda.py
   ```

   O script realiza as seguintes etapas:
   
   - Carregamento e pré-processamento dos dados;
   - Geração de gráficos e visualizações;
   - Análise de correlação e distribuição de variáveis;
   - Processamento textual, criação de wordcloud e análise de frequência de palavras;
   - Preparação dos dados e treinamento de um modelo de regressão linear para previsão de preços;
   - Exemplo de previsão para um novo imóvel;
   - Salvamento do modelo preditivo em um arquivo (`modelo1.pkl`).

## Observações

- Certifique-se de que o arquivo CSV de dados esteja disponível e no caminho especificado.
- Se estiver utilizando o Google Colab, faça upload do arquivo CSV para o ambiente.
- Caso necessite ajustar hiperparâmetros ou caminhos, edite o script conforme necessário.

