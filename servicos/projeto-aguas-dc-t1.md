> **Estado do conteúdo de engenharia** (cabeçalho gerado)
>
> Cabeçalho gerado a partir do próprio relatório: diz o que está provisório, por preencher ou por cumprir, antes do corpo.
>
> - **Campos.** Há 5 campos por preencher, entre parênteses rectos ([morada da obra], [concelho], [nome do dono da obra], [nome do técnico responsável], [n.º de inscrição do técnico]): dependem do lote, do dono da obra ou de um técnico e estão vazios.
> - **Assinatura.** Documento não assinado: sem assinatura de técnico habilitado; o relatório não foi revisto por técnico com inscrição válida.
>
> Documento técnico de referência: não é projecto e não serve para construir sem profissionais licenciados (ver `AVISO.md`, na raiz da publicação).

# Projecto de abastecimento de água — Casa Base T1 (`DC-T1`)

**Regime.** DL n.º 23/95 (RGSPPDADAR — Regulamento Geral dos Sistemas
Públicos e Prediais de Distribuição de Água e de Drenagem de Águas
Residuais) + NP EN 806 (série) + regulamento municipal do concelho da
obra. Projecto de especialidade para licenciamento RJUE.

**Obra.** [morada da obra], [concelho] · **Dono da obra.**
[nome do dono da obra] · **Técnico responsável.** [nome do técnico responsável],
[n.º de inscrição do técnico].

---

## 1. Descrição da instalação (do modelo paramétrico)

| Parâmetro | Valor | Referência regulamentar |
|---|---|---|
| Pontos de água fria (modelo) | 8 | RGSPPDADAR Art. 86.º (dotações) |
| Pontos de água quente (modelo) | 4 | idem |
| Caudal de cálculo Q | **1.137 ℓ/s** | RGSPPDADAR Art. 90.º + NP EN 806-3 fig. 7 |
| Consumo diário estimado | 260 ℓ/dia | Art. 86.º (capitação ≥ 100 ℓ/hab·dia) |
| Pressão de serviço mínima | 1.5 bar | Art. 87.º (conforto: 50 + 5·n kPa) |
| AQS | bomba de calor 1500 W, depósito 80 ℓ | Art. 93.º-95.º (rede AQ) + EN 16147 |

## 2. Concepção

1. **Manifold central PEX-AL-PEX** na central técnica com ramais individuais 16×2 a
   cada ponto (Art. 88.º-89.º — traçado acessível, sem troços mortos):
   substituição de qualquer ramal sem abrir paredes (rodapé técnico).
2. **Entrada** DN20 com contador (Art. 105.º — a instalar pela entidade
   gestora), válvula de seccionamento e **anti-retorno categoria 3
   (EN 1717)** (Art. 96.º — protecção da rede pública).
3. **AQ**: produção por bomba de calor na central técnica; retorno dispensado
   (comprimentos < 15 m — Art. 95.º).
4. Materiais com certificação de contacto com água potável (Art. 84.º).
5. Válvula de corte motorizada + sensor de inundação na central técnica (acima do
   regulamentar — mitigação de dano).

## 3. Peças

1. Esta memória + dimensionamento (`mep-aguas-dc-t1.csv`).
2. Planta com pontos AF/AQ: folha `planta` em `desenhos/`
   (camada MEP do modelo).
