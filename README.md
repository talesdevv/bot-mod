<div align="center">
# 🛡️ Mod Bot

**Bot de moderação para Discord com sistema de keys integrado**  
Desenvolvido com [discord.js v14](https://discord.js.org) · Components V2 · ESModules

[![Discord](https://img.shields.io/badge/Suporte-Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/xCy8yqSFr3)
[![GitHub](https://img.shields.io/badge/Criador-talesdevv-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/talesdevv)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org)
[![discord.js](https://img.shields.io/badge/discord.js-v14-5865F2?style=for-the-badge)](https://discord.js.org)
![Status](https://img.shields.io/badge/Status-Em%20desenvolvimento-yellow?style=for-the-badge)

</div>

---

## ✨ Funcionalidades

### 🔨 Moderação Completa
Comandos slash com verificação de hierarquia de cargos, respostas com embed e ID de caso gerado automaticamente.

| Comando | Descrição | Permissão Necessária |
|---|---|---|
| `/ban` | Bane um membro (com opção de apagar mensagens) | `Banir Membros` |
| `/unban` | Remove o banimento de um usuário por ID | `Banir Membros` |
| `/kick` | Expulsa um membro do servidor | `Expulsar Membros` |
| `/mute` | Aplica timeout com duração configurável | `Moderar Membros` |
| `/unmute` | Remove o timeout de um membro | `Moderar Membros` |
| `/clear` | Apaga mensagens em massa (com filtro por usuário) | `Gerenciar Mensagens` |
| `/lock` | Bloqueia um canal para membros | `Gerenciar Canais` |
| `/unlock` | Desbloqueia um canal | `Gerenciar Canais` |
| `/ping` | Verifica a latência do bot | — |

### 🔑 Sistema de Keys
Painel interativo completo para gerenciar keys de acesso diretamente pelo Discord.

- **Criar keys** com nome, descrição, tipo (texto ou cargo) e conteúdo
- **Limite de usos** configurável (finito ou ilimitado `∞`)
- **Data de expiração** opcional por key
- **Resgatar keys** com código no formato `XXXX-XXXX-XXXX-XXXX`
- **Editar e excluir** keys existentes
- **Publicar** keys em canais configurados
- **Log de resgates** em canal dedicado
- **Controle de acesso** por cargo permitido

---

## ⚙️ Configuração

### Pré-requisitos

- [Node.js](https://nodejs.org) **v18 ou superior**
- Uma aplicação criada no [Discord Developer Portal](https://discord.com/developers/applications)

### Instalação

```bash
# 1. Clone o repositório
git clone https://github.com/talesdevv/mod-bot.git
cd mod-bot

# 2. Instale as dependências
npm install

# 3. Configure as variáveis de ambiente
cp .env.example .env
```

### Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto com os seguintes valores:

```env
TOKEN=seu_token_aqui
CLIENT_ID=id_da_aplicacao_aqui
GUILD_ID=id_do_servidor_aqui
```

| Variável | Onde encontrar |
|---|---|
| `TOKEN` | [Portal do Desenvolvedor](https://discord.com/developers/applications) → seu app → Bot → Token |
| `CLIENT_ID` | Portal do Desenvolvedor → seu app → General Information → Application ID |
| `GUILD_ID` | Clique com botão direito no servidor → Copiar ID do servidor |

### Deploy e Inicialização

```bash
# Registra os slash commands no servidor
npm run deploy

# Inicia o bot
npm start
```

---

## 📁 Estrutura do Projeto

```
mod-bot/
├── src/
│   ├── commands/          # Slash commands (ban, kick, mute, keysystem...)
│   ├── events/            # Eventos do Discord (ready, interactionCreate)
│   ├── handlers/          # Carregadores de comandos e eventos
│   ├── interactions/
│   │   └── keysystem/     # Lógica do sistema de keys (criar, editar, resgatar...)
│   ├── database/
│   │   └── keystore.js    # Armazenamento em memória das keys e configurações
│   ├── utils/             # Utilitários (cores, emojis, painéis, logger)
│   ├── assets/            # Imagens e ícones usados nos embeds
│   ├── config.js          # Leitura das variáveis de ambiente
│   └── index.js           # Entry point do bot
├── .env                   # Variáveis de ambiente (não versionar!)
├── package.json
└── README.md
```

---

## 🗺️ Roadmap

> O projeto está em desenvolvimento ativo. Atualizações futuras estão planejadas!

- [ ] Persistência de dados com banco de dados (SQLite ou MongoDB)
- [ ] Sistema de advertências (`/warn`, histórico por usuário)
- [ ] Logs de moderação em canal dedicado
- [ ] Suporte a múltiplos servidores com configuração independente
- [ ] Painel de configuração geral via Discord
- [ ] Anti-raid e proteções automáticas
- [ ] Dashboard web para administração

---

## 🤝 Suporte

Encontrou um bug ou tem alguma dúvida? Acesse nosso servidor de suporte:

<div align="center">

[![Entrar no Discord](https://img.shields.io/badge/Entrar%20no%20servidor-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/xCy8yqSFr3)

</div>

---

## 👨‍💻 Criador

Desenvolvido com 💙 por **[talesdevv](https://github.com/talesdevv)**

---

<div align="center">

*Este projeto está em desenvolvimento. Contribuições e feedbacks são bem-vindos!*

</div>
