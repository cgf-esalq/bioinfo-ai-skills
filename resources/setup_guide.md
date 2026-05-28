# 🛠️ Guia de Setup — Antigravity IDE

Este guia cobre a instalação e configuração do ambiente necessário para os workshops.

## 1. Instalar o Antigravity IDE

1. Acesse [antigravity.dev](https://antigravity.dev/)
2. Faça download da versão para seu sistema operacional
3. Instale seguindo as instruções do instalador
4. Abra o Antigravity e faça login com sua conta Google

## 2. Instalar o R

Se você ainda não tem o R instalado:

```bash
# Ubuntu/Debian
sudo apt update
sudo apt install r-base r-base-dev

# macOS (via Homebrew)
brew install r
```

Verifique a versão (precisa ser ≥ 4.3):

```bash
R --version
```

## 3. Instalar o Quarto

O Quarto é usado para renderizar os slides dos workshops.

```bash
# Ubuntu/Debian
wget https://github.com/quarto-dev/quarto-cli/releases/latest/download/quarto-linux-amd64.deb
sudo dpkg -i quarto-linux-amd64.deb

# macOS
brew install quarto
```

Verifique:

```bash
quarto --version
```

## 4. Instalar pacotes R necessários

Abra o R e execute:

```r
install.packages(c(
  "VariantAnnotation",
  "GenomicRanges",
  "BiocManager",
  "tidyverse",
  "ggplot2",
  "MatrixEQTL"
))

# Pacotes do Bioconductor
BiocManager::install(c(
  "VariantAnnotation",
  "GenomicRanges",
  "Biostrings",
  "rtracklayer"
))
```

## 5. Instalar Science Skills (opcional)

Para instalar as skills de ciência usadas nos workshops:

```bash
npx -y skills add google-deepmind/science-skills/
```

## 6. Clonar o repositório do curso

```bash
git clone https://github.com/cgf-esalq/bioinfo-ai-skills.git
cd bioinfo-ai-skills
```

## 7. Verificar que tudo funciona

Abra o Antigravity IDE na pasta do repositório e peça ao agente:

> "Me diga quais pacotes R estão instalados no meu sistema"

Se ele responder corretamente, seu setup está funcionando! 🎉

---

## Problemas comuns

| Problema | Solução |
|----------|---------|
| `R` não encontrado no terminal | Adicione o R ao `PATH` do sistema |
| Erro ao instalar pacotes Bioconductor | Atualize o R para ≥ 4.3 e reinstale o `BiocManager` |
| Quarto não renderiza | Verifique que o Quarto ≥ 1.4 está instalado |
| Antigravity não conecta | Verifique sua conexão de internet e faça login novamente |
