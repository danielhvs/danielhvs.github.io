{:title "Removendo métodos não usados"
 :layout :post
 :tags  ["java" "clean code" "eclipse"]}

De vez em quando a gente vê um monte de métodos que não sabemos se são usados ou não.
Sabe um jeito rápido de capar fora os que não são usados usando o eclipse?

1. Abra a classe
2. Mude todos os métodos "public" para "private"
3. Salve a classe
4. Veja onde não compila mais as outras classes
5. Onde não compila, clica em cima, ctrl+1, transforma em public, enter.
6. Faz isso até compilar tudo
7. Volta pra classe
8. Veja os privates que sobraram e remove com: ctrl+1, remove!
9. Vai pra casa fazer o que der na telha.

Disclaimer: Não use isso se estiver usando frameworks xml que injetam as coisas usando reflexão! Ou use, mas depois confira se nenhum dos métodos removidos são chamados pelos frameworks (exemplo, JSF, Spring).
