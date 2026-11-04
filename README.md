# Tópico 3 — Introdução à Avaliação Físico-Química de Proteínas

Minicurso **Introdução à Biologia Computacional aplicada à Saúde**
14ª Semana de Biociências e Biotecnologia em Saúde — FIOCRUZ-PE / Instituto Aggeu Magalhães

## Abrir a aula

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jsartori12/SBBS2026-PyRosetta/blob/main/Topico3_PyRosetta.ipynb)

Clique no botão acima. O notebook roda inteiro no Google Colab — **não é preciso instalar
nada na sua máquina nem baixar os arquivos à parte.**

Antes de começar, recomendamos `Arquivo → Salvar uma cópia no Drive`, para que suas
anotações e resultados fiquem guardados.

> ⏱️ A **primeira célula** instala o PyRosetta e leva de 3 a 8 minutos. Rode-a assim que
> abrir o notebook — ela trabalha enquanto a aula começa.

## O que tem aqui

| Arquivo | O que é |
|---|---|
| `Topico3_PyRosetta.ipynb` | o notebook da aula |
| `binderEC_65_job*.pdb` | os três modelos de *binder* usados na Parte C |

Os três PDBs são complexos de 286 resíduos: a cadeia **A** é um ligante proteico de novo
(65 resíduos) e a cadeia **B** é o alvo (221 resíduos), o mesmo nos três. Os modelos foram
dobrados pelo AlphaFold2 e relaxados no Rosetta. O notebook os baixa daqui sozinho.

## O que a aula cobre

- **Parte A** — o objeto `Pose`, a função de score REF2015, minimização e `FastRelax`
- **Parte B** — modelagem de variantes e cálculo de ΔΔG, com decomposição por termo de energia
- **Parte C** — análise de interface proteína–proteína e comparação de candidatos de design

## Rodando fora do Colab

```bash
pip install pyrosetta-installer py3Dmol
python -c "import pyrosetta_installer; pyrosetta_installer.install_pyrosetta()"
jupyter lab Topico3_PyRosetta.ipynb
```

O notebook encontra os PDBs automaticamente se eles estiverem na mesma pasta.

> O PyRosetta exige licença, gratuita para uso acadêmico:
> <https://els2.comotion.uw.edu/product/pyrosetta>
