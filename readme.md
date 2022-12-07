## Install  
```R
install.packages("https://github.com/Ali-Mahzarnia/brainconn2/archive/master.tar.gz", repos = NULL, type="source")
```

## Licence

The licence is taken from the original R package (MIT). For more information on this licence please check [https://en.wikipedia.org/wiki/MIT_License](https://en.wikipedia.org/wiki/MIT_License)


****



## Example

Plot mouse 3d brains 
Equivalent of IIT MNI coordinate of "CHASS" atlas (Calabrese et al., 2015; Anderson et al., 2019) with 332 abbreviated region names (and the CHASS_num atlas with only region index instead of region names), and compatible mouse glass brains (background="Chass").

```R
library(brainconn2)
x=matrix(0,332,332)
x[1:3,9:11]= 1:3
x[5:7,15:17]= -(2:4)
x=t(x)+x; 
brainconn(atlas ="CHASS", conmat=x, 
          view="ortho", node.size =0.5, 
          node.color = "black", 
          edge.width = 1, edge.color="red", 
          edge.alpha = 0.65,
          edge.color.weighted = T,
          scale.edge.width=T,
          labels = T,
          all.nodes =T, 
          show.legend = T, 
          label.size=3, background.alpha=1, 
          label.edge.weight=F, background = "Chass")  
          
```

![](https://github.com/Ali-Mahzarnia/brainconn2/raw/main/temp2.png)



Plot Human 3d brains with celebrelum

Added features: IIT MNI coordinate Desikan84 Atlas with 84 region names (and the Desikan84num atlas with only region index instead of region names based on [this list](https://github.com/Ali-Mahzarnia/atlasindex/blob/main/atlasindex.csv)), and a glass brain compatible including the cerebellum that didn't exist in the previous version.


Example:

```R
library(brainconn2)
 x=matrix(0,84,84)
  x[1:3,9:11]= 1:3
  x[5:7,15:17]= -(1:3)
  x=t(x)+x; 
  brainconn(atlas ="Desikan84", conmat=x, 
            view="ortho", node.size =2, 
            node.color = "pink", 
            edge.width = 1, edge.color="red", 
            edge.alpha = 0.65,
            edge.color.weighted = T,
            scale.edge.width=T,
            labels = T,
            all.nodes =F, 
            show.legend = T, 
            label.size=3, background.alpha=1, 
            label.edge.weight=F, background = "ICBM152")  
          
```

![](https://github.com/Ali-Mahzarnia/brainconn2/raw/main/temp.png)



In order to learn more about the Desikan84, CHASS, or Desikan84num, CHASS_num Atlases added to the package run the following command:
```R
library(brainconn2)
as.data.frame(Desikan84);
as.data.frame(Desikan84num);
as.data.frame(CHASS);
as.data.frame(CHASS_num);
```

### Citations
Upon using this package please cite the following refrences.

Ali Mahzarnia, Jacques A. Stout, Robert J. Anderson, Hae Sol Moon, Zay Yar Han, Kate Beck, Jeffrey N. Browndyke,
David B. Dunson, Kim G. Johnson, Richard J. O’Brien, Alexandra Badea, (2022), "Identifying vulnerable brain networks associated with
Alzheimer’s disease risk" Cerebral Cortex, 2022, 1–16

Orchard, E. R., Chopra, S., Ward, P. G., Storey, E., Jamadar, S. D., & Egan, G. F. (2020). *Neuroprotective effects of motherhood on brain function in late-life: a resting state fMRI study.* Cerebral Cortex. \
https://pubmed.ncbi.nlm.nih.gov/33067999/

 
