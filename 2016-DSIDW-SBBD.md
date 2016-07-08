### Estruturação:

---

#### Motivação:

Ambientes de pesquisa comumente apresentam:

  + Experimentação com diferentes recursos e configurações (e.g., ferramentas, dados, ambientes, etc.)
  + Disputa por utilização de recursos de hardware (processamento e memória)
  + Execução paralela de experimentos de pessoas diferentes em mesmo servidor
  + Reuso ou extensão de trabalhos de colegas
  + Compartilhamento de recursos com colaboradores distantes geograficamente

#### Proposta:

Uso de containers Docker para conduzir atividades individuais ou em grupo em ambientes de pesquisa

Motivos para se usar a estratégia:

- Isolamento de instalações e recursos em containers:
  + Garante a execução dos experimentos dentro dos limites de recursos (disco, memória e cpu) definidos na inicialização do container
  + Facilita a experimentação de múltiplos ambientes/recursos
- Facilidade de migração da execução de um computador pessoal para um servidor
- Flexibilidade de mudança de configuração de recursos de hardware dos computadores
- Versionamento e controle apurado das configurações do ambiente
- Reutilização de uma configuração de containers por múltiplos usuários:
  + Os desafios de configuração do ambiente se concentram na fase de criação da imagem usada para instanciar containers;
  + Facilita reprodução de experimentos;
  + Gestão eficiente de recursos;
- Redução de recursos para armazenamento e transferência de configurações de ambiente
  + Possibilita escolha de diversas estratégias de armazenamento conforme as características do experimento


Estudo de Caso:
  - Cassandra
  - Spark
  - Jupyter
  - Python
  - R

### Texto
---

**Introdução I**
Vivemos em um mundo altamente conectado, o número de pessoas e agora até dispositivos conectados e gerando dados está na casa do bilhões o volume de dados e imenso demandando o desenvolvimento de novas tecnologias que possibilitem análise e exploração desses dados. Porém a corrida no desenvolvimento dessas tecnologias culminou na gama ferramentas, técnicas,  modelos arquiteturais que prometem agilizar e ou viabilizar o trabalho de análise inclusive perto de  tempo real para alguns casos. Considerando este cenário uma linha de ferramentas flexíveis e configuráveis tornam-se obrigatórias o Docker se apresenta como uma plataforma viável para a criação de ambientes heterogéneos de pesquisa possibilitando a execução virtualmente de qualquer tipo de experimentação seja de exploração de dados, comparações, processamento, etc. E tudo isso aproveitando um mesmo conjunto de hardware. Este trabalho tem por objetivo apresentar um estudo de caso utilizando diversas dessas tecnologias sendo executadas em um ambiente dockerizado demonstrando a otimização e compartilhamento de recursos, execução de diferentes experimentos, usando python e r como linguagens de programação , spark como plataforma de processamento distribuído e execução de técnicas analíticas, cassandra como banco de dados ze persistência dos dados para análise e visualização e Júpiter como interface de programação para os pesquisadores realozarem o trabalho. O ambiente construído. .....

**Introdução II**
Ambientes de desenvolvimento, pesquisa e inovação têm como atividade inerente a criação e experimentação. Projetos de grande porte podem ter início na concepção de provas de conceito ou demonstrações em pequena escala. Estas passam a ganhar maior complexidade ou demanda à medida em que expectativas e ideias são postas à prova e o projeto se desenvolve. Nesse trajeto de desenvolvimento, há diversas situações e necessidades que desafiam a capacidade do time em conseguir realizar a transição do projeto entre diferentes escalas, manter a organização do artefatos produzidos e permitir o melhor aproveitamento dos recursos disponíveis. 


---

A exemplo disso, pode-se citar desafios comumente encontrados no ambiente acadêmico:

 - Experimentação com diferentes recursos e configurações (e.g., ferramentas, dados e ambientes);
 - Disputa por utilização de recursos de hardware (e.g., processamento e memória primária ou de massa);
 - Execução paralela de experimentos de pessoas diferentes em mesmo servidor;
 - Reuso ou extensão de trabalhos de colegas;
 - Compartilhamento de recursos com colaboradores distantes geograficamente.


Este trabalho tem como objetivo apresentar um conjunto de boas práticas e recomendações obtidas na condução de projetos de pesquisa e desenvolvimento envolvendo times com diferentes competências e distribuídos geograficamente. Como elemento central dessas práticas, será apresentado o uso de containers. 


Containers são... **COLOCAR EXPLICAÇÃO E DETALHES SOBRE CONTAINERS/DOCKER**

Dentre os motivos para se utilizar a organização de projetos e experimentações com containers podem ser citados:

- Isolamento de instalações e recursos em containers:
  + Garante a execução dos experimentos dentro dos limites de recursos (disco, memória e cpu) definidos na inicialização do container;
  + Facilita a experimentação de múltiplos ambientes/recursos;
- Facilidade de migração da execução de um computador pessoal para um servidor
- Flexibilidade de mudança de configuração de recursos de hardware dos computadores
- Versionamento e controle apurado das configurações do ambiente
- Reutilização de uma configuração de containers por múltiplos usuários:
  + Os desafios de configuração do ambiente se concentram na fase de criação da imagem usada para instanciar containers;
  + Facilita reprodução de experimentos;
  + Gestão eficiente de recursos;
- Redução de recursos para armazenamento e transferência de configurações de ambiente
  + Possibilita escolha de diversas estratégias de armazenamento conforme as características do experimento

A fim de exemplificar o uso da abordagem proposta, este trabalho apresenta as recomendações que auxiliam a amenizar os problemas motivadores supracitados e que fazem parte de ambientes de pesquisa, desenvolvimento e inovação. O ambiente envolve o uso de diferentes linguagens para análise e processamento de dados (Python e R), ferramenta para reprodutibilidade (Jupyter) e processamento e armazenamento escaláveis (Spark e Cassandra).
