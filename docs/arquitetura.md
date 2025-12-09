# Arquitetura do Jarvis

## Visão Geral

A arquitetura do Jarvis Lite é projetada para ser modular, expansível e flexível. Cada parte do sistema funciona como um bloco independente, permitindo que novas funcionalidades sejam adicionadas sem comprometer o restante da aplicação.

Este documento descreve todos os módulos planejados, o fluxo de dados e como as camadas internas interagem.

---

## Componentes Principais

### 1. **Input Layer (Entrada)**

Responsável por capturar qualquer forma de entrada do usuário:

* Comandos de voz
* Texto digitado
* Atalhos

Submódulos:

* Speech-to-Text (opcional)
* Parser inicial de texto

---

### 2. **NLU Layer (Interpretação de Intenção)**

Camada que interpreta o comando do usuário e identifica intenção e parâmetros.

Funções:

* Detectar intenção (abrir programa, pesquisar, executar script)
* Extrair entidades (nome do programa, termo de busca, etc.)
* Normalizar texto

Pode futuramente usar modelos maiores ou motores alternativos.

---

### 3. **AI Engine (Planejado)**

Motor responsável por:

* Analisar a intenção
* Gerar respostas
* Conversar de forma natural
* Ajudar na tomada de decisões

O plano inicial é usar **ChatGPT 5 Mini**, mas ainda existem considerações e alternativas que serão avaliadas futuramente.

---

### 4. **Action Manager (Gerenciador de Ações)**

Recebe a intenção já interpretada e executa a ação correta.

Responsável por:

* Abrir softwares
* Criar arquivos
* Enviar notificações
* Executar scripts
* Controlar automações

Possui ponte com:

* Sistema operacional
* API internas
* Scripts locais

---

### 5. **Modules Layer (Módulos Funcionais)**

Cada funcionalidade do Jarvis é tratada como um módulo independente.
Exemplos:

* Módulo de Automação do PC
* Módulo de Pesquisa Rápida
* Módulo de Organização de Projetos
* Módulo de Scripts
* Módulo de Contexto

Cada módulo responde a ações específicas.

---

### 6. **Data & Storage Layer**

Camada responsável por guardar:

* Configurações do usuário
* Histórico de comandos
* Preferências
* Logs

Formato planejado:

* JSON local
* SQLite (possível no futuro)

---

### 7. **Output Layer (Saída)**

Camada que devolve a resposta ao usuário.


Principalmente pela síntese de voz, assim como no filme, só será  mostrado texto ou imagem (se nescessario) para complementar o áudio.

---

## Fluxo Geral do Sistema

1. Usuário envia um comando (voz ou texto)
2. Input Layer captura o comando
3. NLU interpreta intenção
4. AI Engine analisa e complementa o comando (se necessário)
5. Action Manager escolhe o módulo ideal
6. O módulo executa a ação
7. Output Layer retorna o resultado

---

## Escalabilidade

A arquitetura permite:

* Adicionar novos módulos sem quebrar o sistema
* Trocar o motor de IA futuramente
* Integrar com APIs de terceiros
* Migrar para interface gráfica

---

## Estado Atual

A arquitetura está definida em nível conceitual. Implementações finais serão ajustadas conforme as decisões sobre o motor de IA e a estrutura final de módulos.
