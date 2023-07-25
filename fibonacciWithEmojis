const emojis = ['🚀', '☘️', '🧑🏼‍🚀', '🤘🏼', '🇧🇷'];
import * as readline from 'readline';

function fibonacciWithEmojis(n: number): string {
  // Verifica se o número fornecido é menor ou igual a 0, caso seja, retorna uma mensagem de erro
  if (n <= 0) {
    return "Por favor, insira um número válido maior que 0.";
  }

  const fibonacciSequence = [0, 1];

  // Gera a sequência de Fibonacci até o número inserido como entrada
  for (let i = 2; i <= n + 1; i++) {
    fibonacciSequence[i] = fibonacciSequence[i - 1] + fibonacciSequence[i - 2];
  }

  /* Mapeia a sequência de Fibonacci gerada e substitui os números pares pelos emojis nos índices correspondentes. Números ímpares não são modificados */
  const modifiedSequence = fibonacciSequence.map(num => {
    if (num % 2 === 0) {
      const emojiIndex = num % emojis.length;
      return emojis[emojiIndex];
    } else {
      return num.toString();
    }
  });

  return modifiedSequence.join(", ");
}

//O motivo de usar a biblioteca readline foi permitir a interação com o usuário durante a execução do script, sendo útil para quando o programa precisa receber entradas do usuário em tempo de execução, tornando a experiência de uso mais "amigável" e interativa.

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});
rl.question('Digite um número para calcular a sequência de Fibonacci: ', (input) => {
  const numero = parseInt(input);
  if (isNaN(numero)) {
    console.log('Por favor, insira um número válido.');
  } else {
    const resultado = fibonacciWithEmojis(numero);
    console.log(`Sequência de Fibonacci com emojis: ${resultado}`);
  }
  rl.close();
});
