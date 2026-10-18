> **Estado do conteúdo de engenharia** (cabeçalho gerado)
>
> Cabeçalho gerado a partir do próprio relatório: diz o que está provisório, por preencher ou por cumprir, antes do corpo.
>
> - **Limitações que o próprio relatório imprime.** 2 pendências declaradas no corpo; não foram escondidas nem resolvidas aqui.
> - **Assinatura.** Documento não assinado: sem assinatura de técnico habilitado; o relatório não foi revisto por técnico com inscrição válida.
> - **Autoconsumo.** Ntc, R e classe SCE incluem autoconsumo fotovoltaico de uma opção não publicada.
>
> Documento técnico de referência: não é projecto e não serve para construir sem profissionais licenciados (ver `AVISO.md`, na raiz da publicação).

# Doitms Casa — Cálculo REH sazonal completo (Nic/Nvc/Ntc) e classe energética

**Regime.** DL 101-D/2020 + Portaria 138-I/2021 (NZEB); método
sazonal (Despacho 15793-I/K/2013, mantido pelo SCE). Complementa a
verificação de requisitos mínimos (`memoria-reh.md`) com as
necessidades nominais e a classe energética estimada para a zona climática de referência (I1/V2).

**Estatuto.** Estimativa completa da equipa Doitms para o dossier-tipo;
o pré-certificado e o certificado SCE são actos próprios do **PQ**
(pendentes — ver minutas em ficheiro não publicado).

## 1. Quadro-resumo — zona climática de referência (I1/V2)

| ZI/ZV | Nic ≤ Ni | Nvc ≤ Nv | Ntc ≤ Nt | R | Classe |
|---|---|---|---|---|---|
| I1/V2 | 26.1 ≤ 49.5 ✓ | 23.7 ≤ 31.6 ✓ | 2.7 ≤ 93.4 ✓ | 0.028 | **A+** |

**Resultado: zona climática de referência (I1/V2) conforme**; classe estimada: A+.

## 2. Método e pressupostos

1. **Nic** = (Qtr,i + Qve,i − η·(Qint,i + Qsol,i)) / Ap, com GD e M da zona climática de referência (I1/V2); U de parede corrigido de pontes térmicas dos montantes
   (ISO 6946 §6.7) + 5 % de agravamento plano para pontes lineares.
2. **Ni** com edifício de referência (U_ref da Portaria 138-I/2021,
   A_w/Ap = 20 %, ganhos solares de referência 0.182·G_sul).
3. **Nvc** por balanço da estação convencional (Jun-Set, 2928 h),
   factor de utilização EN ISO 13790 com inércia média (a = 2.6),
   protecção móvel activada F_m,v = 0.60; Nv de referência com piso
   histórico por zona (V1 16 · V2 18 · V3 22 kWh/m²·ano).
4. **Ntc** com sistemas reais (BC AVAC SCOP 3.4/SEER 3.0; BC AQS
   COP 2.8; Fpu 2.5) abatido do autoconsumo fotovoltaico (opção), Art. 26.º;
   **Nt** com sistemas de referência SEM renovável.
5. Classe SCE por R = Ntc/Nt (A+ ≤ 0.25 < A ≤ 0.50 < B ≤ 0.75 <
   B- ≤ 1.00).

## 3. Pendentes obrigatórios (PQ)

1. Validação dos pressupostos + emissão do pré-certificado SCE no
   portal (licenciamento) e do certificado SCE (venda/utilização).
2. Correcção de pontes térmicas lineares por catálogo ITE/LNEC ou
   ISO 10211 quando o PQ correr o modelo de detalhe.
