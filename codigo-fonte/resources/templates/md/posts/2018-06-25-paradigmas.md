{:title "Map e loop for"
 :layout :post
 :tags  ["paradigmas" "programação"]}

Olha que interessante sobre como toda vez usamos loop "for" em linguagem imperativa para fazer um "map" das linguagens funcionais, declarativas.

### Loop for

Por exemplo, em Java (versões mais antigas), para obter o dobro de cada elemento de uma lista de 0 a 9, faz-se algo como:

```java
List<Integer> saidas = new ArrayList<Integer>();
List<Integer> entradas = Arrays.asList(0, 1, 2, 3, 4, 5, 6, 7, 8, 9);
for(Integer entrada : entradas) {
        saidas.add(entrada + 1);
}
```
Sempre que se quer fazer alguma operação em todos os elementos de uma lista, usa-se essa forma: loop for, às vezes se usa uma variável contadora, opera em cada elemento. De forma geral:

```java
private S opera(E elemento) {
        (...);
}

private List<E> obtemEntradas() {
        (...);
}

List<S> saidas = new ArrayList<S>();
List<E> entradas = obtemEntradas();
for(E entrada : entradas) {
            saidas.add(opera(entrada));
}
```

### Map

Para o mesmo exemplo acima, daria pra fazer, em Clojure:

```clojure
(map inc (range 10))
```

```clojure
(defn obtem-entradas [] (...))
(defn opera [e] (...))

(map opera obtem-entradas)
```

Assim, a função "map" generaliza o conceito de "aplicar uma operação em todos elementos de uma lista", além de tornar o código mais expressivo e enxuto. Java possui esta funcionalidade a partir da versão 8. Ficaria assim, o primeiro exemplo:

```java
Integer[] saidas = Arrays.stream(new Integer[] { 0, 1, 2, 3, 4, 5, 5, 6, 7, 8, 9 })
			 .map(e -> e + 1)
			 .toArray(Integer[]::new);
```

Meio bizarro, mas mais expressivo que o loop for com certeza.

### Conclusão

Em várias coisas é "depende", cada um tem suas vantagens e desvantagens, etc. Mas para esses dois jeitos de fazer a mesma coisa acima aí, prefiro "map" na grande maioria das vezes.