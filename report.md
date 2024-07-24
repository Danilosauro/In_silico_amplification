# Relatório de Análise Genômica e Amplificação In Silico

## 1. Introdução

Este relatório descreve o procedimento e os resultados de uma análise de amplificação in silico para identificar a presença de sequências alvo em genomas bacterianos, utilizando primers com ambiguidades. A análise inclui a extensão dos primers, a busca de amplificação em genomas, a obtenção da sequência amplificada e a identificação do microrganismo e do gene envolvido.

## 2. Procedimento Realizado

### 2.1 Extensão dos Primers com Ambiguidade

Para lidar com primers que contêm símbolos de ambiguidade IUPAC, os seguintes passos foram realizados:

- **Definição dos Primers com Ambiguidade:**
  - **Forward Primer:** `GCDGCHGCNATGCGTTAYAC`
  - **Reverse Primer:** `ACAAGMTCWGCKATTTTTTC`
                

- **Expansão dos Primers:**
  A expansão dos primers com símbolos de ambiguidade foi realizada manualmente, criando todas as possíveis combinações de nucleotídeos para cada símbolo de ambiguidade. As possíveis combinações foram calculadas considerando as definições IUPAC para cada símbolo.

  **Combinações:**

  - **Forward Primer:** 72 combinações possíveis.
  - **Reverse Primer:** 8 combinações possíveis.

### 2.2 Busca dos Primers nos Genomas

Após a expansão dos primers, obtivemos os primers reverso-complementares e buscamos essas sequências nos genomas bacterianos disponíveis. O processo envolveu:

- **Carregamento dos Genomas:**
  - Genomas foram carregados de arquivos FASTA localizados na pasta `data`.

- **Verificação de Amplificação:**
  - Cada genoma foi analisado para verificar se as sequências expandidas dos primers forward e reverse estavam presentes, considerando a orientação e a distância entre os primers para avaliar a possibilidade de amplificação.

  - **Nota Importante:** A avaliação da amplificação foi realizada com base no par de primers como um todo e não de forma individual. Ou seja, a presença dos primers forward e reverse foi verificada simultaneamente, garantindo que ambos estivessem na orientação e distância corretas para formar um produto de amplificação.

  **Resultado:**
  - Identificou-se apenas um genoma que amplificava a sequência entre os primers fornecidos - este, inerente ao arquivo 'genome_05.fna'.
 
  - Informações acerca da amplificação: 'data/genome_05.fna contig_0 amplificação dupla -  com o foward primer: GCGGCCGCGATGCGTTACAC e    amplificação com o reverso complementar GAAAAAATCGCAGATCTTGT'

### 2.3 Obtenção da Sequência Amplificada

Para o genoma identificado, a sequência amplificada foi extraída com base nas posições fornecidas pelo BLAST. A sequência foi salva no formato FASTA.

- **Região Amplificada:**
  - **Início:** 6943
  - **Fim:** 7433
  - A sequência amplificada foi extraída e salva para análise posterior.

### 2.4 Identificação do Microrganismo

A sequência amplificada foi submetida ao BLAST para identificar o microrganismo:

- **Microrganismo Identificado:**
  - **Bacillus velezensis strain AP215**
  - **Genoma Completo:** CP160221.1
  - **Sequenciamento:** Utilização da ferramenta Oxford-Nanopore para sequenciamento de genoma completo.

### 2.5 Hipótese do Gene Utilizado

Com base na identificação do microrganismo e na análise da sequência amplificada, formulamos a seguinte hipótese sobre o gene envolvido:

- **Gene:**
  A sequência amplificada corresponde a uma região específica do genoma do **Bacillus velezensis strain AP215**. A análise sugere que essa região pode estar associada a genes que desempenham funções relevantes para o microrganismo, como a biossíntese de lipopeptídeos. Lipopeptídeos são conhecidos por suas propriedades antibióticas e podem desempenhar um papel crucial na interação do microrganismo com seu ambiente. Obtivemos a identificação do gene gyrA, um marcador biológico utilizado em estudos ecológicos envolvendo o gênero Bacillus.

## 3. Resultados

1. **Primers Expandidos:**
   - Forward Primer: 72 combinações.
   - Reverse Primer: 8 combinações.

2. **Genoma Identificado:**
   - **Bacillus velezensis strain AP215**
   - **Fonte de Sequenciamento:** Nanopore

3. **Sequência Amplificada:**
   - Região: 6943 a 7433 no genoma CP160221.1.

4. **Sequência:**
   - GCGGCCGCGATGCGTTACACAGAAGCGAGAATGTCAAAAATCGCAATGGAAATCCTCCGGGACATTACGAAAGATACGATTGATTATCAAGATAACTATGACGGCGCAGAAAGAGAACCTGTCGTCATGCCTTCGAGATTTCCGAATCTGCTCGTAAACGGAGCTGCCGGTATTGCGGTCGGAATGGCGACAAATATTCCTCCGCATCAGCTTGGGGAAGTCATTGAAGGCGTGCTTGCCGTAAGTGAGAATCCTGAGATTACAAACCAGGAGCTGATGGAATACATCCCGGGCCCGGATTTTCCGACTGCAGGTCAGATTTTGGGCCGGAGCGGCATCCGCAAGGCATATGAATCCGGACGGGGATCCATTACGATCCGGGCTAAGGCTGAAATCGAAGAGACATCATCGGGAAAAGAAAGAATTATTGTCACAGAACTTCCTTATCAGGTGAACAAAGCGAGATTAATTGAAAAAATCGCAGATCTTGT

5. **Hipótese do Gene:**
   - Gene gyrA, tido como um marcador molecular para estudo ecológico do gênero Bacillus.

## 4. Discussão

- **Árvore Filogenética:** A construção de uma árvore filogenética não foi realizada neste estudo, pois o foco foi na avaliação da amplificação in silico e na identificação da sequência amplificada em um genoma específico. A análise filogenética geralmente requer uma comparação de várias sequências de diferentes organismos e foi considerada fora do escopo atual.

- **Busca do Par de Primers:** A amplificação foi avaliada com base na presença do par de primers como um todo, e não individualmente. A abordagem garantiu que o produto amplificado fosse formado corretamente, considerando a orientação e a distância entre os primers.

## 5. Conclusão

A análise demonstrou que, entre os genomas testados, apenas o genoma do **Bacillus velezensis strain AP215** apresentou amplificação com os primers fornecidos. A sequência amplificada corresponde a uma região específica do genoma relacionada com o gene gyrA.

## 6. Referências

- **NCBI Genomic Data for Bacillus velezensis strain AP215**
    https://www.ncbi.nlm.nih.gov/nuccore/CP160221.1?report=graph&rid=A2GC48G4016[CP160221.1]&tracks=[key:gene_model_track,CDSProductFeats:false] key:sequence_track,name:Sequence,display_name:Sequence,id:STD1,category:Sequence,annots:Sequence,ShowLabel:true][key:gene_model_track,CDSProductFeats:false][key:alignment_track,name:other%20alignments,annots:NG%20Alignments|Refseq%20Alignments|Gnomon%20Alignments|Unnamed,shown:false]&v=6943:6962&appname=ncbiblast&link_loc=fromHSP
