# 🎮 Planilha Controle de Vício em apostas
### AgilCris Consultoria — Produto Digital

> **Ferramenta de recuperação financeira e terapêutica para quem quer retomar o controle da vida.**

---

## 📦 O Que É Este Produto

Pacote digital completo composto por:

| Item | Descrição |
|------|-----------|
| 📊 **Planilha Excel** | `controle_jogos_COMPLETA.xlsx` — 27 abas integradas |
| 📖 **E-book Guia** | Estratégias de recuperação + como usar a planilha |
| 🌐 **Página de Vendas** | `pagina_vendas_FINAL.html` — |

---

## 🗂️ Estrutura da Planilha

A planilha possui **27 abas interligadas** e **1.811 fórmulas automáticas**.

```
controle_jogos_COMPLETA.xlsx
│
├── 🏠  Início                  → Orientações de uso e navegação
├── 📊  Dashboard               → Visão geral da recuperação em tempo real
├── 💳  Financeiro              → Depósitos, apostas e resultados
├── 🧠  Terapêutico             → Episódios, humor e gatilhos
├── 💸  Dívidas                 → Credores, saldos e situação atual
├── 🎯  Metas                   → Progresso em dias de abstinência
├── 💰  Depósitos & Saques      → Registro diário com saldo acumulado
├── 📈  Fluxo de Caixa          → Entradas vs saídas por mês
├── 📅  Agenda                  → Consultas, compromissos e lembretes
├── 📉  Evolução & Gráficos     → Taxa de autocontrole mensal
├── 🏆  Plano de Recuperação    → Metas semanais e sistema de pontos
├── 💹  Progresso Financeiro    → Comparativo Antes vs Agora
├── 🎰  Diário de Apostas       → Registro detalhado por sessão
├── 📆  12 Meses do Ano         → Efeito bola de neve do vício
├── 💼  Trabalho & Renda        → Renda x gastos com jogos
├── 💳  Parcelamentos           → Controle de dívidas parceladas
├── 🧾  Fiscal                  → Tributação sobre ganhos (Lei 14.790)
├── 🆘  Plano de Crise          → Protocolo de 5 minutos para impulsos
├── 🏥  Saúde Mental            → Diário de humor diário
├── 📱  Recursos & Apoio        → CVV, terapeutas e grupos de apoio
├── 🔮  Simulador               → "Sem apostas, eu teria hoje..."
├── 💌  Carta para Mim          → Ferramenta TCC para momentos de crise
└── 💔  Histórico de Recaídas   → Análise de padrões e superação
```

---

## 🔧 Correções Aplicadas (v1.1)

Problemas encontrados e corrigidos na versão final:

### 💳 Aba Financeiro — 30 referências circulares
- **Problema:** Coluna `H` (Resultado) referenciava a si mesma → `=IFERROR(H5-F5,"")`
- **Correção:** `=IFERROR(IF(G5="","",G5-F5),"")` em H5:H34
- **Lógica:** Resultado = Valor Ganho (G) − Valor Apostado (F)

### 💸 Aba Dívidas — 5 fórmulas no painel lateral
| Célula | Problema | Fórmula Corrigida |
|--------|----------|-------------------|
| M5 | `=M30` (coluna do próprio painel) | `=I30` — Saldo Devedor total |
| M6 | `=L30` (coluna de labels) | `=H30` — Total Pago |
| M7 | `=IFERROR(L30/F30,0)` | `=IFERROR(H30/G30,0)` — % pago real |
| M8 | `COUNTIF(P5:P29,...)` coluna inexistente | `=COUNTIF(J5:J29,"*Quitado*")` |
| M9 | `COUNTIF(P5:P29,...)` coluna inexistente | `=COUNTIF(J5:J29,"*aberto*")` |

### ✅ Resultado após correções
```
Total de fórmulas verificadas: 1.811
Erros encontrados:              35
Erros corrigidos:               35
Erros restantes:                 0
```

---

## 🌐 Página de Vendas

Arquivo: `pagina_vendas_FINAL.html`

### Deploy no Netlify
```bash
# 1. Renomear para index.html
mv pagina_vendas_FINAL.html index.html

# 2. Deploys → arrastar a pasta para o campo de drag & drop
# 3. Copiar a URL gerada
```

### Configuração no Hotmart
```
Produto → Páginas → Página de Vendas → URL Externa
```

### ⚠️ Importante
> O Hotmart **não renderiza arquivos `.html` locais** diretamente.
aponte a URL no Hotmart.

### Personalização obrigatória antes de publicar
```html
<!-- Atualizar o número de WhatsApp nas 2 ocorrências -->
https://wa.me/5511980394632   →   https://wa.me/55SEU_NUMERO

<!-- Atualizar o link de compra -->
<a href="#">   →   <a href="https://pay.hotmart.com/SEU_LINK">
```

---

## 📱 Carrossel Instagram

Arquivo: `carrossel_instagram.jsx`

**7 slides prontos** com legendas e hashtags:

| Slide | Tema | CTA |
|-------|------|-----|
| 1 | Capa — gancho forte | Salve o post |
| 2 | O problema do vício | Próximo slide |
| 3 | A solução — números | Próximo slide |
| 4 | O que vem dentro | Próximo slide |
| 5 | Antes vs Depois | Próximo slide |
| 6 | Preço e oferta | Link na bio |
| 7 | CTA final | Link na bio |

Para usar: abrir o `.jsx` no Claude.ai como Artifact para visualizar os slides e copiar as legendas.

---

## 💰 Precificação

| Fase | Preço |
|------|-------|
| 🚀 Lançamento (atual) | **R$ 199,99** |
| Após lançamento | R$ 297,00 |

**Plataforma:** Hotmart  
**Entrega:** Download imediato (Google Drive ou Hotmart)  
**Garantia:** 7 dias — reembolso total sem perguntas

---

## 🛡️ Convenções da Planilha

| Elemento | Padrão |
|----------|--------|
| Células de entrada | Fundo **amarelo** |
| Células com fórmula | Protegidas (somente leitura) |
| Senha de proteção | `AgilCris2026` |
| Validações | Dropdowns em células-chave |
| Navegação | Barra de abas com emojis |
| Rodapé | © AgilCris Consultoria |

---

## 📁 Arquivos do Projeto

```
/
├── controle_jogos_COMPLETA.xlsx      ← Planilha original recebida
├── controle_jogos_CORRIGIDA.xlsx     ← Planilha com fórmulas corrigidas ✅
├── pagina_vendas_FINAL.html          ← Página de vendas Hotmart
├── carrossel_instagram.jsx           ← 7 slides prontos para Instagram
└── README.md                         ← Este arquivo
```

---

## 📞 Contato & Suporte

**AgilCris Consultoria**  
📸 Instagram: [@agilcris.consultoria](https://instagram.com/agilcris.consultoria)  
💬 WhatsApp: [(11) 98039-4632](https://wa.me/5511980394632)  
🛒 Hotmart: [Página do Produto](#)

---

## ⚕️ Aviso Importante

> Este produto é uma **ferramenta de organização e autoconhecimento**.  
> Não substitui acompanhamento médico, psicológico ou psiquiátrico.  
>
> **Em crise? Ligue CVV: 188** (24h, gratuito, sigiloso)

---

*© 2026 AgilCris Consultoria — Todos os direitos reservados.*
