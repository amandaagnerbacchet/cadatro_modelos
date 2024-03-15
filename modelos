#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define MAX_MODELS 100

// Estrutura para representar um modelo
typedef struct {
    char nome[50];
    int idade;
    float altura;
} Modelo;

// Função para adicionar um novo modelo
void adicionarModelo(Modelo modelos[], int *numModelos) {
    if (*numModelos < MAX_MODELS) {
        Modelo novoModelo;
        printf("Nome do modelo: ");
        scanf("%s", novoModelo.nome);
        printf("Idade do modelo: ");
        scanf("%d", &novoModelo.idade);
        printf("Altura do modelo: ");
        scanf("%f", &novoModelo.altura);

        modelos[*numModelos] = novoModelo;
        (*numModelos)++;
        printf("Modelo adicionado com sucesso!\n");
    } else {
        printf("Não é possível adicionar mais modelos. Limite atingido.\n");
    }
}

// Função para exibir todos os modelos cadastrados
void exibirModelos(Modelo modelos[], int numModelos) {
    printf("\nLista de modelos:\n");
    for (int i = 0; i < numModelos; i++) {
        printf("Nome: %s\n", modelos[i].nome);
        printf("Idade: %d\n", modelos[i].idade);
        printf("Altura: %.2f\n", modelos[i].altura);
        printf("--------------------\n");
    }
}

int main() {
    Modelo modelos[MAX_MODELS];
    int numModelos = 0;
    int opcao;

    do {
        printf("\nAgência de Modelos\n");
        printf("1. Adicionar Modelo\n");
        printf("2. Exibir Modelos\n");
        printf("3. Sair\n");
        printf("Escolha uma opção: ");
        scanf("%d", &opcao);

        switch(opcao) {
            case 1:
                adicionarModelo(modelos, &numModelos);
                break;
            case 2:
                exibirModelos(modelos, numModelos);
                break;
            case 3:
                printf("Saindo do programa...\n");
                break;
            default:
                printf("Opção inválida. Tente novamente.\n");
        }
    } while(opcao != 3);

    return 0;
}
