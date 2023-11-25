#include <stdio.h>

int main() {
    
int totalVendas = 0;
char nomesProdutos[100][50];
float precos[100];
int quantidades[100];
int opcao;
int i;


do {
printf("\nMenu:\n");
printf("1 - Adicionar uma venda\n");
printf("2 - Exibir total de vendas e sair\n");
printf("Escolha uma opção: ");
scanf("%d", &opcao);

 switch (opcao) {
   case 1:
      if (totalVendas < 100) {

printf("Digite o nome do produto: ");
scanf("%s", nomesProdutos[totalVendas]);

printf("Digite o preço do produto: ");
scanf("%f", &precos[totalVendas]);

printf("Digite a quantidade vendida: ");
scanf("%d", &quantidades[totalVendas]);

  totalVendas++;
printf("Venda registrada com sucesso!\n");
 } else {
printf("Limite de vendas atingido. Não é possível adicionar mais vendas.\n");
}
    break;

    case 2:
     if (totalVendas > 0) {
       float total = 0;
    for (i = 0; i < totalVendas; ++i) {
                        
        float subtotal = precos[i] * quantidades[i];
printf("Produto: %s, Preço: %.2f, Quantidade: %d, Subtotal: %.2f\n",

nomesProdutos[i], precos[i], quantidades[i], subtotal);
      
      total += subtotal;
}
                    
printf("Total de vendas: %.2f\n", total);
  } else {
printf("Nenhuma venda registrada ainda.\n");
}
    break;

    default:
printf("Opção inválida. Tente novamente.\n");
}

} while (opcao != 2);


    return 0;
}