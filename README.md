# Phenolyzer
Phenolyzer is a software that implements phenotype-based prioritization of candidate  genes for human diseases.

## Introduction
Prior biological knowledge and phenotype information may help pinpoint disease contributory genes in whole genome/exome sequencing studies on human diseases. We developed a computational tool called Phenolyzer, which follows a biologist's natural thought processes through four steps: term interpretation, seed gene generation, seed gene growth and data integration. Compared to competing approaches, Phenolyzer has superior performance on finding known disease genes, and on prioritizing recently published novel disease genes.

## Synopsis

- print help message
```
perl disease_annotation.pl --help
```

- Prioritize 'sleep' genes: 
```
perl disease_annotation.pl sleep -p -ph -logistic -out sleep/out
```

- Use the terms in 'disease' file:
```
perl disease_annotation.pl disease -f -p -ph -logistic -out disease/out
```

- Use the cnv.bed region:
```
perl disease_annotation.pl alzheimer -bedfile cnv.bed -p -ph -logistic -out alzheimer/out
```

- Use the Mentha gene-gene interaction database as Addon
```
perl disease_annotation.pl alzheimer -p -ph -logistic -out alzheimer/out -addon_gg DB_MENTHA_GENE_GENE_INTERACTION -addon_gg_weight 0.05
```

## License Agreement
By using the software, you acknowledge that you agree to the terms below:

For academic and non-profit use, you are free to fork, download, modify, distribute and use the software without restriction.

For commercial use, you are required to contact [Stevens Institute of Innovation](https://stevens.usc.edu/contact-us/) at USC directly to discuss licensing options.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

The terms above do not apply to `external` directory, which contains optional components for running Phenolyzer and each component has its own license restrictions. We include them in the package for the convenience of users.

## Contact
- Hui Yang (yanghui@usc.edu)
- Kai Wang (kaiwang@usc.edu)


