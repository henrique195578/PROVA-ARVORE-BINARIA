# PROVA-ARVORE-BINARIA
![UNIPAR ](https://www.calendariodovestibular.com.br/wp-content/uploads/2013/03/post_unipar.png) 
2º A.A.R.E - ESTRUTURA DE DADOS
=============================
   ##  Árvores Binárias 

### Acadêmico: Henrique Borges da Silva 
### R.A: 00195578
### Orientador: Geferson Luis Simonette
*******
#####   Toledo, 27/06/2021

*****
# Árvore Binárias
Uma árvore binária ou árvore de busca binária ou árvore de pesquisa binária é uma estrutura de dados baseada em nós. Cada nó armazena valores e pode estar associado a uma sub-árvore à esquerda ou à direita. Todos nós da sub-árvore à esquerda contêm valores menores que o do nó raiz, e a subárvore da direita contém apenas valores maiores.

##### Alguns Termos:
* **Nós** contêm todos os itens armazenados na árvore.
* **Raiz** é o item do topo da árvore (neste caso, o número 50).
* **Filhos** são os itens logo abaixo da raiz, 30 e 90 e assim sucessivamente. Por exemplo, o
20 é filho do 30.
* **Folha** é um nó que não tem filho, é o último item da árvore. Por exemplo, 20, 40 e 100.
Uma árvore binária de busca serve para o armazenamento de dados na memória do computador e a sua subseqüente recuperação. Em uma árvore binária busca cada nó contém um campo chamado key, podendo haver outras informações, além dos ponteiros left e right.

![Arvore Binaria](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTv3eGAytEQOMN6caXhOyWH9JiOkxc4h9kFcQjOaJkL1yldEGylkPQ6PPui-7j0OWoTzfU&usqp=CAU)
***
#### Exemplo de Árvore Binária
* Primeiro Passo iremos cria a estrutura da arvore, dentro da classe então criar um método, conforme a imagem abaixo, pode ser abaixo do método principal do java. public static void main(String[] args) {} isso dentro da classe **main** nossa.  
![Arvore Binaria](https://3.bp.blogspot.com/-ra8Xvh_8QDw/WuCEpN6glzI/AAAAAAAABoM/N61tPvqy5V8q4XwpMIaI-N1ndmDAaFxeACK4BGAYYCw/s400/arvore.PNG)
******
* Após a criação da estrutura vamos cria o método de inserção da nossa arvores
![Arvore2](https://3.bp.blogspot.com/-HxyxMtW7YqA/WuCFURBLmdI/AAAAAAAABoY/cJiOsvj2JSg9DET8BcEF5gzXBIsDQAanwCK4BGAYYCw/s640/inser%25C3%25A7%25C3%25A3o%2Barvore.PNG)
******
* Pronto Nossa Arvores já esta completa, falta apenas inserir os valores para cada no, então dentro do método principal iremos chamar o método que criamos acima, ficando igual a foto abaixo desconsidere os código comentados, mas logico o for acima comentado inseri valor na arvore de fora randômico de interações de até 10 laço ou mais se assim for alterado o mesmo
#### Exemplo de algoritmo de busca em Java.**
![Arvore3](https://4.bp.blogspot.com/-6IrvS1wBga8/WuCGs56OVzI/AAAAAAAABok/pXevd6mfuOglo0kq9mxvJI-TZD4zY7AqQCK4BGAYYCw/s640/main.PNG)
*****
## Árvore Balanceada
* Árvore binária de busca balanceada ou árvore binária de busca auto-balanceada é qualquer árvore de busca binária que automaticamente mantém a sua altura número máximo de níveis abaixo da raiz pequeno mesmo depois de sucessivas inserções e exclusões arbitrárias. Árvores binárias de busca balanceadas podem ser usadas para construir e manter listas ordenadas, tais como filas de prioridade. Elas também podem ser usadas para arrays associativos; Árvores binárias de busca balanceadas podem ser usadas para implementar qualquer algoritmo que requeira listas ordenadas, para alcançar o melhor desempenho assintótico. Muitos algoritmos de geometria computacional exploram variações de BSTs balanceadas para resolver problemas, tais como a interseção entre segmentos de reta e o problema de localização do ponto de forma eficiente.
* Uma árvore é considerada balanceada se e somente se para qualquer nó, a altura de suas duas subárvores diferem de no máximo uma unidade." O nó desta árvore que satisfaz o balanceamento é chamado de nó regulado. Se não satisfizer, ele é considerado desregulado.
* A idéia central de fazer o balanceamento em uma árvore e exigir que a altura seja O(log n), e que esta propriedade se estenda a todas as subárvores: cada subárvore com m nós deve possuir altura O(log m). Um nó v de uma árvore binária T é dito regulado se as alturas de suas subárvores esquerda e direita diferem de até uma unidade. A maioria das operações em uma árvore binária de busca leva um tempo diretamente proporcional à altura da árvore, por isso, é desejável manter a altura pequena. Uma árvore binária de altura h pode conter no máximo 20+21+···+2h = 2h+1-1 nós.
#### Exemplo de algoritmo de busca em Java.
> // O método de procura numa AVL é semelhante ao busca binária de uma árvore binária de busca comum.
public BSTNode<T> search(T element) {
    return search(element, this.root);
}
> // Método auxiliar à recursão.
private BSTNode<T> search(T element, BSTNode<T> node) {
    if (element == null || node.isEmpty()) {
        return new BSTNode<T>();
    }
      > if (node.isEmpty() || node.getData().equals(element)) {
        return node;
    } else if (node.getData().compareTo(element) > 0) {
        return search(element, node.getLeft());
    } else {
        return search(element, node.getRight());
    }
}

****
## Árvore completamente balanceada 
Nós folha (externos) aparecem em no máximo dois níveis diferentes, otimizando o tempo médio de pesquisa assumindo assim uma distribuição uniforme das chaves. Problema clássico deste tipo é de manter árvore completamente balanceada após cada inserção é muito caro. Para inserir a chave 1 na árvore à esquerda e manter a árvore completamente balanceada precisamos movimentar todos os nós
![ArvoreBalanceada](data:image/png;base64,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)
****
## Diferença entre Árvore Binária e Balanceada AVL
* Uma árvore binária de busca depende da ordem da inserção para ter um tempo assintótico de busca ótimo, visto que o primeiro valor inserido será usado como uma raiz e os demais irão para esquerda ou para direita se forem maiores ou menores. Sendo assim, se você adicionar os valores em ordem crescente de s ficarão todos à direita do valor anterior, logo o tempo de busca será de O(n), sendo n o número de valores.
* Já em uma árvore AVL isso não ocorre pois cada valor na árvore possui um dado que determina seu balanceamento baseado na altura do seu nó a direita menos a altura do seu nó a esquerda, lembrando que esses valores podem ser **-1=<FB<=1**. 
* Caso, após uma inserção qualquer valor da árvore fique com um fator de balanceamento
diferente desses valores, a árvore se reestrutura mudando suas ligações para que todos os
seus nós tenham esse fator de balanceamento.

## Diferença entre as Árvores Binária e AVL
* Uma árvore binária de busca depende da ordem da inserção para ter um tempo assintótico de busca ótimo, visto que o primeiro valor inserido será usado como uma raiz e os demais irão para esquerda ou para direita se forem maiores ou menores. Sendo assim se vc adicionar os valores  m ordem crescente de s ficarão todos a direita do valor anterior, logo o tempo de busca será de O(n), sendo n o número de valores.  
* Já em uma árvore AVL isso não ocorre pois cada valor na árvore possui um dado que determina seu balanceamento baseado na altura do seu nó a direita menos a altura do seu nó a esquerda, lembrando que esses valores podem ser -1=<FB<=1.  
* Caso, após uma inserção qualquer valor da árvore fique com um fator de balanceamento diferente desses valores, a arvore se reestrutura mudando suas ligações para que todos os seu nós tenha esse fator de balanceamento. Sendo assim o tempo de busca assintótico ficará em torno de O![](https://tex.z-dn.net/?f=(Log%20_%7B2%7D%20n)) independente da ordem de inserção dos valores.
*****

### Referências 
 *  [Árvore Binária](https://pt.wikipedia.org/wiki/Árvore_AVL)
 *  [Árvore Binária Artigo](https://homepages.dcc.ufmg.br/~cunha/teaching/20121/aeds2/sbbs.pdf)
  *  [Árvore Balanceada Artigo](https://www.ime.usp.br/~pjssilva/disciplinas/2005/mac2014/notas_de_aula/aula9/arvores3.pdf)
