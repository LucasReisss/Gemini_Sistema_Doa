<h1>Sistema de Busca de Doações com Google Gemini</h1>

Este projeto demonstra um sistema de busca de locais de doação usando embeddings de texto gerados pelo Google Gemini e uma interface interativa com ipywidgets.

Descrição

**O sistema permite que os usuários insiram uma consulta em linguagem natural, como "Onde posso doar roupas em São Paulo?", e retorna uma lista de locais de doação relevantes.**

**Funcionalidades:**

- **Processamento de Linguagem Natural:** Normaliza a consulta do usuário e extrai a cidade.
- **Geração de Embeddings:** Usa o Google Gemini para gerar embeddings de texto para os locais de doação e a consulta do usuário.
- **Busca por Similaridade:** Calcula a similaridade entre a consulta e os locais de doação usando o produto escalar dos embeddings.
- **Ranking e Randomização:** Classifica os locais de doação por similaridade e randomiza a ordem dos resultados para apresentar variedade.
- **Geração de Resposta:** Usa o Google Gemini para gerar uma resposta textual concisa e informativa, incluindo o nome, cidade, endereço e horário do local de doação.
- **Interface Interativa:** Fornece uma interface amigável com widgets para entrada de texto e botões de busca e limpeza.

Pré-requisitos

- **Conta do Google Cloud:** Você precisa de uma conta do Google Cloud com a API do Google Generative AI habilitada.
- **Chave de API:** Obtenha sua chave de API do Google Cloud e armazene-a em um local seguro.
- **Biblioteca google.generativeai:** Instale a biblioteca Python google.generativeai usando pip install google-generativeai.
- **Biblioteca ipywidgets:** Instale a biblioteca Python ipywidgets usando pip install ipywidgets.
- **Arquivo CSV "doacoes.csv":** Crie um arquivo CSV com os seguintes campos:
- Cidade: Cidade do local de doação.
- Nome: Nome do local de doação.
- Endereco: Endereço do local de doação.
- Tipo\_de\_Doacao: Tipo de doação aceita (ex: roupas, alimentos, brinquedos).
- Horario: Horário de funcionamento do local de doação.

Como Usar

1. **Configure a Chave de API:** Substitua YOUR\_API\_KEY no código pela sua chave de API do Google Cloud.
1. **Carregue o Arquivo CSV:** Carregue o arquivo "doacoes.csv" com as informações dos locais de doação.
1. **Execute o Código:** Execute o código Python em um ambiente Colab.
1. **Digite sua Consulta:** Use a interface de widgets para inserir sua consulta em linguagem natural.
1. **Veja os Resultados:** O sistema exibirá uma lista de locais de doação relevantes com nome, cidade, endereço e horário.
1. **Limpe os Resultados:** Use o botão "Limpar" para limpar a lista de resultados.

Exemplo de Consulta

**Entrada:** Onde posso doar brinquedos em Belo Horizonte?

**Saída:**

- **Resultado 1:** [Resposta gerada pelo modelo com informações sobre o local de doação]
- **Resultado 2:** [Resposta gerada pelo modelo com informações sobre o local de doação]
- **Resultado 3:** [Resposta gerada pelo modelo com informações sobre o local de doação]

Notas

- Os dados no arquivo "doacoes.csv" são fictícios para fins de demonstração.
- O modelo de linguagem Gemini pode gerar respostas ligeiramente diferentes a cada vez que é executado.
- O número de resultados exibidos pode ser ajustado modificando o parâmetro num\_resultados na função gerar\_e\_buscar\_consulta.

Próximos Passos

- **Integrar com uma API de Mapas:** Exibir os locais de doação em um mapa para facilitar a visualização.
- **Adicionar Filtros:** Permitir que os usuários filtrem os resultados por tipo de doação, horário de funcionamento, etc.
- **Melhorar a Interface:** Criar uma interface mais visualmente atraente e intuitiva.
- **Treinar um Modelo Personalizado:** Treinar um modelo de embedding personalizado com um conjunto de dados de doações mais abrangente para melhorar a precisão da busca.
