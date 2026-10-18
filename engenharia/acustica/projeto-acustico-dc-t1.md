> **Estado do conteúdo de engenharia** (cabeçalho gerado)
>
> Cabeçalho gerado a partir do próprio relatório: diz o que está provisório, por preencher ou por cumprir, antes do corpo.
>
> - **Limitações que o próprio relatório imprime.** 2 pendências declaradas no corpo; não foram escondidas nem resolvidas aqui.
> - **Campos.** Há 5 campos por preencher, entre parênteses rectos ([morada da obra], [concelho], [zona acústica], [nome do dono da obra], [nome do projectista acústico]): dependem do lote, do dono da obra ou de um técnico e estão vazios.
> - **Assinatura.** Documento não assinado: sem assinatura de técnico habilitado; o relatório não foi revisto por técnico com inscrição válida.
> - **Resultados que não cumprem o critério.** 1 célula diz «NÃO» ou «✗»: «Casa Base T1 — fachada mais desfavorável», coluna «≥ 33 dB (mista)».
> - **Incoerência conhecida.** Valores acústicos da memória e do mapa de vãos não reconciliados.
> - **Incoerência conhecida.** Leitura do §1 contradiz a tabela (margem negativa).
>
> Documento técnico de referência: não é projecto e não serve para construir sem profissionais licenciados (ver `AVISO.md`, na raiz da publicação).

# Projecto de condicionamento acústico — Casa Base T1 (`DC-T1`)

**Regime.** DL n.º 96/2008 (RRAE) + DL n.º 9/2007 (RGR). Moradia
unifamiliar isolada: aplicam-se o isolamento de fachada (Art. 5.º) e os
limites de ruído de equipamentos; requisitos entre fogos não se aplicam.
A conformidade é declarada na licença de utilização — **este projecto é
subscrito por projectista acústico/OE (assinatura pendente)**.

**Obra.** [morada da obra], [concelho] · zona acústica municipal:
[zona acústica] (mista/sensível — do PDM). **Dono da obra.**
[nome do dono da obra] · **Projectista.** [nome do projectista acústico].

---

## 1. Fachadas — D2m,nT,w (método EN ISO 12354-3 simplificado, −3 dB de incerteza)

| Fachada | Área (m²) | Vãos (m²) | R_w composto | D2m,nT,w est. | ≥ 33 dB (mista) | ≥ 28 dB (sensível) |
|---|---|---|---|---|---|---|
| Casa Base T1 — fachada mais desfavorável | 24.3 | 2.88 | 36.4 dB | **31.4 dB** | ✗ | ✓ |

Elementos: parede LGSF + lã + tijolo R_w ≈ 47 dB; vão vidro
duplo R_w ≈ 33 dB; porta vedada R_w ≈ 30 dB.

**Leitura.** Em zona SENSÍVEL (≥ 28 dB) a margem é confortável. Em zona
MISTA (≥ 33 dB) a margem mínima é **-1.6 dB** — positiva mas
marginal no papel. Consequências de projecto:

1. O ensaio in situ do piloto (secção 3) é OBRIGATÓRIO antes de fechar
   o valor declarado de catálogo.

## 2. Equipamentos (RRAE Art. 5.º n.º 8 + RGR)

* Bomba de calor (unidade exterior): L_w = 62 dB(A);
  a ≥ 3 m do limite → L_p ≈ 44.5 dB(A)
  ≤ 45 dB(A) nocturno de zona sensível ✓.
* Regra de implantação (lista de verificação por lote): unidade exterior a ≥ 3 m do
  limite, fachada oposta ao vizinho mais próximo, apoios anti-vibráteis.
* Interior: equipamentos do edifício ≤ 32 dB(A) (funcionamento
  intermitente) nos compartimentos de repouso — bomba de calor no
  compartimento técnico com porta + AVAC dimensionado a NR 25.

## 3. Protocolo de ensaio in situ (piloto — pendente)

1. **Norma:** ISO 16283-3 (medição de isolamento de fachada em campo),
   método do altifalante (loudspeaker, 45°).
2. **Compartimentos a ensaiar:** Quarto principal (fachada Sul — pior
   rácio vão/parede) e Sala (fachada Sul + Oeste).
3. **Grandeza:** D2m,nT,w + C/Ctr (ponderação tráfego).
4. **Critério de aceitação:** D2m,nT,w ≥ 33 dB (zona mista assumida) com
   a tolerância regulamentar de 3 dB do Art. 11.º do RRAE aplicável na
   avaliação in situ.
5. **Laboratório:** entidade acreditada IPAC; relatório arquivado na
   compilação técnica + pasta de conformidade; valores alimentam de volta as constantes R_w de catálogo.
