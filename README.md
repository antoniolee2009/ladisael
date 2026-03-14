# ⚖️ Ladisael Advocacia — Plataforma Jurídica com IA

Sistema completo de gestão jurídica integrado com Inteligência Artificial (Claude da Anthropic), desenvolvido para o escritório **Ladisael Advocacia**.

---

## ✨ Funcionalidades

### 🤖 IA Jurídica (Integrado com Claude API)
- **Assistente IA** — Chat jurídico com histórico de conversa multi-turno
- **Redação Jurídica** — 9 tipos de peças: petição inicial, contestação, recurso, contrato, notificação, parecer, acordo, habeas corpus, embargos
- **Análise & Resumos** — Resumo de processos/documentos, análise de risco, detecção de cláusulas abusivas
- **Gerador de Argumentos** — Argumentos favoráveis, contra-argumentos, jurisprudência aplicável, preliminares processuais
- **Pesquisa Legal** — Jurisprudência STJ/STF, legislação, doutrina, prazos e prescrição

### 📋 Gestão de Processos
- Painel com métricas em tempo real
- Lista de processos com filtros por área e status
- Controle de prazos processuais com alertas visuais por urgência
- Agenda de audiências e compromissos com sugestões da IA

### 👥 Clientes
- Cadastro de clientes (PF e PJ)
- Histórico de processos por cliente
- Controle de honorários

### 💰 Financeiro
- Controle de honorários recebidos e a receber
- Monitoramento de inadimplência
- Honorários contingentes (êxito)

### 📊 Analytics
- Gráfico de novos processos por mês
- Distribuição por área do direito
- Taxa de êxito por área
- Previsão financeira com IA

### 📁 Documentos
- Repositório de peças geradas
- Download de documentos em .txt
- Histórico de geração por IA

---

## 🚀 Como Usar

### Pré-requisitos
- Navegador moderno (Chrome, Firefox, Edge, Safari)
- Chave de API da Anthropic

### Instalação

```bash
git clone https://github.com/seu-usuario/ladisael-ia.git
cd ladisael-ia
```

### Configuração da API

O sistema usa a **Anthropic Claude API**. Para funcionar, é necessário rodar o arquivo através de uma plataforma que injete automaticamente a chave de API (como claude.ai Artifacts), **ou** adicionar sua chave no código.

Para uso local, abra `index.html` e substitua a chamada da API:

```javascript
// No arquivo index.html, nas funções callAI() e sendChat(), adicione o header:
headers: {
  'Content-Type': 'application/json',
  'x-api-key': 'SUA_CHAVE_ANTHROPIC_AQUI',
  'anthropic-version': '2023-06-01',
  'anthropic-dangerous-direct-browser-access': 'true'
}
```

> ⚠️ **Atenção**: Nunca exponha sua chave de API em repositórios públicos. Use variáveis de ambiente em produção.

### Execução Local

Basta abrir o arquivo `index.html` no navegador — nenhum servidor é necessário.

```bash
# Opção 1: Abrir diretamente
open index.html

# Opção 2: Servidor local simples (Python)
python3 -m http.server 8080
# Acesse: http://localhost:8080
```

---

## 🛠️ Tecnologias

| Tecnologia | Uso |
|-----------|-----|
| HTML5 / CSS3 | Interface e estilização |
| JavaScript (Vanilla) | Lógica da aplicação |
| Claude API (Anthropic) | IA jurídica e geração de textos |
| Google Fonts | Tipografia (Playfair Display + DM Sans) |

---

## 📁 Estrutura

```
ladisael-ia/
└── index.html      # Aplicação completa em arquivo único
└── README.md       # Este arquivo
```

---

## 🔧 Personalização

### Trocar nome do escritório
Busque e substitua `Ladisael` no HTML pelas informações do seu escritório.

### Adicionar processos reais
Os dados na tabela de processos são estáticos (demo). Para dados dinâmicos, integre com uma API ou banco de dados (Supabase, Firebase, etc.).

### Modelo de IA
Atualmente usa `claude-sonnet-4-20250514`. Para alterar:
```javascript
model: 'claude-opus-4-20250514'  // Mais poderoso, mais lento
model: 'claude-haiku-4-5-20251001' // Mais rápido, mais barato
```

---

## 📄 Licença

MIT License — uso livre para escritórios de advocacia.

---

**Desenvolvido com IA para o escritório Ladisael Advocacia** ⚖️
