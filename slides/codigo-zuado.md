##  codigo_zuado

```
if (info->numCC < (*pRaiz)->conta.numCC) {
      inserir(&(*pRaiz)->esq,& (*pRaiz), info);
      (*pRaiz)->bal = alturaAvl((*pRaiz)->esq) - alturaAvl((*pRaiz)->dir);
      if ((*pRaiz)->bal == 2)  {
        if ((*pRaiz)->esq->bal==1)
          (*pRaiz) = rotacaoLL((*pRaiz));
        else if ((*pRaiz)->esq->bal == -1) {
          (*pRaiz)->esq = rotacaoRR((*pRaiz)->esq);
          (*pRaiz) = rotacaoLL((*pRaiz));
        }
      }
    } else {
      if (info->numCC > (*pRaiz)->conta.numCC) {
        inserir(& (*pRaiz)->dir,& (*pRaiz), info);
        (*pRaiz)->bal=alturaAvl ((*pRaiz)->esq) - alturaAvl ((*pRaiz)->dir);
        if ((*pRaiz)->bal==-2) {
          if ( (*pRaiz)->dir->bal==-1)
            (*pRaiz)= rotacaoRR ((*pRaiz));
          else if ( (*pRaiz)->dir->bal==1) {
            (*pRaiz)->dir=rotacaoLL ((*pRaiz)->dir);
            (*pRaiz)= rotacaoRR ((*pRaiz));
          }
        }
      }
    }
```
