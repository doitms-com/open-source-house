# Doitms Casa — DC-T1: documentação técnica de referência

Desenhos de arquitectura, ficheiros 3D da casa, cálculos de engenharia e documentação das redes de serviços da casa DC-T1 (tipologia T1) da Doitms Casa, gerados a partir do modelo da Doitms Casa e publicados sob a licença CC BY-SA 4.0. Selo do modelo: `c2d1ffeb79f1`.

Selo calculado sobre a árvore de trabalho com alterações não registadas; a publicação oficial faz-se a partir de um commit limpo.

> **Leia primeiro o [AVISO](AVISO.md).** Esta publicação é documentação de referência: não é um projecto, não tem termo de responsabilidade de arquitecto nem de engenheiro e não serve para construir sem profissionais habilitados.

## O que está publicado

- **Desenhos de arquitectura** em `desenhos/`: 11 folhas do DC-T1 (planta, cobertura, fundação, alçados norte, sul, este e oeste, cortes AA e BB, planta de mobiliário e esquema unifilar), cada uma em SVG (`desenhos/svg`), DXF (`desenhos/dxf`) e PDF (`desenhos/pdf`). A legenda de cada folha leva o selo do modelo, a licença e o aviso.
- **Mapa de vãos** em `desenhos/mapa-vaos/`: quadro das janelas e portas do T1 (dimensões, orientação e características térmicas e acústicas), em CSV, JSON e Markdown.
- **Modelo 3D da casa** em `3d/`: `T1.blend` (Blender) e `T1.glb` (glTF binário) com a casa no estado base, em materiais genéricos, sem equipamento do produto nem peças de montagem; `3d/T1.nomes.json` é a lista dos nomes dos objectos do modelo.
- **Cálculos de engenharia** em `engenharia/`: extracto da memória de cálculo estrutural e combinações de acções (Eurocódigo 0); verificação sísmica do T1 (Eurocódigo 8; tabela `engenharia/ec8-estado-t1.csv`, só com o estado T1); desempenho térmico (REH) para uma zona climática de referência (I1/V2); acústica de fachadas; iluminação artificial e luz natural; estudos de percurso solar. As tabelas por concelho (acções sísmica, do vento e da neve, entre outras) não fazem parte desta publicação; estão disponíveis a pedido.
- **Documentação de serviços** em `servicos/`: águas, drenagem, instalação eléctrica, telecomunicações (ITED) e segurança contra incêndio (SCIE) do T1, com as tabelas de circuitos e de pontos. O esquema unifilar está entre as folhas de desenho.
- **`MANIFESTO.json`**: lista de todos os ficheiros desta publicação, com o caminho, o tamanho e o sha256 de cada um, o selo do modelo e a data. Serve para confirmar que um ficheiro é o que foi publicado.

Os ficheiros são gerados, não escritos à mão: quando o modelo muda, a publicação é regenerada e o selo muda com ela.

## Licença

A documentação (desenhos, relatórios, tabelas e ficheiros 3D) está licenciada sob **CC BY-SA 4.0** (Creative Commons Attribution-ShareAlike 4.0 International: atribuição e partilha nas mesmas condições).

- Pode copiar, redistribuir, adaptar e usar comercialmente, desde que dê o crédito, com a atribuição da secção «Como citar» (é a que o licenciante pede), indique se fez alterações e partilhe o material adaptado sob a mesma licença.
- A licença cobre os direitos de autor sobre esta documentação. Não licencia marcas nem patentes (ver [MARCA](MARCA.md)) e não faz desta documentação um projecto (ver [AVISO](AVISO.md)). Também não se estende ao material de terceiros que a documentação cite ou use (normas técnicas, legislação, cartografia e dados de entidades públicas), que mantém as suas próprias condições.
- O texto integral está em [LICENSE](LICENSE): é a cópia do texto «Attribution-ShareAlike 4.0 International» que acompanha o pacote de software cryptsetup (ficheiro COPYING.CC-BY-SA-4.0). Em caso de dúvida vale o texto oficial da Creative Commons, em https://creativecommons.org/licenses/by-sa/4.0/legalcode.

## Aviso

Esta publicação não é projecto de licenciamento nem de execução; não tem termo de responsabilidade de arquitecto nem de engenheiro; não substitui o projecto subscrito por técnico com inscrição válida na Ordem dos Arquitectos ou na Ordem dos Engenheiros. **Não construa a partir destes ficheiros sem profissionais habilitados.** Sem garantia: verifique tudo contra o terreno, o plano director municipal e a lei em vigor. O texto completo está em [AVISO](AVISO.md).

## Marca

«Doitms», «DOITMS», «Doitms Casa» e o logótipo não estão licenciados: a marca é reservada. Pode citar o nome para identificar a origem desta documentação; não o use para nomear produtos, empresas ou obras derivadas, nem para sugerir patrocínio ou aprovação. Ver [MARCA](MARCA.md).

## Desenhos em DXF e FreeCAD

- Os DXF das folhas são DXF versão R2018 (AC1032) e abrem no AutoCAD e no FreeCAD. O DXF do esquema unifilar é DXF R12 (uma versão mais antiga do formato) e também abre nos dois.
- Os ficheiros nativos do FreeCAD (`.FCStd`) só se produzem quando a publicação é gerada com a opção `--fcstd` numa máquina com o FreeCAD instalado: o exportador converte cada DXF com um script próprio, executado pelo FreeCADCmd, que não faz parte desta publicação. Esta publicação não inclui ficheiros `.FCStd`.
- Em qualquer caso pode abrir ou importar o DXF no FreeCAD e guardá-lo como `.FCStd`.

## Estado do conteúdo de engenharia

O conteúdo de engenharia (cálculo estrutural, verificação sísmica, desempenho térmico, acústica, iluminação e redes de serviços) é publicado com o estado que tem na data da publicação:

- É **PROVISÓRIO** e não está assinado: não foi revisto por engenheiro com inscrição válida e não tem termo de responsabilidade nem assinatura de técnico. Os campos que dependem de um técnico estão por preencher e dizem-no.
- Cada relatório em Markdown de `engenharia/` e `servicos/` começa por um cabeçalho de estado, gerado a partir do próprio relatório, que lista o que está provisório, por preencher ou por cumprir. Leia-o antes do corpo do relatório. As tabelas CSV e as figuras SVG não têm cabeçalho: valem o estado do relatório a que pertencem e o que se diz aqui.
- Nesta versão há resultados que não cumprem os requisitos ou que têm margens abaixo do desejável (por exemplo, o isolamento sonoro de fachada e a margem da verificação sísmica), e há inconsistências conhecidas entre documentos (por exemplo, o esquema unifilar e o quadro de circuitos da instalação eléctrica ainda não foram reconciliados). Não foram escondidas nem corrigidas aqui.
- Cálculos do REH: Ntc, R e classe SCE incluem autoconsumo fotovoltaico de uma opção não publicada, pelo que esses valores não são os da casa sem essa opção.
- Nada nesta publicação deve ser lido como afirmação de que a casa cumpre um regulamento: isso só pode ser afirmado por técnico habilitado, sobre o projecto e o lote concretos.

## Visão Geral

Visão Geral pública: pendente; será incluída quando o gerador de documentação estiver pronto.

## Contribuições

Esta publicação é gerada a partir de um modelo que não é publicado e é refeita em cada nova versão. O repositório desta publicação é https://github.com/doitms-com/open-source-house. Correcções, dúvidas e propostas entram como *issues* deste repositório, em https://github.com/doitms-com/open-source-house/issues; os *pull requests* não são fundidos aqui, porque seriam substituídos na versão seguinte. O que for aceite aplica-se no modelo e chega a esta publicação na versão seguinte. As tabelas por concelho, quando não estão publicadas, pedem-se da mesma forma.

## Como citar

Doitms Casa — DC-T1 documentação técnica de referência, selo c2d1ffeb79f1, 2026-10-15T13:56:08+01:00

Ao partilhar material adaptado, indique que foi alterado e use a mesma licença (CC BY-SA 4.0).
