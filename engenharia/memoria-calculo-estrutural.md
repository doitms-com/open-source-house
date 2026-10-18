> **Estado do conteúdo de engenharia** (cabeçalho gerado)
>
> Cabeçalho gerado a partir do próprio relatório: diz o que está provisório, por preencher ou por cumprir, antes do corpo.
>
> - **PROVISÓRIO.** O original é a versão 0.1; 1 valor marcado PLACEHOLDER de engenharia. Os valores marcados são hipóteses de trabalho, não resultados verificados.
> - **Limitações que o próprio relatório imprime.** 1 achado de engenharia assinalado (⚠) e 1 pendência declarada no corpo; não foram escondidas nem resolvidas aqui.
> - **Assinatura.** Documento não assinado: sem assinatura de técnico habilitado; o relatório não foi revisto por técnico com inscrição válida.
>
> Documento técnico de referência: não é projecto e não serve para construir sem profissionais licenciados (ver `AVISO.md`, na raiz da publicação).

# Doitms Casa — Memória de Cálculo Estrutural (caso mais desfavorável em Portugal)

**Versão.** Gerado a partir do modelo com o selo `c2d1ffeb79f1`.

**Âmbito.** Verificação do projecto-tipo Doitms Casa T1 contra as cargas regulamentares para os 65 municípios
representativos do envelope geográfico português (continente + RA Açores +
RA Madeira). O projecto Doitms é dimensionado para o pior caso de
Portugal, com factor de reserva **1.5×** sobre o regulamentar.

**Norma base.** Eurocódigos EN 1990 + EN 1991-1-1 / -1-3 / -1-4 + EN
1998-1, com os respectivos Anexos Nacionais Portugueses; e DL 364/98
para regime jurídico de cheias.

**Responsabilidade.** Cálculos preliminares executados pela equipa
Doitms a partir de modelos paramétricos. Validação final pelo engenheiro responsável (OE).
Açores e Madeira têm parecer adicional do LREC respectivo conforme legislação.

---

## 1. Envelope geográfico do caso mais desfavorável (65 municípios)

| Carga | Valor extremo | Município governante |
|---|---|---|
| sismo t1 max mps2 | 2.00 | Faro |
| sismo t2 max mps2 | 2.50 | Ponta Delgada (S. Miguel) |
| vento max mps | 42.00 | Madalena (Pico) |
| neve sk max kNm2 | 1.80 | Penhas Douradas (Manteigas) |
| cheia t100 max m | 2.00 | Santarém |
| cheia t500 max m | 3.50 | Santarém |
| storm surge max m | 1.60 | Vila do Corvo (Corvo) |
| altitude max m | 1380.00 | Penhas Douradas (Manteigas) |
| temp min inv min c | -10.00 | Penhas Douradas (Manteigas) |
| temp max ver max c | 45.00 | Mértola |
| precipitacao max mm | 2000.00 | Lajes das Flores (Flores) |
| graus dia max | 3200.00 | Penhas Douradas (Manteigas) |

Os 65 municípios cobrem TODAS as combinações de zona sísmica (Tipo 1 e
Tipo 2 do Anexo Nacional EC8), zona REH (I1-I3 × V1-V3), zona de vento
(A/B + RA), zona de neve (Z1-Z3 + RA), classe de solo (A-E) e cota de
cheia centenária do PGRI/APA documentadas no território nacional.

---

## 2. Acção sísmica EC8

**Modelo estrutural.** Edifício de 1 piso, sistema LGSF com diafragmas
rígidos (OSB-3 12 mm + tirantes diagonais X em painel exterior).
Classe de importância II (habitação), γ_I = 1.0.

Período fundamental T_1 ≈ 0.05 × H^(3/4) = 0.118 s (H = 3.15 m).
Como T_1 está no patamar do espectro elástico:

    Sd(T_1) = ag × S × 2.5 / q,  com q = 2.0 (DCM conservador)

**Validade do patamar (T_B ≤ T_1 ≤ T_C).** Anexo Nacional NP EN
1998-1, quadros NA-3.2/3.3: acção Tipo 1 T_B = 0.1 s, T_C = 0.6 s;
acção Tipo 2 T_B = 0.1 s, T_C = 0.25 s; RA-Açores (Tipo 2) T_B =
0.1 s, T_C = 0.25 s. Com T_1 = 0.118 s ≥ T_B = 0.1 s, o patamar
aplica-se às três formas espectrais; se a rigidez real elevar a
frequência (T_1 < 0.1 s), Sd desce pelo ramo ascendente — o patamar
é o MAJORANTE, logo conservador.

**Justificação de q = 2.0.** Paredes LGSF strap-braced em X são
classificáveis como DCM «frames with concentric bracings» (EN 1998-1
§6.3, q até 4 para diagonais); adopta-se q = 2.0 pela via conservadora
(EC8 remete o dimensionamento dissipativo de cold-formed para o EC3-1-3
+ ensaio). Decisão a ratificar pelo OE; se o OE preferir DCL, q = 1.5
agrava Sd em 33 % — as margens de ancoragem actuais (≥ 4×) absorvem-no.

**Massa sísmica — composição por m² de área bruta, estado "deck"**
(base — EN 1998-1 §3.2.4):

| Parcela | kg/m² | Base |
|---|---|---|
| Laje aligeirada elevada | ≈ 300 | 30 cm aligeirada + betonilha |
| Arredondamento por excesso | ≈ 170 | política conservadora |
| **Total adoptado (deck)** | **1020** | soma das parcelas, incluindo as não publicadas; recalibrar com pesagem (OE) |

**Massa (estado deck).** T1 = 55.1 t (54 m²).

**Ancoragem.** Chumbadouro químico M10 em betão C25/30, espaçamento
600 mm c/c no perímetro. Capacidade característica F_Rk = 25 kN (corte).
Capacidade de cálculo F_Rd = 25/1.25 = 20 kN. Factor reserva Doitms =
1.5× → **F_admissível de política = 13.3 kN** — as margens reportadas nesta
memória são contra F_Rd; a margem contra a política é margem/1.5.

**Drift.** A verificação de drift usa rigidez lateral k = 40 MN/m —
**PLACEHOLDER de engenharia** até haver ensaio de racking (EN 594) ou
cálculo do OE; ver `ec8-estado-t1.csv` para o requisito de
resistência por metro de painel no estado T1.

### Município governante — sismo

**Ponta Delgada (S. Miguel)** (R.A. Açores) governa o dimensionamento
sísmico do projecto-tipo Doitms.

* Sismo Tipo 1 (1.5): ag_R = 0.5 m/s²
* Sismo Tipo 2 (RA-Acores): ag_R = 2.5 m/s²
* Classe solo: C → S_T1 = 1.60, S_T2 = 1.60
* Sd crítico = 5.000 m/s² (T2)
* Corte basal V = m × Sd = 55100 kg × 5.000 m/s² = **275.5 kN**
* N ancoragens M10 = 50
* F por ancoragem = V/N = **5.51 kN** (alvo ≤ 13.3 kN com reserva 1.5×)
* Margem do projecto-tipo = **3.63× F_Rd** = ✓ OK + reserva Doitms 1.5×

**Conclusão.** Os 65 municípios passam EC8 + reserva Doitms 1.5×.

---

## 3. Acção do vento EC1-1-4

**Modelo (estado base).** h_ref = 3.0 m, A_fachada = 27.0 m², A_cobertura (plana) = 54.0 m².

Coeficientes pressão exterior (NP EN 1991-1-4 §7):

* Fachada barlavento c_pe = +0.8
* Fachada sotavento c_pe = -0.5
* Cobertura (zona G/H — bordo) sucção c_pe = -1.4

### Município governante — vento (estado deck)

**Vila do Corvo (Corvo)** (R.A. Açores) — vento básico v_b,0 = 42.0 m/s.

* Velocidade média a z=3 m: v_m = 40.7 m/s
* Pressão de pico q_p = **2309 Pa**
* Força fachada F_w = 81.0 kN
* Uplift cobertura = 174.5 kN
* Massa cobertura (deck) = 68.9 kN

**⚠ Achado de engenharia (reportado, não escondido).** A MESMA
verificação simplificada de uplift (peso próprio vs sucção × 1.5) NÃO
confirma a premissa "massa ≫ uplift" no deck: em 65/65 municípios (incluindo Vila do Corvo (Corvo), o pior caso) o peso próprio do deck a 130 kg/m² continua a perder para a sucção de
pico × 1.5 — mesmo sendo +73 % mais pesado que o telhado antigo de
75 kg/m². A decisão de retirar tirantes de cobertura do deck só se
sustenta se a fixação distribuída à viga de bordo (rim joist) resistir ao uplift por
si — plausível (diafragma contínuo vs asna pontual), mas **fora do
âmbito deste cálculo simplificado e NÃO verificado aqui — verificação
OE pendente**, com nota explícita no dossier de fixação (documento não publicado).

---

## 4. Acção da neve EC1-1-3 + Anexo Nacional

**Cobertura (estado deck):**

* **Deck (base)** — painel contínuo, sem vara nem asna,
  dimensionado à sobrecarga de uso cat. C3 = 5.0 kN/m²,
  muito acima de qualquer neve nacional (μ_1 = 0.8, cobertura plana).
  Margem = sobrecarga de dimensionamento / (μ_1·s_k) — o deck NUNCA é
  governado pela neve.

Valor característico: s_k pela fórmula do Anexo Nacional
s_k = C_z·[1+(H/500)²] (Z1 = 0.30 — zona mais severa, interior
norte/serras; Z2 = 0.20; Z3 = 0.10), tomando o MÁXIMO entre a
fórmula e o valor histórico do dataset.

### Município governante — neve, estado deck (base)

**Penhas Douradas (Manteigas)** (altitude 1380 m).

* Zona NA Z1, s_k cálculo = 2.59 kN/m² (NA Z1)
* μ_1 (cobertura plana) = 0.8
* s cobertura = **2.072 kN/m²** ≪ 5.0 kN/m² de dimensionamento
* Margem do deck = **2.4×** (alvo ≥ 1.5×) — nunca reforça

**Conclusão (deck).** Os 65 municípios passam com folga no estado
deck (5.0 kN/m² de dimensionamento).

---

## 5. Cheia centenária + storm surge (DL 364/98 + PGRI)

**Regra Doitms.** A cota da soleira é dimensionada para o pior caso de:

    cota_soleira ≥ max(
        30 cm (mínima sempre),
        cota T100 + 30 cm (reserva sobre regulamentar),
        cota T500 + 0 cm (cenário alterações climáticas IPCC moderado),
        cota storm surge + 50 cm (zonas costeiras)
    )

**Solução técnica.** Laje aligeirada elevada com altura ajustável entre
15 e 60 cm. Acima de 120 cm: variante elevada (não publicada) com
estrutura LGSF pilastra + acesso por escada/rampa.

### Município governante — cheia

**Santarém** (Alentejo).

* Cheia T100: 2.0 m
* Cheia T500: 3.5 m
* Storm surge: 0.0 m
* **Cota soleira mínima = 350 cm** (T500)
* Solução recomendada: variante elevada (não publicada)

**Resumo do envelope de 65 municípios:**

* Soleira mínima 30 cm suficiente: 25 municípios
* Necessitam reserva T100: 0
* Necessitam reserva T500: 6
* Necessitam reserva storm surge: 34
* **Variante elevada (não publicada) recomendada** (cota > 120 cm): 36

---

## 7. Combinações de acções EN 1990 (anexo EC0)

As verificações por acção isolada das secções 2-5 são compiladas em
combinações de cálculo no anexo `ec0-combinacoes.csv`, no município governante de cada uma:

| # | Combinação | Expressão | Verificação alvo |
|---|---|---|---|
| C1b | ULS gravítica deck (base) | 1.35·G_deck + 1.5·5.0 (cat. C3/I) | painel do deck |
| C2a | ULS uplift deck (base) | 0.9·G − 1.5·W, c_pe −1.4 **+ c_pi +0.2** | configuração sem tirantes |
| C3 | ULS vento lateral | 1.5·W fachada | ancoragens ao corte |
| C4 | sísmica (deck) | G + ψ₂·Q + E (ψ₂ = 0.3, cat. A) | ancoragens ao corte |

**Sobrecarga de cobertura do deck.** A cobertura acessível
cat. I (uso A; dimensionamento gravítico a 5,0 kN/m² — C3) NÃO acumula com neve nem com vento (EN 1991-1-1 §3.3.2) — é
sempre o maior dos dois valores que governa a combinação gravítica,
nunca a soma; a combinação 6.10b (1.25·G + 1.5·Q) não governa nenhum
elemento do projecto-tipo de 1 piso, registada por completude.

---

## 8. Durabilidade 50 anos — corrosividade EN ISO 12944

A promessa «estrutura 50 anos» exige mapear a exposição salina de
cada município para classe de corrosividade e especificação de
protecção (ficheiro não publicado, 65 linhas):

| Exposição (dataset) | Classe ISO 12944-2 |
|---|---|
| nula | C2 |
| baixa | C3 |
| moderada | C3 |
| elevada | C4 |
| muito_elevada | C5/CX |

Interiores secos (dentro do envelope estanque): C1-C2 — a
galvanização Z275 de série cobre 50+ anos. A classe da tabela
governa APENAS elementos expostos (tirantes de cobertura, ferragens
exteriores, chumbadouros na soleira).

---

## 9. Anexos

As tabelas por município (65 linhas) não fazem parte desta publicação; estão disponíveis a pedido.
