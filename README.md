# Agente de IA sobre o Impacto da IA na Educação 🤖📚

Um agente inteligente construído com **LangGraph** e **LangChain** que responde perguntas sobre o impacto da Inteligência Artificial na educação. Ele é capaz de raciocinar, decidir quando buscar informações atualizadas na web, e responder através de uma interface interativa criada com **Gradio**.

Este projeto foi desenvolvido durante o programa **Oracle Next Education (ONE)**, em parceria entre a **Oracle** e a **Alura** ([cursos.alura.com.br](https://cursos.alura.com.br)), como parte da trilha de **IA Tech**. Todo o desenvolvimento e os testes foram feitos no **Google Colab**.

---

## 🎯 O que o agente faz

Você pergunta qualquer coisa sobre o impacto da IA na educação — métodos de ensino, resultados de aprendizagem, questões éticas, tendências de adoção — e ele:

1. Raciocina se já sabe a resposta ou se precisa pesquisar
2. Usa ferramentas (como busca na web) quando precisa de informação atualizada
3. Roteia a tarefa para o nó/agente correto dentro do grafo
4. Retorna uma resposta clara e fundamentada

---

## 🛠️ Tecnologias utilizadas

- **LangChain** – criação de cadeias (chains) de processamento com LLM
- **LangGraph** – orquestração do agente em forma de grafo de estados
- **Google Gemini** – modelo de linguagem responsável pelo raciocínio
- **Gradio** – interface web para interagir com o agente
- **Padrão ReAct** – ciclo de raciocínio + ação para uso de ferramentas
- **Google Colab** – plataforma usada para desenvolver e rodar o projeto

---

## 🧠 Como funciona (arquitetura)

O agente não é um único prompt — ele é um **grafo** de etapas:

1. **Nó de entrada** – recebe a pergunta do usuário
2. **Nó roteador / supervisor** – decide qual caminho seguir (responder direto ou acionar uma ferramenta)
3. **Nó de ferramenta** – executa ações como busca na web quando a pergunta exige dados atuais
4. **Nó de resposta** – formata e retorna a resposta final

Essa estrutura multiagente (roteador + supervisor) permite que partes diferentes do sistema cuidem de responsabilidades diferentes, em vez de um único prompt tentando fazer tudo.

---

## 📚 O que aprendi construindo esse projeto

Esse projeto foi meu primeiro contato real com orquestração de agentes, feito durante a trilha de IA Tech (Oracle Next Education + Alura). Principais aprendizados:

- **Cadeias com LangChain** – como estruturar etapas de processamento com LLM, em vez de um prompt único
- **LLMs equipadas com ferramentas** – dar ao modelo acesso a ferramentas reais (como busca) para executar tarefas práticas, não só gerar texto
- **Fluxos ReAct** – implementar ciclos de raciocínio + ação para o agente decidir *quando* e *como* agir
- **Orquestração multiagente** – usar roteadores e supervisores para coordenar múltiplos agentes/tarefas, em vez de um fluxo único e monolítico
- **Publicação com Gradio** – transformar um script de back-end em algo que as pessoas realmente conseguem usar pelo navegador
- **Manipulação de bibliotecas prontas** – ganhar autonomia para usar ferramentas e pacotes já existentes, em vez de construir tudo do zero
- **Pensar o design do agente de forma diferente** – ir além de "o que ele responde" e considerar também:
  - *Como* ele responde
  - *Onde* ele busca a informação
  - *Como* ele busca (qual ferramenta, qual consulta)
  - **Consciência de custo** — pensar em como reduzir chamadas de ferramentas e uso de tokens desnecessários, não só fazer o agente funcionar

---

## 🎬 Demonstração

Abaixo, um clipe curto mostrando o agente recebendo uma pergunta e retornando a resposta em tempo real:

<!-- Opção 1: GIF (recomendado, funciona direto no README)
![<img width="692" height="388" alt="executandooagente" src="https://github.com/user-attachments/assets/aa484f6b-fe38-4b3a-a87f-92b8ef3d1393" />
](./assets/demo.gif)
-->



### 📸 Imagens do projeto

<img src="./assets/interface.png" alt="Interface do agente no Gradio" width="700"/>

<img src="./assets/grafo.png" alt="Grafo do LangGraph mostrando os nós do agente" width="700"/>

<img src="./assets/resposta.png" alt="Exemplo de resposta do agente" width="700"/>

---

## 👩‍💻 Sobre

Projeto desenvolvido por [Carla](https://github.com/srtsayonara) durante a trilha de IA Tech do programa **Oracle Next Education (ONE)**, em parceria com a **Alura**.
