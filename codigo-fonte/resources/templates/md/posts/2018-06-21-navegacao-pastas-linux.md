{:title "Navegação em pastas"
 :layout :post
 :tags  ["linux" "linha de comando"]}

Quando você está no console do linux (tela preta cheia de letra branca ou branca cheia de letra preta), geralmente você está dentro de uma pasta (muitos chamam de diretório). Existem caracteres especiais pra ajudar na navegação entre pastas via linha de comando. Abaixo mostro os exemplos mais usados.

### Ponto (.)

“.” é a pasta “atual” em que se está. Por exemplo, “cd .” não faz “nada”? Whuuuut?! Na realidade este comando “cd .” faz um “refresh” na pasta atual! Ou seja, se alguém copiou coisa lá pra dentro, tu já vê! Se alguém deletou, depois copiou, depois moveu, depois soltou um arquivo lá dentro, tu já vê!

### Til (~)

“~” é a pasta “home” do usuário logado. Geralmente se tu é “joao.da.silva”, seu “~” é a pasta “/home/joao.da.silva”. Resumindo, tu usa “cd ~/Downloads” para acessar a pasta “/home/joao.da.silva/Downloads”.

### Ponto ponto (..)

“..” é a pasta “pai” da pasta em que se está. Um uso comum é, por exemplo, se tu tá em “/home/joao.da.silva/Downloads”, pode usar o comando “cd ..” para entrar na pasta “/home/joao.da.silva”.

### Hífen (-)

“-” é a pasta “anterior” à pasta em que se está. Por exemplo, se estou em “/home/joao.da.silva/Downloads” e faço “cd /usr/bin” e depois “cd -“, eu volto para “/home/joao.da.silva/Downloads”

