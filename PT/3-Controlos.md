# 3 - Controlos

Agora que já configuraste o rato está na hora de configurar o teclado.
Mas primeiro, vou falar sobre ficheiros _.cfg_ (para quem não sabe o que são). Dentro de ficheiros _.cfg_ é possivel ter todas as definições do jogo (rato, teclado, gráficos, internet,...), _scripts_ (parecido com macros, mas faz parte do jogo) e mais.

O ficheiro _config.cfg_ é criado pelo jogo da primeira vez que arranca. É o primeiro ficheiro a ser lido pelo jogo (_autoexec.cfg_ vem logo a seguir) e contém todas as definições do TF2. Apesar de o poderes alterar para conter as tuas definições, não é recomendado pois o TF2 reescreve o ficheiro ao abrir (a não ser que tenham definido o ficheiro para _read-only_, mas mesmo assim, quando vêm _updates_ grandes, o ficheiro é reescrito pelo Steam).

A melhor opção é guardar as definições no _autoexec_ (ou vários ficheiros separados). Se usares mais ficheiros além do _autoexec_, podes chamá-los (dizer ao TF2 para os executar) assim:
```source-scripting
exec <ficheiro>
```
Por exemplo, se tiveres os _binds_ num ficheiro chamado _binds.cfg_ executa-lo assim:
```source-scripting
exec binds // sem o .cfg (extensão do ficheiro)
```
_**NOTA:** as duas barras ("//") indicam o início de um comentário de uma linha, tudo o que estiver a seguir, na mesma linha, é ignorado pelo jogo e portanto podes escrever o que te apetecer_

## 3.1 - _Binds_

Esta parte é fácil. Abre o TF2 e escolhe as teclas que queres em jogo, grava e feicha o jogo. Feito.
Se, no entanto, quiseres algo mais complexo, abre o _config.cfg_ (depois de fazer o acima descrito), copia todas as linhas que comecem com _bind_ (e o "unbind all" também - _"unbind all" apaga todas as teclas que tiveres escolhido, por isso põe-no no início do ficheiro, ou antes de todos os comandos "bind") para o _autoexec_ (ou outro ficheiro da tua preferência, como expliquei anteriormente). Agora que tens uma cópia dos _binds_ podes começar a brincar com eles.

Usar o comando _bind_ é simples:
```source-scripting
bind [tecla] [comando] // faz bind de uma tecla a um comando
bind [tecla] "[comando1];[comando2];..." // faz bind de uma tecla a dois ou mais comandos distintos.
```
Mais sobre o comando _bind_ [aqui](https://wiki.teamfortress.com/wiki/Scripts#Bind "Binds - TF2W").

Um exemplo de como usar _binds_: Eu não uso a roda do rato para trocar entre todas as armas, em vez disso, uso-a para trocar entre as armas primária e _melee_.
Este código faz isso mesmo:
```source-scripting
bind "mwheelup" "slot3" // esta linha faz bind da roda cima à melee
bind "mwheeldown" "slot1" // esta linha faz bind da roda baixo à arma primária
```
[Aqui](https://wiki.teamfortress.com/wiki/Scripts#List_of_key_names "List of Key names - TF2W") está uma lista com os nomes das teclas do teclado.
