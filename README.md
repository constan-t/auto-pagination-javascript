# Auto-Paging JavaScript

---
Um sistema de auto-paginação simples.
---
`Este repositório para que eu me lembre de como faz este sistema, caso eu precise usa-lo denovo, e tabém deixei público, pois pode ajudar alguém!`
---

## Sobre
Este é um sistema de auto-paginação usando *Arrays* , de forma resumida, ele lista uma *Array* e cria páginas adicionando *X* elementos em cada uma.

> Código:

```javascript
//-> Configurações
let count1 = 0;
let count2 = 0;
let arr = [];

//Esta variavel guarda a quantidade de itens que será exibido em cada página!
let itensPerPage = 2;
    
let arr2 = [{nome:'minha rola'},{nome:'pirokinha'},{nome: 'buseta'},{nome: 'cu'},{nome: 'felp gay'}];
    
let pages = Math.ceil(arr2.length / itensPerPage)
    
let actual_page = 0;
    
for(let i = 0;i<pages;i++){
    arr.push([])
}
    
for(let i = 0;i<arr2.length;i++){
    count1++;
    arr[actual_page].push(arr2[i])
    if(count1 == itensPerPage){
        count2++;
        actual_page++;
        count1=0;
        if(count2 == arr2.length) break;
    }
}
```
