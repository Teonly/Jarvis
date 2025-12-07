# JarvisLite

## Project Overview / Visão Geral (EN / PT)

**EN:**  
JarvisLite is a lightweight personal assistant designed to automate common tasks on a computer. It focuses on modularity, speed and practicality, allowing users to execute actions via voice or text commands. Core capabilities include launching programs, running scripts, local searches, organizing notes and supporting future automations. Visual interface and design elements are open for future definition.

**PT:**  
JarvisLite é um assistente pessoal leve projetado para automatizar tarefas comuns no computador. Foca em modularidade, velocidade e praticidade, permitindo que usuários executem ações por comandos de voz ou texto. Capacidades principais incluem abrir programas, executar scripts, realizar pesquisas locais, organizar notas e suportar automações futuras. Elementos visuais e de design ficam em aberto para definição futura.

---

## Key Features / Recursos Principais (EN / PT)

**EN:**  
- Voice or text command interface for quick actions  
- Program launcher with customizable shortcuts  
- Script executor for automation workflows (local scripts)  
- Local search for files, notes and simple information  
- Modular plugin system for feature extensions  
- Lightweight runtime with minimal dependencies  
- Configurable permissions and safety rules

**PT:**  
- Interface de comandos por voz ou texto para ações rápidas  
- Inicializador de programas com atalhos personalizáveis  
- Executor de scripts para fluxos de automação (scripts locais)  
- Busca local de arquivos, notas e informações simples  
- Sistema modular de plugins para extensões de funcionalidades  
- Tempo de execução leve com dependências mínimas  
- Permissões configuráveis e regras de segurança

---

## AI Command Engine / Motor de Interpretação de Comandos (EN / PT)

**EN:**  
JarvisLite includes a command interpretation layer that maps natural language commands to internal actions. Primary logic uses a local command database (actions, parameters, constraints). External data or web queries are used only as fallback. This design favors predictability, privacy and offline capability.

**PT:**  
O JarvisLite inclui uma camada de interpretação de comandos que mapeia instruções em linguagem natural para ações internas. A lógica principal usa um banco de dados local de comandos (ações, parâmetros, restrições). Dados externos ou consultas à web são usados apenas como fallback. Esse design prioriza previsibilidade, privacidade e funcionamento offline.

---

## Architecture (Planned) / Arquitetura (Planejada) (EN / PT)

**EN:**  
- `core/` — command dispatcher, plugin manager, configuration loader  
- `voice/` — optional voice capture and recognition layer (pluggable engines)  
- `commands/` — local command definitions and handlers (JSON / YAML + handler scripts)  
- `scripts/` — user scripts and script runner with sandboxing rules  
- `storage/` — local database for notes, preferences and command metadata (SQLite or similar)  
- `ui/` — optional UI panel (tray app / web dashboard)  
- `tests/` — unit and integration tests

**PT:**  
- `core/` — despachante de comandos, gerenciador de plugins, carregador de configurações  
- `voice/` — camada opcional de captura e reconhecimento de voz (motores plugáveis)  
- `commands/` — definições locais de comandos e handlers (JSON / YAML + scripts manipuladores)  
- `scripts/` — scripts do usuário e executor de scripts com regras de sandbox  
- `storage/` — banco local para notas, preferências e metadados de comandos (SQLite ou similar)  
- `ui/` — painel de interface opcional (aplicativo na bandeja / dashboard web)  
- `tests/` — testes unitários e de integração

---

## Security & Privacy Considerations / Considerações de Segurança e Privacidade (EN / PT)

**EN:**  
- Keep sensitive data (API keys, tokens, credentials) out of the repo and use `.env` files excluded by `.gitignore`.  
- Provide configurable permission scopes for commands that can change system state.  
- Sandbox execution of user scripts to avoid arbitrary code risks.  
- Prefer local models/engines for voice and command parsing when privacy is required.

**PT:**  
- Mantenha dados sensíveis (chaves API, tokens, credenciais) fora do repositório, usando arquivos `.env` ignorados por `.gitignore`.  
- Forneça escopos de permissão configuráveis para comandos que alterem o estado do sistema.  
- Execute scripts do usuário em sandbox para evitar riscos de execução arbitrária.  
- Prefira modelos/engines locais para voz e parsing quando a privacidade for necessária.

---

## Status / Status Atual (EN / PT)

**EN:**  
Early planning. Core modules and command set are being defined. Implementation will start after initial architecture and roadmap are approved.

**PT:**  
Planejamento inicial. Módulos principais e o conjunto de comandos estão sendo definidos. Implementação começará após aprovação da arquitetura inicial e do roadmap.

---

## Future Plans / Planos Futuros (EN / PT)

**EN:**  
- Define base command taxonomy and parameters  
- Implement core dispatcher and local command DB  
- Add plugin interface and example plugin  
- Implement script sandbox and runner  
- Add optional voice recognition with a pluggable engine  
- Build minimal UI (tray or web dashboard)  
- Create tests and CI pipeline
- Pray for my computer stay working 

**PT:**  
- Definir taxonomia base de comandos e parâmetros  
- Implementar despachante principal e banco local de comandos  
- Adicionar interface de plugins e plugin de exemplo  
- Implementar sandbox e executor de scripts  
- Adicionar reconhecimento de voz opcional com engine plugável  
- Construir UI mínima (bandeja ou dashboard web)  
- Criar testes e pipeline de CI
- Rezar para meu computador continuar fuincionando

---

## License / Licença

This project is licensed under the MIT License.  
Este projeto está licenciado sob a Licença MIT.
