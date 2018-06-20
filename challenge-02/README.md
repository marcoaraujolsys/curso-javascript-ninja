# Desafio da semana #2

Nesse exercício, você está livre para escolher os nomes para suas variáveis e funções! :smile:

```js
// Crie uma função que receba dois argumentos e retorne a soma dos mesmos.
function soma(x,y){
  return x+y ;
}

// Declare uma variável que receba a invocação da função criada acima, passando dois números quaisquer por argumento, e somando `5` ao resultado retornado da função.
var _soma = soma(2,3)+5;

// Qual o valor atualizado dessa variável?
10

// Declare uma nova variável, sem valor.
var _newvar;

/*
Crie uma função que adicione um valor à variável criada acima, e retorne a string:
    O valor da variável agora é VALOR.
Onde VALOR é o novo valor da variável.
*/
function rec(valor){
  _newvar = 'O valor da variável agora é ' + valor;
  return _newvar;
}

// Invoque a função criada acima.
rec(100);

// Qual o retorno da função? (Use comentários de bloco).
?
/*
O valor da variavel agora é 100
*/


/*
Crie uma função com as seguintes características:
1. A função deve receber 3 argumentos;
2. Se qualquer um dos três argumentos não estiverem preenchidos, a função deve retornar a string:
    Preencha todos os valores corretamente!
3. O retorno da função deve ser a multiplicação dos 3 argumentos, somando `2` ao resultado da multiplicação.
*/
?
function rec2(p1,p2,p3){
  var ret = '';
  if (p1 == '' || p2 == '' || p3 == ''){
    ret = 'Preencha todos os valores corretamente!';
  }
  else{
    ret = p1*p2*p3;
  }
  return ret;
}

// Invoque a função criada acima, passando só dois números como argumento.
rec2(1,2,'s');

// Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).
Preencha todos os valores corretamente!

// Agora invoque novamente a função criada acima, mas passando todos os três argumentos necessários.
rec2(1,2,3);

// Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).
6

/*
Crie uma função com as seguintes características:
1. A função deve receber 3 argumentos.
2. Se somente um argumento for passado, retorne o valor do argumento.
3. Se dois argumentos forem passados, retorne a soma dos dois argumentos.
4. Se todos os argumentos forem passados, retorne a soma do primeiro com o segundo, e o resultado, dividido pelo terceiro.
5. Se nenhum argumento for passado, retorne o valor booleano `false`.
6. E ainda, se nenhuma das condições acima forem atendidas, retorne `null`.
*/
function rec3(p1,p2,p3){
  var ret=false;
  if (p1 != undefined && p2 == undefined && p3 == undefined){
    ret = p1;  
  else if (p1 != undefined && p2 != undefined && p3 == undefined){
    ret = p1+p2;    
  else if (p1 != undefined && p2 != undefined && p3 != undefined){
    ret = (p1+p2) / p3;
  else
    ret = null;
  }  
  return ret;    
}

// Invoque a função acima utilizando todas as possibilidades (com nenhum argumento, com um, com dois e com três.) Coloque um comentário de linha ao lado da função com o resultado de cada invocação.
rec3();
rec3(1);
rec3(1,2);
rec3(1,2,3);
