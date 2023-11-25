#include <stdio.h>

int main() {

char nomes[5][50];
int idades[5];
float pesos[5];
float alturas[5];
int i;
float maiorAltura = 0, menorAltura = 0, maiorPeso = 0, menorPeso = 0;
int maisVelho = 0, maisNovo = 0;
char pessoaAlta[50], pessoaBaixa[50], pessoaPesada[50], pessoaLeve[50], pessoaVelha[50], pessoaNova[50];



    for (i = 0; i < 5; i++) {
        printf("Informe o nome da pessoa %d: ", i + 1);
        scanf("%s", nomes[i]);
        printf("Informe a idade de %s: ", nomes[i]);
        scanf("%d", &idades[i]);
        printf("Informe o peso de %s: ", nomes[i]);
        scanf("%f", &pesos[i]);
        printf("Informe a altura de %s: ", nomes[i]);
        scanf("%f", &alturas[i]);
    }

    for (int i = 0; i < 5; i++) {
        if (alturas[i] > maiorAltura) {
            maiorAltura = alturas[i];
            strcpy(pessoaAlta, nomes[i]);
        }

        if (alturas[i] < menorAltura || menorAltura == 0) {
            menorAltura = alturas[i];
            strcpy(pessoaBaixa, nomes[i]);
        }

        if (pesos[i] > maiorPeso) {
            maiorPeso = pesos[i];
            strcpy(pessoaPesada, nomes[i]);
        }

        if (pesos[i] < menorPeso || menorPeso == 0) {
            menorPeso = pesos[i];
            strcpy(pessoaLeve, nomes[i]);
        }

        if (idades[i] > maisVelho) {
            maisVelho = idades[i];
            strcpy(pessoaVelha, nomes[i]);
        }

        if (idades[i] < maisNovo || maisNovo == 0) {
            maisNovo = idades[i];
            strcpy(pessoaNova, nomes[i]);
        }
    }

    printf("Pessoa mais alta: %s - Altura: %.2f\n", pessoaAlta, maiorAltura);
    printf("Pessoa mais baixa: %s - Altura: %.2f\n", pessoaBaixa, menorAltura);
    printf("Pessoa mais pesada: %s - Peso: %.2f\n", pessoaPesada, maiorPeso);
    printf("Pessoa mais leve: %s - Peso: %.2f\n", pessoaLeve, menorPeso);
    printf("Pessoa mais velha: %s - Idade: %d\n", pessoaVelha, maisVelho);
    printf("Pessoa mais nova: %s - Idade: %d\n", pessoaNova, maisNovo);

    return 0;
}