# 04 — ERROS E INCONSISTÊNCIAS

> Agente 04 — varredura técnica integral, sem pesquisa jurisprudencial.
> Postura crítica e combativa: cada achado abaixo é um defeito documental que compromete a segurança jurídica da licitação, a precificação da proposta ou a execução do contrato.

> **Observação preliminar de escopo**: o Anexo 1 (corpo do Edital), o Apêndice 1 (Definições do Edital e Contrato), o Manual B3 (Apêndice 5) e os Esclarecimentos (Apêndice 6) constam no repositório APENAS como folhas de rosto (capas). Sem o corpo do Edital e sem o Apêndice de Definições, parte expressiva dos defeitos relatados abaixo só pode ser examinada parcialmente — e a própria ausência desses documentos é o defeito mais grave de todos.

---

## A. REFERÊNCIAS CRUZADAS QUEBRADAS

### A.1. [GRAVE] Cláusula 30.8 do Contrato remete a Anexo errado

**Apêndice 2 — Contrato, cláusula 30.8 (p. 70):**
> "O REGULADOR realizará a avaliação do cumprimento dos INDICADORES DE DESEMPENHO pela CONCESSIONÁRIA, nos termos do ANEXO 5 deste CONTRATO."

**Defeito**: o Sistema de Mensuração do Desempenho está no **ANEXO 4**. O ANEXO 5 é a MATRIZ DE RISCOS (cl. 2.1.5 e 2.1.6).
**Correção**: trocar "ANEXO 5" por "ANEXO 4".

### A.2. [GRAVE] Cláusula 8.4.2 do Contrato remete a Anexo errado

**Cláusula 8.4.2 (p. 9):**
> "atendimento à nota mínima dos INDICADORES DE DESEMPENHO previstos no ANEXO 5 deste CONTRATO, relativos ao ano imediatamente anterior ao da solicitação pela CONCESSIONÁRIA."

**Defeito**: novamente "ANEXO 5" no lugar de "ANEXO 4". Em 20.3(ii) a referência ao mesmo anexo está correta como "ANEXO 4".
**Correção**: trocar "ANEXO 5" por "ANEXO 4".

### A.3. [GRAVE] Cláusula 23.4 remete o Coeficiente de Geração a Anexo errado

**Cláusula 23.4 (p. 51):**
> "Caso constatado [...] que a variação do COEFICIENTE DE GERAÇÃO é inferior a 3% (três por cento) do valor previsto no ANEXO 3 deste CONTRATO, para mais ou para menos, não será realizada qualquer modificação no valor do COEFICIENTE DE GERAÇÃO então vigente."

**Defeito**: o COEFICIENTE DE GERAÇÃO é definido e quantificado no **Apêndice 4-A — Estrutura Tarifária** (item 1.3 e 1.3.1, fórmula `CG = QRes/VFÁgua` e o campo `[●] kg/m3`). O ANEXO 3 (Caderno de Encargos) NÃO traz o CG (verificado via `grep` por "COEFICIENTE DE GERAÇÃO" no Caderno: 0 ocorrências).
**Correção**: trocar "ANEXO 3 deste CONTRATO" por "APÊNDICE 4-A do EDITAL" (ou pelo ANEXO 2 — Proposta Comercial e Estrutura Tarifária da Concessionária —, ajustando a fonte conforme a vontade negocial).

### A.4. [MÉDIO] Cláusula 19.8 e 19.9 invocam rol em subcláusula errada

**Cláusula 19.8 (p. 33):**
> "As eventuais RECEITAS EXTRAORDINÁRIAS não listadas na subcláusula 19.3 [...]"

**Cláusula 19.9 (p. 33):**
> "Para fins das aprovações referidas na subcláusula 19.3, a CONCESSIONÁRIA deverá enviar ao PODER CONCEDENTE [...]"

**Defeito**: o ROL das atividades previamente autorizadas está em **19.4**, não em 19.3. A cláusula 19.3 traz a regra geral de necessidade de autorização prévia "ressalvado o disposto na subcláusula 19.4".
**Correção**: trocar "subcláusula 19.3" por "subcláusula 19.4" em 19.8 e em 19.9.

### A.5. [GRAVE] Numeração interna 20.14 / 20.14.1 / 20.14.2 / 20.19 — caput vem DEPOIS dos subitens

**Cláusulas 20.13–20.19.1 (pp. 40–41):**
```
20.13. [...]
   20.14.1. O percentual anual de inadimplência será apurado pela média aritmética [...]
   20.14.2. O Fator de Inadimplência (FI) [...]
20.14. A inadimplência apurada será enquadrada nas seguintes faixas [...]
20.15. [...]
[...]
20.19.1. Cada Fator de Inadimplência (FI) apurado refletirá exclusivamente [...]
```

**Defeito**: 20.14.1 e 20.14.2 aparecem ANTES do caput 20.14 (com o qual não guardam relação lógica — pelo conteúdo, são subitens de 20.13). E 20.19.1 aparece SEM caput 20.19. A subcláusula 20.18 traz a fórmula final do FI, e o 20.19.1 (não-existente como 20.19 caput) é a regra de não-acumulação. A numeração precisa ser refeita.
**Correção sugerida**: renumerar 20.14.1 → 20.13.1; 20.14.2 → 20.13.2; 20.19.1 → 20.18.1 (ou criar caput 20.19 antes de 20.19.1).

### A.6. [MÉDIO] Cláusula 38.5.1 remete a 38.4 (cálculo) em vez de 38.5 (assunção de contratos)

**Cláusula 38.5 (p. 92):**
> "Em ocorrendo a extinção da CONCESSÃO, o PODER CONCEDENTE poderá [...] assumir os contratos celebrados pela CONCESSIONÁRIA com terceiros [...]"

**Cláusula 38.5.1 (p. 92):**
> "Na impossibilidade de cumprimento do disposto na subcláusula 38.4, em razão de recusa do ente financiador ou qualquer outro motivo, a indenização [...]"

**Defeito**: a "impossibilidade de cumprimento" pela "recusa do ente financiador" diz respeito à assunção dos contratos de financiamento — isto é, à cláusula 38.5, não à 38.4 (que trata do cálculo da indenização pela consultoria especializada).
**Correção**: trocar "subcláusula 38.4" por "subcláusula 38.5" em 38.5.1.

### A.7. [GRAVE] "Error! Reference source not found." em 4 pontos

Erro de campo do Word visível no texto:

- **Anexo 3 — Caderno de Encargos, Tabela 1 (p. 14):** "Implantação e reforma das Unidades de Triagem manual de recicláveis, conforme determinado no capítulo Error! Reference source not found."
- **Anexo 5 — Matriz de Riscos, p. 28, item 68:** "Para fins do disposto neste item Error! Reference source not found. a inadimplência deve ser superior a 12 (doze) meses [...]"
- **Anexo 5 — Matriz de Riscos, p. 29, item 69 (mesma mensagem)**
- **Anexo 5 — Matriz de Riscos, p. 31, item 70 (mesma mensagem)**

**Correção**: substituir o erro pelo identificador correto (o número do próprio item ou da subcláusula do Contrato). Sem isso, o sentido literal de cada item de inadimplência da Matriz fica TRUNCADO.

### A.8. [MÉDIO] Apêndice 4-A remete a "tabela que consta no CADERNO DE ENCARGOS" mas a tabela só nasce do percentual ofertado

**Apêndice 4-A, item 1.6 (p. 3):**
> "1.6. [...] os valores das TARIFAS [...] serão sujeitos a retenção e posterior liberação conforme as porcentagens indicadas na tabela que consta no CADERNO DE ENCARGOS. A cada marco do projeto, a CONCESSIONÁRIA terá acesso a uma porcentagem específica do valor das TARIFAS, começando com [●]% e aumentando progressivamente até atingir 100% da TARIFA, conforme o cumprimento das metas estabelecidas."

**Caderno de Encargos, Tabela 7 (p. 69):**
> "Início da prestação dos SERVIÇOS — 75%; ao atingir as 3 metas conjuntas — 93%; ao atingir 80% de desvio de aterro — 100%."

**Defeito**: o item 1.6 do Apêndice 4-A diz que o ponto de partida é `[●]%` (campo aberto), mas a Tabela 7 do Caderno de Encargos já fixa o valor inicial em **75%** — incompatibilidade textual.
**Correção**: ou (i) preencher `[●]` no Apêndice 4-A com 75% e remover a redação "começando com [●]% e aumentando progressivamente", harmonizando com a Tabela 7, ou (ii) deixar claro que a "tabela" do Caderno é a Tabela 7 e ela vincula.

---

## B. ERROS DE REDAÇÃO E FORMATAÇÃO

### B.1. [GRAVE] Resolução do Consórcio — numeração de incisos pula (de VIII para X)

**Doc. de Suporte — Resolução Tarifária, art. 5 (p. 4):**
```
VI - resíduos que [...]
VII - resíduos de animais mortos [...]
VIII - resíduos de restos de construção;
X - outros que, por sua composição, se enquadrem [...]
XI - resíduos originários do serviço público de limpeza urbana [...]
```

**Defeito**: não existe inciso IX. Imediatamente após VIII vem X.
**Correção**: introduzir um inciso IX ou renumerar X → IX e XI → X. O § 1° refere "incisos I a X" — se mantido o X atual, a contagem fica errada (há somente 10 incisos efetivos, mas a maior numeração é XI).

### B.2. [MÉDIO] Estatuto do Consórcio Pró-Sinos — Cláusula Trigésima-Oitava-D — atribuições numeradas confusas

**Doc. de Suporte — Alteração do Estatuto, art. 38-D (p. 8):**
- Após o inciso VIII vem novamente "VIII" (linha "VIII - manifestar-se sobre conflitos relacionados ao CONTRATO DE PROGRAMA [...]"), seguido de "IX – manifestar-se sobre conflitos relacionados ao contrato de CONCESSÃO" e em seguida de "IX – ratificar a indicação e a destituição de membros da Comissão de Fiscalização" — **dois incisos IX**.
- A linha "IX – manifestar-se [...]" começa após "para sua análise por qualquer dos MUNICÍPIOS integrantes da CONCESSÃO;" e tem texto colado, sem quebra adequada.

**Correção**: renumerar para VIII, IX, X, XI... atribuindo numeração única a cada atribuição.

### B.3. [MÉDIO] Contrato — "FASE 1 - PRÉ-OPERACIONAL" vs "FASE 1 - PRÉ OPERACIONAL"

Cláusula 11.1 usa "PRÉ-OPERACIONAL" (com hífen); cláusulas 11.2, 11.3 e 11.4 usam "PRÉ OPERACIONAL" (sem hífen). Pequeno, mas é defeito redacional. O Caderno de Encargos usa "PRÉ-OPERACIONAL" (item 1.4.1).

### B.4. [MÉDIO] "ORDEM DE EXECUÇÃO" vs "ORDEM DE SERVIÇO" — duas designações no mesmo documento

- Contrato (cláusulas 11.1, 11.6, 17.4.4, 25.1.3, 30.7 etc.): "ORDEM DE EXECUÇÃO".
- Caderno de Encargos:
  - Item 1.4.1 e Tabela 1 (p. 14): "ORDEM DE EXECUÇÃO" e "Ordem de Serviço" (nota de rodapé "1 OS – ORDEM DE SERVIÇO");
  - Item 1.2.40, 5.x: "ORDEM DE SERVIÇO".

**Defeito**: o Caderno define que "OS = ORDEM DE SERVIÇO", mas o Contrato só prevê "ORDEM DE EXECUÇÃO". Trata-se do mesmo ato administrativo? Se sim, padronizar; se não, definir cada um e indicar a relação temporal.

### B.5. [MÉDIO] "RECEITA BRUTA OPERACIONAL" vs "RECEITA OPERACIONAL BRUTA"

- Cláusula 17.4: "RECEITA BRUTA OPERACIONAL"
- Cláusulas 30.14, 35.8.1, 35.8.2, 35.8.3: "RECEITA OPERACIONAL BRUTA"

Provavelmente mesma grandeza. Sem o Apêndice 1 de Definições não é possível confirmar. **Correção**: padronizar.

### B.6. [MÉDIO] "RECEITA ACESSÓRIA" / "RECEITAS ACESSÓRIAS" vs "RECEITAS EXTRAORDINÁRIAS"

- Cláusula 19 do Contrato e cláusula 35.7.2(i): há "RECEITAS EXTRAORDINÁRIAS" e "RECEITAS ACESSÓRIAS" usados como sinônimos. A cláusula 35.7.2(i) (Grupo 2 de infrações) refere "RECEITAS ACESSÓRIAS", quando o Contrato adota como termo-chave "RECEITAS EXTRAORDINÁRIAS".
- Caderno de Encargos, item 2.7.1 (p. 23): "Receitas Acessórias: Apresentação das receitas acessórias pretendidas no início do contrato com a utilização da capacidade instalada [...]" — termo é "RECEITAS ACESSÓRIAS" no Caderno.

**Correção**: padronizar para "RECEITAS EXTRAORDINÁRIAS" em todos os documentos (ou para "RECEITAS ACESSÓRIAS" se a vontade for tratá-las como termo único — a Lei 8.987/1995, art. 11, fala em "fontes provenientes de receitas alternativas, complementares, acessórias ou de projetos associados").

### B.7. [GRAVE] "PRESTADOR DO SERVIÇO DE ÁGUA" vs "PRESTADOR DE SERVIÇOS DE ÁGUA E ESGOTO"

- Apêndice 7 (Convênio): "PRESTADOR DO SERVIÇO DE ÁGUA" (sem esgoto).
- Anexo 7 (Atualização Cadastral): "PRESTADOR DE SERVIÇOS DE ÁGUA E ESGOTO" (com esgoto) — itens 2.2, 2.5, 2.7, 2.10, 2.13.

**Defeito relevante**: a inclusão de "ESGOTO" no Anexo 7 amplia o escopo da contraparte para um serviço (esgotamento sanitário) que NÃO integra a base de cálculo da tarifa (que é o volume de água consumido). Pode confundir municípios atendidos apenas por água ou apenas por esgoto. O Convênio do Apêndice 7 — instrumento operativo — só fala em água.
**Correção**: padronizar para "PRESTADOR DO SERVIÇO DE ÁGUA" em todos os documentos, OU definir expressamente no Apêndice 1 se "água" abrange "esgoto" para fins de cadastro.

### B.8. [BAIXO] Resolução Tarifária usa "SMRSU" / "RSU" / "RDO" — inconsistência conceitual

- A Resolução chama o objeto de "CONCESSÃO DO SMRSU" (art. 1, parte final do CAPÍTULO I) e ainda usa "Manejo de RSU" no cabeçalho de várias páginas.
- Mas o art. 4 da própria Resolução restringe o escopo a "resíduos domésticos até 240 litros ou 60 kg por dia por economia" (= RDO).
- Todos os demais documentos usam "RDO" (Resíduos Domésticos) — Contrato, Caderno, Matriz, Convênio.

**Defeito**: RSU é mais amplo que RDO (RSU = RDO + RLU + resíduos especiais). O título da Resolução cria ambiguidade sobre o objeto da concessão.
**Correção**: substituir todas as ocorrências de "SMRSU" e "RSU" na Resolução por "SMRDO" e "RDO", harmonizando com o restante.

### B.9. [BAIXO] Resolução Tarifária — cabeçalho de páginas oscila entre "RDO" e "RSU"

- Página 1: "Concessão de Serviço Público de Manejo de RDO da Bacia dos Sinos (RS)"
- Páginas 2 a 9: "Concessão de Serviço Público de Manejo de RSU da Bacia dos Sinos (RS)"

Mesmo defeito de B.8.

### B.10. [MÉDIO] Apêndice 4-B — Modelo A com erro de concordância e tipografia

**Apêndice 4-B, modelo A, p. 4:**
> "e) a TARIFA BASE aqui proposta possui viabilidade e é suficientes à recuperação dos custos incorridos [...]"

**Defeito**: "é suficientes" — erro de concordância (devia ser "é suficiente" — singular).

### B.11. [BAIXO] Apêndice 4-A — fórmula desalinhada em PDF

A fórmula `TB = CG × PU` (item 1.3) e a fórmula do FI (Contrato, 20.15 a 20.18) e do FAC (Anexo 7) saem com má formatação no PDF (subscritos baixados, espaços faltantes, parênteses partidos em duas linhas). Embora não altere semanticamente, dificulta a leitura por licitantes não nativos de português.

### B.12. [BAIXO] Apêndice 3 — modelo de Termo de Renúncia à Visita Técnica pula inciso (iii)

**Apêndice 3, item 3 (p. 6):**
> "(i) que tinha a possibilidade de fazer a visita técnica [...]
> (ii) renunciou à realização da VISITA TÉCNICA facultativa;
> (iv) tem pleno conhecimento [...]
> (v) tem total capacidade [...]"

**Defeito**: falta o item (iii).

### B.13. [BAIXO] Cláusula 22.3.3 — "TD = TR * [●%]"

A fórmula da Taxa de Desconto Real Anual deixa o multiplicador `[●%]` em campo aberto, sem unidade clara: se for ad-on percentual sobre a NTNB, deve estar em pontos percentuais; se for multiplicador, deve ser puro. A redação ambígua impede licitantes de modelar o reequilíbrio. **Não é só campo em branco — é fórmula incompleta.**

### B.14. [BAIXO] Cláusula 17.3 — tabela de valores de Conta Verde com TODOS os 30 anos em `[●]`

Toda a tabela de valores anuais a serem depositados na Conta Verde está com `[●]` — sem indicação sequer de ordem de grandeza. Sem isso, é impossível modelar o ônus na proposta comercial.

### B.15. [MÉDIO] Cláusula 7.1 — Valor estimado do contrato em `[•]`

> "O valor estimado deste CONTRATO é de R$ [•], correspondente ao somatório estimado das receitas [...]"

Sem valor estimado, não há referência para a Garantia de Proposta (geralmente percentual do valor estimado), nem para limites de subcontratação, nem para o critério de "vultoso" do art. 6, XXII, da Lei 14.133/2021. **Provavelmente preenchível só na CP; mas crítico para os licitantes.**

---

## C. CAMPOS NÃO PREENCHIDOS — INVENTÁRIO

### C.1. Devem estar definidos no momento da publicação do Edital (críticos)

| Documento | Local | Campo | Por que é crítico |
|---|---|---|---|
| Apêndice 4-A | item 1.2 | `R$ [●] por m³` (TARIFA BASE teto) | Não há teto regulatório explícito sem o valor — embora o Multiplicador K seja a variável de competição, o licitante precisa do TB-teto. |
| Apêndice 4-A | item 1.3.1 | `R$ [●]/kg` para PU e `[●] kg/m³` para CG | Parametriza toda a fórmula da Tarifa. Sem isso a Proposta Comercial fica sem base. |
| Apêndice 4-A | item 1.6 | `[●]%` inicial de liberação | Cf. A.8. Em conflito com Caderno (75%). |
| Apêndice 4-A | item 1.7 | (categorias "Residencial Comum" e "Público" sem FTBi nem FU) | Estrutura tarifária resta abstrata. |
| Resolução do Consórcio | art. 6 § 4° e § 7° | FTBi e FU por categoria, todos `[●]` | Idem. |
| Anexo 7 | item 2.22.1 | Q_modelado por categoria, todos `[●]` | Sem isso o FAC não pode ser calculado. |
| Contrato | cl. 6.1 | "[30 (trinta) anos]" — entre colchetes | Prazo, variável estruturante de toda concessão, ainda não consolidado na minuta. |
| Contrato | cl. 7.1 | `R$ [•]` (valor estimado) | Cf. B.15. |
| Contrato | cl. 8.1 | "Município de [•]" (sede da SPE) | Cláusula 11 do Apêndice 3 (Modelo de Declaração) exige sede em "um dos MUNICÍPIOS do CONSÓRCIO PÚBLICO que integram a CONCESSÃO" — diferente da redação do Contrato. |
| Contrato | cl. 8.3 e 8.3.1 | `R$ [•]` (capital social mínimo) | Eliminatório para habilitação econômica. |
| Contrato | cl. 17.3 | Tabela 30 anos × valores Conta Verde, todos `[●]` | Cf. B.14. |
| Contrato | cl. 22.3.3 | `[●%]` no spread da Taxa de Desconto | Cf. B.13. |
| Contrato | cl. 22.3.3 | "Tesouro IPCA+ [...] com vencimento em [●]" | A NTN-B referencial deve ser fixada. |
| Contrato | cl. 22.11.7 | "[1,3]" e "[4,5]" (gatilhos de cautelares) | Em colchetes — não consolidado. |
| Apêndice 7 | partes "AGÊNCIA REGULADORA [•]" (2 referências) | Quem é o regulador do SMRDO e quem é o regulador do serviço de água? | Cf. tópico G. |
| Anexo 5 | Tabela 7.3 do Caderno (p. 69) — em conjunto, há referência cruzada quebrada | Definição dos percentuais de retenção tem cabeçalho deslocado | Cf. A.8 e A.7. |
| Edital (Apêndice 7 do Contrato — Convênio) | minuta inteira | Várias cláusulas dependem de campos `[•]` da agência reguladora | Cf. tópico G. |
| Contrato, cl. 1.1.9 a 1.1.23 | "Lei Municipal de [Município] nº [•]" — 15 vezes | Sem citar a lei autorizativa, há vício de motivação legal específica. |
| Contrato | cl. 9 a 49 | "Concorrência pública nº [•] / Processo nº [•]" no cabeçalho de TODAS as páginas | Identificação do certame. |

**Contagem aproximada**: ~261 ocorrências de `[•]` e ~12 de `[●]` no Contrato; o Anexo 5 tem ~30; a Resolução tem ~5; o Convênio (Apêndice 7) tem ~40; o Apêndice 3 (Modelos) usa massivamente para preenchimento posterior pelo licitante (legítimo).

### C.2. Legítimo preencher depois (não-críticos)

- Número/data da Concorrência e do Processo.
- Modelos do Apêndice 3 — preenchidos pelo licitante na ocasião.
- "Local", "Data" e dados de representante legal — preenchidos pelo licitante.

---

## D. INCONSISTÊNCIAS ENTRE DOCUMENTOS

### D.1. [GRAVÍSSIMO] Fórmula tarifária — Apêndice 4-A x Resolução do Consórcio

**Apêndice 4-A do EDITAL (modelo monofásico):**
- TMRS calculada "a partir da TARIFA BASE e da média do volume de água consumido" (item 1.1.1).
- TARIFA BASE = `CG × PU`, expressa em R$ por m³ de água consumida (item 1.2 e 1.3).
- Cobrança mínima por consumo: 4 m³ social / 8 m³ residencial e público / 10 m³ comercial; máximo 200 m³ (itens 1.4 e 1.5).
- 4 categorias: Residencial Social, Residencial Comum, Público, Comercial (deduzido do item 1.4).

**Resolução do Consórcio (modelo bifásico TBD + TVU):**
- TMRS = **TBD + TVU** (art. 6, caput).
- TBD = TARIFA BASE × **Fator de Disponibilidade (FTBi)** por categoria (art. 6 § 1°).
- TVU = TARIFA BASE × Volume de água consumido × **Fator de Uso (FU)** por categoria, "incide apenas sobre o consumo que exceder o FTBi" (art. 6 § 6°).
- 4 categorias: Residencial Social, Residencial Comum, Comercial, Pública.

**Defeito**: as duas fórmulas são incompatíveis no modelo de cobrança. A da Resolução cobra "parcela fixa de disponibilidade + parcela variável sobre o excedente" (modelo dual-block clássico); a do Apêndice 4-A cobra uma única tarifa volumétrica com piso e teto.

Pior: o Apêndice 4-A é Anexo do Edital e, conforme a ordem de prevalência da cláusula 3.1.3 do Contrato, prevalece sobre o Caderno de Encargos e sobre a Proposta. A Resolução não está listada na hierarquia interpretativa do Contrato — mas ela é norma habilitante da própria cobrança (art. 9 da Lei 8.987/1995) e foi referenciada como pressuposto do Contrato no Doc. de Suporte e no Contrato de Programa (cláusulas 1.3.2).

**Consequência**: licitantes não sabem qual modelagem aplicar. Sem essa definição, as Propostas Comerciais não são comparáveis. **Risco de impugnação certo.**

**Correção**: optar por um único modelo, eliminar o outro do documento conflitante e ajustar a hierarquia da cláusula 3.1.3 para incluir expressamente a Resolução.

### D.2. [GRAVE] Aterro sanitário próprio — Contrato e Caderno divergem do Caderno

Contrato (cl. 11.9.2): "Na hipótese de construção de aterro sanitário próprio, [...] **não reverterá ao PODER CONCEDENTE**, **não sendo considerado um BEM REVERSÍVEL**."

Caderno de Encargos (item 3.6.3.3): "Caso a CONCESSIONÁRIA opte pela implantação de aterro sanitário próprio, este bem **não será considerado um BEM REVERSÍVEL** para as finalidades previstas no CONTRATO." — consistente.

Caderno de Encargos (item 2.5.2, p. 21): "Após o término do contrato, **todos os bens serão reversíveis ao PODER CONCEDENTE, exceto o novo aterro sanitário**, caso seja construído pela CONCESSIONÁRIA. O Ente Público não assumirá os custos de monitoramento e manutenção do novo aterro sanitário após o término do contrato de concessão [...]" — consistente.

**Mas no item 1.1.4 (Diretrizes Gerais, p. 5):** "Destinação Adequada de Subprodutos: qualquer tecnologia implantada pela CONCESSIONÁRIA deverá prever utilização dos subprodutos como composto, digestato, recicláveis, biogás, CDR e energia, **sendo vedada a disposição final em aterro**."

**Defeito**: o item 1.1.4 do Caderno proíbe disposição final em aterro, mas vários outros itens (1.3.2.g, 1.3.2.h, 3.6.3) tratam o aterro como destinação prevista. A vedação do 1.1.4 é absoluta em sua redação, o que tornaria sem sentido o capítulo 3.6.3.

**Correção**: a vedação no item 1.1.4 deveria ser "vedada a disposição final, em aterro, de subprodutos passíveis de aproveitamento" — ou seja, a vedação refere-se aos subprodutos (composto, digestato, recicláveis, biogás, CDR, energia), não aos rejeitos finais não aproveitáveis.

### D.3. [GRAVE] Lista de municípios — Contrato/Resolução vs. Estatuto

- Contrato (cl. 8, capa e considerandos), Resolução Tarifária, Apêndice 4-A, Apêndice 4-B, Anexo 3, Caderno de Encargos, Apêndice 7, Anexo 7 e Contrato de Programa: 15 municípios.
- Estatuto do Consórcio (Doc. de Suporte), "considerando (b)": 26 municípios listados como ratificantes do Protocolo de Intenções (Canela, Canoas, Caraá, Dois Irmãos, Gramado, Ivoti, Novo Hamburgo, Santo Antônio da Patrulha, São Leopoldo, Sapiranga, Três Coroas — 11 a mais).
- Estatuto "considerando (h)": 15 municípios que ratificaram o Primeiro Termo Aditivo (= núcleo da Concessão).

**Defeito**: o Estatuto da Concessão (não confundir com o Estatuto do Consórcio) confirma 15 municípios na concessão, mas o ESTATUTO DO CONSÓRCIO inclui 26 municípios consorciados. A redação do Convênio do Apêndice 7 (preâmbulo, parágrafo "ii") fala em "MUNICÍPIOS" como ente único, sem distinção. Isso pode gerar confusão entre municípios consorciados e municípios da concessão — especialmente para fins de assento no Conselho Superior de Acompanhamento (Cláusula Trigésima-Oitava-B do Estatuto).

### D.4. [GRAVE] Convênio de Compartilhamento — silêncio sobre contraprestação ao Prestador de Água

O Apêndice 7 (Convênio de Compartilhamento de Dados) NÃO prevê:
- pagamento ao Prestador de Água pelo serviço de leitura, cadastro e compartilhamento (que são serviços com custo);
- ressarcimento de tarifa de cofaturamento;
- contraprestação de qualquer natureza.

**Caderno de Encargos** não traz previsão tampouco.
**Contrato (cl. 17)** trata a "cobrança direta pela CONCESSIONÁRIA" como única forma — sem reservar parcela tarifária ao prestador de água.

**Conflito implícito**: o art. 5.6 e seguintes da NR 1/ANA (Resolução 79/2021) — que rege especificamente o cofaturamento — exige que, quando o serviço de manejo é cobrado com base na conta de água, haja **previsão de ressarcimento** ao prestador do serviço de água pelo custo do cofaturamento. A omissão do Convênio pode ser tida como **inadimplência regulatória já no nascedouro**.

A Matriz de Riscos (Anexo 5, itens 71–74) ainda agrava: aloca à Concessionária o risco de atraso e qualidade dos dados, mas não exige contraprestação que dê à Prestadora de Água incentivo para cumprir. Conflito também com o Contrato de Programa, que prevê o Consórcio como articulador, mas sem instrumento financeiro previsto.

### D.5. [GRAVE] Conta Verde — divergência sobre destinação dos recursos

- **Contrato, cl. 17.3.1**: "Os recursos depositados na CONTA VERDE serão geridos e aplicados pelo PODER CONCEDENTE."
- **Contrato de Programa, cl. 7.1.3.2**: "Os recursos deverão ser utilizados para (i) contratação de cooperativas ou associação de catadores de materiais recicláveis [...]; e (ii) ações de educação ambiental relacionadas com o manejo de resíduos domésticos, podendo ainda ser utilizado para a finalidade prevista na subcláusula 7.1.3.3 abaixo."
- **Contrato de Programa, cl. 7.1.3.3**: "No caso de sobra de recursos depositados na 'conta verde', o CONSÓRCIO PRÓ-SINOS poderá optar por utilizar da sobra para arcar com os custos de redução tarifária na CONCESSÃO."

**Defeito**: o Contrato de Concessão é silente sobre a destinação específica dos recursos da Conta Verde. As regras vinculantes estão no Contrato de Programa, que não é (textualmente) anexo do Contrato de Concessão. Isso cria um **descolamento de hierarquia** — o Contrato de Programa rege a relação Consórcio-Municípios e a Concessionária não é parte dele; portanto, não há vínculo direto.
**Correção**: incorporar a regra de destinação no Contrato de Concessão (cláusula 17.3 ou cláusula nova específica).

### D.6. [MÉDIO] PRÉ-OPERACIONAL — vedação de faturamento vs. obrigação de pagamento à Conta Verde

- Cláusula 11.3 do Contrato: "Durante a FASE 1 - PRÉ OPERACIONAL, a CONCESSIONÁRIA **não poderá efetuar qualquer faturamento aos USUÁRIOS**."
- Cláusula 17.3: "A partir da **DATA DE INÍCIO DA OPERAÇÃO COMERCIAL**, a CONCESSIONÁRIA deverá depositar [...] na CONTA VERDE [...]"
- Cláusula 17.4.4: "O primeiro pagamento [da quantia para gestão do contrato] deverá ser feito no prazo de 5 (cinco) dias, contados da emissão da **ORDEM DE EXECUÇÃO**" — ou seja, antes da DATA DE INÍCIO DA OPERAÇÃO COMERCIAL.

**Defeito**: a cláusula 17.4.4 obriga a Concessionária a fazer um pagamento à Conta Específica do Poder Concedente já a partir da ORDEM DE EXECUÇÃO (início da FASE 1), mas a cláusula 11.3 veda qualquer faturamento aos usuários nessa fase. O pagamento à Conta Específica seria feito do próprio caixa da Concessionária, sem fonte de receita ainda. **A previsão é coerente economicamente (pré-operação)** mas dever ser explicitada — ou suprimida a regra de pagamento na FASE 1, mantendo-a a partir da DATA DE INÍCIO DA OPERAÇÃO COMERCIAL.

### D.7. [MÉDIO] Frequência mínima da coleta seletiva orgânica vs. exigência de coleta seletiva universal

- Caderno de Encargos, item 3.3.1.1: a coleta seletiva de **recicláveis secos** será disponibilizada em "100% dos domicílios dos MUNICÍPIOS [...] a partir da emissão da ORDEM DE INÍCIO DA OPERAÇÃO COMERCIAL."
- Tabela 1 do Caderno (p. 14): "Expansão da coleta seletiva de **orgânicos**, de modo a atender todos os municípios da concessão — 48 meses após emissão da OS" — ou seja, só ao final da FASE 2, no início da FASE 3.

**Defeito**: a coleta seletiva universal de **orgânicos** se completa apenas ao final do 4º ano da concessão, mas as metas de orgânicos do Anexo 4 (Tabela 7) já fixam 1,0% nos anos 5–6, 2,0% nos anos 7–10. Sem coleta universal antes do ano 5, a meta do ano 5–6 é viável mas justa; sem ela antes do ano 5, é provavelmente inalcançável fora da rota de tratamento centralizado.

### D.8. [MÉDIO] Tarifa Social — divergência sobre limite e mecanismo de gatilho

- Apêndice 4-A, item 1.7: Tarifa Social conforme art. 2 da Lei 14.898/2024.
- Matriz de Riscos, item 26: "Aumento superior a 15% (quinze por cento) do número de ECONOMIAS sujeitas ao pagamento de TARIFA na categoria 'Residencial Social' [...] O reequilíbrio econômico-financeiro em razão de eventual materialização deste risco só será devido caso o risco se materialize **após a primeira REVISÃO ORDINÁRIA**." — alocado ao Poder Concedente.

**Defeito**: a primeira Revisão Ordinária ocorre 4 anos após a DATA DE INÍCIO DA OPERAÇÃO COMERCIAL. Se o aumento >15% da base social ocorrer no ano 2 ou ano 3, a Concessionária absorve totalmente o impacto, sem reequilíbrio, mesmo com o risco "alocado ao Poder Concedente". Isso na prática transfere o risco à Concessionária durante 4 anos. **A redação inverte o vetor do risco contratual.**

### D.9. [MÉDIO] Receita Extraordinária — divergência entre tratamento como "obrigatória" no Caderno e "aleatória" no Contrato

- Caderno de Encargos, item 1.1 (Diretrizes Gerais, p. 5): "qualquer tecnologia implantada pela CONCESSIONÁRIA deverá prever **utilização dos subprodutos** como composto, digestato, recicláveis, biogás, CDR e energia [...]"
- Caderno de Encargos, item 2.2.2 (p. 16): "A apresentação da rota tecnológica deverá conter, no mínimo: [...] Estimativa de **geração de energia (MWh), se for o caso**; [...]" — obrigatoriamente informada no Plano de Trabalho.
- Caderno de Encargos, item 2.7.1 (p. 23): "Receitas Acessórias: Apresentação das **receitas acessórias pretendidas** no início do contrato com a utilização da capacidade instalada [...]" — obrigatório informar.
- Contrato, cl. 19.14 e 19.15: receitas extraordinárias são **aleatórias**, sem direito a reequilíbrio.
- Matriz de Riscos, item 49: "Todos os riscos relacionados à exploração de atividades que gerem RECEITAS EXTRAORDINÁRIAS [...] — CONCESSIONÁRIA."

**Defeito**: o Caderno empurra o aproveitamento de subprodutos como obrigação técnica e exige que conste do Plano de Trabalho com estimativas. Isso significa que o Plano de Negócios da Concessionária ESTRUTURALMENTE conta com essas receitas. Mas o Contrato as classifica como aleatórias, sem direito a reequilíbrio se frustrarem-se. **Há um descompasso entre obrigação técnica e tratamento contratual.**

Há ainda contradição com o regime da Lei 8.987/1995 (art. 11), que prevê receitas alternativas para favorecer a modicidade tarifária — incoerente classificar como totalmente "aleatórias" sem direito a reequilíbrio, especialmente quando o Caderno as condiciona tecnicamente.

### D.10. [MÉDIO] Comissão de Fiscalização vs. Comitê de Acompanhamento vs. Conselho Superior

Três órgãos diferentes criados pelo Estatuto e pelo Contrato de Programa, com finalidades sobrepostas, sem definição clara de hierarquia:

- **Comissão de Fiscalização** (Contrato de Programa, cláusula 3.3.4): fiscalização cotidiana, com membros do Consórcio e dos municípios; "deliberações da Entidade Reguladora prevalecem sobre as da Comissão" (3.3.4.14).
- **Comitê de Acompanhamento** (Contrato de Programa, cláusula 4): "fórum de disseminação de informações, alinhamento, discussão e endereçamento de temas relacionados com o dia a dia"; consultivo; 2 membros do Consórcio + cada Município.
- **Conselho Superior de Acompanhamento da Concessão** (Estatuto, cláusula 38-A a 38-F): consultivo e deliberativo, 1 membro por Município.

**Defeito**: três órgãos paralelos, com competências que se sobrepõem (especialmente Comitê de Acompanhamento e Conselho Superior). Cláusula 4.4 do Contrato de Programa afirma textualmente que "as competências do Comitê de Acompanhamento [...] não se confundem com aquelas do Conselho Superior de Acompanhamento" — mas não diz qual é a fronteira. Aumenta o custo de governança e cria potencial de bloqueio decisório.

### D.11. [MÉDIO] Estatuto Cláusula 38-D — duplicação de "IX" e função vedada

- Cláusula 38-D do Estatuto: duas atribuições numeradas "IX" (vide B.2).
- Cláusula 38-D, PARÁGRAFO ÚNICO: "É vedado ao CONSELHO SUPERIOR DE ACOMPANHAMENTO DA CONCESSÃO adotar medidas ou emanar decisões que contrariem ou alterem o disposto no contrato de CONCESSÃO ou que extrapolem a finalidade para o qual foi criado."

A Cláusula 38-D incluí entre as competências deliberativas: "XI - manifestar-se previamente sobre a assunção de novas obrigações pelo CONSÓRCIO PRÓ-SINOS no âmbito do contrato CONCESSÃO". Mas o Contrato de Concessão coloca a discricionariedade no Poder Concedente (= Consórcio). A vedação genérica do Parágrafo Único pode ser usada para esvaziar o Conselho. **Falta clareza sobre o efeito jurídico da "manifestação prévia" do Conselho.**

### D.12. [BAIXO] Cláusula 17.4 ("0,75% da RBO") vs. cláusula 30.14 ("0,5% da ROB")

- Contrato cl. 17.4: 0,75% da RECEITA BRUTA OPERACIONAL para gestão contratual do Poder Concedente.
- Contrato cl. 30.14: 0,5% da RECEITA OPERACIONAL BRUTA para taxa de regulação e fiscalização.

Total: **1,25%** da ROB destinado fora da operação. Não há defeito de redação aqui, mas a soma das duas obrigações é relevante para o licitante modelar — e os termos divergem (cf. B.5).

### D.13. [MÉDIO] PRÓ-SINOS como interveniente — Estatuto + Convênio + Contrato — papéis sobrepostos

O PRÓ-SINOS:
- é PODER CONCEDENTE (Contrato);
- é interveniente-anuente do Convênio de Compartilhamento (Apêndice 7);
- é parte do Contrato de Programa (signatário com municípios);
- é interveniente-anuente do Contrato de Administração de Contas (Anexo 6);
- é delegante da regulação ao REGULADOR (cláusula 3.3.1 do Contrato de Programa).

Sem o Apêndice 1 de Definições, falta termo unificador que enquadre todas essas posições jurídicas. A mistura "PRÓ-SINOS x PODER CONCEDENTE x CONSÓRCIO" aparece sem sistematização nos documentos.

---

## E. INCONSISTÊNCIAS INTERNAS (MESMO DOCUMENTO)

### E.1. [GRAVE] Caderno de Encargos — vedação de aterro em 1.1.4 vs. opção de aterro em 3.6.3 e Tabela 1

Vide D.2.

### E.2. [GRAVE] Matriz de Riscos, itens 68/69/70 — referência cruzada quebrada à própria numeração

Os itens 68, 69 e 70 da Matriz contêm referência "neste item Error! Reference source not found." que truncam o sentido literal. Vide A.7.

### E.3. [MÉDIO] Cláusula 11.9.3 vs. 11.9.2 — direito de uso de aterro

- 11.9.2: o aterro próprio NÃO é bem reversível.
- 11.9.3: "O Plano de Desmobilização Operacional deverá prever que o PODER CONCEDENTE terá o direito de contratar o uso de aterro sanitário da CONCESSIONÁRIA ou de terceiro por prazo mínimo de 5 (cinco) anos."

**Defeito**: o aterro "da Concessionária" não é bem reversível, mas o Poder Concedente terá direito de **contratar o uso** dele após a extinção. Não há definição do preço, da forma e dos critérios para definir esse contrato. Se a Concessionária for hostil, pode inviabilizar a continuidade do serviço. O dispositivo cria uma servidão futura sobre bem da própria Concessionária sem definir parâmetros (não obriga preço, não fixa modelo de contrato, não impõe ANP/ANA, etc.).

### E.4. [MÉDIO] Cláusula 11.10.4 e 11.10.5 (inexistente) — sequência interrompida

Item 11.10 e seus 11.10.1 a 11.10.4 detalham o procedimento de aprovação do Plano de Desmobilização. Cláusula 11.10.4 fala que "a CONCESSIONÁRIA deverá enviar [...] semestralmente, relatório [...]". Depois pula para 11.11 sem 11.10.5. Não é erro grave — apenas vale conferir se o procedimento de cumprimento e divergência foi todo coberto.

### E.5. [MÉDIO] Anexo 5 — alocação inconsistente nos itens 69 e 70 — duas marcações na mesma linha

Item 69 (Faixa Compartilhada de inadimplência): marca tanto **PODER CONCEDENTE** quanto **CONCESSIONÁRIA** com "X" — está correto, é risco compartilhado. Mas a tabela coloca os dois "X" no MESMO item, sem distinguir percentual. A explicação do compartilhamento está no Contrato (20.14), não na Matriz.

### E.6. [BAIXO] Caderno de Encargos — "OS" como abreviação inconsistente

A nota de rodapé da Tabela 1 do Caderno define "OS — ORDEM DE SERVIÇO". Mas o Contrato sempre fala em ORDEM DE EXECUÇÃO. Vide B.4.

---

## F. LACUNAS

### F.1. [GRAVE] Lista material de BENS REVERSÍVEIS — inexistente

Nem o Contrato, nem o Caderno de Encargos, nem qualquer outro documento juntado define a lista, o rol exemplificativo ou o critério positivo para qualificar bem como REVERSÍVEL. A definição material certamente está no APÊNDICE 1 DO EDITAL — DEFINIÇÕES, **ausente do repositório**. Lacuna grave para licitantes e para a operação do art. 27.1.18 do Contrato (vistorias periódicas pelo Regulador).

### F.2. [GRAVE] Identificação do REGULADOR — pendente

Vide tópico G abaixo. O campo `[•]` da agência reguladora está em todos os documentos. Sem essa definição, dezenas de cláusulas do Contrato dependem de ato administrativo de quem é, no momento da publicação, indeterminado.

### F.3. [GRAVE] Contraprestação ao Prestador de Água — ausente do Convênio (D.4)

Lacuna estrutural. O Convênio do Apêndice 7 não prevê remuneração, ressarcimento ou contrapartida.

### F.4. [GRAVE] Procedimento de aplicação do Fator de Inadimplência — referências quebradas

A integralidade do procedimento da cláusula 20.12–20.18 (FI) está afetada pela numeração quebrada (A.5) e pelas referências "Error! Reference source not found." da Matriz (A.7). Lacuna processual significativa.

### F.5. [MÉDIO] Detalhamento da Conta Verde

O Contrato (cl. 17.3) fixa a obrigação de depósito mensal "até o 10º dia do mês subsequente" mas não traz tabela de valores (todos `[●]`) nem o detalhamento da destinação (cf. D.5). Lacuna.

### F.6. [MÉDIO] Penalidades específicas por atraso em CTR, galpões de cooperativas, novo aterro

O Contrato (cláusulas 35–36) define penalidades por gravidade (leve/média/grave) com multas de 0,25% / 0,5% / 1% da ROB. Mas o Caderno de Encargos prevê marcos críticos específicos (CTR, galpões, aterro). Não há penalidades específicas casadas com esses marcos — apenas o regime geral. Lacuna que enfraquece o enforcement de obrigações materiais relevantes.

### F.7. [MÉDIO] Tarifa para casos sem hidrômetro — pouco detalhada

A Resolução do Consórcio (art. 6 § 8°) prevê apenas TBD para usuários sem hidrômetro. Mas, sendo a fórmula do Apêndice 4-A monofásica (sem TBD), a regra fica sem base aplicável no modelo do Edital. Não há provisão para reestimativa de consumo "presuntivo" (ex.: água própria de poço, áreas rurais sem rede). Lacuna agravada pelo conflito D.1.

### F.8. [MÉDIO] Procedimento de exclusão/saída de Município — só no Contrato de Programa

O Contrato de Programa (cláusula 11) regula a saída/exclusão de Município com obrigação de pagamento do reequilíbrio + 10%. Mas o Contrato de Concessão (cl. 11–49) só prevê isso reflexamente (Matriz de Riscos, item 24 — alocado ao Poder Concedente). Não há cláusula expressa no Contrato dizendo como o serviço continuará no município excluído, pelo prazo de quê, e como se evita ruptura. Lacuna processual relevante.

### F.9. [MÉDIO] Regulamentação infralegal pelo Regulador — sem prazos

Várias cláusulas dependem de regulamentos do Regulador (ex.: forma de pagamento da taxa de regulação — cl. 30.14.2; conteúdo dos relatórios — cl. 30.7; mediação institucional — cl. 46.2.2). Nenhuma fixa prazo para a emissão desses regulamentos pelo Regulador. Sem o ato regulamentar, parte significativa do Contrato fica em vácuo regulatório. Lacuna processual.

### F.10. [MÉDIO] Diretrizes técnicas para o cálculo da TARIFA DE RESÍDUOS quando há mais de uma economia em um único hidrômetro

Em condomínios e edificações com múltiplas economias e único hidrômetro, qual é a forma de rateio? O Convênio (cl. 4) prevê cadastro de "economias", mas o Apêndice 4-A é silente sobre rateio. Lacuna.

### F.11. [MÉDIO] Direitos e deveres dos USUÁRIOS — referência genérica

Cláusula 26 do Contrato refere "Direitos e Deveres dos Usuários" — sem texto detalhado no Contrato. O Caderno de Encargos (item 2.6) trata do "Manual de Prestação do Serviço e de Atendimento ao USUÁRIO" mas em diretrizes gerais. Sem o corpo do Edital, lacuna.

### F.12. [MÉDIO] Custo das auditorias do Regulador

Cláusula 27.2: "O REGULADOR poderá contratar ENTIDADE INDEPENDENTE a seu custo [...]". Cláusula 30.5: "às suas custas". Mas a Concessionária recolhe TRF de 0,5% da ROB; não há regra explícita de que essa taxa cobre as auditorias. Lacuna.

### F.13. [BAIXO] Indicador IG05 — fórmula a ser definida pelo Regulador

Anexo 4, item 4.1.7.2: "Para o indicador IG05 — Recuperação de Despesas do Serviço Público [...] ficará a cargo do REGULADOR definir a fórmula e métrica de apuração [...]". Sendo um indicador com efeitos sobre o reajuste, a delegação à futura agência (não identificada) cria insegurança ao licitante. Lacuna estrutural.

---

## G. CAMPOS [•] DA "AGÊNCIA REGULADORA" — TRATAMENTO SEPARADO POR GRAVIDADE

A definição material do REGULADOR é o item mais grave. Sem ele:
- Não há a quem entregar Planos para parecer técnico (cl. 11.1.16).
- Não há a quem submeter pedido de reajuste (cl. 18 e 20).
- Não há quem decida o reequilíbrio (cl. 21–23).
- Não há quem aplique penalidades (cl. 27, 30, 35–36).
- Não há quem auditar bens reversíveis (cl. 27.1.18, 45.9).
- Não há quem assine o Convênio do Apêndice 7 como interveniente-anuente — paralisia operacional desde a FASE 1.

**Defeito**: a Lei 11.445/2007, alterada pela Lei 14.026/2020, exige que a regulação preceda a concessão (art. 11, II). A NR 1/ANA (Resolução 79/2021) reforça isso. Não basta deixar `[•]` — é provável que a Lei 14.026/2020 sequer permita a publicação do Edital sem essa definição prévia.

---

## H. RANKING CONSOLIDADO DOS DEFEITOS (do mais grave ao menos)

1. **D.1** — Fórmula tarifária incompatível entre Apêndice 4-A e Resolução do Consórcio. **Risco de impugnação certo.**
2. **F.2 / G** — REGULADOR não identificado em nenhum documento.
3. **F.1** — Lista material de BENS REVERSÍVEIS não consta (Apêndice 1 ausente).
4. **D.4 / F.3** — Convênio omisso sobre contraprestação ao Prestador de Água.
5. **A.7 / B.1 / E.2** — Erros "Error! Reference source not found." na Matriz de Riscos truncam o sentido de itens críticos (inadimplência).
6. **A.1 / A.2 / A.3 / A.4** — Quatro referências cruzadas a Anexos errados em cláusulas-chave (30.8, 8.4.2, 23.4, 19.8/9.9).
7. **A.5** — Numeração quebrada de 20.13–20.19 (FI).
8. **D.2 / E.1** — Vedação de aterro em 1.1.4 do Caderno entra em choque com 3.6.3 e Tabela 1.
9. **D.5** — Conta Verde sem destinação no Contrato de Concessão (só no Contrato de Programa).
10. **D.8** — Risco de Residencial Social >15% só reequilibra após primeira Revisão Ordinária — transfere risco à Concessionária por 4 anos.
11. **D.9** — Conflito Caderno (subprodutos como obrigação técnica + estimativa de energia) x Contrato (receitas extraordinárias aleatórias).
12. **B.7** — "Água" vs. "Água e Esgoto" entre Apêndice 7 e Anexo 7.
13. **D.3** — Lista de municípios — 15 na concessão, 26 no Estatuto consorcial.
14. **B.1** — Inciso IX faltante e dois X na Resolução Tarifária (art. 5).
15. **D.6** — Pagamento à Conta Específica do PC no início da FASE 1 sem fonte de receita.
16. **F.4** — Procedimento do FI truncado.
17. **D.10** — Três órgãos de governança paralelos sem hierarquia clara.
18. **B.6 / D.9** — "Receita Acessória" x "Receita Extraordinária" — mesmo conceito, dois nomes.
19. **B.4** — "Ordem de Execução" vs. "Ordem de Serviço".
20. **B.3 / B.5 / B.8 / B.9** — Inconsistências terminológicas menores ("FASE 1 – PRÉ-OPERACIONAL", "ROB" vs. "RBO", "SMRSU" vs. "SMRDO").
21. **D.7 / D.11 / D.12 / D.13 / E.3 / E.4 / F.5–F.13** — defeitos médios/leves remanescentes.

---

**Fim do Agente 04.** Próximos: Agente 05 (escopo operacional), Agente 02a/02b (licitação) e Agente 03a/03b (riscos), seguidos da Fase 2 do Agente 01 (jurisprudência sobre os achados acima).
