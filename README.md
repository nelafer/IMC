# IMC
def calcular_imc(peso, altura):
    imc = peso / (altura ** 2)
    
    # Categorias
    if imc < 18.5:
        categoria = "Abaixo do peso"
    if 18.5 <= imc < 24.9:
        categoria = "Peso normal"
    if 25 <= imc < 29.9:
        categoria = "Sobrepeso"
    if 30 <= imc < 34.9:
        categoria = "Obesidade grau 1"
    if 35 <= imc < 39.9:
        categoria = "Obesidade grau 2"
    if imc >= 40:
        categoria = "Obesidade grau 3"
    
    return imc, categoria

# Exemplo de uso:
peso = float(input("Digite seu peso em kg: "))
altura = float(input("Digite sua altura em metros: "))

imc, categoria = calcular_imc(peso, altura)

print(f"Seu IMC é: {imc:.2f}")
print(f"Categoria: {categoria}")
