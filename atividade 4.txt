#include <stdio.h>

int main() {

int numeros[5];
int i;
int maior, menor;
int quantidadeImpares = 0;
int somaPares = 0, somaNegativos = 0;


printf("Digite 5 números inteiros:\n");
    for (i = 0; i < 5; ++i) {

printf("Número %d: ", i + 1);
scanf("%d", &numeros[i]);

    if (i == 0 || numeros[i] > maior)
        maior = numeros[i];
    if (i == 0 || numeros[i] < menor)
        menor = numeros[i];

    if (numeros[i] % 2 == 0) {
         somaPares += numeros[i];
        }

        if (numeros[i] < 0) {
            somaNegativos += numeros[i];
        }

        if (numeros[i] % 2 != 0) {
            quantidadeImpares++;
        }
    }

    float mediaPares = 0;
    for (i = 0; i < 5; ++i) {
        if (numeros[i] % 2 == 0) {
            mediaPares += numeros[i];
        }
    }
    if (somaPares > 0) {
        mediaPares /= somaPares;
    }

    float mediaTotal = 0;
    for (i = 0; i < 5; ++i) {
        mediaTotal += numeros[i];
    }
    mediaTotal /= 5;

    printf("\nResultados:\n");
    printf("Quantidade de números ímpares: %d\n", quantidadeImpares);
    printf("Quantidade de números negativos: %d\n", somaNegativos);
    printf("Maior número: %d\n", maior);
    printf("Menor número: %d\n", menor);
    printf("Média de números pares: %.2f\n", mediaPares);
    printf("Média de todos os números: %.2f\n", mediaTotal);

    return 0;
}