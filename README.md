<h1 align="center">Teste --- Target Sistemas</h1>
<h2 align="center">Repositório criado com as respostas do teste para vaga Estágio Análise e Desenvolvimento.</h2> 


### 1) Observe o trecho de código abaixo:

  int INDICE = 13, SOMA = 0, K = 0;

  enquanto K < INDICE faça

  {

  K = K + 1;

  SOMA = SOMA + K;

  }

  imprimir(SOMA);



  Ao final do processamento, qual será o valor da variável SOMA?


    RESPOSTA: 91


### 2) Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.

IMPORTANTE:

Esse número pode ser informado através de qualquer entrada de sua preferência ou pode ser previamente definido no código;

    RESPOSTA:

    function fibonacci(limite) {
        -- Aqui declarei os termos da sequência
        let a = 0;
        let b = 1;
        -- Criei uma lista vazia para armazenar os termos da sequência
        let list = [];

        while (a <= limite) {
            list.push(a);
            let c = a + b;
            a = b;
            b = c;
        }
        return lista;
    }

    -- Aqui terá que informar um número inteiro positivo
    let numero = parseInt(prompt('Informe um número: '));
    let sequencia = fibonacci(numero);

    -- Aqui vai ser a verificação se o número informado pertence à sequência de Fibonacci
    if (sequencia.includes(numero)) {
        console.log(`O número ${numero} pertence à sequência de Fibonacci.`);
    } else {
        console.log(`O número ${numero} não pertence à sequência de Fibonacci.`);
    }

    console.log(`A sequência de Fibonacci até ${numero} é: ${sequencia}`);


### 3) Descubra a lógica e complete o próximo elemento:

    RESPOSTA:
    
    a) 1, 3, 5, 7, 9  -  a lógica é somar por 2 o termo anterior.

    b) 2, 4, 8, 16, 32, 64, 128  -  a lógica é multiplicar por 2 o termo anterior.

    c) 0, 1, 4, 9, 16, 25, 36, 49 - a lógica é o quadrado do termo anterior.

    d) 4, 16, 36, 64, 100  -  a lógica é o quadrado do termo ímpar anterior.

    e) 1, 1, 2, 3, 5, 8, 13  -  a lógica é somar os dois termos anteriores para obter o próximo termo na sequência.

    f) 2,10, 12, 16, 17, 18, 19, 20  -  a lógica é que cada termo na sequência é igual à soma dos dígitos do termo anterior.



### 4 - Dois veículos (um carro e um caminhão) saem respectivamente de cidades opostas pela mesma rodovia. O carro de Ribeirão Preto em direção a Franca, a uma velocidade constante de 110 km/h e o caminhão de Franca em direção a Ribeirão Preto a uma velocidade constante de 80 km/h. Quando eles se cruzarem na rodovia, qual estará mais próximo a cidade de Ribeirão Preto?



IMPORTANTE:

a) Considerar a distância de 100km entre a cidade de Ribeirão Preto <-> Franca.

b) Considerar 2 pedágios como obstáculo e que o caminhão leva 5 minutos a mais para passar em cada um deles e o carro possui tag de pedágio (Sem Parar)

c) Explique como chegou no resultado.


     RESPOSTA:

     Para encontrar a posição em que se encontram, usei a fórmula abaixo;

     - Distância = Velocidade x Tempo
       Tempo = t

       Distância percorrida pelo carro = 110t
       Distância percorrida pelo caminhão = 80t + 10/6 (5 minutos em horas, considerando que o caminhão leva 5 minutos a mais em cada pedágio)

       190t = 98 e 1/3
       t = 0,517 horas

       Distância percorrida pelo carro = 110 x 0,517 = 56,87 km
       Distância percorrida pelo caminhão = 80 x 0,517 + 10/6 = 42,33 km

       Como o carro está mais próximo de Ribeirão Preto, a distância que falta para chegar a Ribeirão Preto é de:

       100 - 56,87 = 43,13 km

       o caminhão falta percorrer:

       42,33 km

       Quando se encontram, o carro está mais próximo de Ribeirão Preto.
   

 

### 5) Escreva um programa que inverta os caracteres de um string.



IMPORTANTE:

a) Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código;

b) Evite usar funções prontas, como, por exemplo, reverse;


    let string = "!em erih ,esaelP";
    let invertedString = [];

    for (let i = 0; i < string.length; i++) {
      invertedString.unshift(string[i]);
    }

    invertedString = invertedString.join("");

    console.log(invertedString);
