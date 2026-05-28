# 🎯 Engenharia de Prompt para Bioinformática

Um guia prático de como formular boas perguntas e instruções para agentes de IA em contextos de bioinformática.

---

## Princípios Fundamentais

### 1. Seja Específico sobre o Contexto Biológico

❌ **Ruim:**
> "Analise esse arquivo VCF"

✅ **Bom:**
> "Leia o arquivo `bovine_variants.vcf.gz` que contém variantes de SNP de *Bos taurus* (genoma de referência ARS-UCD1.3). Filtre variantes com qualidade QUAL > 30 e profundidade DP > 10. Use o pacote `VariantAnnotation` do R."

### 2. Defina o Output Esperado

❌ **Ruim:**
> "Faça um gráfico das variantes"

✅ **Bom:**
> "Crie um Manhattan plot das variantes do cromossomo 1 ao 29 de bovinos, usando ggplot2. O eixo X deve mostrar a posição genômica e o eixo Y o -log10(p-value). Destaque variantes com p < 5e-8 em vermelho."

### 3. Especifique Ferramentas e Pacotes

❌ **Ruim:**
> "Anote essas variantes"

✅ **Bom:**
> "Use o pacote `VariantAnnotation` do Bioconductor para anotar as variantes no VCF contra o banco TxDb do Ensembl para *Bos taurus* (ARS-UCD1.3). Classifique cada variante como intergênica, intrônica, sinônima ou missense."

### 4. Forneça Contexto do Projeto

Antes de pedir análises complexas, dê contexto:

> "Estou trabalhando em um projeto de GWAS em bovinos da raça Nelore. Temos dados de genotipagem por sequenciamento (GBS) de 200 animais. O fenótipo de interesse é ganho de peso diário. Preciso construir um pipeline que vá do VCF filtrado até a identificação de regiões candidatas."

---

## Padrões Úteis

### Padrão: Pedir Explicação Antes do Código

> "Antes de escrever o código, me explique conceitualmente quais são as etapas necessárias para uma análise de eQTL em bovinos, considerando que temos dados de RNA-seq e genotipagem. Depois, implemente cada etapa em R."

### Padrão: Revisão Crítica

> "Revise este script R de análise de variantes. Identifique: (1) possíveis bugs, (2) etapas que podem ser otimizadas, (3) verificações de qualidade que estão faltando."

### Padrão: Criar a Partir de Exemplo

> "Veja o script `01_filter_variants.R` e crie um script similar para filtrar variantes estruturais (SVs) ao invés de SNPs. Mantenha o mesmo estilo de código e estrutura de diretórios."

### Padrão: Documentação

> "Documente este script R com: (1) cabeçalho explicando o propósito, (2) comentários em cada bloco lógico, (3) descrição dos parâmetros de entrada e saída."

---

## Erros Comuns a Evitar

| ❌ Evite | ✅ Faça |
|----------|---------|
| Aceitar código sem revisar | Leia e entenda cada linha antes de executar |
| Pedir tudo de uma vez | Divida em etapas menores e valide cada uma |
| Ignorar warnings da IA | Preste atenção quando a IA diz "não tenho certeza" |
| Copiar genomas/caminhos sem verificar | Sempre confirme versões de referência (ex: ARS-UCD1.3) |
| Confiar em estatísticas sem validar | Verifique cálculos com dados de teste conhecidos |

---

## Template de Prompt para Análises

```
## Contexto
- Organismo: [espécie]
- Genoma de referência: [versão]
- Tipo de dado: [WGS/RNA-seq/GBS/etc]
- N amostras: [número]

## Objetivo
[Descreva o que você quer alcançar]

## Ferramentas preferidas
- Linguagem: R
- Pacotes: [liste os que já usa ou prefere]

## Output esperado
- [Arquivo/tabela/gráfico específico]

## Restrições
- [Memória RAM disponível, tempo, etc]
```

---

## Leitura Adicional

- [Prompt Engineering Guide](https://www.promptingguide.ai/) — Guia geral de engenharia de prompt
- [Bioconductor](https://www.bioconductor.org/) — Pacotes R para bioinformática
- [Ensembl Bos taurus](https://www.ensembl.org/Bos_taurus/Info/Index) — Genoma bovino de referência
