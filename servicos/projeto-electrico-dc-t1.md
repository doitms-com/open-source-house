> **Estado do conteúdo de engenharia** (cabeçalho gerado)
>
> Cabeçalho gerado a partir do próprio relatório: diz o que está provisório, por preencher ou por cumprir, antes do corpo.
>
> - **Campos.** Há 5 campos por preencher, entre parênteses rectos ([morada da obra], [concelho], [nome do dono da obra], [nome do TRIE], [n.º de inscrição do técnico]): dependem do lote, do dono da obra ou de um técnico e estão vazios.
> - **Assinatura.** Documento não assinado: sem assinatura de técnico habilitado; o relatório não foi revisto por técnico com inscrição válida.
> - **Incoerência conhecida.** O esquema unifilar publicado tem os circuitos Q1-Q6; o quadro de circuitos deste projecto vem do modelo, com os circuitos C1-C12 e disjuntores diferentes. Ainda não foram reconciliados.
> - **Totais.** Os totais incluem C11/C12 (circuitos de opções não publicadas); as linhas desses circuitos foram retiradas do quadro.
>
> Documento técnico de referência: não é projecto e não serve para construir sem profissionais licenciados (ver `AVISO.md`, na raiz da publicação).

# Projecto eléctrico (ficha electrotécnica preparatória) — Casa Base T1 (`DC-T1`)

**Regime.** RTIEBT (Portaria n.º 949-A/2006, com alterações) + NP HD
60364. Instalação tipo C (habitação). A ficha electrotécnica FINAL é
emitida pelo técnico responsável (TRIE) e verificada pela entidade
inspectora (CERTIEL/DGEG) — este projecto prepara-a a partir do modelo.

**Obra.** [morada da obra], [concelho] · **Dono da obra.**
[nome do dono da obra] · **TRIE.** [nome do TRIE], [n.º de inscrição do técnico].

---

## 1. Alimentação e potência

| Parâmetro | Valor |
|---|---|
| Potência simultânea estimada (NP HD 384; inclui circuitos não publicados) | 7.41 kVA |
| Potência contratada recomendada | **6.9 kVA** |
| Tipo de ligação | BTN, cabo entrada 10-16 mm² Cu (ver ficheiro não publicado) |

## 2. Quadro eléctrico (circuitos ACTIVOS do modelo)

| ID | Circuito | Disjuntor | Secção | Pontos | Diferencial |
|---|---|---|---|---|---|
| C1 | Iluminação geral (LED 18 W médio) | 10 A | 1.5 mm² | 16 | 30 mA |
| C10 | Tomadas + luz exterior | 16 A | 2.5 mm² | 4 | 30 mA |
| C2 | Tomadas sala + quartos + hall | 16 A | 2.5 mm² | 12 | 30 mA |
| C3 | Tomadas cozinha (6 unid. bancada) | 16 A | 2.5 mm² | 7 | 30 mA |
| C4 | Frigorífico dedicado | 16 A | 2.5 mm² | 1 | 30 mA |
| C5 | Máquina lavar/secar roupa + loiça | 16 A | 2.5 mm² | 3 | 30 mA |
| C6 | Placa indução + forno | 32 A | 6.0 mm² | 2 | 30 mA |
| C7 | AQS (bomba calor) | 16 A | 2.5 mm² | 1 | 30 mA |
| C8 | AVAC (climatização) | 16 A | 2.5 mm² | 4 | 30 mA |
| C9 | WC (luz + tomada IP44) | 16 A | 2.5 mm² | 6 | 30 mA |

Protecções de cabeceira: interruptor geral, **diferenciais 30 mA tipo A**
(RTIEBT secção 531), **SPD tipo 2** (secção 443/534 — sobretensões),
selectividade por agrupamento de circuitos.

## 3. Terra e equipotencialidade

* Eléctrodo de terra no anel de fundação (Ra ≤ 100 Ω, NP 4413);
  ligador amovível junto à central técnica.
* Equipotencialidade das massas metálicas (LGSF!) — barramento de terra
  ligado à estrutura em ≥ 2 pontos opostos (RTIEBT 411/415, protecção
  por corte automático em TT).
* Zonas de banho: volumes 0-2 respeitados; IP44 e ligações
  equipotenciais suplementares (RTIEBT secção 701).

## 4. Peças

1. Esta memória + `mep-circuitos-dc-t1.csv` + `mep-pontos-dc-t1.csv`.
2. **Esquema unifilar TRIE-ready**: folha `unifilar` em `desenhos/`.
3. Planta com pontos (camada MEP): folha `planta` em `desenhos/`.
4. Projecto ITED associado: `servicos/projeto-ited-dc-t1.md`.
