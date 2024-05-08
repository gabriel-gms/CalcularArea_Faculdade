#include <stdio.h>
#include <stdlib.h>
#include <windows.h>
#include <locale.h>

int main() {
    int op;
    float area, base, baseMenor, altura, lado, raio;

    setlocale(LC_ALL, "Portuguese");
	system ("color 0A");

    do {
        printf("\n\n=====CALCULAR AREA DO:=====\n1 - Triangulo\n2 - Quadrado\n3 - Retangulo\n4 - Trapezio\n5 - Circulo\n6 - Sair\nOpcao: ");
        scanf("%d", &op);

        switch (op)
        {
        case 1:
        	system ("cls");
            printf("\nInforme o tamanho da base: ");
            scanf("%f", &base);
            printf("\nInforme a altura: ");
            scanf("%f", &altura);

            area = (base * altura) / 2;
            printf("Area do triangulo: %f", area);
            break;
        case 2:
        	system ("cls");
            printf("\nInforme o lado: ");
            scanf("%f", &lado);

            area = lado*lado;
            printf("\nArea do quadrado: %f", area);
            break;
        case 3:
        	system ("cls");
            printf("\nInforme o tamanho da base: ");
            scanf("%f", &base);
            printf("\nInforme a altura: ");
            scanf("%f", &altura);

            area = base * altura;
            printf("\nArea do retangulo: %f", area);
            break;
        case 4:
        	system ("cls");
            printf("\nInforme o tamanho da base maior: ");
            scanf("%f", &base);
            printf("\nInforme o tamanho da base menor: ");
            scanf("%f", &baseMenor);
            printf("\nInforme a altura: ");
            scanf("%f", &altura);

            area = ((base + baseMenor) * altura) / 2;
            printf("\nArea do trapezio: %f", area);
            break;
        case 5:
        	system("cls");
            printf("\nInforme o raio: ");
            scanf("%f", &raio);

            area = 3.14159 * raio;
            printf("\nArea aproximada do circulo: %f", area);
            break;
        case 6:
        	system("cls");
            printf("\nPrograma finalizado.");
            break;
        default:
        	system ("cls");
            printf("\nOpcao invalida.");
            break;
        }
    } while (op != 6);
    
    return 0;
}
