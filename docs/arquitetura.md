# Arquitetura do Sistema — JarvisLite

A arquitetura do **JarvisLite** foi planejada para ser modular, expansível e simples de manter. Cada parte do sistema é separada em responsabilidades claras, permitindo que novas funções sejam adicionadas sem alterar o núcleo principal.

---

## Visão Geral

O sistema é dividido em quatro grandes componentes:

1. **Núcleo (Core)** — Coordena tudo.
2. **Módulos** — Funções independentes adicionadas como plugins.
3. **IA (mente do sistema)** — Ainda não definida, mas responsável por interpretação e auxílio.
4. **Interface** — Voz, texto e possíveis UIs futuras.

---

## 1. Núcleo (Core)

O núcleo é o responsável por:

* Carregar e gerenciar todos os módulos.
* Receber comandos (voz, texto ou eventos).
* Interpretar e encaminhar esses comandos para o módulo correto.
* Manter logs, permissões e comunicações internas.

### Funções esperadas

* Inicialização dos módulos.
* Monitoramento de erros.
* Roteamento de comandos.
* Controle da IA.

---

## 2. Módulos do Sistema

Cada módulo é independente e deve seguir uma estrutura clara.

### Estrutura sugerida de um módulo

```
/modules
  ├── nome_do_modulo/
  │     ├── __init__.py
  │     ├── main.py
  │     ├── config.json
  │     └── README.md
```

### Tipos de módulos

* **Automação** — abrir programas, manipular arquivos, organizar pastas.
* **Informação** — clima, pesquisas, utilidades.
* **Produtividade** — lembretes, timers, tarefas.
* **IA/Análise** — comandos complexos, interpretação.

Cada módulo comunica-se apenas com o núcleo, nunca diretamente com outros módulos.

---

## 3. Mecanismo de IA

A IA usada no JarvisLite ainda não foi escolhida. As opções incluem:

* Modelo local (ex.: LLaMA, Gemma, Phi).
* API externa (ex.: GPT-5 Mini).
* Solução híbrida.

### Funções da IA

* Interpretar comandos complexos.
* Auxiliar na escolha do módulo certo.
* Responder perguntas gerais.
* Ajudar a depurar erros e sugerir ações.

A IA será acessada através de uma camada intermediária, nunca diretamente pelos módulos.

---

## 4. Reconhecimento de Voz

Também está em definição, mas os candidatos incluem:

* Whisper (OpenAI)
* Vosk
* SpeechRecognition API

### Funções esperadas

* Converter áudio para texto.
* Enviar o texto para o Núcleo.
* Reagir a ativadores (wake words).

---

## 5. Interface do Usuário

O JarvisLite começa com interface textual e comandos de voz, mas poderá evoluir para:

* Painel web.
* Aplicativo desktop.
* Aplicativo mobile.

---

## 6. Fluxo Básico

1. Usuário fala ou digita um comando.
2. Reconhecimento de voz converte (se necessário).
3. Núcleo recebe o comando.
4. IA interpreta (se for um comando complexo).
5. Núcleo encaminha para o módulo correto.
6. Módulo executa a ação.
7. Núcleo retorna a resposta.

---

## 7. Filosofia da Arquitetura

* **Modularidade máxima.**
* **Independência entre módulos.**
* **Facilidade de adicionar novas funções.**
* **Flexibilidade na escolha da IA.**
* **Código limpo e documentado.**

---

Este documento será expandido conforme o desenvolvimento avançar.
