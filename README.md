# :rocket: Search Engine (IMDB Movies)
![Sonic](./projeto/multimedia/imagem_tema.jpg)
---

:memo: Este é um pequeno motor de busca do top 1000 de filmes do IMDB.
Fácil de utilizar e de visualização agradável.

---
## Indíce
---

- [Pré-requisitos](#hammer_and_wrench-pré-requisitos)
- [Instalação](#gear-instalação)
    - [Python](#python)
    - [Poetry](#poetry)
    - [Instalação do programa](#instalação-do-programa)
- [Execução](#arrow_forward-execução)
    - [Execução do Programa](#execução-do-programa)
- [Estrutura do motor de busca](#building_construction-estrutura-do-motor-de-busca)
    - [Página Inicial](#página-inicial)
    - [Pesquisa](#pesquisa)
        - [Ano](#ano)
        - [Avaliação](#avaliação)
        - [Nome](#nome)
    - [Resultado da pesquisa](#resultados-da-pesquisa)
    - [Detalhes do filme](#mag-detalhes-do-filme)
    - [Barra Lateral](#barra-lateral)
- [Possivéis melhorias](#possíveis-melhorias)
- [Autor](#-autor)
- [Licença](#-licença)

---
## :hammer_and_wrench: Pré-requisitos
---
* Necessita de ter instalado o **Python 3.14** ou superior no sistema operativo.

* Este projeto foi desenvolvido utilizando o gerenciador de pacotes **Poetry**.
Como tal será necessário também o **pipx** para instalar o Poetry.


* Ter o dataset: **[filmes_imdb.csv](projeto/base_dados/filmes_imdb.csv)** que está presente no pacote do projeto.

[:top: Indice](#indíce)

---
## :gear: Instalação
---
Garantir que tem o Python (versão 3.14) instalado bem como o Poetry. Se assim não for, para instalar:

#### Python

Através do [site oficial](https://www.python.org/downloads/?hl=pt):

- 1.Clicar no botão 'Download'.

- 2.Clique [aqui](https://www.youtube.com/watch?v=8cAEH1i_5s0) e siga as instruções do video.

#### Poetry

Após a instalação do Python, para instalar o Poetry:

- 1º Instalação do ***pipx***:

    Abra o terminal e escreva:

```cmd
pip install --user pipx
```

- 2º Garantir o funcionamento correto do pipx, bem como as suas funcionalidades:

```cmd
python -m pipx ensurepath
```

- 3º Instalação do Poetry:

```cmd
pipx install poetry
```

### Instalação do programa

Após a instalação dos pré-requisitos, antes de rodar o projeto, terá que clonar o repositório do Github que se encontra ==[aqui](https://github.com/BrunoMGCardoso/Search_engine_imdb_movies)== e instalar o programa através do poetry.

Para tal, no terminal:
1. Navegue até á pasta onde pretende guardar o repositório e insira o comando:

```cmd
git clone https://github.com/BrunoMGCardoso/Search_engine_imdb_movies
```
2. navegue até á pasta raiz do projeto e escreva:

```cmd
poetry install
```

Este comando irá instalar tudo o que é necessário para rodar o programa.

[:top: Indice](#indíce)

---
## :arrow_forward: Execução
---

### Execução do programa

Para executar o programa, abrir o terminal na pasta raiz do projeto e executar o comando:

```cmd
poetry run streamlit run projeto\app.py
```

Após este comando irá aparecer no terminal 2 URL's:
- Local URL;
- Network URL;

![URL's para exibição de Motor de busca](/docs/img/url_streamlit.png)

Para exibir o Motor de busca, se este não abrir automaticamente, prima `CTRL + clique` em cima de uma das url's.

[:top: Indice](#indíce)

---
## :building_construction: Estrutura do Motor de busca
---

### Página inicial

Quando abrir o programa irá aparecer a página inicial, como segue na imagem abaixo.

![Página Inicial](/docs/img/layout_motor_busca.png)

### Pesquisa

A pesquisa por filmes pode ser feita por [ano](#ano), [avaliação](#avaliação) ou por [nome](#nome).

#### Ano

![Pesquisa por Ano](/docs/img/pesquisa_ano.png
)

Quando selecionado o atributo Ano, irá aparecer uma barra para poder selecionar o ano de pesquisa pretendido.

#### Avaliação

![Pesquisa por Avaliação](/docs/img/pesquisa_avaliacao.png
)

Quando selecionado o atributo Avaliação, aparcerá uma barra com dois valores, onde deverá selecionar o intervalo desejado, um para o valor mínimo e outro para o valor máximo. 
#### Nome

![Pesquisa por Nome](/docs/img/pesquisa_nome.png
)

Por último, quando seleciona o atributo Nome, irão aparecer dois campos a preencher, um primeiro onde deve escrever o nome do filme ou palavras que possam identificar o mesmo, e outro onde deverá selecionar o nível de semelhança que pretende na pesquisa.

==ATENÇÃO!!!==
==A pesquisa pelo nome terá que ter nomínimo 3 caracteres para poder proceder á pesquisa, sendo o único campo de obrigatório preenchimento.==

### Resultados da Pesquisa

Após selecionar o atributo pelo qual quer pesquisar, bem como os campos subsequentes desta seleção, clique em `Pesquisar`. Este botão irá fazer aparecer o resultado da pesquisa.

Todos os resultados irão aparecer dentro de um contentor. A única diferença na apresentação dos resultados será que por caminho do Nome, aparcerá a percentagem de semelhança entre este e o filme correspondente.

*Exemplo de pesquisa por Ano/Avaliação*

![Pesquisa por Ano ou Avaliação](/docs/img/resultado_pesquisa_ano_avaliacao.png)

*Exemplo de pesquisa por Nome*

![Pesquisa por Ano ou Avaliação](/docs/img/resultado_pesquisa_nome.png)

### :mag: Detalhes do filme

Após o processo de pesquisa, a lista do resultado da pesquisa fica disponível nesta parte do programa.

*Exemplo de lista com resultados*

![Lista de filmes](/docs/img/lista_resultados_pesquisa.png)

Pode-se assim, consultar os filmes com mais detalhe, onde aparecem atributos como, o nome, o ano de lançamento, a duração do filme e uma curta descrição.

![Detalhes de filme](/docs/img/exemplo_detalhe_filme.png)

> Para uma nova pesquisa basta alterar por que atributo se quer pesquisar ou o parametro desse atributo.

### Barra Lateral

O motor de busca conta ainda com um menu lateral que contém 2 opções, uma com a lista completa dos filmes presentes na base de dados e outra com uma ligação ao site do Internet Movies Database (IMDB).

Para lhe aceder, basta clicar na seta no canto superior esquerdo do ecrã.

![acesso ao menu lateral](/docs/img/acesso_menu.png)

*Menu Lateral*

![Menu Lateral](/docs/img/menu_lateral.png)

[:top: índice](#indíce)
 
---
## Possíveis melhorias
---

Como todo o projeto, haverá sempre melhorias a fazer, não havendo uma versão definitiva, estando sempre susceptível a alterações.
Algumas melhorias podem ser:

* Melhoria da interface do utilizador (UI);

* Adição outros métodos de pesquisa;

* Aplicação da base de dados dos filmes através de uma API do IMDB;

* Adição de outras funcionalidades e ligações externas;

[:top: índice](#indíce)

---
## 👤 Autor
---

Bruno Cardoso
2026
[:cat: Github](https://github.com/BrunoMGCardoso)
[:e-mail: E-mail](mailto:bruno.cardoso.professional@gmail.com)
[:briefcase: LinkedIn](https://www.linkedin.com/in/brunomgcardoso/)

[:top: índice](#indíce)

---
## 📜 Licença
---

Este projeto foi desenvolvido sob a [MIT License](LICENSE)

[:top: índice](#indíce)