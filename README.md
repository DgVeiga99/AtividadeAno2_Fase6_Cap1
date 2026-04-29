# AtividadeAno2_Fase6_Cap1


## 📌 Sobre o Projeto

Este projeto implementa um sistema de Inteligência Artificial baseado em arquitetura multiagente, no qual diferentes agentes colaboram entre si para resolver uma tarefa de análise e geração de recomendações.

A proposta central é demonstrar, na prática, a transição de modelos monolíticos para sistemas distribuídos inteligentes, onde a inteligência emerge da interação entre agentes especializados. Esse tipo de abordagem permite maior modularidade, escalabilidade e eficiência na resolução de problemas complexos, especialmente em cenários que envolvem múltiplas etapas de processamento.

---

## 🎯 Objetivo Principal

O objetivo principal do projeto é desenvolver um sistema capaz de:

Processar dados de entrada utilizando múltiplos agentes especializados
Demonstrar a colaboração entre agentes de IA
Aplicar conceitos de:
- Decomposição de problemas
- Pipeline de processamento inteligente
- Tomada de decisão baseada em IA
- Validar na prática a arquitetura de sistemas multiagentes

Além disso, o projeto busca servir como base para aplicações mais complexas envolvendo automação inteligente e sistemas distribuídos.

---

## 🏗️ Arquitetura do Software

O sistema foi desenvolvido com base em uma arquitetura multiagente, onde cada agente possui uma responsabilidade bem definida dentro do fluxo de processamento. A interação entre esses agentes permite a construção de uma solução mais robusta, modular e escalável.

### 1. Agente Osquestrador

O Agente Orquestrador é o componente central do sistema, responsável por coordenar toda a execução do fluxo multiagente.

Sua principal função é:

- Receber a entrada do usuário
- Determinar a sequência de execução dos agentes
- Gerenciar o fluxo de informações entre os agentes (handoff)
- Garantir que cada etapa do processamento ocorra de forma organizada

Esse agente atua como um controlador de pipeline, decidindo qual agente deve ser acionado em cada momento, além de consolidar as respostas intermediárias para gerar a saída final.

Do ponto de vista arquitetural, ele representa a camada de coordenação e controle, essencial para evitar acoplamento direto entre os agentes e manter a escalabilidade do sistema.

### 2. Agente Analista de Risco

O Agente Analista de Risco é responsável por interpretar os dados recebidos e realizar uma análise crítica, identificando possíveis riscos, falhas ou pontos de atenção.

Suas principais responsabilidades incluem:

- Analisar dados textuais ou estruturados
- Identificar padrões de risco
- Avaliar impacto potencial de problemas
- Gerar diagnósticos iniciais

Além disso, esse agente pode utilizar ferramentas auxiliares (tools) para enriquecer sua análise, como:

- Processamento de dados
- Regras de negócio
- Funções de cálculo ou validação
- Integração com bases externas (quando aplicável)

O uso de ferramentas permite que o agente vá além de uma análise puramente baseada em linguagem natural, incorporando lógica computacional e tornando suas decisões mais precisas e confiáveis.

### 3. Agente Especialista de Protocolo

O Agente Especialista de Protocolos é responsável por transformar a análise de risco em ações práticas e estruturadas, seguindo diretrizes, normas ou boas práticas previamente definidas.

Suas funções incluem:

- Interpretar os riscos identificados pelo agente anterior
- Aplicar protocolos de resposta adequados
- Sugerir ações corretivas ou preventivas
- Gerar recomendações técnicas estruturadas

Assim como o agente de risco, ele também pode utilizar ferramentas (tools) para:

- Aplicar regras específicas
- Consultar protocolos definidos
- Padronizar respostas
- Simular cenários de ação

Esse agente atua como uma camada de especialização, responsável por garantir que as decisões finais estejam alinhadas com práticas técnicas e operacionais adequadas.

---

## 📊 Resultados

A implementação do sistema multiagente apresentou resultados consistentes na organização e análise das informações, evidenciando a eficiência da divisão de responsabilidades entre os agentes. O Agente Orquestrador garantiu o correto fluxo de execução, coordenando a interação entre os agentes de forma sequencial e estruturada.

O Agente Analista de Risco demonstrou capacidade adequada na interpretação dos dados de entrada, identificando padrões e possíveis problemas de forma coerente. Já o Agente Especialista de Protocolos foi responsável por transformar essa análise em recomendações práticas, gerando respostas mais objetivas e aplicáveis.

De forma geral, o sistema foi capaz de processar entradas textuais e produzir saídas contextualizadas, simulando um fluxo de tomada de decisão automatizado. A arquitetura multiagente se mostrou eficaz ao melhorar a organização do processamento e a qualidade das respostas quando comparada a uma abordagem centralizada.

Como limitações, destacam-se a dependência de modelos de linguagem, possíveis variações nas respostas e a ausência de memória persistente. Ainda assim, os resultados validam a proposta do projeto e indicam potencial para evoluções futuras, como integração com bases de dados e expansão do número de agentes.

---

## ⚙️ Tecnologias Utilizadas (Bibliotecas)

A aplicação foi desenvolvido em Python, utilizando bibliotecas específicas para integração com serviços de IA.

- **os** → manipulação de variáveis de ambiente  
- **pandas** → tratamento e análise de dados  
- **numpy** → operações numéricas  
- **matplotlib** → geração de gráficos  
- **seaborn** → visualização estatística  
- **scikit-learn** → criação e avaliação do modelo de machine learning  
- **joblib** → salvamento e carregamento do modelo  
- **pydantic** → validação de dados de entrada  
- **agents (OpenAI SDK)** → implementação do sistema multiagente  
- **google.colab** → execução do projeto em ambiente notebook  

---

## ▶️ Como Executar

O projeto foi desenvolvido e executado utilizando o **Google Colab**, não sendo necessário configurar um ambiente local.

Para executar o sistema, siga os passos abaixo:

1. Acesse o Google Colab:  
   https://colab.research.google.com/

2. Faça o upload do notebook do projeto (`.ipynb`) ou abra diretamente pelo repositório.

3. Execute as células na ordem definida, garantindo que todas as bibliotecas sejam carregadas corretamente.

4. Caso necessário, instale dependências adicionais diretamente no Colab com:

5. Configure eventuais variáveis de ambiente ou credenciais (como API Keys) utilizando o próprio ambiente do Colab.

6. Após a execução completa, o sistema estará pronto para uso, processando as entradas diretamente nas células do notebook e exibindo os resultados no próprio ambiente.

Todo o fluxo de execução, incluindo o processamento de dados, treinamento do modelo e interação entre os agentes, ocorre dentro do notebook de forma sequencial e interativa.

---

## 🎥 Demonstração do Projeto

Para uma visualização completa do funcionamento do sistema, acesse o vídeo demonstrativo no link abaixo:

👉 [Assista ao vídeo do projeto](https://youtu.be/hjQX7jjAl3I)

O vídeo apresenta a execução prática do sistema, mostrando como os dados são processados e como os agentes interagem para gerar resultados de forma estruturada e automatizada.

---

## ⚠️ Aviso Importante

Este projeto possui finalidade **exclusivamente educacional** e **não deve ser utilizado para diagnóstico clínico**.  
Os resultados simulam um ambiente de pesquisa e não substituem avaliação profissional em saúde.
