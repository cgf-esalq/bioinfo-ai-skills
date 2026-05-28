# 🧬 bioinfo-ai-skills

**Workshop de IA Responsável para Bioinformática Genômica**

Material de apoio para uma série de workshops práticos ensinando alunos de pós-graduação (mestrado e doutorado) a utilizar inteligência artificial de forma responsável como ferramenta de auxílio em projetos de genômica.

---

## 📋 Sobre o Curso

| | |
|---|---|
| **Público-alvo** | Alunos de pós-graduação em genômica/bioinformática |
| **Nível** | Intermediário (familiaridade com R e conceitos de genômica) |
| **Ferramenta** | [Antigravity IDE](https://antigravity.dev/) |
| **Organismo modelo** | *Bos taurus* (bovino) |
| **Formato** | Workshops de ~2h, a cada 3 semanas |
| **Linguagem principal** | R |

## 🗓️ Cronograma

| Workshop | Tema | Status |
|----------|------|--------|
| WS1 | [Anatomia de Skills e Ecossistema de Tools](workshops/01-anatomia-skills/) | 🔜 Próximo |
| WS2 | [Criando sua Primeira Skill](workshops/02-criando-skills/) | ⏳ Planejado |

> **Nota:** Este curso assume conhecimento básico de Git/GitHub e do funcionamento básico de LLMs.

## 🚀 Setup

Antes do primeiro workshop, siga o [Guia de Setup](resources/setup_guide.md) para instalar e configurar o ambiente.

### Pré-requisitos

- R ≥ 4.3
- [Quarto CLI](https://quarto.org/docs/get-started/) (para renderizar slides)
- [Antigravity IDE](https://antigravity.dev/) instalado e configurado
- Conta no GitHub

### Clonar o repositório

```bash
git clone https://github.com/cgf-esalq/bioinfo-ai-skills.git
cd bioinfo-ai-skills
```

## 📂 Estrutura do Repositório

```
bioinfo-ai-skills/
├── workshops/           # Material de cada workshop (slides, exercícios)
│   ├── 01-anatomia-skills/
│   └── 02-criando-skills/
├── rules/               # "Constituições" globais de segurança e estilo
├── skills/              # Skills de referência modulares
├── workflows/           # Pipelines orquestrando múltiplas skills
├── data/                # Dados de exemplo para exercícios
│   └── sample/
├── resources/           # Guias, cheatsheets e referências
└── LICENSE              # CC-BY-4.0
```

## 🎯 Objetivos de Aprendizagem

Ao final do curso, os alunos serão capazes de:

1. **Compreender** o que são skills e como agentes de IA os utilizam
2. **Criar** skills personalizadas para automatizar tarefas de bioinformática
3. **Construir** pipelines de análise de variantes genômicas com auxílio de IA
4. **Avaliar criticamente** outputs gerados por IA e garantir reprodutibilidade
5. **Aplicar** princípios de uso responsável de IA em pesquisa científica

## 📖 Recursos Adicionais

- [Guia de Setup](resources/setup_guide.md)
- [Engenharia de Prompt para Bioinformática](resources/prompt_engineering.md)
- [Links Úteis](resources/useful_links.md)

## 📄 Licença

Este material é distribuído sob a licença [CC-BY-4.0](LICENSE). Você é livre para compartilhar e adaptar, desde que atribua crédito apropriado.

---

**Organização**: [CGF-ESALQ](https://github.com/cgf-esalq)  
**Contato**: [@cavalheiromf](https://github.com/cavalheiromf)
