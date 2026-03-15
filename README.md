# Sistema de Gestão de Funcionários 

Uma aplicação em Python desenvolvida para o gerenciamento básico de informações de funcionários, permitindo o controle de cadastro, consulta por diferentes critérios e exclusão de registros.

## 📋 Funcionalidades
* **Cadastro:** Registro automatizado de funcionários com atribuição de ID único (auto-incremento).
* **Consultas Flexíveis:**
    * **Geral:** Lista todos os funcionários cadastrados.
    * **Por ID:** Busca específica por identificador único.
    * **Por Setor:** Filtro para listar todos os funcionários de um determinado departamento.
* **Remoção:** Exclusão de funcionários através do seu ID com validação de entrada de dados.

## 🛠 Lógica de Funcionamento
* **Armazenamento:** Utiliza uma lista (`lista_funcionarios`) de dicionários para armazenar os dados em tempo de execução.
* **Busca:** Implementa o uso de `next()` e *list comprehensions* para otimizar a localização de dados baseados em critérios específicos.
* **Modularização:** O sistema é dividido em funções lógicas (`exibir_funcionario`, `cadastrar_funcionario`, `consultar_funcionarios`, `remover_funcionario`), facilitando a manutenção e a legibilidade do código.
