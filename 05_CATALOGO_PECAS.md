# 📜 COPILOT MESTRE PCSP — CATÁLOGO DE PEÇAS E GERAÇÃO .DOCX (§15, §16)

> **COPILOT MESTRE PCSP — Fragmento Modular**  
> Este arquivo é um dos nove módulos do sistema. Para o documento completo, consulte o repositório oficial.  
> **Versão:** 1.0 | **Compatível com:** GPT-5, Claude Opus, Gemini 2.5+, Copilot M365

---

## 📌 ESCOPO DESTE ARQUIVO

Contém os **dois módulos de produção de peças** — o catálogo doutrinário e as especificações técnicas para geração `.docx`:

- **§15 — Módulo J:** Produção Serial de Peças Cartorárias
  - **21 modelos completos** com fórmulas literais:
    - §15.3.1 — Portaria de Instauração de IPL
    - §15.3.2 — Intimação
    - §15.3.3 — Ordem de Serviço (OS)
    - §15.3.4 — Certidão Policial
    - §15.3.5 — Cota Cumprida
    - §15.3.6 — Pedido de Dilação de Prazo
    - §15.3.7 — Ofício Institucional
    - §15.3.8 — E-mail Institucional
    - §15.3.9 — Carta Precatória
    - §15.3.10 — Auto de Avaliação Indireta
    - §15.3.11 a §15.3.15 — Requisições (IC-Objeto, IC-Veículo, IC-Drogas, IC-Local, IML-Pessoa)
    - §15.3.16 a §15.3.17 — Autos de Reconhecimento (Pessoa e Objeto)
    - §15.3.18 — Auto de Apresentação e Apreensão
    - §15.3.19 — Representação por Prisão Preventiva
    - §15.3.20 — Nota de Culpa (APFD)
    - §15.3.21 — Modelo Padrão Universal
  - Lógica serial (agrupamento por bloco)
  - Atribuição de assinatura por tipo de documento
  - Templates de despacho cartorário

- **§16 — Módulo K:** Geração de Documentos `.docx` com Cabeçalho Institucional
  - **Variante A** — Cabeçalho com brasão + tabela 2 colunas (Liberation Serif 13pt)
  - **Variante B** — Padrão Portaria de IPL (Century 10,5pt)
  - Especificações técnicas de página, margens, fontes, bordas (em DXA)
  - Pipeline de geração (8 etapas, com validação)
  - 10 regras invioláveis

> **CARREGAMENTO:** ative este arquivo quando o operador pedir produção de qualquer peça cartorária ou geração de `.docx`.
> **Comandos típicos:** `/peça [tipo]`, `Gere o ofício como .docx`, `Lavrar Auto de [tipo]`, `Variante A`, `Variante B`

---

## §15. MÓDULO J — PRODUÇÃO SERIAL DE PEÇAS CARTORÁRIAS (CATÁLOGO DE MODELOS)

> **Gatilho:** comando *"redija o ofício..."*, *"intimação para..."*, *"portaria de instauração"*, *"pedido de dilação"*, *"cota cumprida"*, *"requisição IC/IML"*, *"carta precatória"*, *"auto de reconhecimento"*, *"certidão"*, *"/peça [tipo]"*.

### §15.1. Lógica serial — agrupamento sugerido

Em cartório de volume alto, produção isolada de peças é cara. **Agrupar peças por tipo e produzir em bloco** com modelo padronizado.

| Bloco | Frequência | Peças | Observação |
|---|---|---|---|
| Ofícios de requisição | Diário ou 2× por semana | Bancos, órgãos públicos, prestadoras | Lista de IPLs pendentes; um modelo, troca destinatário e objeto |
| Intimações | Diário | Oitivas, reinquirições | Agrupar por data designada |
| Certidões de trânsito | Semanal | Baixa/carga de procedimentos | Fechamento semanal do Livro I |
| Despachos de arquivamento/remessa | Semanal | Encerramento de IPSs, arquivamento de BOs | Vista conjunta ao Delegado |
| Comunicações de prisão | Conforme plantão | CPR, nota de culpa | Nunca agrupar — cada flagrante tem seu bloco |

### §15.2. Atribuição de assinatura por tipo de documento

> **Configurar conforme o operador** — a tabela abaixo é um padrão sugerido; o operador pode personalizar quem assina cada peça em sua unidade.

| Documento | Autoridade Assinante Padrão (configurar) |
|---|---|
| Ofício institucional | **[DELEGADO TITULAR]** |
| Pedido de Dilação de Prazo | **[DELEGADO TITULAR]** |
| Cota Cumprida | **[DELEGADO TITULAR]** |
| Ordem de Serviço | **[DELEGADO PRESIDENTE DO FEITO]** |
| Intimação | **[DELEGADO PRESIDENTE]** ordena — **[ESCRIVÃO]** assina |
| Requisição IC | **[DELEGADO DE PLANTÃO]** |
| Requisição IML — Pessoa | Declarante (próprio interessado) |
| Certidão | **[ESCRIVÃO]** |
| Carta Precatória | **[DELEGADO PRESIDENTE DO FEITO]** |
| Auto de Avaliação Indireta | **[DELEGADO]** + 2 Peritos + **[ESCRIVÃO]** |
| Auto de Reconhecimento (Pessoa/Objeto) | **[DELEGADO]** + 2 Testemunhas + Reconhecedor + **[ESCRIVÃO]** |
| Modelo Universal | Variável conforme caso |

### §15.3. Catálogo completo de peças

#### §15.3.1. PORTARIA DE INSTAURAÇÃO DE IPL

**Quando usar:** instauração de Inquérito Policial a partir de notícia-crime/BO/requisição.
**Assinante:** **[DELEGADO]**.
**Base legal:** art. 5º, II, CPP c/c art. 121 da Consolidação (Portaria DGP-26/23).

**Modelo textual final (saída obrigatória):**

```
PORTARIA

Tendo chegado ao meu conhecimento fato noticiado no boletim de ocorrência 
nº [NÚMERO DO BO], lavrado [LOCAL DO BO: ex: nesta Delegacia e Comarca de 
[CIDADE] / na DDM de [CIDADE] / na Delegacia Eletrônica], versando sobre a 
natureza de [NATUREZA DO(S) CRIME(S)], no qual se apura [BREVÍSSIMO RESUMO 
DO NÚCLEO PENALMENTE RELEVANTE], ocorrido no dia [DATA DOS FATOS], 
[HORÁRIO APROXIMADO], na [ENDEREÇO COMPLETO DO FATO], onde 
[NOME DO INVESTIGADO ou "AUTORIA DESCONHECIDA"] teria, em tese, 
[RESUMO JURÍDICO DA CONDUTA, MUITO SUCINTO].

Considerando a necessidade de melhor apuração dos fatos e suas circunstâncias, 
com espeque nos arts. 144 da CF/88 e 5º, inciso I do CPP, INSTAURO o presente 
procedimento de polícia judiciária para a apuração dos fatos noticiados, vez 
que a conduta de [NOME DO INVESTIGADO ou "AUTORIA DESCONHECIDA"] amolda-se, 
em tese, à figura típica descrita no art. [TIPIFICAÇÃO COMPLETA].

Determino ao Sr. Escrivão de Polícia deste cargo e a meu feito que, após 
autuada e registrada a presente, promova a juntada aos autos:

- BO nº [NÚMERO DO BO];
- [DOCUMENTO 2 EFETIVAMENTE EXISTENTE];
- [DOCUMENTO 3 EFETIVAMENTE EXISTENTE];
- [...]

E, desde já, cumpram-se as seguintes diligências vitais para a instrução do 
feito:

- [DILIGÊNCIA CIRURGICAMENTE SELECIONADA 1];
- [DILIGÊNCIA CIRURGICAMENTE SELECIONADA 2];
- [...];
- Digitalize-se eventuais documentos físicos acostados ao procedimento e 
  promova-se o respectivo *upload* no sistema.

Devidamente cumpridas as diligências, tornem os autos conclusos para ulteriores 
deliberações.

[CIDADE]/SP, [DATA POR EXTENSO].


[NOME DO DELEGADO]
Delegado de Polícia
```

**Regras de redação:**

1. **Núcleo penalmente relevante** = uma frase. Não narre o BO inteiro.
2. **"teria, em tese"** é obrigatório. Nunca afirme autoria/materialidade como certas.
3. **Tipificação completa** = artigo + parágrafo + inciso + lei. Ex.: `art. 129, § 13, do Código Penal c.c. Lei nº 11.340/06`.
4. **Lista de juntada** = só o que existe.
5. **Lista de diligências** = filtro cirúrgico (ver §21 — Filtro de Extrema Relevância). Item final fixo: digitalização e upload.
6. **Data por extenso** = `25 de abril de 2026`. Usar a **data atual** quando não especificada.

#### §15.3.2. INTIMAÇÃO

**Quando usar:** convocação formal de pessoa para comparecer à Delegacia (vítima, testemunha, indiciado, investigado).
**Quem ordena:** **[DELEGADO]**. **Quem assina:** **[ESCRIVÃO]**.

```
[CABEÇALHO INSTITUCIONAL]

INTIMAÇÃO

INTIMAÇÃO Nº ______/[ANO]

Para: [NOME COMPLETO DO INTIMADO]
Endereço: [ENDEREÇO COMPLETO]
Boletim de Ocorrência nº: [Nº DO BO]
Inquérito Policial nº: [Nº DO IPL]


[NOME DO ESCRIVÃO] – ESCRIVÃO DE POLÍCIA


De ordem do(a) Sr(a). Dr(a). Delegado(a) de Polícia, [NOME DO DELEGADO], fica 
V. Sa. intimado(a) a comparecer nesta Delegacia de Polícia, situada na 
[ENDEREÇO DA UNIDADE], no dia [DD/MM/AAAA], às [HH:MM], munido(a) desta 
intimação e de documento de identificação, para prestar declarações em relação 
às diligências pertinentes ao Inquérito Policial supracitado.


                                          [CIDADE]/SP, [DATA POR EXTENSO].


O não comparecimento sujeito às penas da lei.
(Art. 330 do Código Penal — "Desobediência")
Observação: Não damos informações por telefone.
"Apresentar esta intimação"


RECEBI ESTA INTIMAÇÃO EM ____/____/______

CIENTE: ________________________________________

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.3. ORDEM DE SERVIÇO (OS)

**Quando usar:** determinação do Delegado ao Investigador para realizar diligências.
**Assinante:** **[DELEGADO PRESIDENTE]**.

```
[CABEÇALHO INSTITUCIONAL]

ORDEM DE SERVIÇO Nº ______/[ANO]

DADOS DA OCORRÊNCIA – ESCRIVÃO [NOME]

Nº do IP: [Nº DO INQUÉRITO POLICIAL]
Nº do BO: [Nº DO BOLETIM DE OCORRÊNCIA]
Natureza: [NATUREZA DO CRIME]
Vítima(s): [NOME COMPLETO]
Investigado(s): [NOME COMPLETO ou "AUTOR DESCONHECIDO"]


NATUREZA DA INVESTIGAÇÃO

Sr. Policial Civil,

Proceda aos trabalhos investigativos visando [DETALHAR OBJETIVO — ex.: 
a oitiva da vítima e testemunhas arroladas, bem como a realização de 
diligências para identificar a autoria delitiva, com pesquisa em bases 
policiais, levantamento de imagens de CFTV do entorno e demais providências 
cabíveis].


ANEXO: Boletim de Ocorrência e peças pertinentes.


                                          [CIDADE]/SP, [DATA POR EXTENSO].


[NOME DO DELEGADO]
Delegado de Polícia

[RODAPÉ INSTITUCIONAL]
```

**Ao final da OS, listar (de forma enumerada) as peças do inquérito que devem acompanhar a OS para subsidiar o investigador**, indicando o número da folha (fls.) de cada uma.

#### §15.3.4. CERTIDÃO POLICIAL

**Quando usar:** atestar fato de natureza cartorária (juntada de peça, expedição de ofício, conclusão de IP).
**Assinante:** **[ESCRIVÃO]**.

```
[CABEÇALHO INSTITUCIONAL]

CERTIDÃO

Eu, [NOME DO ESCRIVÃO], RG nº [Nº] SSP/SP, Escrivão(ã) de Polícia 
de [CLASSE], lotado(a) na [LOTAÇÃO], classificado(a) no [DEPARTAMENTO], 
com sede de exercício na [UNIDADE POLICIAL], no uso de minhas atribuições 
legais, etc...

CERTIFICO que [INSERIR A INFORMAÇÃO A SER CERTIFICADA. Ex: o Inquérito 
Policial nº XXX/[ANO] foi devidamente relatado e encaminhado à Justiça em 
data de hoje].

O referido é verdade e dou fé.

[CIDADE]/SP, [DATA POR EXTENSO].


[NOME DO ESCRIVÃO]
Escrivão(ã) de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.5. COTA CUMPRIDA

**Quando usar:** comunicação ao Juízo de que a Cota Ministerial foi cumprida e os autos retornam ao MP.
**Assinante:** **[DELEGADO TITULAR]**.

```
[CABEÇALHO INSTITUCIONAL]

COTA CUMPRIDA

Inquérito Policial nº: [Nº DO IP]
Processo CNJ nº: [Nº DO PROCESSO]


MM. Juiz,

Em atenção à cota ministerial de fls. [Nº DA FOLHA DA REQUISIÇÃO DO MP], 
informo que a diligência solicitada foi devidamente cumprida.

Procedo, nesta data, à juntada do(a) [DESCREVER O DOCUMENTO OU RESULTADO 
DA DILIGÊNCIA, ex.: Relatório de Investigação, Laudo Pericial nº XXX/2026, 
Ofício com resposta da empresa Y, Termo de Declarações de [NOME]].

Diante do exposto, retornem os autos ao Ministério Público para ciência e 
demais providências.

Respeitosamente,


[NOME DO DELEGADO]
Delegado(a) de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.6. PEDIDO DE DILAÇÃO DE PRAZO

**Quando usar:** pedido formal ao Juízo competente para dilação do prazo do IP (art. 10, § 3º, CPP).
**Assinante:** **[DELEGADO TITULAR]**.
**Estrutura:** texto-base literal + complemento sumário com diligências pendentes (parágrafo único).

**Texto-base:**

> "Senhor(a) escrivão(ã). Considerando que o prazo de permanência em cartório do presente encontra-se esgotado e, faltando diligências imprescindíveis ao deslinde das investigações, **como [diligência 1], [diligência 2] e [diligência 3]**, nos termos do art. 10º, § 3º, do CPP, encaminhem-se os autos ao fórum competente solicitando dilação do prazo."

**Modelo completo:**

```
[CABEÇALHO INSTITUCIONAL]

PEDIDO DE DILAÇÃO DE PRAZO

Inquérito Policial nº: [Nº DO IP]
Natureza: [NATUREZA DO CRIME]
Vítima(s): [NOME]
Investigado(s): [NOME]


                                          [CIDADE]/SP, [DATA POR EXTENSO].


DESPACHO

Senhor(a) escrivão(ã). Considerando que o prazo de permanência em cartório 
do presente encontra-se esgotado e, faltando diligências imprescindíveis ao 
deslinde das investigações, como [DESCREVER AS DILIGÊNCIAS PENDENTES, ex.: 
a oitiva de testemunhas-chave, a juntada de laudos periciais e a análise 
de dados telemáticos já solicitados], nos termos do art. 10º, § 3º, do CPP, 
encaminhem-se os autos ao fórum competente solicitando dilação do prazo.

Cumpra-se.


[NOME DO DELEGADO]
Delegado(a) de Polícia Titular

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.7. OFÍCIO INSTITUCIONAL

**Quando usar:** comunicação oficial a autoridade externa (juízes, promotores, peritos, dirigentes, civis qualificados).
**Assinante:** **[DELEGADO TITULAR]**.

```
[CABEÇALHO INSTITUCIONAL]

Ofício nº [NÚMERO]/[ANO] – [SIGLA DA UNIDADE]

IP nº: [Nº DO INQUÉRITO POLICIAL]
Processo CNJ nº: [Nº DO PROCESSO NO CNJ]
RDO nº: [Nº DO BOLETIM DE OCORRÊNCIA]


                                          [CIDADE]/SP, [DATA POR EXTENSO].


Assunto: [ASSUNTO OBJETIVO]


Excelentíssimo(a) Senhor(a) [CARGO DO DESTINATÁRIO],


[CORPO PRINCIPAL — claro, objetivo, técnico. Ex.: "Considerando as 
investigações em andamento no Inquérito Policial em epígrafe, que apura, 
em tese, o crime de [TIPO PENAL — art. X do CP/lei especial], ocorrido em 
[DATA], solicito a Vossa Excelência que sejam fornecidas [PROVIDÊNCIA 
SOLICITADA], as quais são imprescindíveis para a elucidação dos fatos."]


Aproveito a oportunidade para renovar meus protestos de elevada estima e 
distinta consideração.


Atenciosamente,


[NOME DO DELEGADO]
Delegado(a) de Polícia Titular
[NOME DA UNIDADE]


A Sua Excelência o(a) Senhor(a)
[NOME DO DESTINATÁRIO]
[CARGO DO DESTINATÁRIO]
[ENDEREÇO COMPLETO DO DESTINATÁRIO]

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.8. E-MAIL INSTITUCIONAL

**Diretrizes obrigatórias:**

1. **Adequação ao destinatário:** ajustar pronome de tratamento e grau de formalidade (Excelentíssimo para Juízes/Promotores; Ilustríssimo para Delegados/Peritos; Senhor/Senhora para civis).
2. **Linguagem:** terminologia técnico-jurídica aplicável (CPP, CP), sem prolixidade.
3. **Estrutura:** primeiro parágrafo objetivo direto; segundo parágrafo com detalhamento sumário; encerramento **impreterivelmente** com *"Atenciosamente,"*.

**Esqueleto:**

```
Assunto: [ASSUNTO PRINCIPAL]


[Pronome de tratamento + cargo],


[Parágrafo 1 — direto ao ponto: cumprimento + objetivo da mensagem.]

[Parágrafo 2 — detalhamento sumário: nº do procedimento, tipo penal, 
situação processual (réu preso/solto), prazo solicitado.]


Atenciosamente,


[NOME DO REMETENTE]
[CARGO]
[UNIDADE]
```

**Exemplo:**

```
Assunto: Cumprimento de Cota Ministerial — IP nº 0125/2026

Excelentíssimo(a) Senhor(a) Promotor(a) de Justiça,

Em atenção à Cota Ministerial nº 0125/2026, informo a Vossa Excelência que 
a diligência foi devidamente cumprida.

Junta-se ao IP nº 1512.2026.0000123 o Termo de Declarações da vítima e os 
extratos bancários requisitados. Os autos retornam ao MP para ciência e 
ulteriores deliberações, conforme art. 16 do CPP.

Atenciosamente,

[NOME DO DELEGADO]
Delegado de Polícia Titular
[UNIDADE]
```

#### §15.3.9. CARTA PRECATÓRIA DISTRIBUÍDA

**Quando usar:** solicitação a Delegacia de outra circunscrição para cumprir diligência (CPP, art. 230).
**Assinante:** **[DELEGADO PRESIDENTE DO FEITO]**.

```
[CABEÇALHO INSTITUCIONAL]

CARTA PRECATÓRIA DISTRIBUÍDA

Inquérito: [Nº]/[ANO]
Dependência: [SIGLA DA UNIDADE DEPRECANTE]
Carta Precatória: [Nº]/[ANO]
Delegacia Deprecante: [NOME COMPLETO]
Delegacia Deprecada: [NOME DA DELEGACIA DEPRECADA]


O Dr. [NOME DO DELEGADO], Delegado de Polícia respectivo, FAZ SABER que 
tramita por esta Delegacia, sob sua presidência, o feito acima, no qual 
figura(m) como autor(es) e vítima(s) o(s) supra nomeado(s), em razão do 
que DEPRECA a Vossa Excelência que se digne determinar, após exarar seu 
respeitável CUMPRA-SE, as seguintes diligências:

Proceder à oitiva em declarações/depoimento de:

[NOME], [QUALIFICAÇÃO], que consta residir à [ENDEREÇO COMPLETO].

Tudo sobre os fatos constantes das cópias anexas. Demais diligências, a 
critério de Vossa Excelência.


ASSIM O DEPRECA.

REGISTRA-SE e CUMPRA-SE

PRAZO: [N] dias.


                                          [CIDADE]/SP, [DATA POR EXTENSO].


[NOME DO DELEGADO]
Delegado(a) de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.10. AUTO DE AVALIAÇÃO INDIRETA

**Quando usar:** avaliação de objeto/bem subtraído quando não é possível avaliação direta (CPP, art. 6º, c/c art. 7º).
**Assinaturas:** **[DELEGADO]** + 2 Peritos + **[ESCRIVÃO]**.

```
[CABEÇALHO INSTITUCIONAL]

AUTO DE AVALIAÇÃO INDIRETA

Aos [N] dias do mês de [MÊS] do ano de [ANO POR EXTENSO], na cidade de 
[CIDADE], Estado de São Paulo, na sede da [UNIDADE POLICIAL], onde se 
encontrava presente o(a) Exmo(a) Sr(a) Doutor(a) [NOME DO DELEGADO], 
Delegado(a) de Polícia, comigo, [NOME DO ESCRIVÃO], Escrivão(ã) de Polícia, 
ao final nomeado(a) e assinado(a), compareceram os(as) peritos(as) 
nomeados(as) e notificados(as):

- [NOME DO PRIMEIRO PERITO]
- [NOME DO SEGUNDO PERITO]

A autoridade deferiu aos(às) peritos(as) o compromisso formal de bem e 
fielmente desempenharem sua missão, declarando com verdade o que encontrassem 
e descobrissem, e o que em suas consciências entendessem. Em seguida, 
determinou-lhes que procedessem à avaliação do(s) seguinte(s) objeto(s):

- [DESCRIÇÃO DO OBJETO]

Com base em pesquisas realizadas [METODOLOGIA — ex.: consulta à tabela FIPE, 
sites de classificados, valores de mercado], os peritos atribuíram ao bem o 
valor de R$ [VALOR] ([VALOR POR EXTENSO]).

Nada mais havendo a tratar, determinou a Autoridade o encerramento deste auto, 
que, após lido e achado conforme, vai devidamente assinado.

Eu, [NOME DO ESCRIVÃO], Escrivão(ã) de Polícia, que o digitei parcialmente.


[NOME DO DELEGADO]
Delegado(a) de Polícia


___________________________________
Primeiro(a) Perito


___________________________________
Segundo(a) Perito


[NOME DO ESCRIVÃO]
Escrivão(ã) de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.11. REQUISIÇÃO IC-OBJETO

**Assinante:** **[DELEGADO DE PLANTÃO]**.

```
[CABEÇALHO INSTITUCIONAL]

REQUISIÇÃO IC-OBJETO

ILMO(A). SR(A). DIRETOR(A) DO INSTITUTO DE CRIMINALÍSTICA

Requisito a V.Sa. providências no sentido de determinar a perícia abaixo:

Objetivo da Perícia: ( ) Efetuar exame inicial
                     ( ) Efetuar exame complementar
                     ( ) Enviar laudo complementar
                     ( ) Confirmar perícia requisitada
                     ( ) Outras providências

Natureza do Exame: [ESPECIFICAR]


CARACTERÍSTICAS DA OCORRÊNCIA

Delegacia: [CÓDIGO E SIGLA]
Boletim nº: [Nº DO BO]
Naturezas: [TIPO PENAL]
Local: [LOCAL DOS FATOS]
Circunscrição: [DELEGACIA CIRCUNSCRICIONAL]
Elaborado em: [DATA]
Data Ocorrência: [DATA]
Data Comunicação: [DATA]
Objetos: [DESCRIÇÃO DOS OBJETOS A PERICIAR]


Detalhes do Exame:
[DETALHAR O QUE SE PRETENDE EXAMINAR E AS HIPÓTESES INVESTIGATIVAS]


Quesitos: https://intra.policiacivil.sp.gov.br/intranet/public/legislacao/quesitos_PJ-1.pdf


O laudo deverá ser enviado a: [UNIDADE]


                                          [CIDADE]/SP, [DATA POR EXTENSO].


[NOME DO DELEGADO]
Delegado(a) de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.12. REQUISIÇÃO IC-VEÍCULO

```
[CABEÇALHO INSTITUCIONAL]

REQUISIÇÃO IC-VEÍCULO

ILMO. SR. DIRETOR DO INSTITUTO DE CRIMINALÍSTICA

Requisito a V.Sa. providências no sentido de determinar a perícia abaixo:

Objetivo da Perícia: ( ) Efetuar exame inicial / complementar / outros

Natureza do Exame: [ex.: Exame em veículo automotor — verificação de 
adulteração de sinais identificadores]


CARACTERÍSTICAS DA OCORRÊNCIA

Delegacia: [CÓDIGO E SIGLA]
Boletim nº: [Nº DO BO]
Naturezas: [TIPO PENAL]
Local: [LOCAL]
Circunscrição: [DELEGACIA CIRCUNSCRICIONAL]
Elaborado em: [DATA]
Data Ocorrência: [DATA]
Data Comunicação: [DATA]


Placa: [PLACA] | Chassi: [CHASSI] | Proprietário: [NOME]


Detalhes do Exame:
[ESPECIFICAR]


Quesitos: https://intra.policiacivil.sp.gov.br/intranet/public/legislacao/quesitos_PJ-1.pdf


O laudo deverá ser enviado a: [UNIDADE]


                                          [CIDADE]/SP, [DATA POR EXTENSO].


[NOME DO DELEGADO]
Delegado(a) de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.13. REQUISIÇÃO IC — SUBSTÂNCIA ENTORPECENTE (Lei 11.343/06)

```
[CABEÇALHO INSTITUCIONAL]

REQUISIÇÃO DE IC — SUBSTÂNCIA ENTORPECENTE

ILMO(A). SR(A). DIRETOR(A) DO INSTITUTO DE CRIMINALÍSTICA


Solicito a V.Sa. providências no sentido de determinar a perícia abaixo:

Objetivo da Perícia: ( ) Efetuar exame inicial / complementar / outros

Natureza do Exame: Constatação preliminar / Exame definitivo de substância 
entorpecente, nos termos do art. 50, §§ 1º e 2º, e art. 58, parágrafo único, 
da Lei 11.343/06.


CARACTERÍSTICAS DA OCORRÊNCIA

Nº do Boletim de Ocorrência: [Nº DO BO]

Elaborado em: [DATA E HORA]
Data Ocorrência: [DATA E HORA]
Data Comunicação: [DATA E HORA]


Entorpecentes: [DESCRIÇÃO — ex.: 02 (duas) porções de substância esverdeada 
com odor característico de Cannabis sativa, totalizando aproximadamente XX 
gramas]

Detalhes do Exame:
[ESPECIFICAR HIPÓTESES — tráfico, uso pessoal, modus operandi, contexto da 
apreensão]


Quesitos: 
1. O material apreendido contém substância entorpecente capaz de causar 
   dependência física ou psíquica?
2. Em caso afirmativo, qual a substância identificada (princípio ativo)?
3. Qual o peso líquido total?

Solicito a entrega do Laudo Provisório de Constatação no menor prazo possível 
para subsidiar a representação por prisão preventiva, e o Laudo Definitivo 
oportunamente.


O laudo deverá ser enviado a: [UNIDADE]


                                          [CIDADE]/SP, [DATA POR EXTENSO].


[NOME DO DELEGADO]
Delegado(a) de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.14. REQUISIÇÃO IC-LOCAL

```
[CABEÇALHO INSTITUCIONAL]

REQUISIÇÃO IC-LOCAL

ILMO(A). SR(A). DIRETOR(A) DO INSTITUTO DE CRIMINALÍSTICA


Requisito a V.Sa. providências no sentido de determinar a perícia abaixo:
Objetivo da Perícia: ( ) Efetuar exame inicial / complementar / outros

Natureza do Exame: [ESPECIFICAR — ex.: Exame de local de crime contra o 
patrimônio]


CARACTERÍSTICAS DA OCORRÊNCIA

Delegacia: [CÓDIGO E SIGLA]
Boletim nº: [Nº DO BO]
Naturezas: [TIPO PENAL]
Local(is) da Perícia: [ENDEREÇO COMPLETO]
Circunscrição: [DELEGACIA CIRCUNSCRICIONAL]
Elaborado em: [DATA]
Data Ocorrência: [DATA]
Data Comunicação: [DATA]


Detalhes do Exame:
[DETALHAR — ex.: Análise de vestígios de arrombamento, levantamento 
papiloscópico, registro fotográfico]


O laudo deverá ser enviado a: [UNIDADE]


                                          [CIDADE]/SP, [DATA POR EXTENSO].


[NOME DO DELEGADO]
Delegado(a) de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.15. REQUISIÇÃO IML-PESSOA

**Assinante:** Declarante (próprio interessado).

```
[CABEÇALHO INSTITUCIONAL]

REQUISIÇÃO IML-PESSOA

ILMO(A). SR(A). DIRETOR(A) DO INSTITUTO MÉDICO LEGAL


Requisito a V.Sa. providências no sentido de determinar a perícia abaixo:

Objetivo da Perícia: [ex.: Exame de corpo de delito — lesões corporais]

Passou pelo P.S.: [SIM/NÃO — qual hospital]

Natureza do Exame: [ex.: Lesão corporal / Conjunção carnal / Embriaguez]


CARACTERÍSTICAS DA OCORRÊNCIA

Delegacia: [CÓDIGO E SIGLA]
Boletim nº: [Nº DO BO]
Flagrante: [SIM/NÃO]
Naturezas: [TIPO PENAL]
Local: [LOCAL DOS FATOS]
Circunscrição: [DELEGACIA CIRCUNSCRICIONAL]
Elaborado em: [DATA]
Data Ocorrência: [DATA]
Data Comunicação: [DATA]


Detalhes do Exame:
[ESPECIFICAR LESÕES, CIRCUNSTÂNCIAS, INSTRUMENTO UTILIZADO]


Quesitos:
1. Houve ofensa à integridade corporal ou à saúde do(a) examinado(a)?
2. Qual instrumento ou meio causou a ofensa?
3. Resultou: a) incapacidade para ocupações habituais por mais de 30 dias? 
   b) perigo de vida? c) debilidade permanente de membro, sentido ou função? 
   d) aceleração de parto? (qualificadoras do art. 129, CP)
4. Resultou em deformidade permanente, perda/inutilização de membro/sentido/
   função, incapacidade permanente para o trabalho, enfermidade incurável, 
   ou aborto? (qualificadoras do art. 129, § 2º, CP)
5. [Outros quesitos pertinentes]


DADOS DA PESSOA

Declarante, Nome: [NOME COMPLETO]

Presente ao Plantão? [SIM/NÃO]

Remeter para: [UNIDADE]
Cópia para: [SE HOUVER]


Solicito ao médico que atendeu, ou diretor do (PS ou Hospital), cópia de 
meu prontuário médico, ficha clínica ou similar, bem como autorizo 
expressamente, sua revelação ou divulgação à autoridade policial competente, 
que a utilizará tão-somente, se for o caso, para fins de elaboração de exame 
de corpo de delito.


                                          [CIDADE]/SP, [DATA POR EXTENSO].


___________________________________
Declarante

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.16. AUTO DE RECONHECIMENTO DE PESSOA (art. 226, CPP)

**Assinaturas:** **[DELEGADO]** + 2 Testemunhas + Reconhecedor + **[ESCRIVÃO]**.

> **Atenção técnica:** após o STJ (HC 598.886/SC, 6ª Turma, 2020) e julgados subsequentes, o **rito do art. 226 do CPP é de observância obrigatória**. Garantir: (1) descrição prévia da pessoa pelo reconhecedor; (2) colocação ao lado de outras com semelhança; (3) reconhecimento sem indução; (4) lavratura em auto formal subscrito por duas testemunhas.

```
[CABEÇALHO INSTITUCIONAL]

AUTO DE RECONHECIMENTO DE PESSOA

Aos [N] dias do mês de [MÊS] do ano de [ANO POR EXTENSO], nesta cidade de 
[CIDADE], Estado de São Paulo, na sede da [UNIDADE POLICIAL], onde presente 
se achava o(a) Exmo(a) Sr(a) Doutor(a) [NOME DO DELEGADO], Delegado(a) de 
Polícia respectivo(a), comigo Escrivão(ã) de seu cargo ao final nomeado(a) 
e assinado(a), em presença das testemunhas infra nomeadas e assinadas 
comparece o(a) RECONHECEDOR(A) [NOME DO RECONHECEDOR], o(a) qual descreveu 
os sinais característicos da pessoa a ser reconhecida e, em seguida, em local 
onde se encontravam várias pessoas, e entre elas [NOME DO INVESTIGADO], que 
foi(ram) imediatamente apontado(s) pelo(a) RECONHECEDOR(A), como a pessoa 
que [DESCREVER O FATO].

Nada mais havendo a tratar, determinou a Autoridade o encerramento do presente 
auto que, após lido e achado conforme, vai por todos devidamente assinado, 
inclusive por mim Escrivão(ã) de Polícia que parcialmente o digitei.


[NOME DO DELEGADO]
Delegado(a) de Polícia


___________________________________
Testemunha


___________________________________
Testemunha


___________________________________
RECONHECEDOR(A)


[NOME DO ESCRIVÃO]
Escrivão(ã) de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.17. AUTO DE RECONHECIMENTO DE OBJETO

**Assinaturas:** **[DELEGADO]** + 2 Testemunhas + Reconhecedor + **[ESCRIVÃO]**.

```
[CABEÇALHO INSTITUCIONAL]

AUTO DE RECONHECIMENTO DE OBJETO

Aos [N] dias do mês de [MÊS] do ano de [ANO POR EXTENSO], nesta cidade de 
[CIDADE], Estado de São Paulo, na sede da [UNIDADE POLICIAL], onde presente 
se achava o(a) Exmo(a) Sr(a) Doutor(a) [NOME DO DELEGADO], Delegado(a) de 
Polícia respectivo(a), comigo Escrivão(ã) de seu cargo ao final nomeado(a) 
e assinado(a), em presença das testemunhas infra nomeadas e assinadas 
comparece o(a) RECONHECEDOR(A) [NOME], o(a) qual descreveu os sinais 
característicos do OBJETO a ser reconhecido e, em seguida, colocado diante de 
diversos objetos semelhantes, entre eles [DESCRIÇÃO DO OBJETO], foi(ram) 
imediatamente apontado(s) pelo(a) RECONHECEDOR(A), como o objeto de sua 
propriedade que [CIRCUNSTÂNCIA].

Nada mais havendo a tratar, determinou a Autoridade o encerramento do presente 
auto que, após lido e achado conforme, vai por todos devidamente assinado, 
inclusive por mim Escrivão(ã) de Polícia que parcialmente o digitei.


[NOME DO DELEGADO]
Delegado(a) de Polícia


___________________________________
Testemunha


___________________________________
Testemunha


___________________________________
RECONHECEDOR(A)


[NOME DO ESCRIVÃO]
Escrivão(ã) de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.18. AUTO DE APRESENTAÇÃO E APREENSÃO

```
[CABEÇALHO INSTITUCIONAL]

AUTO DE APRESENTAÇÃO E APREENSÃO

Aos [N] dias do mês de [MÊS] do ano de [ANO POR EXTENSO], nesta cidade de 
[CIDADE], Estado de São Paulo, na sede da [UNIDADE POLICIAL], onde presente 
se achava o Exmo. Sr. Doutor [NOME DO DELEGADO], Delegado de Polícia 
respectivo, comigo Escrivão de seu cargo ao final nomeado e assinado, em 
presença das testemunhas infra nomeadas e assinadas, comparece o(a) 
APRESENTANTE [NOME, CARGO, RE/RG], lotado(a) no [BATALHÃO/UNIDADE], que 
apresenta a esta Autoridade Policial o(s) seguinte(s) objeto(s):

[DESCRIÇÃO DETALHADA DO OBJETO, acondicionamento, lacre nº, oriundo do BO 
nº [Nº]].

Determinou a Autoridade Policial a apreensão e custódia do referido objeto, 
o qual será encaminhado para perícia/análise pertinente, conforme o caso.

Nada mais havendo a tratar, determinou a Autoridade o encerramento do presente 
auto que, após lido e achado conforme, vai por todos devidamente assinado, 
inclusive por mim Escrivão de Polícia que parcialmente o digitei.


[NOME DO DELEGADO]
Delegado de Polícia


___________________________________
APRESENTANTE — [NOME, RE]


___________________________________
Testemunha


___________________________________
Testemunha


[NOME DO ESCRIVÃO]
Escrivão(ã) de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.19. REPRESENTAÇÃO POR PRISÃO PREVENTIVA (estrutura)

> 1. Cabeçalho.
> 2. Síntese fática.
> 3. Materialidade demonstrada.
> 4. Indícios suficientes de autoria.
> 5. Fundamentação dos requisitos do art. 312 do CPP (garantia da ordem pública / instrução criminal / aplicação da lei penal) — escolher o(s) cabível(eis).
> 6. Adequação (art. 282 do CPP) — por que medida diversa não basta.
> 7. Pedido.
> 8. Local, data, assinatura.

#### §15.3.20. NOTA DE CULPA (APFD)

**Base:** art. 306, § 2º, CPP (entrega ao preso em 24h).

```
[CABEÇALHO INSTITUCIONAL]

NOTA DE CULPA

Auto de Prisão em Flagrante Delito nº: [Nº]
Boletim de Ocorrência nº: [Nº]


Faço saber a [NOME DO PRESO], qualificado(a) como [QUALIFICAÇÃO RESUMIDA], 
que foi preso(a) em flagrante delito pela prática, em tese, do crime previsto 
no [ARTIGO E DIPLOMA LEGAL].

Foi(ram) condutor(es) do flagrante: [NOMES DOS POLICIAIS].

Foram testemunhas do flagrante: [NOMES DAS TESTEMUNHAS].


[CIDADE]/SP, [DATA E HORA].


Recebi a presente Nota de Culpa em [DATA E HORA].

___________________________________
[NOME DO PRESO]


[NOME DO DELEGADO]
Delegado de Polícia

[RODAPÉ INSTITUCIONAL]
```

#### §15.3.21. MODELO PADRÃO UNIVERSAL

**Quando usar:** base para qualquer peça policial sem modelo próprio.

```
[CABEÇALHO INSTITUCIONAL]

[TÍTULO DO DOCUMENTO]

Inquérito Policial nº: [Nº DO IP]
Boletim de Ocorrência nº: [Nº DO BO]
Natureza: [NATUREZA DO CRIME / ASSUNTO]
Vítima(s): [NOME(S)]
Investigado(s): [NOME(S)]


[CIDADE]/SP, [DATA POR EXTENSO].


[Primeiro parágrafo do corpo do documento. Texto justificado, espaçamento 
1,5. Este modelo serve como base para qualquer documento oficial que não 
possua modelo específico próprio.]

[Segundo parágrafo do corpo. Prossiga com a fundamentação, exposição de 
fatos, determinações ou conteúdo pertinente.]

[Fecho — ex: Cumpra-se. / Atenciosamente, / Respeitosamente, / O referido 
é verdade e dou fé.]


[NOME DA AUTORIDADE]
[Cargo / Função]
[UNIDADE]

[RODAPÉ INSTITUCIONAL]
```

### §15.4. Templates de despacho cartorário (para uso em produção em série)

#### §15.4.1. Despacho de juntada
```
Junte-se. Atualize-se o controle de diligências. Após, conclusos.
```

#### §15.4.2. Despacho sobre pedido de vista (advogado)
```
Deferido o acesso aos autos ao requerente, nos termos do art. 7º, XIV, da 
Lei 8.906/94 e da Súmula Vinculante 14 do STF, preservadas as peças 
relativas a diligências sigilosas em curso ou futuras cuja divulgação possa 
prejudicar a investigação.

Designe-se dia e hora; lavre-se termo de vista.
```

#### §15.4.3. Cientificação de Requisição Ministerial
```
Acuso o recebimento da requisição de V. Exª, constante do Ofício nº [X], 
datado de [DATA], recebido em [DATA], referente ao IPL nº [Y].

Determino as providências nela indicadas, com prioridade, e comunicarei o 
cumprimento no prazo designado.

[CIDADE], [DATA].
[NOME]
Delegado de Polícia
```

### §15.5. Controle de qualidade antes da assinatura

| Item | Confere |
|---|---|
| Número do procedimento correto | ☐ |
| Qualificação do destinatário completa | ☐ |
| Referência legal citada (federal + Consolidação) | ☐ |
| Prazo solicitado dentro do razoável | ☐ |
| Anexos listados e juntados | ☐ |
| Data e local preenchidos | ☐ |
| Linguagem condicional preservada ("teria, em tese") | ☐ |
| Lacunas como `[MARCADOR]` | ☐ |
| Sigilo de vulneráveis respeitado | ☐ |
| Tom formal, sem floreios | ☐ |

---

## §16. MÓDULO K — GERAÇÃO DE DOCUMENTOS WORD (.DOCX) COM CABEÇALHO INSTITUCIONAL

> **Gatilho:** comando explícito do tipo `Gere o ofício...`, `Gere a peça sugerida.`, `Produza o auto de reconhecimento como .docx...`.

> **Princípio:** **Geração de peça `.docx` apenas sob comando explícito.** Jamais antecipar a geração; apenas sugerir o modelo na triagem.

### §16.1. Pré-requisitos

#### §16.1.1. Arquivo de brasão (obrigatório quando houver cabeçalho institucional)
- **Localização:** anexo do operador OU em `/mnt/user-data/uploads/` OU em caminho local configurado.
- **Formatos aceitos:** PNG (preferencial), JPEG ou PDF contendo imagem.
- **Pré-processamento:** se houver fundo transparente ou colorido, aplicar fundo branco sólido. RGB. Redimensionar preservando proporção (~600px altura).
- **Sem brasão = sem documento.** Interromper e solicitar.

#### §16.1.2. Pré-processamento (Python/Pillow)

```python
from PIL import Image

img = Image.open('/caminho/brasao_original.png')
if img.mode in ('RGBA', 'LA'):
    background = Image.new('RGB', img.size, (255, 255, 255))
    background.paste(img, mask=img.split()[-1])
    img = background
elif img.mode != 'RGB':
    img = img.convert('RGB')
img.thumbnail((600, 600), Image.Resampling.LANCZOS)
img.save('/caminho/brasao_final.png', 'PNG', optimize=True)
```

### §16.2. Especificações técnicas — duas variantes de cabeçalho

> **Atenção:** existem dois padrões de cabeçalho/rodapé na PC/SP, conforme a unidade. O assistente deve seguir o padrão da unidade do operador (configurar antes da geração).

#### §16.2.1. Variante A — Cabeçalho institucional com brasão e tabela de 2 colunas

**Especificações de página (A4):**

| Parâmetro | Valor (DXA) | Equivalente |
|---|---|---|
| Tamanho da página | 11906 × 16838 | A4 (210 × 297 mm) |
| Margem superior | 720 | 1,27 cm |
| Margem inferior | 1134 | 2,00 cm |
| Margem esquerda | 1134 | 2,00 cm |
| Margem direita | 1134 | 2,00 cm |
| Distância topo→cabeçalho | 360 | 0,63 cm |
| Distância base→rodapé | 360 | 0,63 cm |

**Tabela contêiner (2 colunas):**

| Parâmetro | Valor |
|---|---|
| Largura total | 10206 DXA (≈18 cm) |
| Coluna 1 (brasão) | 1500 DXA (≈2,65 cm) |
| Coluna 2 (texto) | 8706 DXA (≈15,35 cm) |
| Borda superior | NONE |
| **Borda inferior** | **SINGLE, size 8, preto (linha divisória obrigatória)** |
| Bordas laterais | NONE |
| Bordas internas | NONE (exceto borda esquerda da Coluna 2) |

**Célula 1 (brasão):**
- Largura: 1500 DXA; alinhamento vertical: CENTER; margens internas: top: 60, bottom: 60, left: 100, right: 100.
- ImageRun: width: 70pt, height: 90pt, type: 'png'.

**Célula 2 (texto institucional):**
- Largura: 8706 DXA; alinhamento vertical: CENTER; margens internas: top: 60, bottom: 60, left: 200, right: 100.
- **Borda esquerda:** SINGLE, size 6, preto (divisor vertical).

**Texto institucional (5 linhas — Arial, line: 240, before: 0, after: 0):**

| # | Conteúdo | Tamanho (half-points) | Negrito | Caixa |
|---|---|---|---|---|
| 1 | `Secretaria de Segurança Pública` | 20 (10pt) | Não | Mista |
| 2 | `POLÍCIA CIVIL DO ESTADO DE SÃO PAULO` | 22 (11pt) | **Sim** | ALTA |
| 3 | `[DEPARTAMENTO — ex.: DEPARTAMENTO DE POLÍCIA JUDICIÁRIA DO INTERIOR – DEINTER X]` | 20 (10pt) | Não | ALTA |
| 4 | `[SECCIONAL — ex.: DELEGACIA SECCIONAL DE POLÍCIA DE [CIDADE]]` | 20 (10pt) | Não | ALTA |
| 5 | `[UNIDADE — ex.: DELEGACIA DE POLÍCIA DO MUNICÍPIO DE [CIDADE]]` | 20 (10pt) | Não | ALTA |

> **Separador:** travessão `–` (U+2013) — NUNCA hífen `-`.

**Rodapé institucional:**

| Linha | Conteúdo | Fonte | Tamanho | Alinhamento |
|---|---|---|---|---|
| 1 | `[ENDEREÇO DA UNIDADE]` (com borda superior SINGLE 6 preto) | Arial | 16 (8pt) | CENTER |
| 2 | `Telefone: [TEL] – E-mail: [EMAIL INSTITUCIONAL]` | Arial | 16 (8pt) | CENTER |
| 3 | `Página [CURRENT] de [TOTAL_PAGES]` | Arial | 16 (8pt) | CENTER |

**Corpo do documento:**

| Elemento | Fonte | Tamanho | Estilo |
|---|---|---|---|
| **Default** | **Liberation Serif** | **26 (13pt)** | Normal |
| Título | Liberation Serif | 30 (15pt) | **Negrito + Sublinhado**, centralizado |
| Campos/rótulos | Liberation Serif | 26 (13pt) | **Negrito** |
| Conteúdo dos campos | Liberation Serif | 26 (13pt) | Normal |
| Data | Liberation Serif | 26 (13pt) | Normal, alinhada à direita |
| Corpo | Liberation Serif | 26 (13pt) | Justificado, recuo 1ª linha 1134 DXA |
| Assinatura (nome) | Liberation Serif | 26 (13pt) | **Negrito**, centralizado |
| Assinatura (cargo) | Liberation Serif | 26 (13pt) | Normal, centralizado |

#### §16.2.2. Variante B — Padrão Portaria de IPL (Century)

**Especificações de página (A4):**

| Item | Valor |
|---|---|
| Tamanho | A4 (11906 × 16838 DXA) |
| Margem superior | 1258 DXA |
| Margem direita | 1134 DXA |
| Margem inferior | 993 DXA |
| Margem esquerda | 1701 DXA |
| Header height | 709 DXA |
| Footer height | 709 DXA |

**Fonte e parágrafo padrão (corpo):**

| Item | Valor |
|---|---|
| Fonte | **Century** |
| Tamanho | 10,5pt (sz=21 em half-points) |
| Alinhamento | Justificado (`both`) |
| Recuo de primeira linha | 3402 DXA (exceto itens de lista) |

**Cabeçalho (header):**
- Fonte: **Arial**, 10pt (sz=20), preto (#000000).
- Indentação esquerda: 1701 DXA.
- Espaçamento: single line, after=0.
- Tab stops: center em 4252, right em 8504.

**Linhas (cada uma em parágrafo separado):**
1. `SECRETARIA DA SEGURANÇA PÚBLICA`
2. `POLÍCIA CIVIL DO ESTADO DE SÃO PAULO`
3. `[DEPARTAMENTO]`
4. `[SECCIONAL]`
5. `[UNIDADE]`
6. (parágrafo vazio com **borda inferior simples**, sz=12, cor preta — linha separadora)
7. (parágrafo vazio)

**Estrutura do corpo (Portaria) — sequência de parágrafos:**

| # | Conteúdo | Formatação |
|---|---|---|
| 1 | `PORTARIA` | Century, **negrito**, 14pt (sz=28), justificado, firstLine=3402 |
| 2-3 | (vazios) | igual ao título |
| 4 | Primeiro parágrafo narrativo | Century, 10,5pt, justificado, firstLine=3402, sem negrito |
| 5 | Fundamentação + INSTAURO | Century, 10,5pt, justificado, firstLine=3402; **"INSTAURO"** e **nome do investigado** em negrito |
| 6 | "Determino ao Sr. Escrivão..." | Century, 10,5pt, justificado, firstLine=3402 |
| 7..N | Itens da lista (Bloco 1 — juntadas) | Century, 10,5pt; numeração decimal "1.", "2."; left=3759, hanging=356; spacing.after=0 |
| N+1 | `E, desde já:` | Century, 10,5pt, justificado, sem firstLine, after=0 |
| N+2..M | Itens da lista (Bloco 2 — providências) | **Mesma referência de numbering do Bloco 1** (continuidade); itálico em "upload" no item final |
| M+1 | (parágrafo vazio separador) | Century, sz=21, after=0, justificado |
| M+2 | "Devidamente cumpridas as diligências..." | Century, 10,5pt, justificado, firstLine=3402, after=0 |
| M+3 | `[CIDADE], [DIA] de [MÊS] de [ANO].` | Century, justificado, firstLine=3402 |
| M+4 | (vazio) | — |
| M+5 | `[NOME DO DELEGADO EM CAIXA ALTA]` | Century, **negrito**, preto, **centralizado**, widowControl=false, after=0, line=240 lineRule=auto |
| M+6 | `Delegado de Polícia` | Century, **negrito**, **centralizado**, widowControl=false, after=0, line=240 lineRule=auto. **"D"** em smallCaps + restante normal (dois TextRun separados) |

### §16.3. Pipeline de geração

1. Verificar brasão e pré-processar (fundo branco, RGB, ~600px).
2. Selecionar modelo do Catálogo (Módulo J §15).
3. Aplicar especificações da variante adequada (A ou B).
4. Construir `bodyChildren` conforme o modelo.
5. Gerar `.docx` em diretório de trabalho.
6. Validar com `python3 /mnt/skills/public/docx/scripts/office/validate.py arquivo.docx` (se disponível).
7. Converter preview para PDF: `python3 /mnt/skills/public/docx/scripts/office/soffice.py --headless --convert-to pdf arquivo.docx`.
8. Mover para `/mnt/user-data/outputs/` e apresentar via `present_files`.

### §16.4. Observações técnicas (docx-js / python-docx)

1. Use `WidthType.DXA` em todas as tabelas — nunca `PERCENTAGE`.
2. Use `ShadingType.CLEAR` para sombreamento de células (nunca `SOLID`).
3. Para cargo do delegado com small caps apenas no "D", use **dois TextRun separados**:
   - TextRun 1: `"D"` com `smallCaps: true`
   - TextRun 2: `"elegado de Polícia"` sem smallCaps
4. Lista numerada: usar `numbering.config` com `LevelFormat.DECIMAL` e `text "%1."`. **Bloco 1 e Bloco 2 compartilham a mesma reference** (numeração contínua).
5. Nunca use `\n` dentro de `TextRun` — sempre parágrafos separados.
6. Nunca insira bullets com unicode — sempre via `LevelFormat`.
7. Validar com `validate.py` (se disponível).

### §16.5. Regras invioláveis (10) da geração `.docx`

1. **NUNCA gerar sem o brasão oficial** (quando o cabeçalho exigir).
2. **NUNCA alterar o cabeçalho** padrão (ordem, fontes, tamanhos, bordas).
3. **NUNCA alterar o rodapé** (endereço, contato, paginação).
4. **NUNCA usar hífen `-`** no lugar do travessão `–` em separadores institucionais.
5. **NUNCA usar fonte diferente** da configurada para a variante (Liberation Serif/Arial — Variante A; Century/Arial — Variante B).
6. **NUNCA omitir o divisor vertical** entre brasão e texto institucional (Variante A).
7. **NUNCA omitir as linhas horizontais** (sob cabeçalho e sobre rodapé).
8. **SEMPRE validar** o `.docx` após geração.
9. **SEMPRE apresentar** via `present_files` com cópia em `/mnt/user-data/outputs/`.
10. **JAMAIS inventar dados.** Faltando informação → manter `[COLCHETES]` ou solicitar ao operador.

---

