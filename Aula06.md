# Relatório de Avaliação de Prompts - Cálculo de Média

Este relatório apresenta a avaliação de três diferentes abordagens de engenharia de prompt (**Neutro**, **Persona** e **Restritivo**) para a criação de um código de cálculo de média estudantil.

## Tabela de Avaliação

| Modelo de Prompt | Precisão Lógica | Clareza e Eficiência | Taxa de Alucinação |
| :--- | :--- | :--- | :--- |
| **Neutro** | **Sim.** Cálculo correto e algoritmo funcional em Python e JS. | **Limpo e direto.** Código organizado e de fácil leitura. | **Não.** Manteve-se estritamente ao pedido. |
| **Persona** | **Sim.** Algoritmo correto, funcional e com validações de entrada. | **Voltas desnecessárias.** Código longo devido à persona de "dev sênior". | **Não.** Obedeceu ao prompt fielmente. |
| **Restritivo** | **Sim.** Cálculo funciona e utiliza Python puro conforme solicitado. | **Totalmente limpo.** Código conciso (one-liner), sem excessos. | **Não.** Respeitou todas as restrições impostas. |

---

## Detalhes dos Prompts e Respostas da IA

### 1. Modelo Neutro
**Prompt:** *"faça um codigo funcional para calcular a media de notas de um aluno"*

```python
def calcular_media(notas):
    if not notas:
        return 0
    soma = sum(notas)
    media = soma / len(notas)
    return media

# Exemplo de uso:
lista_de_notas = [7.5, 8.0, 6.0, 9.5]
resultado = calcular_media(lista_de_notas)

print(f"As notas do aluno foram: {lista_de_notas}")
print(f"A média final é: {resultado:.2f}")

if resultado >= 7.0:
    print("Status: Aprovado")
else:
    print("Status: Recuperação")
```
### 2. Modelo Persona (Dev Sênior)
**Prompt:** *"voce e um dev sênior exigente que trabalhar em uma universidade muito pretigíada, e preciso que elabore um programa que calcule a média de um estudante"*

```python
def calcular_media():
    try:
        quantidade = int(input("Quantas notas deseja inserir? "))

        if quantidade <= 0:
            print("Quantidade inválida.")
            return

        soma = 0

        for i in range(quantidade):
            nota = float(input(f"Digite a nota {i + 1}: "))
            
            if nota < 0 or nota > 10:
                print("Nota inválida. Digite valores entre 0 e 10.")
                return

            soma += nota

        media = soma / quantidade

        print(f"\nMédia final: {media:.2f}")

        if media >= 7:
            print("Status: Aprovado")
        elif media >= 5:
            print("Status: Recuperação")
        else:
            print("Status: Reprovado")

    except ValueError:
        print("Entrada inválida. Digite apenas números.")

calcular_media()

```

### 3. Modelo Restritivo
**Prompt:** *"Crie um codigo funcional que calcule a media de notas de um aluno (use apenas python puro sem blibliotecas, entregue em formato de codigo, sem explicaçoes, o codigo precisar ser o menor possivel)"*

```python
n = [float(x) for x in input("Notas: ").split()]
print(sum(n)/len(n) if n else 0)
