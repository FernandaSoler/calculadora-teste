# calculadora-teste: Soma e Subtração

def soma(a, b):
    return a + b

def subtrai(a, b):
    return a - b

def main():
    print("Bem-vindo à Calculadora Simples!")
    while True:
        print("\nEscolha a operação:")
        print("1 - Somar")
        print("2 - Subtrair")
        print("0 - Sair")
        opcao = input("Digite a opção: ")

        if opcao == "0":
            print("Encerrando a calculadora. Até logo!")
            break

        if opcao not in ["1", "2"]:
            print("Opção inválida! Tente novamente.")
            continue

        try:
            num1 = float(input("Digite o primeiro número: "))
            num2 = float(input("Digite o segundo número: "))
        except ValueError:
            print("Por favor, digite números válidos.")
            continue

        if opcao == "1":
            resultado = soma(num1, num2)
            print(f"O resultado da soma é: {resultado}")
        else:
            resultado = subtrai(num1, num2)
            print(f"O resultado da subtração é: {resultado}")

if _name_ == "_main_":
    main()
