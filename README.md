🏠 Previsão de Preços Airbnb — Aplicação em Streamlit

Este projeto implementa uma aplicação interativa em Streamlit que permite prever o valor de imóveis listados no Airbnb, com base em características do imóvel, do anfitrião e das condições de reserva. O modelo de Machine Learning foi previamente treinado e está disponível no arquivo modelo.joblib.

🚀 Funcionalidades

Interface web amigável para entrada de dados
Suporte a variáveis:
Numéricas: latitude, longitude, número de hóspedes, banheiros, quartos, camas, noites mínimas, etc.
Binárias (Sim/Não): anfitrião é superhost, reserva instantânea
Categóricas: tipo de propriedade, tipo de quarto, política de cancelamento
Padronização automática das variáveis para compatibilidade com o modelo
Previsão imediata do valor do imóvel no Airbnb

🛠️ Tecnologias Utilizadas

Tecnologia	Finalidade

Streamlit	Interface web interativa

Pandas	Manipulação de dados tabulares

Joblib	Carregamento do modelo de Machine Learning

Scikit-Learn	Treinamento do modelo (fora deste script)

📂 Estrutura de Arquivos

📦 airbnb-previsao

 ┣ 📜 DeployAirbnb.py    # Código principal da aplicação
 
 ┣ 📜 modelo.joblib      # Modelo de Machine Learning treinado
 
 ┣ 📜 dados.csv          # Base de dados usada no pré-processamento
 
 ┣ 📜 Descrição do Projeto.ipynb  # Documentação exploratória
 
 ┣ 📜 main.ipynb         # Notebook principal de análise e treino

▶️ Como Executar

Instale as dependências:
pip install streamlit pandas joblib scikit-learn


Certifique-se de ter na pasta do projeto:
modelo.joblib
dados.csv
Execute a aplicação:
streamlit run DeployAirbnb.py
Acesse no navegador o endereço exibido (ex.: http://localhost:8501).

📊 Funcionamento

O usuário insere as características do imóvel através da interface:

Ex.: property_type = Apartment, room_type = Entire home/apt, bathrooms = 2

As entradas são convertidas para um vetor de variáveis dummy compatível com o modelo.

O modelo modelo.joblib é carregado e aplicado às entradas.

O preço previsto é exibido na tela.

📷 Exemplo de Interface

Campos numéricos para latitude, longitude, banheiros, quartos etc.

Menus suspensos (selectbox) para categorias como:
Tipo de propriedade,
Tipo de quarto,
Política de cancelamento,
Botão "Prever Valor do Imóvel",
Resultado exibido diretamente na tela.
