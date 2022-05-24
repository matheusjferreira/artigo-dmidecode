> # Dmidecode

> ## O Artigo:

Você pode estar em uma situação em que deseje descobrir o limite máximo que o seu hardware disponibiliza para expansão de memoria ram, quanto de momória presente, ou slots presentes (vazios e ocupados) assim como outras informações do hardware.
O dmidecode é um pacote que pode ajudar a descobrir todas essas informações e muito mais.
Sua descrição segundo o guialinux (https://guialinux.uniriotec.br/dmidecode/) é:
"Este comando decodifica tabelas DMI (Destktop Management Information)."

> ## Como utilizar:

No linux o dmidecode já está presente e não precisa ser baixado, para usuário windows ou outros sistemas operacionais é possível fazer o douwnload no site oficial (http://download.savannah.gnu.org/releases/dmidecode/).

O dmidecode em sua execução, lê arquivos críticos do sistema, desse modo prcisa ser executado com previlégios de administrador.

Uma sugestão é executar o dmidecode salvando o retorno de sua execução em um arquivo para ficar mais fácil de analisar.

> ## 1. Saída Total

> ### Linux

Para exibir no terminal, use o comando:

    $ sudo dmidecode

Ou para salvar o retorno em um arquivo:

    $ sudo dmidecode > dmidecode.txt

> ### Windows

Para exibir no prompt de comando (cmd), execute-o como administrador, e use o comando:

    dmidecode

Ou para salvar o retorno em um arquivo:

    dmidecode > dmidecode.txt

Este comando executará o dmidecode e todas as informações do seu hardware que ele encontrar serão salvas no arquivo "dmidecode.txt" no diretório em que se encontra.

> ## 2. Saída Expecífica

Você também pode usar comandos para determinado componente como a memória RAM:

> ###  Linux

Use o comando:

    # sudo dmidecode -t 16

![dmi1](https://user-images.githubusercontent.com/59848966/91907745-c9925180-ec80-11ea-83bc-6ea98fa60708.png)

> ###  Windows

Use o comando:

    dmidecode -t 16

> ## 3. Saída Expecífica++

Ou sendo mais específico como:

> ### Linux

Use o comando:

    # sudo dmidecode -t 16 | grep Maximum

![dmi2](https://user-images.githubusercontent.com/59848966/91907813-e62e8980-ec80-11ea-862c-70948d24b07b.png)

> ###  Windows

Use o comando:

    dmidecode -t 16 | grep Maximum

> ## Saiba mais em:

https://guialinux.uniriotec.br/dmidecode/;

> ## Referências:

Guia Linux - https://guialinux.uniriotec.br/dmidecode/;

dmidecode oficial - http://download.savannah.gnu.org/releases/dmidecode/;

> ## Licença

    MIT License

    Copyright (c) 2022 Matheus Ferreira

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
