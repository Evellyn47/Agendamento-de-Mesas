# Esclarecimento

Quando esta atividade foi passada, tive dificuldade em definir a quantidade mínima de elementos que o array poderia suportar. 
No caso desta atividade, o array mesas suporta apenas 10 mesas dentro de si. A estrutura usada para definir a quantidade de elementos no array foi:
`let mesas = new Array(10).fill(false);  ->`  **Essa linha cria um array com 10 posições, todas inicialmente preenchidas com o valor false, indicando que todas as mesas estão desocupada**


### Outra parte da estrutura que entrei em conflito foi:
`function ReservarMesa() {
    let mesaNumero = parseInt(prompt("Digite o número da mesa (1-10): "));
}`
Eu não compreendia o motivo de subtrair 1. Agora entendo melhor que os índices de um array começam em 0, enquanto o número inserido pelo usuário (como 1, 2, 3...) segue a contagem humana, que começa em 1.
Portanto, o -1 é aplicado ao número digitado pelo usuário para acessar a posição correta no array.
### Por exemplo:
Se utilizarmos diretamente mesas[1], estaremos acessando a segunda posição do array, porque o índice 1 corresponde à mesa número 2.

Para acessar corretamente a mesa número 1, usamos:

``mesas[mesaNumero - 1];``


