## Install  
```R
install.packages("https://github.com/Ali-Mahzarnia/brainconn2/archive/master.tar.gz", repos = NULL, type="source")
```

## Licence

The licence is taken from the original R package (MIT). For more information on this licence please check [https://en.wikipedia.org/wiki/MIT_License](https://en.wikipedia.org/wiki/MIT_License)


****



## Example
Plot 3d brains with celebrelum

Added features: IIT MNI coordinate Desikan84 Atlas with 84 regions, and a glass brain compatible including the cerebellum that didn't exist in the previous version.


Example:

```R
library(brainconn)
x=matrix(0,84,84)
x[1:3,9:11]= 1:3 ;x[9:11,1:3]= 3:1
brainconn(atlas ="Desikan84", conmat=x, 
          view="ortho", node.size =2, 
          node.color = "pink", 
          edge.width = 1, edge.color="blue", 
          edge.alpha = 0.65,
          edge.color.weighted = T,
          scale.edge.width=T,
          labels = T,
          all.nodes =F, 
          show.legend = T, 
          label.size=3, background.alpha=1, 
          label.edge.weight=F)
          
```

![](https://github.com/Ali-Mahzarnia/brainconn2/raw/main/temp.png)



In order to learn more about the Desikan84 Atlas added to the package run the following command:
```R
library(brainconn)
Desikan84=as.data.frame(Desikan84);Desikan84
```

|                                | ROI                            | X   | Y   | Z   |
|--------------------------------|--------------------------------|-----|-----|-----|
| Cerebellum-Cortex-Left         | Cerebellum-Cortex-Left         | -22 | -65 | -38 |
| Thalamus-Proper-Left           | Thalamus-Proper-Left           | -12 | -17 | 8   |
| Caudate-Left                   | Caudate-Left                   | -13 | 12  | 9   |
| Putamen-Left                   | Putamen-Left                   | -24 | 3   | 1   |
| Pallidum-Left                  | Pallidum-Left                  | -18 | -5  | 1   |
| Hippocampus-Left               | Hippocampus-Left               | -26 | -22 | -13 |
| Amygdala-Left                  | Amygdala-Left                  | -24 | -4  | -19 |
| Accumbens-area-Left            | Accumbens-area-Left            | -9  | 13  | -8  |
| Cerebellum-Cortex-Right        | Cerebellum-Cortex-Right        | 24  | -64 | -38 |
| Thalamus-Proper-Right          | Thalamus-Proper-Right          | 14  | -16 | 8   |
| Caudate-Right                  | Caudate-Right                  | 15  | 12  | 10  |
| Putamen-Right                  | Putamen-Right                  | 26  | 4   | 1   |
| Pallidum-Right                 | Pallidum-Right                 | 20  | -3  | 1   |
| Hippocampus-Right              | Hippocampus-Right              | 27  | -19 | -14 |
| Amygdala-Right                 | Amygdala-Right                 | 24  | -2  | -20 |
| Accumbens-area-Right           | Accumbens-area-Right           | 11  | 14  | -9  |
| bankssts-Left                  | bankssts-Left                  | -56 | -46 | 7   |
| caudalanteriorcingulate-Left   | caudalanteriorcingulate-Left   | -5  | 21  | 31  |
| caudalmiddlefrontal-Left       | caudalmiddlefrontal-Left       | -34 | 14  | 46  |
| cuneus-Left                    | cuneus-Left                    | -6  | -77 | 20  |
| entorhinal-Left                | entorhinal-Left                | -28 | -4  | -36 |
| fusiform-Left                  | fusiform-Left                  | -36 | -45 | -23 |
| inferiorparietal-Left          | inferiorparietal-Left          | -42 | -66 | 27  |
| inferiortemporal-Left          | inferiortemporal-Left          | -49 | -40 | -21 |
| isthmuscingulate-Left          | isthmuscingulate-Left          | -7  | -44 | 23  |
| lateraloccipital-Left          | lateraloccipital-Left          | -33 | -82 | 1   |
| lateralorbitofrontal-Left      | lateralorbitofrontal-Left      | -24 | 34  | -17 |
| lingual-Left                   | lingual-Left                   | -14 | -71 | -5  |
| medialorbitofrontal-Left       | medialorbitofrontal-Left       | -9  | 33  | -17 |
| middletemporal-Left            | middletemporal-Left            | -55 | -37 | -9  |
| parahippocampal-Left           | parahippocampal-Left           | -28 | -28 | -20 |
| paracentral-Left               | paracentral-Left               | -6  | -25 | 60  |
| parsopercularis-Left           | parsopercularis-Left           | -45 | 18  | 15  |
| parsorbitalis-Left             | parsorbitalis-Left             | -41 | 39  | -11 |
| parstriangularis-Left          | parstriangularis-Left          | -44 | 32  | 4   |
| pericalcarine-Left             | pericalcarine-Left             | -8  | -78 | 10  |
| postcentral-Left               | postcentral-Left               | -42 | -24 | 45  |
| posteriorcingulate-Left        | posteriorcingulate-Left        | -4  | -20 | 41  |
| precentral-Left                | precentral-Left                | -39 | -5  | 42  |
| precuneus-Left                 | precuneus-Left                 | -9  | -57 | 40  |
| rostralanteriorcingulate-Left  | rostralanteriorcingulate-Left  | -5  | 36  | -2  |
| rostralmiddlefrontal-Left      | rostralmiddlefrontal-Left      | -33 | 42  | 17  |
| superiorfrontal-Left           | superiorfrontal-Left           | -12 | 27  | 41  |
| superiorparietal-Left          | superiorparietal-Left          | -23 | -62 | 48  |
| superiortemporal-Left          | superiortemporal-Left          | -53 | -16 | -2  |
| supramarginal-Left             | supramarginal-Left             | -51 | -40 | 34  |
| frontalpole-Left               | frontalpole-Left               | -9  | 63  | -11 |
| temporalpole-Left              | temporalpole-Left              | -34 | 11  | -37 |
| transversetemporal-Left        | transversetemporal-Left        | -46 | -21 | 11  |
| insula-Left                    | insula-Left                    | -33 | 1   | -1  |
| bankssts-Right                 | bankssts-Right                 | 58  | -41 | 7   |
| caudalanteriorcingulate-Right  | caudalanteriorcingulate-Right  | 7   | 24  | 29  |
| caudalmiddlefrontal-Right      | caudalmiddlefrontal-Right      | 36  | 15  | 47  |
| cuneus-Right                   | cuneus-Right                   | 11  | -79 | 16  |
| entorhinal-Right               | entorhinal-Right               | 26  | -2  | -35 |
| fusiform-Right                 | fusiform-Right                 | 37  | -42 | -23 |
| inferiorparietal-Right         | inferiorparietal-Right         | 45  | -61 | 28  |
| inferiortemporal-Right         | inferiortemporal-Right         | 49  | -34 | -23 |
| isthmuscingulate-Right         | isthmuscingulate-Right         | 9   | -43 | 25  |
| lateraloccipital-Right         | lateraloccipital-Right         | 36  | -80 | 0   |
| lateralorbitofrontal-Right     | lateralorbitofrontal-Right     | 24  | 32  | -17 |
| lingual-Right                  | lingual-Right                  | 17  | -70 | -4  |
| medialorbitofrontal-Right      | medialorbitofrontal-Right      | 6   | 39  | -16 |
| middletemporal-Right           | middletemporal-Right           | 55  | -34 | -11 |
| parahippocampal-Right          | parahippocampal-Right          | 28  | -29 | -17 |
| paracentral-Right              | paracentral-Right              | 9   | -23 | 61  |
| parsopercularis-Right          | parsopercularis-Right          | 47  | 19  | 15  |
| parsorbitalis-Right            | parsorbitalis-Right            | 41  | 42  | -10 |
| parstriangularis-Right         | parstriangularis-Right         | 45  | 36  | 8   |
| pericalcarine-Right            | pericalcarine-Right            | 12  | -79 | 6   |
| postcentral-Right              | postcentral-Right              | 44  | -21 | 44  |
| posteriorcingulate-Right       | posteriorcingulate-Right       | 7   | -17 | 42  |
| precentral-Right               | precentral-Right               | 40  | -5  | 43  |
| precuneus-Right                | precuneus-Right                | 12  | -57 | 39  |
| rostralanteriorcingulate-Right | rostralanteriorcingulate-Right | 6   | 36  | 0   |
| rostralmiddlefrontal-Right     | rostralmiddlefrontal-Right     | 34  | 43  | 20  |
| superiorfrontal-Right          | superiorfrontal-Right          | 13  | 27  | 42  |
| superiorparietal-Right         | superiorparietal-Right         | 24  | -62 | 47  |
| superiortemporal-Right         | superiortemporal-Right         | 55  | -13 | -4  |
| supramarginal-Right            | supramarginal-Right            | 53  | -36 | 32  |
| frontalpole-Right              | frontalpole-Right              | 10  | 62  | -12 |
| temporalpole-Right             | temporalpole-Right             | 33  | 11  | -36 |
| transversetemporal-Right       | transversetemporal-Right       | 47  | -18 | 10  |
| insula-Right                   | insula-Right                   | 35  | 4   | -2  |


### Citations
Upon using this package please cite both of the following refrences.

Ali Mahzarnia, Alexandra Badea (2022), Joint Estimation of Vulnerable Brain Networks and Alzheimer’s Disease Risk Via Novel Extension of Sparse Canonical Correlation at bioRxiv. 

Orchard, E. R., Chopra, S., Ward, P. G., Storey, E., Jamadar, S. D., & Egan, G. F. (2020). *Neuroprotective effects of motherhood on brain function in late-life: a resting state fMRI study.* Cerebral Cortex. \
https://pubmed.ncbi.nlm.nih.gov/33067999/


