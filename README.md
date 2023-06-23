# repositorio 
import 'dart:io';

void main() {
  while (true) {
    print("Digite o primeiro número:");
    double num1 = double.parse(stdin.readLineSync()!);

    print("Digite o segundo número:");
    double num2 = double.parse(stdin.readLineSync()!);

    print("Escolha uma operação: [+ - * /]");
    String operacao = stdin.readLineSync()!;

    double resultado = 0;

    if (operacao == '+') {
      resultado = num1 + num2;
    } else if (operacao == '-') {
      resultado = num1 - num2;
    } else if (operacao == '*') {
      resultado = num1 * num2;
    } else if (operacao == '/') {
      resultado = num1 / num2;
    } else {
      print("Operação inválida!");
      continue;
    }

    print("O resultado é: $resultado");

    print("Deseja fazer outra operação? [S/N]");
    String continuar = stdin.readLineSync()!.toUpperCase();

    if (continuar != 'S') {
      break;
    }
  }
}
