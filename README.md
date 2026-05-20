# EcoDex: Desvendando os ecossistemas brasileiros com lógica de dados

## Apresentação

 Uma atividade de computação desplugada com uso de cartas para introduzir conceitos de bancos de dados relacionais por meio da biodiversidade dos biomas brasileiros. 

### Disciplinas e conteúdos relacionados 

* **Biologia:** cadeias e teias alimentares, hábitos alimentares, e interações entre seres vivos e fatores abióticos; conservação de espécies e impactos das atividades antrópicas na perda de habitats; adaptações morfológicas e fisiológicas da flora e da fauna aos diferentes ecossistemas.

* **Geografia:** características físicas das grandes paisagens naturais brasileiras (Amazônia, Cerrado, Caatinga, Mata Atlântica, Pampa); localização, distribuição espacial, fronteiras e regionalização do território brasileiro; turismo sustentável, ecoturismo e a interação socioespacial com o patrimônio histórico-cultural e arqueológico brasileiro.

* **Computação:** banco de dados relacionais, tabelas (entidades), atributos (campos), chaves primárias e estrangeiras, filtros de seleção textual e numérica (`WHERE`), operadores lógicos (`AND`, `OR`, `NOT`), funções de agregação (`COUNT`), agrupamento de dados (`GROUP BY`), e junção de dados/tabelas baseada em correspondência de strings (JOIN).

### Habilidades

* **Ciências da Natureza e suas Tecnologias (EM13CNT301):** Construir questões, elaborar hipóteses, previsões e estimativas, empregar instrumentos de medição e representar e interpretar modelos explicativos, dados e/ou resultados experimentais para construir, avaliar e justificar conclusões no enfrentamento de situações-problema sob uma perspectiva científica.

* **Ciências Humanas e Sociais Aplicadas (EM13CHS204):** Comparar e avaliar os processos de ocupação do espaço e a formação de territórios, territorialidades e fronteiras, identificando o papel de diferentes agentes (como grupos sociais e culturais, impérios, Estados Nacionais e organismos internacionais) e considerando os conflitos populacionais (internos e externos), a diversidade étnico-cultural e as características socioeconômicas, políticas e tecnológicas.

* **Computação (EM13CO12):** Produzir, analisar, gerir e compartilhar informações a partir de dados, utilizando princípios de ciência de dados.

* **Computação (EM13CO13):** Analisar e utilizar as diferentes formas de representação e consulta a dados em formato digital para pesquisas científicas.

### Nível de ensino

Ensino Médio e Educação profissional ou tecnológica.

### Materiais Necessários

Cada grupo de alunos precisará de:
* **1 Baralho EcoDex** impresso e recortado (composto por 80 cartas divididas em 4 categorias de cores):
  
    * 🟩 **Cartas Verdes:** Plantas (Flora)
  
    * 🟥 **Cartas Vermelhas:** Animais (Fauna)
  
    * 🟦 **Cartas Azuis:** Lugares (Paisagens naturais)

    * 🟨 **Cartas Amarelas:** Biomas Brasileiros

O professor precisará de:

* **1 Listagem de desafios:** que pode ser impressa ou digital, cada pergunta/desfio pode ser feita oralmente, escrita em quadro ou projetada digitalmente.

* **1 Cronômetro**: que pode ser o do celular do professor.


> *Os arquivos do baralho EcoDex (prontos para impressão) e o arquivo aberto (CSV) para personalização das cartas estão disponíveis na pasta `/src` e `/data` deste repositório.*


## EcoDex

### Passo 1: O Caos Construtivo (Rodada 1)
O professor entrega o baralho completo embaralhado para cada equipe. Sem dar explicações prévias sobre bancos de dados, o professor lança os desafios da **Rodada 1** um por um. 
* *Exemplo de Comando:* "Separem todas as cartas de animais que sejam Carnívoros. Valendo!"
* Os alunos precisarão vasculhar o baralho inteiro para achar as cartas. O tempo de resposta será alto e a mesa ficará desorganizada.

### Passo 2: A Parada Pedagógica (A Ponte com a TI)
Terminada a primeira rodada, o professor interrompe o jogo e abre um debate no quadro, correlacionando o comportamento físico dos alunos com a arquitetura de um computador:
* **As Cores das Cartas = Tabelas:** Explicar que separar por cores agiliza a busca porque cria entidades distintas.
* **Os Critérios das Perguntas = Sintaxe SQL:** Mostrar que quando o professor diz *"Plantas do tipo Cacto OU Animais da classe Ave"*, a mente deles executa um filtro `WHERE tipo = 'Cacto' OR classe = 'Ave'`.
* **Técnicas de Otimização:** O professor incentiva os alunos a criarem maneiras de organizar as cartas na mesa para bater os tempos de busca do relógio (Simulando uma **Indexação de Banco de Dados**).

### Passo 3: O Jogo como um Sistema Otimizado (Rodada 2)
O professor aplica a **Rodada 2**, que possui perguntas mais complexas e profundas. Agora, os alunos jogam de forma consciente: deixam as cartas separadas por pilhas e utilizam varreduras de texto por "Chaves Comuns" (como o estado/UF) para cruzar dados. Eles não jogam mais por instinto, jogam agindo como o próprio motor de um banco de dados relacional.

---

## Roteiro de Desafios (Queries da Natureza)

### Rodada 1:
1.  **Filtro Simples (Tabela Fauna):** "Separem todas as cartas de animais que sejam Carnívoros. Valendo!"
2.  **Filtro Simples (Tabela Flora):** "Separem todas as cartas de Plantas cujo uso principal seja Ornamental. Valendo!"
3.  **Filtro Simples (Tabela Lugares):** "Separem todos os Lugares que possuem foco no turismo de Aventura. Valendo!"
4.  **Filtro Simples com Atributo de Risco:** "Encontrem e separem todos os Animais que estão com o nível de ameaça classificado como Vulnerável. Valendo!"
5.  **Uso do Operador Lógico OR:** "Quero que vocês separem duas coisas ao mesmo tempo: todas as Plantas do tipo Cacto OU todos os Animais da classe Ave. Valendo!"
6.  **Filtro Global Dinâmico por Parâmetro:** "Separem todas as Plantas, todos os Animais E todos os Lugares que tenham ligação direta com o estado que vocês moram. Valendo!"
7.  **Operador de Exclusão (AND NOT):** "Encontrem todos os Animais que tenham a palavra Seguro no nível de ameaça, mas que NÃO estejam no ‘RS’ na sua localização. Valendo!"
8.  **Filtro Composto (AND):** "Separem todas as Plantas usadas para fins Medicinais e que sejam do tipo Árvore. Valendo!"
9.  **Introdução ao GROUP BY e COUNT:** "Descubram qual é o Tipo de Turismo que aparece mais vezes no baralho azul. Separem todas as cartas que pertencem a esse tipo campeão. Valendo!"
10. **Filtro Numérico por Valor:** "Quais Biomas brasileiros possuem uma Área Territorial maior do que 1 milhão de km²? Valendo!"
11. **Função de Agregação Avançada:** "Quantos hábitos alimentares existem e quantos animais possuem esses mesmos hábitos alimentares? Valendo!"
12. **O Primeiro INNER JOIN Humano:** "Achem a carta do lugar Jalapão. Descubram sua UF. Agora, separem todas as Plantas e Animais que ocorrem nessa UF, mas atenção: só valem as cartas que forem consideradas Seguras ou de uso Alimentício. Valendo!"

### Rodada 2:
*(A ser aplicada após a explicação do professor, exigindo técnicas explícitas de indexação e consultas estruturadas)*

13. **Uso de Índice de Atributo:** "Aplicando o índice vermelho: separem todos os Animais que possuem o hábito alimentar Onívoro. Valendo!"
14. **Uso de Conectivos Complexos:** "Quero que vocês usem a lógica do `OU`: separem todas as cartas que sejam Biomas com clima Tropical `OU` que sejam Plantas que preferem o clima Subtropical. Valendo!"
15. **Agrupamento Físico (Group By Manual):** "Olhando para as cartas de Plantas, criem sub-montes por Tipo. Descubram qual tipo tem mais cartas e me entreguem essa pilha campeã! Valendo!"
16. **Subconsulta Avançada (Subquery Humana):** "Descubram qual é o Clima do bioma Mata Atlântica na carta amarela. Usem esse resultado para ir até o índice verde e separar todas as Plantas que preferem esse mesmo clima! Valendo!"

> 🔑 *O gabarito completo com as cartas-resposta de cada desafio e os códigos SQL equivalentes para rodar no computador estão disponíveis no arquivo `docs/gabarito_professor.md`.*

---

## 🌍 Relação com o cotidiano

No fechamento da atividade, consolide com a turma que a dinâmica que eles fizeram na mesa é exatamente o que acontece quando usamos a tecnologia no cotidiano:
* **Instagram / TikTok:** Quando você clica em uma hashtag, o servidor faz uma busca parecida com a da *Rodada 1 (Filtro Simples)*.
* **E-Commerce (Mercado Livre/Amazon):** Quando você pesquisa por *"Tênis de Corrida"* e filtra por *"Tamanho 41"* e *"Frete Grátis"*, o banco de dados deles usa a lógica exata do filtro composto da *Rodada 2 (Filtros Combinados)*.
* **Big Data e Sistemas Governamentais:** O cruzamento espacial feito pelas UFs para mapear riscos ambientais simula as consultas automatizadas usadas por cientistas de dados na preservação ambiental.

---

## Como Replicar ou Modificar este Projeto

Se você é desenvolvedor ou professor e deseja adicionar novas cartas ou perguntas:

1.  Clone o repositório:
    ```bash
    git clone [https://github.com/seu-usuario/ecodex-desplugado.git](https://github.com/seu-usuario/ecodex-desplugado.git)
    ```
2.  Para alterar os dados das cartas, modifique a tabela bruta em `data/dataset_original.csv`.
3.  O código em HTML/CSS lerá o arquivo editado para renderizar o novo visual das cartas automaticamente prontas para impressão.

---

## Licença

Este projeto está sob a licença **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)**. Você pode compartilhar, adaptar e usar para fins educativos não comerciais, desde que atribua os créditos e compartilhe sob a mesma licença.