# n8n Fundamentos

### O que é n8n?

- Plataforma de automação de fluxos de trabalho com interface visual intuitiva
- Permite conectar diferentes serviços e ferramentas sem necessidade de codificação avançada
- Open source, com liberdade total para personalização e auto-hospedagem
- Ideal para criar automações entre APIs, bancos de dados, apps e serviços diversos
- Suporta lógica condicional, loops, webhooks e manipulação de dados em tempo real
- Pode ser executado localmente, em servidores cloud ou serviços como Docker e Railway
- Otimiza processos manuais, reduz erros operacionais e economiza tempo em tarefas repetitivas

### Conceitos fundamentais

- **Workflow (fluxo da automação)**: sequência automatizada de ações que conecta diferentes ferramentas e serviços para executar tarefas de forma contínua
- **Node (nó)**: unidade funcional dentro do workflow responsável por realizar uma ação específica, como enviar e-mails, buscar dados ou transformar informações
- **Trigger (gatilho)**: ponto de partida do workflow, ativado por um evento como a chegada de uma mensagem, a execução manual ou um horário programado
- **Controles de Fluxo**: elementos como IF, Switch e Merge que controlam o caminho da automação com base em condições ou resultados
- **Webhook**: permite que serviços externos acionem workflows ao enviar dados diretamente para o n8n por meio de requisições HTTP
- **Execução**: cada vez que um workflow é acionado, o n8n realiza uma execução, processando os dados passo a passo de acordo com os nodes configurados

## Ferramentas

- NodeJS(Aqui estou usando a versão 22.21.1)

## Instalando o n8n

**Verificando se temos o NodeJS instalado**
```shell
    node -v
```

**Instalando o n8n**
```shell
    npx n8n
```

## Triggers

**Triggers são pontos de partida dos workflows**: eles disparam o fluxo de automação a partir de um evento externo ou interno.

**Tipos comuns de triggers**:
- **Webhook Trigger**: escuta requisições HTTP externas. Ideal para integrar com APIs, formulários e sistemas.
- **Schedule Trigger**: executa o workflow com base em datas e horários definidos (ex: todo dia às 10h).
- **Cron Trigger**: dispara fluxos com base em expressões cron avançadas.
- **Interval Trigger**: executa o fluxo em ciclos regulares (ex: a cada 5 minutos).
- **App Triggers (ex: Telegram, Gmail, Slack)**: iniciam o fluxo com base em eventos desses aplicativos.
- **Gatilhos personalizados**:é possível configurar triggers que ouvem eventos de ferramentas específicas via APIs, autenticações ou webhooks.

## Action Nodes

**Action Nodes executam tarefas após o trigger**: são os blocos responsáveis por realizar ações dentro do workflow, como enviar e-mails, manipular dados ou integrar APIs.

**Exemplos de ações que podem ser realizadas**:
- **Envio de mensagens** (Telegram, Slack, Discord)
- **Requisições HTTP** (GET, POST, PUT, DELETE para APIs externas)
- **Manipulação de arquivos** (upload, download, conversões)
- **Interação com bancos de dados** (consultas, inserções, atualizações)
- **Integração com planilhas e CRMs** (Google Sheets, Notion, HubSpot)
- **Personalizáveis e dinâmicos**: cada nó de ação pode usar dados recebidos do trigger ou de outros nós para executar tarefas específicas.

## Trabalhar com dados dos nós

- Cada nó no n8n recebe e envia dados estruturados em JSON
- É possível acessar os dados de nós anteriores usando a sintaxe:
{{$json.nome_do_campo}}
- Utilize o botão de "Exibir dados" para visualizar a saída de qualquer nó
- Campos com ícone de lápis permitem usar Expressões Dinâmicas
- Pode-se transformar os dados com nós de código (Function, Set, etc.)
- Os dados trafegam de um nó para outro como uma lista de itens (array de objetos)
- Filtros, loops e mapeamentos podem ser feitos com nós de controle de fluxo