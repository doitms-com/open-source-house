> **Estado do conteúdo de engenharia** (cabeçalho gerado)
>
> Cabeçalho gerado a partir do próprio relatório: diz o que está provisório, por preencher ou por cumprir, antes do corpo.
>
> - **Campos.** Há 6 campos por preencher, entre parênteses rectos ([morada da obra], [concelho], [nome do dono da obra], [NIF do dono da obra], [nome do técnico ITED], [n.º ANACOM do técnico]): dependem do lote, do dono da obra ou de um técnico e estão vazios.
> - **Assinatura.** Documento não assinado: sem assinatura de técnico habilitado; o relatório não foi revisto por técnico com inscrição válida.
>
> Documento técnico de referência: não é projecto e não serve para construir sem profissionais licenciados (ver `AVISO.md`, na raiz da publicação).

# Projecto ITED — Casa Base T1 (`DC-T1`)

**Regime.** DL n.º 123/2009 (com alterações) + **Manual ITED 4.ª edição
(ANACOM)**. Obrigatório em toda a construção nova: projecto por técnico
ITED inscrito na ANACOM, instalação por instalador ITED, ensaios antes da ligação às redes públicas.

**Produto.** Casa Base T1 — 54.0 m² ·
7 janelas · pontos RIT do modelo paramétrico.
**Local da obra.** [morada da obra] · [concelho].
**Dono da obra.** [nome do dono da obra], NIF [NIF do dono da obra].
**Técnico ITED (projecto).** [nome do técnico ITED], ANACOM n.º
[n.º ANACOM do técnico].

---

## 1. Arquitectura da rede

- **Entrada**: tubagem enterrada Ø63 (2 tritubos + guia)
  do limite do lote ao ATI — ocupação de projecto ≤ 50 % ✓.
- **ATI** integrado na central técnica: RG-PC (par de cobre),
  RG-CC (coaxial), RG-FO (2 fibras SM G.657A2, SC/APC).
- **Rede individual**: tubo Ø25 corrugado em ESTRELA
  do ATI a cada tomada, pelo rodapé técnico Doitms (sem roços; acesso
  por alçapões AI-0x do modelo).
- **Cabos**: S/FTP Cat 6A LSZH (RJ45), RG-6 LSZH (coaxial).

## 2. Tomadas por compartimento (pontos RIT do MODELO — não estimativa)

| Compartimento | RJ45 Cat 6A | Coaxial | Tubagem | Ocupação/tubo |
|---|---|---|---|---|
| quarto | 1 | 0 | Ø25 × 1 | 7.8 % |
| sala | 1 | 1 | Ø25 × 2 | 7.8 % |

**Totais: 2 × RJ45 + 1 × tomada mista (coaxial +
RJ45).** Verificação dos mínimos do Manual ITED 4.ª ed. (moradia): 1
tomada de dados por compartimento principal ✓ (sala + cada quarto —
pontos do modelo); ≥ 1 tomada coaxial por fogo ✓ (sala, tomada mista);
fibra óptica terminada no ATI ✓ (2 FO). O técnico ITED confirma a
edição do Manual em vigor à data do projecto.

## 3. Dimensionamento de tubagem

Regra de ocupação ≤ 50 % (Manual ITED §6): cada tubo Ø25
transporta 1 cabo Ø7 → ocupação 7.8 % ✓. Reserva: 1 tubo
vago do ATI ao tecto falso do hall (expansão futura).

## 4. Ensaios obrigatórios (conclusão)

1. Par de cobre: mapa de pares, comprimento, classe E_A certificada
   (certificador de cablagem).
2. Coaxial: continuidade + atenuação.
3. Fibra: continuidade óptica + atenuação (power-meter/reflectómetro).

Registar no ficheiro não publicado.

## 5. Peças do projecto

1. Esta memória (gerada do modelo — ficheiro não publicado).
2. Planta com pontos RIT: folha `planta` (camada MEP) em `desenhos/`.
3. Quadro de tomadas (secção 2) + `servicos/ited-tomadas.csv`.
