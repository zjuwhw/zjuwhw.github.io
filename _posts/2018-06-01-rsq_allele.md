---
layout: post
title: LD and Allele frequency
date: 2018-06-01
tags: ["GWAS","genetics"]
---

-   [Linkage Disequilibrium (LD)](#linkage-disequilibrium-ld)
    -   [Haplotype and Allele
        Frequencies](#haplotype-and-allele-frequencies)
    -   [Measure D](#measure-d)
    -   [Measure *r*<sup>2</sup>](#measure-r2)
    -   [Measure D'](#measure-d-1)
    -   [Notes](#notes)
-   [Quantification of relationship between allele frequencies and
    *r*<sup>2</sup>](#quantification-of-relationship-between-allele-frequencies-and-r2)
-   [Further reading](#further-reading)



### Linkage Disequilibrium (LD)

#### Haplotype and Allele Frequencies

<table>
<thead>
<tr class="header">
<th align="left">Locus A</th>
<th align="left">Locus B Allele 1</th>
<th align="left">Allele 2</th>
<th align="left">Allele frequency</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">Allele 1</td>
<td align="left"><span class="math inline"><em>p</em><sub><em>A</em><em>B</em></sub></span></td>
<td align="left"><span class="math inline"><em>p</em><sub><em>A</em><em>b</em></sub></span></td>
<td align="left"><span class="math inline"><em>p</em><sub><em>A</em></sub></span></td>
</tr>
<tr class="even">
<td align="left">Allele 2</td>
<td align="left"><span class="math inline"><em>p</em><sub><em>a</em><em>B</em></sub></span></td>
<td align="left"><span class="math inline"><em>p</em><sub><em>a</em><em>b</em></sub></span></td>
<td align="left"><span class="math inline"><em>p</em><sub><em>a</em></sub></span></td>
</tr>
<tr class="odd">
<td align="left">Allele frequency</td>
<td align="left"><span class="math inline"><em>p</em><sub><em>B</em></sub></span></td>
<td align="left"><span class="math inline"><em>p</em><sub><em>b</em></sub></span></td>
<td align="left">1</td>
</tr>
</tbody>
</table>

Firstly, as $p_a = 1 - p_A$, $p_b = 1 - p_B$, we can calculate $p_a$ or $p_b$, if we know $p_A$ or $p_B$.

Secondly, as $p_{Ab} = p_{A} - p_{AB}$, $p_{aB} = p_{B} - p_{AB}$, $p_{ab} = 1 - p_{A} - p_{B} + p_{AB}$, we can calcuate $p_{Ab}\text{, }p_{aB}\text{ and }p_{AB}$, if we know $p_{AB}$.

As the frequency of all four haplotype need to be greater or equal to 0, so we can know:

$$p_A + p_B - 1 \le p_{AB} \le min[p_A,p_B]$$

#### Measure D

Define that $D = p_{AB} - p_A \times p_B$, so we can know:

$$-(1-p_A)(1-p_B) \le D \le min[p_A(1-p_B), p_B(1-p_A)]$$

, and

$$p_{AB} = p_A \times p_B\text{, then }D = 0$$

#### Measure *r*<sup>2</sup>

The LD measure $r^2$ is the squared correlation, where r scales D by the standard deviations of the allele frequencies at two loci:

$$r^2 = \frac{D^2}{p_Ap_B(1-p_A)(1-p_B)}$$

As I assume A and B are the major allele for loci 1 and 2, respectively, we can see:

$$(1-p_A)^2(1-p_B)^2 \le p_A^2(1-p_B)^2$$

$$(1-p_A)^2(1-p_B)^2\le(1-p_A)^2p_B^2$$

and the range of $r^2$ is

$$0 \le r^2 \le min[\frac{p_A(1-p_B)}{(1-p_A)p_B}, \frac{(1-p_A)p_B}{p_A(1-p_B)}]$$ 

#### Measure D'

The D' scales D by its maximum value given the allele frequencies:

$$D' = \frac{D}{min[p_A(1-p_B), p_B(1-p_A)]}\text{, if D > 0}$$

$$D' = \frac{D}{min[p_Ap_B, (1-p_A)(1-p_B)]}\text{, if D < 0}$$

\|D'\| has range 0-1 regardless of allele frequency

#### Notes

- high \|D'\| and high $r^2$: the presence of only two haplotypes, small difference in allele frequency;
- high \|D'\| and low $r^2$: presence of only three haplotypes, different allele frquencies;
- low \|D'\| and low $r^2$: random coupling of alleles and presence of all four haplotypes.

### Quantification of relationship between allele frequencies and $r^2$

Furthermore, if we assume $p_B = p_A + v$, we can know:

$$2p_A+v-1 \le p_{AB} \le min[p_A,p_A+v]$$

$$-(1-p_A)(1-p_A -v) \le D \le min[p_A(1-p_A-v),(p_A+v)(1-p_A)]$$

$$0 \le r^2 \le min[\frac{p_A(1-p_A-v)}{(p_A+v)(1-p_A)}, \frac{(p_A+v)(1-p_A)}{p_A(1-p_A-v)}] $$

If we set a threshold for $r^2$, i.e. $r^2 \ge t \ge 0$, then

$$-\frac{p_A(1-p_A)(1-t)}{1-p_A(1-t)} \le v \le \frac{p_A(1-p_A)(1-t)}{p_A(1-t)+t}$$

$$\frac{tp_A}{1-p_A(1-t)} \le p_B \le \frac{p_A}{p_A(1-t)+t}$$

### Further reading

1. shiny app: [https://huanwei.shinyapps.io/ldfrq/](https://huanwei.shinyapps.io/ldfrq/)
2. [Naomi R. Wray. Twin Research and Human Genetics. 2005.](https://www.ncbi.nlm.nih.gov/pubmed/15901470)
