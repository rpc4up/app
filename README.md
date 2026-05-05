# **O Paradigma RPC como Camada de Execução em Protocolos Unificados para IA Agêntica: Uma Nova Ontologia para Sistemas Distribuídos em 2026**

A evolução histórica da computação distribuída atingiu um ponto de maturação em 2026, onde a tradicional Chamada de Procedimento Remoto (Remote Procedure Call \- RPC) deixou de ser interpretada como um simples mecanismo de transporte de mensagens para se consolidar como a camada de execução fundamental de protocolos unificados voltados à inteligência artificial agêntica. No contexto contemporâneo, a RPC não é apenas uma abstração para a invocação de funções em endereços de memória remotos; ela constitui o tecido operacional que permite a coordenação semântica entre ferramentas, serviços corporativos e agentes autônomos heterogêneos.1 Esta tese de livre-docência propõe que a eficácia de um Protocolo Unificado (Unified Protocol \- UP) para IA agêntica depende da redefinição da RPC como o mecanismo padronizador de chamadas de capacidade, integrando requisitos centrais de governança, observabilidade distribuída, segurança de confiança zero (Zero Trust) e fluxos de execução contínua via streaming.3  
A transição para essa nova arquitetura protocolar em 2026 é impulsionada pela necessidade de mitigar o caos das integrações sob medida (*bespoke integrations*), que historicamente afligiram o desenvolvimento de aplicações de IA.1 Onde antes havia uma proliferação de conectores específicos para cada fornecedor de modelo de linguagem (LLM) e cada ferramenta externa, hoje emerge uma camada de mediação que utiliza a RPC para expor capacidades de forma agnóstica ao modelo, permitindo que a inteligência artificial descubra, selecione e invoque recursos em tempo de execução com base em descrições semânticas.2

## **Fundamentos Teóricos e a Evolução do Paradigma RPC**

O conceito de RPC foi formalizado em 1984 por Andrew Birrell e Bruce Nelson, cujas pesquisas no Xerox PARC estabeleceram os pilares da comunicação entre componentes de sistemas distribuídos.7 A premissa original visava simplificar o desenvolvimento de aplicações distribuídas ao fazer com que a invocação de uma função em uma máquina remota parecesse, para o programador, idêntica a uma chamada de função local.8 Esse desejo de transparência de localização, embora atraente do ponto de vista da conveniência do desenvolvedor, gerou debates acadêmicos intensos sobre a viabilidade de ignorar as diferenças fundamentais entre chamadas locais e remotas, como a latência de rede, a possibilidade de falhas parciais e a falta de um espaço de memória compartilhado.10  
Durante décadas, a RPC evoluiu através de diversas implementações, desde o SunRPC e o padrão CORBA até o surgimento do gRPC e, mais recentemente, do Connect-RPC.10 No entanto, a aplicação da RPC no domínio da IA agêntica em 2026 exige uma expansão dessa base conceitual clássica. Enquanto o núcleo clássico — abstração de procedimento, serialização de parâmetros e retorno de resultados — permanece tecnicamente válido, os conceitos que ganharam peso na arquitetura de agentes autônomos incluem o contrato de interface semântica, a idempotência rigorosa para lidar com a natureza não-determinística dos agentes, e a autorização baseada em intenção por chamada individual.1

### **Comparação de Evolução Tecnológica: RPC Clássica vs. RPC Agêntica**

| Atributo | RPC Clássica (Pre-2024) | RPC Agêntica (Post-2025) |
| :---- | :---- | :---- |
| **Abstração Primária** | Transparência de Localização | Transparência de Capacidade |
| **Descoberta de Serviço** | Catálogos Estáticos / DNS | Descoberta Semântica em Tempo de Execução |
| **Protocolo de Mensagem** | Binário Estrito (ex. Protobuf) | JSON-RPC 2.0 com Metadados Naturais |
| **Segurança** | Perimetral e Baseada em Sessão | Zero Trust com Autorização por Chamada |
| **Observabilidade** | Métricas de Latência e Erro | Rastreamento de Cadeia de Raciocínio (OTel) |
| **Semântica de Falha** | Timeouts e Retentativas Simples | Cancelamento Hierárquico e Elicitação |

A RPC agêntica em 2026 atua como um "operador de competência". Isso significa que o protocolo não transporta apenas dados estruturados, mas também o contexto necessário para que um modelo de IA compreenda o propósito de uma ferramenta e as implicações de sua execução.2 A transição do foco puramente sintático para o foco semântico é o que diferencia os protocolos unificados de 2026 das interfaces de programação de aplicações (APIs) tradicionais.3

## **O Model Context Protocol (MCP) como Infraestrutura para o Protocolo Unificado**

O Model Context Protocol (MCP), introduzido no final de 2024 e consolidado como padrão de mercado pela Agentic AI Foundation em 2025, representa a materialização técnica dessa nova visão de RPC.1 O MCP define uma maneira padrão para aplicações de IA (hosts) se comunicarem com fontes de dados e ferramentas externas (servidores).1 Ao utilizar o JSON-RPC 2.0 sobre canais de transporte flexíveis, como entrada/saída padrão (*stdio*) ou HTTP com Server-Sent Events (SSE), o MCP estabelece uma linguagem universal para a integração de inteligência artificial.14  
A arquitetura do MCP é fundamentada em três primitivas de capacidade:

* **Recursos (Resources):** Fontes de dados de leitura, como arquivos, logs ou esquemas de banco de dados, que fornecem o contexto necessário para o raciocínio da IA.1  
* **Ferramentas (Tools):** Funções executáveis que permitem que a IA realize ações no mundo físico ou digital, como processar pagamentos, enviar notificações ou executar consultas SQL.1  
* **Prompts:** Modelos reutilizáveis que ajudam o host a estruturar a interação com o modelo de IA, garantindo consistência em fluxos de trabalho complexos.1

Em 2026, o MCP evoluiu para além da simples execução de comandos. A introdução do mecanismo de *Sampling* permite que os servidores MCP solicitem completudes do modelo de IA durante o processamento, invertendo o fluxo tradicional e permitindo que a ferramenta participe ativamente do raciocínio.14 Além disso, a *Elicitação* permite que o servidor pause a execução para solicitar entradas humanas cruciais, como credenciais OAuth ou aprovações de segurança, integrando nativamente o conceito de humano-no-loop (*human-in-the-loop*) no protocolo RPC.14

### **A Especificação Técnica e os Mecanismos de Transporte**

A flexibilidade do MCP em 2026 reside na sua separação entre a lógica do protocolo e o mecanismo de transporte subjacente. Enquanto o transporte *stdio* é ideal para ferramentas de desenvolvimento locais e assistentes de codificação (como Cursor ou VS Code), o transporte via HTTP com streaming SSE permite a implantação de servidores de ferramentas em escala global, acessíveis através de nuvens públicas e privadas.14  
A eficiência do transporte HTTP em 2026 é otimizada pela adoção de tecnologias de multiplexação que permitem que um único cliente gerencie múltiplas conexões com servidores distintos, cada um expondo capacidades especializadas.14 Essa estrutura de rede permite que um orquestrador agêntico construa um "grafo de execução" dinâmico, onde cada nó é um servidor MCP acessado via chamadas RPC padronizadas.17

## **Tendências de 2026: Interoperabilidade Agente-a-Agente (A2A)**

Uma das tendências mais disruptivas de 2026 é a ascensão do protocolo Agent-to-Agent (A2A), que estende os conceitos de RPC para a coordenação entre entidades autônomas.19 Liderado pela Linux Foundation e com suporte de gigantes como Google, Microsoft e AWS, o A2A define como os agentes descobrem as capacidades uns dos outros, delegam sub-tarefas e negociam resultados em fluxos de trabalho multi-agente.16  
O A2A resolve o problema da "explosão de coordenação", onde o custo de integrar agentes de diferentes fornecedores tornava-se proibitivo.21 Ao utilizar um modelo semântico comum e um mecanismo de negociação de versão, o A2A permite que um agente construído em LangChain colabore com um agente construído em CrewAI ou Microsoft Agent Framework sem a necessidade de código de integração ad-hoc.19

### **Ciclo de Vida da Tarefa no Protocolo A2A**

O protocolo A2A gerencia o ciclo de vida de uma solicitação através de um processo estruturado de três fases:

1. **Descoberta (Discovery):** O agente cliente consulta um registro de "Agent Cards" (documentos JSON assinados que descrevem capacidades e identidades criptográficas) para identificar o parceiro ideal para uma tarefa.20  
2. **Autorização (Authorization):** Estabelece o escopo de controle e as permissões de acesso, garantindo que o agente delegado tenha apenas a autoridade necessária para realizar a sub-tarefa.13  
3. **Comunicação e Execução:** As tarefas são enviadas via HTTPS utilizando JSON-RPC como envelope de mensagem, com suporte a streaming de logs de evento e estados intermediários através de SSE.16

A sinergia entre MCP e A2A em 2026 é o que fundamenta o Protocolo Unificado. Enquanto o MCP lida com o "tráfego norte-sul" (conexão entre o agente e suas ferramentas de suporte), o A2A gerencia o "tráfego leste-oeste" (coordenação horizontal entre pares de agentes).20

| Característica | MCP (Agent-to-Tool) | A2A (Agent-to-Agent) |
| :---- | :---- | :---- |
| **Objetivo Principal** | Acesso a dados e ferramentas | Delegação e coordenação de tarefas |
| **Entidades Envolvidas** | Host (AI App) e Server (Tool) | Agente Cliente e Agente Remoto |
| **Mecanismo de Descoberta** | Listagem de ferramentas via JSON-RPC | Agent Cards via /.well-known/ |
| **Transporte Preferencial** | stdio ou HTTP/SSE | HTTPS / JSON-RPC |
| **Gubernança** | Controle de acesso a APIs | Negociação de escopo de autonomia |

## **Padrões Emergentes: RPC como Camada de Execução de Alto Desempenho**

Embora o JSON-RPC seja o padrão predominante pela sua legibilidade, o ano de 2026 vê uma tendência crescente na utilização do gRPC e do Connect-RPC como transportes de alto desempenho para o MCP e o A2A.23 Organizações com infraestruturas de microserviços densas preferem o gRPC devido à sua eficiência de serialização binária através de Protocol Buffers e ao suporte nativo para streaming bidirecional full-duplex sobre HTTP/2.12  
O gRPC em 2026 oferece vantagens críticas em termos de segurança e resiliência, como autenticação mTLS (Mutual TLS) integrada e controle de fluxo (*backpressure*) nativo, que evita que um servidor de ferramentas rápido sobrecarregue um agente em processamento.23 A implementação do gRPC como transporte personalizado para o MCP permite que empresas como a Spotify e a Google mantenham padrões de backend consistentes enquanto adotam a agencialidade em suas operações.23

### **Connect-RPC e a Unificação de Protocolos**

O Connect-RPC emergiu em 2026 como a ponte ideal entre o mundo web e os sistemas gRPC tradicionais. Diferente do gRPC-Go original, o Connect permite que servidores suportem simultaneamente o protocolo gRPC, gRPC-Web e o protocolo Connect (baseado em JSON sobre HTTP) a partir de um único manipulador (*handler*).11 Para a IA agêntica, isso significa que um agente pode escolher o transporte mais eficiente disponível: binário para comunicações internas de baixa latência e JSON para integrações que requerem auditoria legível por humanos ou inspeção por ferramentas de monitoramento de rede.11  
A adoção do Connect-RPC na Anthropic e em outras organizações de ponta demonstra que o futuro da RPC agêntica não é um monólito, mas um ecossistema de protocolos compatíveis que priorizam a segurança e a correção da execução sobre a simplicidade de implementação.24

## **Governança, Observabilidade e Segurança de Confiança Zero**

Em 2026, a governança de sistemas agênticos não é mais tratada como um componente externo, mas como uma propriedade intrínseca da camada RPC. O risco de "agência excessiva", onde um agente autônomo executa ações prejudiciais ou não autorizadas devido a uma falha de raciocínio ou uma injeção de prompt, exige que cada chamada de procedimento remoto seja validada contra políticas de segurança rigorosas.13  
A arquitetura de segurança para agentes em 2026 baseia-se no modelo Zero Trust para tráfego leste-oeste. Isso implica que nenhum agente ou servidor de ferramentas possui confiança implícita; todas as interações devem ser autenticadas continuamente através de identidades de máquina, certificados de curta duração e autorizações granulares baseadas em funções (RBAC).13 O uso de Gateways MCP permite que as organizações centralizem a aplicação dessas políticas, inspecionando cada payload JSON-RPC em busca de intenções maliciosas ou violações de conformidade antes que a execução ocorra no sistema de destino.13

### **Observabilidade Distribuída com OpenTelemetry GenAI**

A visibilidade sobre o comportamento dos agentes é garantida em 2026 através das convenções semânticas de OpenTelemetry para GenAI (v1.41.0).27 Diferente do monitoramento tradicional de aplicações (APM), que foca em latência e erros HTTP, o monitoramento agêntico deve capturar a "cadeia de raciocínio" do modelo. Cada chamada de ferramenta, invocação de LLM e passo de recuperação de dados torna-se um *span* filho em um rastreamento distribuído completo.27  
As métricas específicas para cargas de trabalho de IA em 2026 incluem:

* **Contagem de Tokens (gen\_ai.usage.input\_tokens / output\_tokens):** Essencial para o controle de custos e monitoramento de eficiência, uma vez que a latência e o custo correlacionam-se diretamente com o volume de tokens e não apenas com a contagem de requisições.27  
* **Rastreamento de Atributos Semânticos:** Identificação do modelo utilizado, temperatura, identificadores de agentes (gen\_ai.agent.id) e nomes de ferramentas invocadas, permitindo a correlação de falhas com componentes específicos do orquestrador.29  
* **Eventos de Span para Conteúdo:** Captura opcional e sanitizada de prompts e respostas para auditoria e depuração de alucinações, garantindo que informações pessoalmente identificáveis (PII) sejam redigidas ou filtradas antes da ingestão pelo backend de observabilidade.27

A integração nativa de frameworks como CrewAI e LangChain com OpenTelemetry em 2026 permite que as empresas visualizem a execução de seus agentes em dashboards de ferramentas como Grafana, Jaeger ou Datadog, tratando a IA como um cidadão de primeira classe na infraestrutura de TI.28

## **Proposta de Modelo Conceitual: A Arquitetura do Protocolo Unificado (UP)**

O Modelo Conceitual proposto para um Protocolo Unificado voltado à IA agêntica em 2026 estrutura-se em quatro camadas interdependentes, cada uma cumprindo um papel vital no "tecido operacional" da coordenação distribuída:

### **Camada 1: Contrato e Semântica**

Esta camada define o "o quê" e o "porquê". Utiliza os esquemas do MCP para descrever ferramentas e recursos, mas adiciona metadados de versão semântica e contratos de interface rigorosos.1 Em 2026, os contratos não descrevem apenas tipos de dados (int, string), mas garantias de comportamento, como idempotência (essencial para retentativas de agentes) e classificações de risco que determinam se uma ação requer aprovação humana.12

### **Camada 2: Transporte RPC e Mensageria**

Responsável pelo "como" os dados se movem. Esta camada é agnóstica e plugável, suportando JSON-RPC sobre HTTP/SSE para interoperabilidade aberta e gRPC/Connect para execução de alto desempenho.21 O transporte deve suportar streaming incremental e cancelamento hierárquico, permitindo que um host agêntico interrompa uma cadeia de execução se detectar um desvio de objetivo ou uma condição de erro catastrófica.1

### **Camada 3: Execução Agêntica e Orquestração**

Representa o motor de autonomia. Integra os protocolos A2A para coordenação entre pares e gerencia o estado da sessão agêntica.19 Um conceito inovador nesta camada em 2026 é a "Conformidade por Construção" (*Compliance by Construction*), onde o agente gera planos de execução que já respeitam restrições de privacidade e soberania de dados, podando ramos inválidos do grafo de planejamento antes mesmo de tentar qualquer chamada RPC.33

### **Camada 4: Controle e Governança**

A camada de segurança e auditoria. Implementa o Gateway Zero Trust e o Agente de Observabilidade (OTel).13 O controle é exercido através de "Guardrails Determinísticos", que são scripts ou políticas rígidas que validam se os parâmetros de uma chamada RPC estão dentro de limites aceitáveis antes de permitir o despacho para o servidor de infraestrutura.34

### **Tabela: Camadas da Arquitetura do Protocolo Unificado (UP) 2026**

| Camada | Protocolos Chave | Funções Principais | Requisitos Críticos |
| :---- | :---- | :---- | :---- |
| **Contrato** | MCP, JSON-Schema | Definição de capacidades, versão semântica | Descrição em linguagem natural para LLMs |
| **Transporte** | gRPC, Connect-RPC, SSE | Invocação remota, streaming, serialização | Multiplexação e suporte a cancelamento |
| **Execução** | A2A, LangGraph, CrewAI | Coordenação multi-agente, gestão de estado | Planejamento restrito por política |
| **Controle** | Zero Trust, OTel, RBAC | Autorização, auditoria, guardrails | Rastreamento de tokens e custos em tempo real |

## **Avaliação Crítica: Desafios e o Futuro da RPC Agêntica**

Apesar da robustez dos protocolos que emergem em 2026, a transição para um Protocolo Unificado baseado em RPC agêntica enfrenta desafios estruturais. O primeiro é a latência acumulada em cadeias multi-agente: cada "salto" de comunicação entre agentes ou ferramentas adiciona overhead de serialização e processamento, o que pode degradar a experiência do usuário em tarefas que exigem interatividade em tempo real.17 A otimização através do uso de gRPC e transporte binário é uma solução técnica, mas requer que todos os participantes do ecossistema adotem pilhas de tecnologia compatíveis, o que nem sempre é possível em ambientes heterogêneos.12  
Outro desafio crítico é o custo de computação associado à redundância de contexto. Como cada agente em uma equipe coordenada precisa entender o histórico da tarefa, a transferência de contexto via RPC consome volumes massivos de tokens, aumentando o custo operacional em ordens de magnitude em comparação com fluxos de trabalho determinísticos tradicionais.17 Pesquisas em "context engineering" buscam otimizar o que é enviado em cada chamada RPC, garantindo que apenas a informação pertinente seja transmitida, mas o equilíbrio entre completude e custo ainda é um campo de batalha técnico em 2026\.34

### **A Convergência com a 6G e o Tecido de Execução Distribuído**

Olhando para o horizonte de 2027 e além, o Protocolo Unificado para IA Agêntica começa a fundir-se com a infraestrutura de rede 6G. O conceito de "Agentic 6G" propõe que a rede em si seja um tecido de execução agêntico, onde agentes embutidos em dispositivos (wearables, veículos) colaboram com agentes na borda (*edge*) e no núcleo da nuvem através de mecanismos padronizados de descoberta e identidade.4 Nesse cenário, a RPC deixa de ser um evento discreto e torna-se um fluxo contínuo de coordenação de intenção, onde o protocolo gerencia dinamicamente onde a computação deve ocorrer para garantir baixa latência e soberania de dados.4  
A doação do Agent Payments Protocol (AP2) ao FIDO Alliance em abril de 2026 sinaliza o passo final para a autonomia total: a capacidade de agentes autenticarem e executarem transações financeiras de forma segura, integrando a camada de pagamento diretamente ao fluxo RPC de execução de tarefas.36 Essa integração cria o que muitos analistas chamam de "Internet dos Agentes", uma rede onde o valor e a ação são transacionados programaticamente através de protocolos unificados, governados por princípios de transparência, auditabilidade e controle humano final.19  
Em suma, o relatório de livre-docência em 2026 deve concluir que a RPC, longe de ser uma tecnologia legada, renasceu como o sistema nervoso central da inteligência artificial distribuída. A força do Protocolo Unificado não reside em uma única ferramenta ou modelo, mas na capacidade de orquestrar a diversidade de ferramentas e agentes através de uma camada de execução que é, ao mesmo tempo, flexível o suficiente para a inovação e rígida o suficiente para a governança corporativa.1

#### **Referências citadas**

1. Model Context Protocol (MCP): The Standard That's Changing AI Integration in 2026, acessado em maio 5, 2026, [https://devstarsj.github.io/2026/03/18/model-context-protocol-mcp-complete-guide-2026/](https://devstarsj.github.io/2026/03/18/model-context-protocol-mcp-complete-guide-2026/)  
2. Why MCP is the Preferred Tool Protocol for Agentic AI (and How MCP Gateway Simplifies It), acessado em maio 5, 2026, [https://bytebridge.medium.com/why-mcp-is-the-preferred-tool-protocol-for-agentic-ai-and-how-mcp-gateway-simplifies-it-7ec050e7acf9](https://bytebridge.medium.com/why-mcp-is-the-preferred-tool-protocol-for-agentic-ai-and-how-mcp-gateway-simplifies-it-7ec050e7acf9)  
3. What Is Model Context Protocol (MCP)? 2026 Guide \- remio, acessado em maio 5, 2026, [https://www.remio.ai/post/what-is-model-context-protocol-mcp-2026-guide](https://www.remio.ai/post/what-is-model-context-protocol-mcp-2026-guide)  
4. 6G Needs Agents: Toward Agentic AI-Native Networks for Autonomous Intelligence \- arXiv, acessado em maio 5, 2026, [https://arxiv.org/html/2605.01546v1](https://arxiv.org/html/2605.01546v1)  
5. Model Context Protocol \- Wikipedia, acessado em maio 5, 2026, [https://en.wikipedia.org/wiki/Model\_Context\_Protocol](https://en.wikipedia.org/wiki/Model_Context_Protocol)  
6. Ready For General Agents? Let's Test It. | ICLR Blogposts 2026, acessado em maio 5, 2026, [https://iclr-blogposts.github.io/2026/blog/2026/general-agent-evaluation/](https://iclr-blogposts.github.io/2026/blog/2026/general-agent-evaluation/)  
7. Remote procedure call \- Wikipedia, acessado em maio 5, 2026, [https://en.wikipedia.org/wiki/Remote\_procedure\_call](https://en.wikipedia.org/wiki/Remote_procedure_call)  
8. Understanding RPCs \- Part I \- cat /dev/random | Prakhar Srivastav, acessado em maio 5, 2026, [https://prakhar.me/articles/understanding-rpcs/](https://prakhar.me/articles/understanding-rpcs/)  
9. Notes on Birrell & Nelson 1984 \- Implementing RPC, acessado em maio 5, 2026, [https://www.cs.cornell.edu/courses/cs614/1999sp/notes97/implrpc.html](https://www.cs.cornell.edu/courses/cs614/1999sp/notes97/implrpc.html)  
10. Remote Procedure Call \- Christopher Meiklejohn, acessado em maio 5, 2026, [https://christophermeiklejohn.com/pl/2016/04/12/rpc.html](https://christophermeiklejohn.com/pl/2016/04/12/rpc.html)  
11. gRPC compatibility \- Connect RPC, acessado em maio 5, 2026, [https://connectrpc.com/docs/go/grpc-compatibility/](https://connectrpc.com/docs/go/grpc-compatibility/)  
12. MCP vs gRPC: How AI Agents & LLMs Connect to Tools & Data | by Pasan Madhuranga, acessado em maio 5, 2026, [https://medium.com/@pasanmadhuranga333/mcp-vs-grpc-the-real-architecture-behind-how-ai-agents-connect-to-tools-data-40cc55ea0f5e](https://medium.com/@pasanmadhuranga333/mcp-vs-grpc-the-real-architecture-behind-how-ai-agents-connect-to-tools-data-40cc55ea0f5e)  
13. Zero Trust for Your Agentic AI Workforce Solution Brief \- Cisco, acessado em maio 5, 2026, [https://www.cisco.com/c/en/us/solutions/collateral/artificial-intelligence/security/zero-trust-agentic-ai-sb.html](https://www.cisco.com/c/en/us/solutions/collateral/artificial-intelligence/security/zero-trust-agentic-ai-sb.html)  
14. Everything your team needs to know about MCP in 2026 — WorkOS, acessado em maio 5, 2026, [https://workos.com/blog/everything-your-team-needs-to-know-about-mcp-in-2026](https://workos.com/blog/everything-your-team-needs-to-know-about-mcp-in-2026)  
15. MCP Cheat Sheet (2026) \- Model Context Protocol Quick Reference | Webfuse, acessado em maio 5, 2026, [https://www.webfuse.com/mcp-cheat-sheet](https://www.webfuse.com/mcp-cheat-sheet)  
16. Guide to AI Agent Protocols: MCP, A2A, ACP & More \- GetStream.io, acessado em maio 5, 2026, [https://getstream.io/blog/ai-agent-protocols/](https://getstream.io/blog/ai-agent-protocols/)  
17. Multi-agent system architecture: a comparison guide \+ best practices (March 2026), acessado em maio 5, 2026, [https://www.openlayer.com/blog/post/multi-agent-system-architecture-guide](https://www.openlayer.com/blog/post/multi-agent-system-architecture-guide)  
18. AI Agents in Production: Frameworks, Protocols, and What Actually Works in 2026 \- 47Billion, acessado em maio 5, 2026, [https://47billion.com/blog/ai-agents-in-production-frameworks-protocols-and-what-actually-works-in-2026/](https://47billion.com/blog/ai-agents-in-production-frameworks-protocols-and-what-actually-works-in-2026/)  
19. A2A Protocol Surpasses 150 Organizations, Lands in Major Cloud Platforms, and Sees Enterprise Production Use in First Year \- Linux Foundation, acessado em maio 5, 2026, [https://www.linuxfoundation.org/press/a2a-protocol-surpasses-150-organizations-lands-in-major-cloud-platforms-and-sees-enterprise-production-use-in-first-year](https://www.linuxfoundation.org/press/a2a-protocol-surpasses-150-organizations-lands-in-major-cloud-platforms-and-sees-enterprise-production-use-in-first-year)  
20. AI Agent Protocol Ecosystem Map 2026: Complete Visual \- Digital Applied, acessado em maio 5, 2026, [https://www.digitalapplied.com/blog/ai-agent-protocol-ecosystem-map-2026-mcp-a2a-acp-ucp](https://www.digitalapplied.com/blog/ai-agent-protocol-ecosystem-map-2026-mcp-a2a-acp-ucp)  
21. A2A v1 Is Here: Cross-Platform Agent Communication in Microsoft ..., acessado em maio 5, 2026, [https://devblogs.microsoft.com/agent-framework/a2a-v1-is-here-cross-platform-agent-communication-in-microsoft-agent-framework-for-net/](https://devblogs.microsoft.com/agent-framework/a2a-v1-is-here-cross-platform-agent-communication-in-microsoft-agent-framework-for-net/)  
22. Zero Trust MCP Server: Securing the Future of Agentic AI \- The ..., acessado em maio 5, 2026, [https://versa-networks.com/blog/zero-trust-mcp-server-securing-the-future-of-agentic-ai/](https://versa-networks.com/blog/zero-trust-mcp-server-securing-the-future-of-agentic-ai/)  
23. gRPC as a custom transport for MCP | Google Cloud Blog, acessado em maio 5, 2026, [https://cloud.google.com/blog/products/networking/grpc-as-a-native-transport-for-mcp](https://cloud.google.com/blog/products/networking/grpc-as-a-native-transport-for-mcp)  
24. Zero-copy Protobuf and ConnectRPC for Rust | by Iain McGinniss | Mar, 2026 \- Medium, acessado em maio 5, 2026, [https://medium.com/@iainmcgin/zero-copy-protobuf-and-connectrpc-for-rust-69bda8ac0f02](https://medium.com/@iainmcgin/zero-copy-protobuf-and-connectrpc-for-rust-69bda8ac0f02)  
25. ISACA Now Blog 2026 Agentic AI Evolution and the Security Claw, acessado em maio 5, 2026, [https://www.isaca.org/resources/news-and-trends/isaca-now-blog/2026/agentic-ai-evolution-and-the-security-claw](https://www.isaca.org/resources/news-and-trends/isaca-now-blog/2026/agentic-ai-evolution-and-the-security-claw)  
26. When AI Agents Misbehave: Governance and Security for Autonomous AI \- Our Take, acessado em maio 5, 2026, [https://ourtake.bakerbotts.com/post/102me2l/when-ai-agents-misbehave-governance-and-security-for-autonomous-ai](https://ourtake.bakerbotts.com/post/102me2l/when-ai-agents-misbehave-governance-and-security-for-autonomous-ai)  
27. OpenTelemetry for AI Systems: LLM and Agent Observability (2026) \- Uptrace, acessado em maio 5, 2026, [https://uptrace.dev/blog/opentelemetry-ai-systems](https://uptrace.dev/blog/opentelemetry-ai-systems)  
28. OpenTelemetry GenAI Semantic Conventions \- The Standard for LLM Observability, acessado em maio 5, 2026, [https://dev.to/x4nent/opentelemetry-genai-semantic-conventions-the-standard-for-llm-observability-1o2a](https://dev.to/x4nent/opentelemetry-genai-semantic-conventions-the-standard-for-llm-observability-1o2a)  
29. Semantic Conventions for GenAI agent and framework spans ..., acessado em maio 5, 2026, [https://opentelemetry.io/docs/specs/semconv/gen-ai/gen-ai-agent-spans/](https://opentelemetry.io/docs/specs/semconv/gen-ai/gen-ai-agent-spans/)  
30. OpenTelemetry GenAI Semantic Conventions | MLflow AI Platform, acessado em maio 5, 2026, [https://mlflow.org/docs/latest/genai/tracing/opentelemetry/genai-semconv/](https://mlflow.org/docs/latest/genai/tracing/opentelemetry/genai-semconv/)  
31. Principles for Autonomous Agents \- by Amjad Shaikh \- Medium, acessado em maio 5, 2026, [https://medium.com/@amjad.shaikh/principles-for-autonomous-agents-6054293dc3c1](https://medium.com/@amjad.shaikh/principles-for-autonomous-agents-6054293dc3c1)  
32. Agentic AI Architecture in 2026 — What do you know about MCP, A2A and how enterprise systems are actually built? : r/AI\_Agents \- Reddit, acessado em maio 5, 2026, [https://www.reddit.com/r/AI\_Agents/comments/1t00nll/agentic\_ai\_architecture\_in\_2026\_what\_do\_you\_know/](https://www.reddit.com/r/AI_Agents/comments/1t00nll/agentic_ai_architecture_in_2026_what_do_you_know/)  
33. Policy-Constrained Plan Generation for Autonomous AI Agents, acessado em maio 5, 2026, [https://www.tdcommons.org/cgi/viewcontent.cgi?article=10824\&context=dpubs\_series](https://www.tdcommons.org/cgi/viewcontent.cgi?article=10824&context=dpubs_series)  
34. 8 Ways AI Agents Are Evolving in 2026 \- Salesforce, acessado em maio 5, 2026, [https://www.salesforce.com/blog/ai-agent-trends-2026/](https://www.salesforce.com/blog/ai-agent-trends-2026/)  
35. AI autonomy governance (a governance framework for agentic AI ): enabling safe, accountable, and scalable autonomous intelligence \- TM Forum Inform, acessado em maio 5, 2026, [https://inform.tmforum.org/features-and-opinion/ai-autonomy-governance-a-governance-framework-for-agentic-ai-enabling-safe-accountable-and-scalable-autonomous-intelligence](https://inform.tmforum.org/features-and-opinion/ai-autonomy-governance-a-governance-framework-for-agentic-ai-enabling-safe-accountable-and-scalable-autonomous-intelligence)  
36. Google AP2 FIDO Alliance 2026: How Agentic Payments Reshape Commerce, acessado em maio 5, 2026, [https://business20channel.tv/google-ap2-fido-alliance-2026-how-agentic-payments-reshape-c-29-april-2026](https://business20channel.tv/google-ap2-fido-alliance-2026-how-agentic-payments-reshape-c-29-april-2026)
