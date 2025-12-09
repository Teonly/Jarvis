# API e Integrações de IA

Este documento descreve como o Jarvis se conecta a serviços externos, especialmente provedores de IA, para realizar processamento de linguagem, interpretação de comandos e automações inteligentes.

## Objetivo da API

A API do Jarvis serve como ponte entre:
- o módulo principal do assistente,
- serviços de inteligência artificial,
- APIs de automação do sistema operacional,
- integrações externas (música, navegador, mensagens, utilidades, etc.).

Ela centraliza chamadas, autenticação, segurança e logs de uso, garantindo flexibilidade para troca posterior de provedores.

---

## Plano Atual de IA

Atualmente, o **plano inicial** é utilizar o **ChatGPT 5 Mini**, graças a:

- excelente custo-benefício,  
- boa velocidade,  
- qualidade de raciocínio e instrução,  
- baixa latência e consumo de tokens,  
- facilidade de implementação com API OpenAI.

No entanto, **esta ainda não é a decisão final**.  
Outras opções de IA — como Gemini Flash, modelos locais via Ollama, ou modelos mais avançados (ex.: ChatGPT 5.1) — **ainda estão sendo avaliadas** para uso futuro conforme as necessidades do projeto crescerem.

A arquitetura do Jarvis é planejada para suportar troca rápida de modelo, sem grandes mudanças no código.

---

## Estrutura de Integração

A API seguirá uma estrutura flexível:

- **/ai/query** – envia prompts para o modelo selecionado  
- **/ai/interpret** – interpreta comandos do usuário  
- **/ai/context** – gerencia contexto e memória  
- **/system/** – controle de automações no PC  
- **/services/** – integrações externas (clima, música, web, etc.)

Isso garante que o Jarvis possa expandir-se com novos módulos ou provedores sem reescrever a base existente.

---

## Chaves e Segurança

- As chaves de API nunca serão incluídas no código público.  
- Variáveis de ambiente (`.env`) serão utilizadas.  
- A API poderá aplicar limites de segurança para evitar uso indevido.

---

## Possíveis Provedores Futuros

Embora o **ChatGPT 5 Mini** seja o candidato inicial, outros motores permanecem em consideração:

- **Gemini Flash / Gemini 2.0**  
- **DeepSeek API** 
- **Modelos locais via Ollama** (para modo offline)  
- **ChatGPT 5.1** 

Essas alternativas poderão ser adotadas dependendo de desempenho, custo e requisitos de privacidade.

---

## Status Atual

A integração ainda está **em rascunho**.  
Nenhuma API está conectada oficialmente — apenas a arquitetura inicial está definida.

Atualizações futuras deste documento incluirão:
- estrutura de requests e responses,  
- exemplos de chamadas,  
- fluxos de autenticação,  
- padrões de fallback entre modelos.

---

