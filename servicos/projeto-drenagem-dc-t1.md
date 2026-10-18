> **Estado do conteúdo de engenharia** (cabeçalho gerado)
>
> Cabeçalho gerado a partir do próprio relatório: diz o que está provisório, por preencher ou por cumprir, antes do corpo.
>
> - **Campos.** Há 4 campos por preencher, entre parênteses rectos ([morada da obra], [concelho], [nome do dono da obra], [nome do técnico responsável]): dependem do lote, do dono da obra ou de um técnico e estão vazios.
> - **Assinatura.** Documento não assinado: sem assinatura de técnico habilitado; o relatório não foi revisto por técnico com inscrição válida.
>
> Documento técnico de referência: não é projecto e não serve para construir sem profissionais licenciados (ver `AVISO.md`, na raiz da publicação).

# Projecto de drenagem de águas residuais e pluviais — Casa Base T1 (`DC-T1`)

**Regime.** DL n.º 23/95 (RGSPPDADAR, Títulos IV-V) + NP EN 12056 +
regulamento municipal. Projecto de especialidade para licenciamento RJUE.

**Obra.** [morada da obra], [concelho] · **Dono da obra.**
[nome do dono da obra] · **Técnico responsável.** [nome do técnico responsável].

---

## 1. Águas residuais domésticas (ARD)

| Parâmetro | Valor | Referência |
|---|---|---|
| Pontos de descarga (modelo) | 5 | RGSPPDADAR Art. 207.º (caudais de descarga) |
| Ramais lavatório/duche | Ø50 mm | Art. 210.º + NP EN 12056-2 |
| Ramal de sanita | Ø100 mm | idem |
| Colector predial | Ø110 mm @ 2.0 % | Art. 214.º (pendente 1-4 %) |
| Ventilação primária | Ø50 até à cobertura | Art. 217.º-221.º (ventilação) |
| Sifões | individuais, fecho hídrico ≥ 50 mm | Art. 211.º-212.º |

Ligação: à rede pública quando exista (Art. 3.º — obrigatória); em
alternativa, sistema autónomo licenciado — ver ficheiro não publicado (fossa/ETAR compacta com
Licença de Utilização dos Recursos Hídricos, DL 226-A/2007).

## 2. Águas pluviais

| Parâmetro | Valor | Referência |
|---|---|---|
| Área de cobertura | 54.0 m² | modelo paramétrico |
| Intensidade de cálculo | caso mais desfavorável nacional (Madeira, 140 mm/h em 10 min, T=10 anos) | RGSPPDADAR Art. 249.º + Anexo IX |
| Caleiras | Ø150 mm | NP EN 12056-3 |
| Tubos de queda | 2 × Ø100 mm | Art. 255.º-258.º |
| Capacidade total (c/ +30 %) | 2.73 ℓ/s | política Doitms (reserva) |

Destino: rede pluvial pública, valeta ou infiltração no lote (poço
absorvente) conforme regulamento municipal — SEM ligação à rede de ARD
(Art. 202.º — sistemas separativos).

## 3. Peças

1. Esta memória + `mep-drenagem-dc-t1.csv`.
2. Planta (camada MEP): folha `planta` em `desenhos/`.
