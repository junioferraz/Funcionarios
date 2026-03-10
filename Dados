lista_funcionarios = []
id_global = 1


def exibir_funcionario(func):
    print("\n------------------------------")
    print(f"ID: {func['id']} | Nome: {func['nome']}")
    print(f"Setor: {func['setor']} | Salário: R$ {func['salario']:.2f}")
    print("------------------------------")


def cadastrar_funcionario(id_func):
    print("\n--- Cadastro de Funcionário ---")
    nome = input("Nome: ")
    setor = input("Setor: ")
    salario = float(input("Salário: "))
    lista_funcionarios.append({'id': id_func, 'nome': nome, 'setor': setor, 'salario': salario})
    print("Funcionário cadastrado!")


def consultar_funcionarios():
    print("\n--- Consultar ---")
    print("1. Todos | 2. Por ID | 3. Por Setor | 4. Voltar")
    opcao = input("Opção: ")

    if opcao == '1':
        for func in lista_funcionarios: exibir_funcionario(func)
    elif opcao == '2':
        id_pesq = int(input("Digite o ID: "))
        encontrado = next((f for f in lista_funcionarios if f['id'] == id_pesq), None)
        if encontrado:
            exibir_funcionario(encontrado)
        else:
            print("ID não encontrado.")
    elif opcao == '3':
        setor_pesq = input("Digite o setor: ").lower()
        encontrados = [f for f in lista_funcionarios if f['setor'].lower() == setor_pesq]
        if encontrados:
            for f in encontrados: exibir_funcionario(f)
        else:
            print("Nenhum funcionário encontrado.")


def remover_funcionario():
    try:
        id_remover = int(input("Digite o ID do funcionário a ser removido: "))
        for func in lista_funcionarios:
            if func['id'] == id_remover:
                lista_funcionarios.remove(func)
                print("Funcionário removido!")
                return
        print("ID não encontrado.")
    except ValueError:
        print("Erro: Digite um ID numérico válido.")


# Loop Principal
while True:
    print("\n--- MENU --- 1. Cadastrar | 2. Consultar | 3. Remover | 4. Sair")
    opcao = input("Opção: ")
    if opcao == '1':
        cadastrar_funcionario(id_global)
        id_global += 1
    elif opcao == '2':
        consultar_funcionarios()
    elif opcao == '3':
        remover_funcionario()
    elif opcao == '4':
        break
