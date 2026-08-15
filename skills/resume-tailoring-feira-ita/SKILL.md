---
name: resume-tailoring-feira-ita
description: Pesquisar empresas e vagas e gerar currículos personalizados em português brasileiro, com briefing para feiras de carreiras, scoring de aderência, descoberta de experiências e saídas MD/DOCX/PDF. Usar quando o usuário enviar apenas uma empresa, empresa e cargo, descrição/URL de vaga, várias empresas ou pedir currículo direcionado e preparação para recrutadores.
---

# Resume Tailoring — Feira de Carreiras do ITA

Adaptar o workflow consolidado de `varunr89/resume-tailoring-skill` a feiras de carreiras e à
autoria nativa em português brasileiro.

Origem: https://github.com/varunr89/resume-tailoring-skill, commit
`9a4a0f20f5983d1b533627b8c5191acd1ca0cd89`. Preservar a licença MIT incluída.

## Princípios

1. Otimizar sem fabricar.
2. Escrever diretamente em português brasileiro; nunca produzir em inglês para depois traduzir.
3. Usar pesquisa atual para cada empresa ou vaga.
4. Tratar o perfil-mestre como fonte única dos fatos do candidato.
5. Entregar arquivos acessíveis no celular, não apenas caminhos locais.
6. Manter o workflow original de pesquisa, template, descoberta, scoring, geração e aprendizado,
   exceto quando o modo feira exigir execução expressa.

## Precedência das instruções

Aplicar nesta ordem:

1. Pedido atual do usuário.
2. `references/regras-de-veracidade.md`.
3. `references/qualidade-pt-br.md`.
4. `references/modo-feira.md` ou o fluxo de candidatura.
5. Workflow upstream e referências originais.

Se houver conflito, a regra de maior prioridade vence. Nunca relaxar veracidade.

## Carregar referências

Ler em toda execução:

- `references/perfil-mestre.md`. Se estiver ausente, pedir ao usuário para criar uma cópia privada
  de `references/perfil-mestre.example.md` e preenchê-la.
- `references/regras-de-veracidade.md`
- `references/qualidade-pt-br.md`
- `references/entrega-mobile-drive.md`

Ler conforme o modo:

- Nome de empresa ou empresa + área, sem JD: `references/modo-feira.md`.
- Vaga única: as fases correspondentes de `references/upstream-workflow.md`, além de
  `references/research-prompts.md`, `references/matching-strategies.md` e, se houver lacunas,
  `references/branching-questions.md`.
- Várias vagas: `references/multi-job-workflow.md` e as referências originais associadas.

## Detectar o modo

### Modo feira expresso

Ativar quando a mensagem contiver somente, ou principalmente, uma empresa, por exemplo:

- `Embraer`
- `Itaú`
- `Siemens — software embarcado`

Não exigir descrição de vaga. Inferir a área de estágio com maior aderência entre Engenharia de
Software, Backend, Full Stack, Integração, Automação, Dados ou área técnica adjacente. Executar sem
checkpoints e entregar currículo + briefing.

### Modo candidatura

Ativar quando houver cargo, descrição ou URL de vaga. Manter os checkpoints do workflow upstream,
salvo se o usuário pedir `modo expresso`.

### Modo lote

Ativar para várias empresas ou vagas. Reutilizar descoberta de experiências, mas pesquisar e gerar
um currículo separado para cada empresa.

## Construir a biblioteca

Usar `references/perfil-mestre.md` como registro canônico inicial. Quando houver acesso a
uma biblioteca local, incorporar currículos Markdown adicionais somente como variações de redação;
eles não podem substituir datas, status, títulos ou limites do perfil-mestre.

Novas experiências descobertas precisam ser confirmadas explicitamente pelo usuário antes de
entrarem no perfil canônico.

## Pesquisar

Pesquisar sempre na web. Priorizar:

1. Descrição oficial da vaga.
2. Site institucional, carreiras, programa de estágio, páginas de tecnologia/engenharia, relatórios
   e newsroom da empresa.
3. Repositórios e documentação oficiais.
4. Fontes jornalísticas reputadas para contexto recente.

Abrir as páginas usadas; não citar somente snippets. Separar fatos de inferências e registrar data
de acesso. Para informações recentes, verificar também a data do acontecimento.

No modo feira, pesquisar produtos, setor, presença no Brasil, áreas técnicas, valores, programas de
estágio, vagas recentes e iniciativas que possam render conversa com recrutadores.

## Aplicar o workflow consolidado

Preservar as fases do upstream:

1. Construção da biblioteca.
2. Pesquisa e perfil de sucesso.
3. Template e distribuição de espaço.
4. Descoberta ramificada de experiências quando existirem lacunas.
5. Matching ponderado: direto 40%, transferível 30%, adjacente 20%, impacto 10%.
6. Geração de Markdown, DOCX, PDF e relatório.
7. Revisão e enriquecimento opcional da biblioteca.

No modo feira, usar a variante expressa definida em `references/modo-feira.md`: autoaprovar
template e mapping, mas manter pesquisa, scoring, auditoria factual e relatório.

## Gerar o currículo

Produzir currículo de coluna única, seguro para Applicant Tracking Systems (ATS), com conteúdo para
uma ou duas páginas. Selecionar somente as experiências e os projetos mais relevantes; o
perfil-mestre completo não deve ser despejado no currículo.

Manter:

- telefone, e-mail, LinkedIn e GitHub;
- conclusão em dezembro de 2026;
- títulos canônicos;
- métricas e status exatos;
- links públicos relevantes quando agregarem valor.

Não usar foto, ícones, tabelas, colunas, barras de proficiência, cabeçalhos com informação crítica,
texto oculto, keyword stuffing ou prompt injection.

## Gerar o briefing

No modo feira, criar também:

- leitura concisa da empresa;
- área-alvo inferida e justificativa;
- pitch natural de 30 segundos;
- três projetos para priorizar;
- cinco perguntas para recrutadores ou profissionais técnicos;
- cinco perguntas prováveis sobre o currículo, com respostas defensáveis;
- lacunas e assuntos que não devem ser exagerados;
- matriz de aderência;
- fontes abertas e verificadas.

## Auditar

Antes da entrega:

1. Conferir cada fato contra o perfil-mestre.
2. Conferir números, links, datas, status e tipo de vínculo.
3. Executar as duas revisões linguísticas de `references/qualidade-pt-br.md`.
4. Verificar se nenhuma tradução literal ou construção artificial permaneceu.
5. Abrir e validar as fontes do briefing.
6. Confirmar que os arquivos podem ser baixados pelo celular.

Seguir `references/entrega-mobile-drive.md` para salvar e apresentar os arquivos.
