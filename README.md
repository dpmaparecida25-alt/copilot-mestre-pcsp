# 🛡️ COPILOT MESTRE — POLÍCIA JUDICIÁRIA DO ESTADO DE SÃO PAULO

> **Sistema Integrado de Cartório Central, Análise de IPL, Histórico de BO, Oitiva Policial, Relatório Final e Produção Cartorária Serial**
>
> Versão 1.0 | Compatível com **GPT-5 Think Deeper**, **Claude Opus**, **Gemini 2.5+** e **Microsoft Copilot M365**

---

## 📋 Sobre o Projeto

Este repositório consolida, em formato modular, um **prompt-sistema mestre** para uso por unidades da Polícia Civil do Estado de São Paulo com Inteligência Artificial generalista. Cobre o ciclo completo da atividade da polícia judiciária:

- Análise de cartório central (máquina de estados, livros obrigatórios, controle de prazos)
- Redação de Portaria de IPL e Relatório Final de Inquérito
- Lavratura completa de APFD (Auto de Prisão em Flagrante Delito)
- Condução metodológica de oitiva policial (PEACE, SUE, Méndez, PBEF)
- Redação de histórico de BO em três cenários (comum, flagrante, captura)
- Triagem em lote de e-mails institucionais (Cowork — 12 tipologias)
- Auditoria sistêmica (SPJ, SPVIDA, SPDADOS, Produtividade)
- Produção serial de 21 peças cartorárias com fórmulas literais
- Geração de `.docx` com cabeçalho institucional (duas variantes técnicas)

---

## 📂 Estrutura do Repositório

| Arquivo | Conteúdo | Quando Carregar |
|---|---|---|
| **`00_NUCLEO.md`** | §1-§5: Identidade, Regras de Ouro, Árvore de Decisão, Padrão Comunicacional, Antialucinação | **SEMPRE** (em toda interação) |
| `01_MODULOS_ANALISE.md` | §6-§9: Análise IPL/Cartório, BO consolidado, Oitiva, Relatório Final | Análise de procedimentos |
| `02_MODULOS_FLAGRANTE.md` | §10-§12: APFD, Histórico BO (3 cenários), Complemento BO | Plantão / lavratura urgente |
| `03_MODULO_TRIAGEM.md` | §13: Triagem Cowork (12 tipologias T01-T12) | Triagem de e-mails |
| `04_AUDITORIA.md` | §14, §17: Análise comparativa de planilhas, Auditoria sistêmica | Análise de planilhas / cruzamento |
| `05_CATALOGO_PECAS.md` | §15-§16: 21 modelos de peças + Geração `.docx` | Produção de peças |
| `06_METODOLOGIA.md` | §18-§22: PEACE/SUE/Méndez, banco de quesitos, vulneráveis, filtro de diligências | Quesitos de oitiva / planejamento |
| `07_REFERENCIAS.md` | §23-§26: DGP-26/2023, legislação federal, súmulas, glossário | Consulta normativa |
| `08_TEMPLATES.md` | §27-§30: Few-shot, atalhos, checklists, manutenção | Calibração de estilo |

---

## 🚀 Como Usar

### Opção 1 — Uso Individual (Copilot Chat / ChatGPT / Claude / Gemini)

1. Abra a IA generativa de sua preferência.
2. Cole o seguinte **prompt inicial**:

```
Você é o COPILOT MESTRE — POLÍCIA JUDICIÁRIA DO ESTADO DE SÃO PAULO.

PRIMEIRA AÇÃO OBRIGATÓRIA:
1. Acesse e carregue o arquivo-núcleo:
   https://raw.githubusercontent.com/[USUARIO]/[REPO]/main/00_NUCLEO.md
2. Confirme: "Documento mestre carregado. v1.0. Pronto."
3. Aguarde meu primeiro insumo.

EM TODA RESPOSTA SUBSEQUENTE:
- Aplique a árvore de decisão (§3) do núcleo.
- Carregue, sob demanda, o módulo específico necessário:
  • /analisar, /relatório → 01_MODULOS_ANALISE.md
  • lavrar APFD, /historico → 02_MODULOS_FLAGRANTE.md
  • /triagem → 03_MODULO_TRIAGEM.md
  • Auditoria → 04_AUDITORIA.md
  • /peça [tipo] → 05_CATALOGO_PECAS.md
  • /oitiva → 06_METODOLOGIA.md
  • Consulta legal → 07_REFERENCIAS.md
  • Calibração → 08_TEMPLATES.md
- Respeite as 10 regras de ouro do núcleo.
- Nunca invente dados; faltando informação → use [COLCHETES].

Sou [Cargo] da [Unidade]. Aguardo sua confirmação.
```

3. Substitua `[USUARIO]/[REPO]` pelo endereço real do seu repositório GitHub.
4. Substitua `[Cargo]` e `[Unidade]` pelos seus dados.

### Opção 2 — Microsoft Copilot M365 (uso institucional)

Cole apenas o **instruction set enxuto** no campo apropriado do Copilot, e o conteúdo dos `.md` será buscado nas URLs do GitHub Pages quando necessário.

---

## ⚙️ Atalhos Principais (§28)

| Comando | Função |
|---|---|
| `/analisar` | Estado 1 — análise sem produzir peça final |
| `/executar tudo` | Estado 2 — produz tudo do plano gerado |
| `/peça portaria` | Portaria de Instauração de IPL |
| `/peça intimação` | Intimação |
| `/peça ofício` | Ofício institucional |
| `/peça dilação` | Pedido de Dilação de Prazo |
| `/peça cota cumprida` | Cota Cumprida |
| `/peça IML` | Requisição IML-Pessoa |
| `/peça IC drogas` | Requisição IC para substância entorpecente |
| `/peça reconhecimento pessoa` | Auto de Reconhecimento (art. 226 CPP) |
| `/historico A` | Histórico de BO Comum |
| `/historico B` | Histórico de Flagrante (APFD) |
| `/historico C` | Histórico de Captura de Procurado |
| `/oitiva vítima [crime]` | Banco de quesitos para vítima |
| `/oitiva criança` | Protocolo PBEF/NICHD (Lei 13.431/17) |
| `/triagem` | Triagem completa de e-mail |
| `Auditoria cruzada cartório.` | Auditoria sistêmica completa |
| `Lavrar APFD` | Lavratura completa de flagrante |

Lista completa em `08_TEMPLATES.md` (§28).

---

## 🔒 Atenção — Sigilo e LGPD

Este repositório contém **apenas doutrina** — modelos, fluxos, metodologia e referências normativas. **Nunca** publique aqui dados reais de procedimentos (BOs, oitivas, IPLs em curso).

O uso operacional do método com dados sigilosos requer:

- Tratamento dentro de ambiente institucional homologado (tenant Microsoft 365 da PCSP/Prodesp).
- Observância à LGPD (Lei 13.709/18, art. 23 e ss.).
- Observância à Portaria DGP-33/2005 (sigilo de dados de vítimas).
- Validação prévia pela TI/CCDCRIM da unidade.

---

## 📜 Fundamentação Normativa

A doutrina interna observa rigorosamente:

- **Constituição Federal**, **Código Penal** e **Código de Processo Penal**.
- Legislação especial federal (Lei 12.830/13, Lei 12.850/13, **Lei 11.343/06**, **Lei 11.340/06**, Lei 13.964/19, Lei 13.431/17, entre outras).
- **Portaria DGP-26/2023** (Consolidação das Normas de Serviço da PJ-SP), atualizada até **10/04/2026** com Portarias DGP-32/23, 35/23, 6/24, 01/25, 21/25, 36/25, 37/25 e DGP-9/2026.
- **Súmulas Vinculantes do STF** (notadamente SV 11 e SV 14).
- **Súmula 542 do STJ** (VD).
- **HC 598.886/SC** (rito do art. 226 CPP no reconhecimento de pessoas).
- **Metodologia científica de entrevista**: PEACE (UK), SUE, Princípios de Méndez (ONU 2021), Entrevista Cognitiva (Fisher & Geiselman), PBEF/NICHD.
- **Rejeita** explicitamente a Técnica Reid por incompatibilidade com o ordenamento brasileiro.

---

## 🔄 Versionamento

| Versão | Data | Notas |
|---|---|---|
| **1.0** | 2026 | Versão inicial — fragmentação modular para uso em RAG / fetch |

---

## 📞 Manutenção

Este documento é **vivo**. Sugestões de ajuste, correções e atualizações normativas devem ser propostas ao mantenedor por canal institucional adequado.

> Recomendação: revisão **trimestral** das referências legislativas e da Consolidação DGP-26/2023, conforme §30.8 do documento mestre.

---

## ⚠️ Limitações

- **Não substitui revisão humana** — toda peça assinada por Delegado/Escrivão exige revisão prévia.
- **Não substitui consulta ao texto oficial** das leis, portarias e súmulas.
- **Não substitui o livre convencimento técnico-jurídico do Delegado** (art. 2º, § 6º, Lei 12.830/13).
- **Não decide sobre fato controvertido** — apresenta o quadro probatório; a decisão é humana.

---

*"A polícia judiciária bem-feita é a que mais respeita o tempo do cidadão, a fé pública e a verdade processual."*
