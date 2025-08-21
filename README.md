# Esse reposiório descreve 3 ténicas dentro de POO

# Herança

- Estudar o código e fazer uma breve descriação do que entendeu

    O codigo utiliza a herança, que é quando uma classe (filha) recebe atributos e métodos 
    da classe (pai).
    Nesse codigo a classe **Animal** é a classe pai e as classes **Cavalo, Aguia, Cachorro, etc** 
    sao as filhas que herdam os métodos e atributos definidos em **Animal**.
    Mas cada uma pode reescrever um metodo pra se comportar diferente.

    Ex:
    A classe **Animal** tem um método "fazerSom" e todas as subclasses herdam esse metodo 
    mas em cada animal o resultado e diferente.

# Composição / Associação

- Estudar o código e fazer uma breve descriação do que entendeu

    Esse codigo usa a Composição, que basicamente é quando uma classe possui objetos de outras
    classes pra representar as caracteristicas ou comportamentos.
    Diferente da Herança aqui a classe **Cavalo** nao herda de uma classe **Animal**, em vez
    disso ela tem objetos das classes **Dormir, Respirar, EmitirSom, Locomover** para fazer 
    essas ações.

    Ex:
    A classe **Dormir** define o metodo "dormir(String animal)" o **Cavalo** chama esse 
    método passando seu nome e **Coruja** faz o mesmo, ambos dormem mas o codigo está 
    centralizado em **Dormir**.

    Isso e útil para reaproveitar as classes de comportamentos em vários animais sem
    duplicar código.

# Injeção de Dependencia

- Estudar o código e fazer uma breve descriação do que entendeu

    Aqui o código usa a Injeção de Dependencia, que significa que uma classe não cria
    diretamente os objetos que ela precisa e sim recebe esses objetos prontos de fora.
    Diferente de um código que **Cavalo** teria os metodos fixos, aqui ele vai receber 
    comportamentos já prontos, e só utilizar. Quem decide qual a implementação usar nesse
    caso vai ser a **Main**.

    Ex:
    A classe **Cavalo** não implementa diretamente a logica de "Correr", ela possui atributos
    que representam esses comportamentos (Locomover) e só chama os métodos.
    Da mesma forma, **Coruja** pode receber outros comportamentos, como "Voar" reutilizando as
    mesmas classes de ação.

    Assim o código que define como correr, voar ou emitir som nao fica duplicado em cada animal
    mas sim centralizado nas classes de comportamento.

    Isso é útil porque separa responsabilidades
    Os animais ficam responsaveis apenas de usar os comportamentos, as classes de comportamento de
    como a ação acontece e se um novo animal for adcionado so precisa injetar as dependências, evitando
    duplicação de código.

