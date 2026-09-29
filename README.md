# Prova-tecnica---Ade-Sampa
Projeto desenvolvido para a segunda etapa do processo seletivo, conforme Edital nº 05/2026 - Ade Sampa


# Nome do projeto: 📚 Troca Livro SP

> Uma proposta de solução digital para facilitar a circulação de livros entre estudantes, educadores e responsáveis da Rede Municipal de Ensino de São Paulo, por meio de troca ou doação.

---

## 📌 Sobre o projeto

O **Troca Livro SP** é um protótipo de solução digital (vibe code) desenvolvido a partir de uma oportunidade de melhoria relacionada à circulação e ao reaproveitamento de livros didáticos e/ou literários dentro da Rede Municipal de Ensino.

A proposta é criar um ambiente em que estudantes ou responsáveis possam disponibilizar livros vinculados a uma escola municipal, escolhendo entre duas modalidades:

- 🔄 **Troca** — disponibilizar um livro e receber outro em troca;
- 🎁 **Doação** — disponibilizar um livro gratuitamente para outro interessado.

A plataforma permite cadastrar livros, buscar livros, solicitar, acompanhar solicitações, aceitar ou recusar pedidos e registrar a conclusão da operação.

Além da experiência do usuário, o projeto foi pensado desde o início para gerar dados estruturados que possam apoiar análises e decisões de gestão, permitindo visualizar a distribuição territorial dos pontos relacionados à solução e analisar padrões de utilização.

---

## 🎯 Problema e oportunidade

A circulação de livros pode contribuir para o reaproveitamento de materiais, o acesso a conteúdos educacionais e literários e a ampliação do uso de recursos que já estão disponíveis na comunidade escolar.

Já existem iniciativas presenciais relacionadas à circulação e troca de livros, como feiras e encontros. A proposta deste projeto não é substituí-las, mas explorar como uma camada digital de busca, conexão e acompanhamento das operações poderia complementar essas iniciativas.

A partir dessa oportunidade, surgiu a seguinte pergunta:

> Como uma plataforma digital poderia facilitar a conexão entre quem possui um livro disponível e quem procura determinado material, ao mesmo tempo em que gera dados úteis para a gestão?

---

## 💡 A solução

O Troca Livro SP conecta:

```text
Pessoa que disponibiliza um livro
              ↓
Livro associado a uma escola municipal
              ↓
Busca por título, autor ou categoria
              ↓
Solicitação de troca ou doação
              ↓
Aceitação ou recusa
              ↓
Voucher/comprovante da transação
              ↓
Confirmação da retirada
              ↓
Dados estruturados para análise
```

A escola funciona como referência para a disponibilidade e retirada do livro.

---

## 🔄 Fluxo da operação

### Doação

1. Usuário cadastra um livro como **Doação**.
2. O livro fica disponível para busca.
3. Outro usuário solicita o livro.
4. A pessoa que disponibilizou o livro recebe a solicitação.
5. A solicitação pode ser aceita ou recusada.
6. Quando aceita, o livro passa para **Reservado**.
7. O sistema gera um **Voucher de Retirada / Comprovante da Transação**.
8. Após a retirada, a operação é concluída como **Doado**.

### Troca

1. Usuário cadastra um livro como **Troca**.
2. Outro usuário solicita a troca.
3. O interessado informa o livro que pretende oferecer.
4. A pessoa que disponibilizou o livro analisa a solicitação.
5. A solicitação pode ser aceita ou recusada.
6. Após a aceitação, a operação passa para **Reservado**.
7. O sistema gera o comprovante.
8. Após a retirada, a operação é concluída como **Trocado**.

---

## 📊 Dados e estrutura

A aplicação foi estruturada para registrar os principais eventos da operação:

- livros;
- usuários por meio de identificadores técnicos;
- escolas;
- solicitações;
- transações.

A base de escolas utilizada no projeto foi obtida a partir de dados oficiais da Rede Municipal de Ensino e utilizada como referência para associar os livros às escolas. Nesse processo, a base oficial passou por um tratamento considerando apenas escolas ativas e pública; as particulares e parcerias foram desconsideradas nesse projeto.


> **Atenção:** os dados utilizados para demonstrar o funcionamento da plataforma são sintéticos e não representam estatísticas reais da Prefeitura de São Paulo.

---

## 🔐 Privacy by Design

A preocupação com privacidade foi incorporada à concepção da solução.

A plataforma não precisa conhecer ou disponibilizar, para fins de análise, informações pessoais desnecessárias do cidadão.

Para relacionar operações de um mesmo usuário, é utilizado um identificador técnico (`user_id`), sem necessidade de exportar nome, e-mail, CPF, telefone ou endereço residencial.

Por outro lado, os dados institucionais das escolas são preservados, pois podem ser relevantes para análises territoriais e de gestão.

A proposta segue o princípio de **minimização de dados**, buscando utilizar somente as informações necessárias para cada finalidade.

O protótipo também possui uma política de privacidade demonstrativa, pensada como referência para uma eventual implementação institucional futura.


---

## 📈 Dados para gestão e análise

A exportação dos dados foram pensados em dados estruturados para posterior análise em ferramentas de análise. Nesse caso, para fins de demonstração, foi utilizada uma base sintética/simulada, preenchida com o auxílio de AI, sendo utilizados exclusivamente para testar os fluxos analíticos e construir visualizações e demonstrar possibilidades de geração de indicadores. 


---

## 📊 Análise de dados

A análise foi dividida em duas frentes complementares.

### BI — visão gerencial

A ferramenta de BI foi utilizada para construir uma visão destinada ao acompanhamento da operação.

### Python — exploração e análise

Python foi utilizado como uma segunda camada de análise, permitindo explorar os dados de forma espacial, temporal e previsão.


---

## 🧪 Testes e abordagem de QA

O desenvolvimento do protótipo também envolveu uma etapa contínua de testes e validação das funcionalidades.

As funcionalidades não foram consideradas concluídas apenas porque a interface estava visualmente pronta.

Foram realizados testes dos fluxos, identificação de comportamentos inesperados e ajustes sucessivos.

Esse processo foi importante para identificar problemas que não eram necessariamente perceptíveis apenas pela interface.

A experiência também reforçou uma característica importante do desenvolvimento de produtos digitais, mesmo que "no code".

> Uma primeira versão raramente é a versão final. Testar, identificar problemas, corrigir e testar novamente faz parte do desenvolvimento de qualquer aplicação.

---

## 🎨 Identidade visual

A identidade visual foi desenvolvida especificamente para o projeto.

O nome **Troca Livro SP** foi escolhido para comunicar de forma direta a finalidade da plataforma e sua relação com a cidade.

A identidade utiliza uma abordagem visual minimalista, evitando uma aparência excessivamente infantil apesar do público relacionado ao ambiente escolar.

### Mascote — Matias

O projeto também possui um mascote original chamado **Matias**: um livro amarelo utilizando uma mochila azul.

O nome foi escolhido em referência a Matias Aires, considerado o primeiro filósofo brasileiro. A escolha surgiu de uma associação pessoal.


---

## 🤖 Uso de IA no desenvolvimento

A inteligência artificial foi utilizada como ferramenta de apoio durante o desenvolvimento do protótipo, especialmente na construção e evolução da aplicação por meio de *Vibe Coding*.

Entretanto, a utilização de IA não eliminou a necessidade de planejamento, validação e testes.

A IA foi utilizada como ferramenta de desenvolvimento do protótipo. 


---

## Tecnologias e ferramentas

Foram utilizadas diferentes ferramentas ao longo do desenvolvimento:

- Claude - desenvolviento da aplicação;
- Gemini - desenvolvimento do mascote;
- Power BI — construção de análises e visualizações gerenciais;
- Python (Pandas , geopandas, folium, Statsmodels, Matplotlib)
- Git e GiHub — versionamento e documentação do projeto;



## 🏫 Base de escolas


Foi utilizada uma base aberta de escolas relacionada à Preeitura de São Paulo.

Fonte: https://dados.prefeitura.sp.gov.br/dataset/cadastro-de-escolas-municipais-conveniadas-e-privadas


## Base geográfica

Também foi utilizada uma base aberta geográfica para apoiar a representação territorial dos dados

https://dadosabertos.urbis.prefeitura.sp.gov.br/sl/dataset/subprefeituras/resource/0e38226b-f623-444f-8069-9dd6c8a2a0af


## Considerações finais

O projeto foi desenvolvido como uma proposta de solução e como exercício de aplicação de diferentes competências relacionadas a dados, tecnologia e gestão pública.

Além do protótipo da aplicação, o projeto explora diferentes dimensões dos dados — espacial, temporal, exploratória e preditiva — demonstrando como diferentes ferramentas podem ser utilizadas de forma complementar para compreender um problema e apoiar sua gestão.

Os resultados apresentados devem ser interpretados considerando o caráter demonstrativo do projeto e as limitações dos dados sintéticos utilizados.
