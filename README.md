# ProjetoPI
Esse e o gerenciador de estoque. Qualquer coisa podem me perguntar.
1. A primeira parte do código importa os módulos necessários: sqlite3 para interagir com o banco de dados SQLite, sys para interromper o programa e time para adicionar atrasos nas operações.

2. Em seguida, temos a definição da classe GerenciadorProdutos. Essa classe lida com a criação do banco de dados, a adição e remoção de produtos. No método __init__, é feita a conexão com o banco de dados (ou criação do arquivo do banco de dados, se não existir) e a criação da tabela "produtos" caso ela não exista.

3. O método add_produto da classe GerenciadorProdutos permite adicionar um novo produto ao banco de dados. Ele recebe o nome, preço e quantidade do produto como argumentos, insere esses valores na tabela "produtos" e confirma a transação.

4. O método remover_produto da classe GerenciadorProdutos permite remover um produto do banco de dados com base em seu nome. Ele executa uma consulta para excluir o produto da tabela "produtos" com base no nome fornecido e confirma a transação.

5. O método fechar_conexao da classe GerenciadorProdutos fecha a conexão com o banco de dados.

6. Em seguida, temos a definição da classe InterfaceUsuario. Essa classe lida com a interação do usuário, exibindo um menu e executando as ações correspondentes com base na escolha do usuário.

7. O método __init__ da classe InterfaceUsuario cria uma instância da classe GerenciadorProdutos para acessar seus métodos.

8. O método add_produto da classe InterfaceUsuario solicita ao usuário que insira o nome, preço e quantidade do produto e chama o método add_produto do GerenciadorProdutos para adicionar o produto ao banco de dados.

9. O método remover_produto da classe InterfaceUsuario solicita ao usuário que insira o nome do produto a ser removido e chama o método remover_produto do GerenciadorProdutos para remover o produto do banco de dados.

10. O método interromper_programa da classe InterfaceUsuario encerra o programa exibindo uma mensagem de encerramento e chamando o método fechar_conexao do GerenciadorProdutos para fechar a conexão com o banco de dados. Em seguida, o programa é encerrado usando sys.exit().

11. O método fechar_conexao da classe InterfaceUsuario chama o método fechar_conexao do GerenciadorProdutos para fechar a conexão com o banco de dados.

12. Por fim, o bloco if __name__ == "__main__" cria uma instância da classe InterfaceUsuario e inicia um loop que exibe um menu de opções para o usuário. O programa solicita ao usuário que escolha uma opção (adicionar produto, remover produto ou sair) e executa a ação correspondente com base na escolha do usuário.
