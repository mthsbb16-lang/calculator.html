def calculadora():
    print("Calculadora Simples")
    print("Operações disponíveis: +, -, *, /")
    
    while True:
        try:
            # Entrada do usuário
            num1 = float(input("Digite o primeiro número: "))
            operacao = input("Digite a operação (+, -, *, /): ")
            num2 = float(input("Digite o segundo número: "))
            
            # Verifica a operação e calcula
            if operacao == '+':
                resultado = num1 + num2
            elif operacao == '-':
                resultado = num1 - num2
            elif operacao == '*':
                resultado = num1 * num2
            elif operacao == '/':
                if num2 == 0:
                    print("Erro: Divisão por zero!")
                    continue
                resultado = num1 / num2
            else:
                print("Operação inválida! Use +, -, * ou /")
                continue
                
            # Exibe o resultado
            print(f"Resultado: {num1} {operacao} {num2} = {resultado}")
            
            # Pergunta se quer continuar
            continuar = input("Deseja fazer outro cálculo? (s/n): ")
            if continuar.lower() != 's':
                print("Calculadora encerrada.")
                break
                
        except ValueError:
            print("Erro: Digite números válidos!")
            
# Executa a calculadora
calculadora()
