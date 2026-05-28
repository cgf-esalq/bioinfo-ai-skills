# Exercícios — Workshop 1: Anatomia de Skills

## Exercício 1: Explorando Skills Instaladas

Abra o terminal e explore a estrutura das skills instaladas:

```bash
# Liste todas as skills
ls .agents/skills/

# Explore a skill do UniProt
cat .agents/skills/uniprot-database/SKILL.md

# Compare com a skill do STRING
cat .agents/skills/string-database/SKILL.md
```

**Perguntas:**
1. Quais seções em comum as duas skills têm?
2. Alguma skill tem scripts auxiliares? Quais?
3. Como as instruções são organizadas (lista, texto corrido, etc.)?

---

## Exercício 2: Busca de Gene com gget

Abra o Antigravity e peça ao agente:

> "Use o gget para buscar informações do gene **DGAT1** em *Bos taurus*. Me diga: em qual cromossomo está, quantos transcritos tem, e qual a sua função principal."

**Validação:** Compare com as informações no [Ensembl](https://www.ensembl.org/Bos_taurus/Gene/Summary?g=ENSBTAG00000026356).

---

## Exercício 3: Busca de Artigos no PubMed

Peça ao agente:

> "Busque no PubMed os 5 artigos mais recentes sobre **structural variants in Bos taurus**. Liste título, autores e ano."

**Validação:** Abra o [PubMed](https://pubmed.ncbi.nlm.nih.gov/?term=structural+variants+Bos+taurus) e compare.

---

## Exercício 4: Interações Proteicas no STRING

Peça ao agente:

> "Quais são as 10 principais proteínas que interagem com DGAT1 em bovinos segundo o STRING database? Qual o score de confiança de cada interação?"

**Reflexão:** O agente usou uma skill, um tool MCP, ou ambos? Como você sabe?

---

## Exercício 5: Obter Sequência do UniProt

Peça ao agente:

> "Obtenha a sequência de aminoácidos da proteína DGAT1 bovina do UniProt em formato FASTA. Salve em `data/sample/DGAT1_bos_taurus.fasta`."

**Verificação:** O arquivo foi criado? O conteúdo parece correto?

---

## Exercício 6 (Para casa): Brainstorm de Skills

Pense em **2-3 tarefas repetitivas** do seu projeto de pesquisa que poderiam ser automatizadas com uma skill.

Para cada ideia, anote:
1. **Nome** da skill
2. **O que ela faz** (1-2 frases)
3. **Inputs** (o que ela precisa receber)
4. **Outputs** (o que ela produz)
5. **Por que** seria útil ter como skill

Traga essas ideias para o **Workshop 2**!
