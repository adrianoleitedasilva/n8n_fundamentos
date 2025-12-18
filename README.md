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

- Workflow (fluxo da automação): sequência automatizada de ações que conecta diferentes ferramentas e serviços para executar tarefas de forma contínua
- Node (nó): unidade funcional dentro do workflow responsável por realizar uma ação específica, como enviar e-mails, buscar dados ou transformar informações
- Trigger (gatilho): ponto de partida do workflow, ativado por um evento como a chegada de uma mensagem, a execução manual ou um horário programado
- Controles de Fluxo: elementos como IF, Switch e Merge que controlam o caminho da automação com base em condições ou resultados
- Webhook: permite que serviços externos acionem workflows ao enviar dados diretamente para o n8n por meio de requisições HTTP
- Execução: cada vez que um workflow é acionado, o n8n realiza uma execução, processando os dados passo a passo de acordo com os nodes configurados

## Ferramentas

- NodeJS

## Instalando o n8n

**Verificando se temos o NodeJS instalado**
```shell
    node -v
```

**Instalando o n8n**
```shell
    npx n8n
```

**Iniciando o servidor local do n8n**
```shell
    n8n
```