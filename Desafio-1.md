# Desafio-1-Promoção Relâmpago
###  Estrutura de Dados
## Desafio
Na loja de departamentos "SuperCompras", o gerente decidiu fazer uma promoção especial. Dependendo do valor da compra, os clientes receberão diferentes descontos. Sua missão é implementar um programa que determine o desconto aplicado com base no valor gasto!

### Entrada
A entrada deve receber uma string representando o valor da compra em reais, utilizando duas casas decimais. O valor será sempre positivo e não conterá caracteres especiais.

### Saída
Deverá retornar uma string informando o desconto aplicado. As regras são: se o valor for menor que 50, o desconto é de 0%. Se estiver entre 50 e 100, o desconto é de 10%. Acima de 100, o desconto é de 20%.

Exemplos
A tabela abaixo apresenta exemplos com alguns dados de entrada e suas respectivas saídas esperadas. Certifique-se de testar seu programa com esses exemplos e com outros casos possíveis.

| Entrada	| Saída |
| :---: | ----- |
| 49.99	| Desconto de 0% |
| 75.00	| Desconto de 10% |
| 150.00 | Desconto de 20% |

~~~~
import java.math.BigDecimal;
import java.util.Scanner;

        // TODO: Verifique se o valor é menor que 50.00:
        

       // TODO: Verifique se o valor é entre 50.00 e 100.00 (inclusive):
       

        // TODO: Caso contrário, o valor é maior que 100.00:
        
        
        // TODO: Retorne a string formatada com o desconto aplicado, conforme exigido no desafio:


public class PromocaoRelampago {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String valorCompra = scanner.nextLine();
        System.out.println(calcularDesconto(valorCompra));
        scanner.close();
    }

    public static String calcularDesconto(String valorCompra) {
        BigDecimal valor = new BigDecimal(valorCompra);

        if (valor.compareTo(new BigDecimal("50.00")) < 0) {
            return "Desconto de 0%";
        } else if (valor.compareTo(new BigDecimal("100.00")) <= 0) {
            return "Desconto de 10%";
        } else {
            return "Desconto de 20%";
        }
    }
}

// This code calculates the discount based on the purchase amount and prints the final price after applying the discount.

~~~~
