#include <stdio.h>

int main() {

    char codigo1[4];
    char cidade [10];
    int populacao1, populacao2;
    float area1, area2, pib1, pib2, densidade1, densidade2, poder1, poder2, capta1, capta2;
    int pontos_turisticos1, pontos_turisticos2;

    char codigo2[4];
    char cidade2 [10];
   
    printf("Digite o código da primeira cidade (Ex: A01): ");
    scanf("%s", codigo1);

    printf("Digite a população: ");
    scanf("%d", &populacao1);

    printf("Digite a área (em km): ");
    scanf("%f", &area1);

    printf("Digite o PIB (em milhões): ");
    scanf("%f", &pib1);

    printf("Pontos turísticos: ");
    scanf("%d", &pontos_turisticos1);

    densidade1 = populacao1/area1;
    capta1 = pib1/populacao1;
    poder1 =(1.0/densidade1) + populacao1 + pib1 + area1 + capta1;

    printf("Digite o código da segunda cidade (Ex: B02): ");
    scanf("%s", codigo2);

    printf("Digite a população: ");
    scanf("%d", &populacao2);

    printf("Digite a área (em km²): ");
    scanf("%f", &area2);

    printf("Digite o PIB (em bilhões): ");
    scanf("%f", &pib2);

    printf("Digite o número de pontos turísticos: ");
    scanf("%d", &pontos_turisticos2);

    densidade2 = populacao2/area2 ;
    capta2 = pib2/populacao2;
    
    poder2 = (1.0/densidade2) + populacao2 + pib2 + area2 + capta2;

    printf("Cidade %s:", codigo1);
    printf("População: %d habitantes", populacao1);
    printf("Área: %.2f km²", area1);
    printf("PIB: %.2f bilhões", pib1);
    printf("Pontos turísticos: %d", pontos_turisticos1);
    printf("A densidade da cidade é %f pessoas por km²", densidade1);
    printf("O PIB per capta é %f R$ por pessoa",capta1);
    printf("O poder da cidade %s é %f", codigo1, poder1);

    printf("\nCidade %s:", codigo2);
    printf("População: %d habitantes", populacao2);
    printf("Área: %.2f km²", area2);
    printf("PIB: %.2f bilhões", pib2);
    printf("Pontos turísticos: %d", pontos_turisticos2);
    printf("A densidade da cidade é %f pessoas por km²", densidade2);
    printf("O PIB per capta é %f R$ por pessoa",capta2);
    printf("o poder da cidade %s é %f", codigo2, poder2);
    if (populacao1 > populacao2) 
    printf("População: %s vence", codigo1);
    else if (populacao2 > populacao1) printf("População: %s vence", codigo2);
    else printf("População: Empate\n");

    if (area1 > area2)
    printf("Área: %s vence", codigo1);
    else if (area2 > area1) 
    printf("Área: %s vence", codigo2);
    else printf("Área: Empate");

    if (pib1 > pib2) printf("PIB: %s vence", codigo1);
    else if (pib2 > pib1) 
    printf("PIB: %s vence", codigo2);
    else printf("PIB: Empate");

    if (pontos_turisticos1 > pontos_turisticos2) 
    printf("Pontos turísticos: %s vence", codigo1);
    else if (pontos_turisticos2 > pontos_turisticos1) 
    printf("Pontos turísticos: %s vence", codigo2);
    else printf("Pontos turísticos: Empate");

    if (densidade1 < densidade2) 
    printf("Densidade populacional: %s vence", codigo1);
    else if (densidade2 < densidade1)
    printf("Densidade populacional: %s vence", codigo2);
    else printf("Densidade populacional: Empate");

    if (capta1 > capta2) 
    printf("PIB per capita: %s vence", codigo1);
    else if (capta2 > capta1) 
    printf("PIB per capita: %s vence", codigo2);
    else printf("PIB per capita: Empate");

    if (poder1 > poder2) 
    printf("Poder da cidade: %s vence", codigo1);
    else if (poder2 > poder1) 
    printf("Poder da cidade: %s vence", codigo2);
    else printf("Poder da cidade: Empate");

    return 0;
}
