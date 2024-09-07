# Gerenciador de Produtos com PyQt5 e MySQL

Este projeto é uma aplicação desktop de gerenciamento de produtos desenvolvida com **PyQt5** para a interface gráfica e **MySQL** para o banco de dados. A aplicação permite realizar as operações básicas de CRUD (Criar, Ler, Atualizar e Deletar) em um banco de dados de produtos e gerar relatórios em formato PDF usando **ReportLab**.

## Funcionalidades

- **Cadastro de Produtos**: Adicione produtos com código, descrição, preço e categoria.
- **Edição de Produtos**: Atualize os detalhes de produtos existentes.
- **Exclusão de Produtos**: Remova produtos da base de dados.
- **Visualização de Produtos**: Exiba os produtos cadastrados em uma tabela interativa.
- **Geração de PDF**: Gere relatórios em PDF dos produtos cadastrados.

## Dependências

As bibliotecas e ferramentas utilizadas neste projeto são:

- **PyQt5**: Para criação da interface gráfica.
- **mysql-connector-python**: Para conectar e interagir com o banco de dados MySQL.
- **ReportLab**: Para geração de relatórios em PDF.

### Instalação das dependências

Você pode instalar as dependências usando o seguinte comando:

```bash
pip install PyQt5 mysql-connector-python reportlab ```

# Configuração do banco de dados

A aplicação conecta-se a um banco de dados MySQL chamado cadastro_produtos. Certifique-se de ter o MySQL instalado e crie o banco de dados e a tabela conforme necessário.
``` python
CREATE DATABASE cadastro_produtos;
USE cadastro_produtos;

CREATE TABLE produtos (
  id INT AUTO_INCREMENT PRIMARY KEY,
  codigo VARCHAR(50),
  descricao VARCHAR(255),
  preco DECIMAL(10, 2),
  categoria VARCHAR(100)
);
```
No código, ajuste as credenciais de conexão ao banco de dados:

```
banco = mysql.connector.connect(
    host ="localhost",
    user="root",
    passwd="**********",
    database="cadastro_produtos"
)
 ```
# Como executar
1. Certifique-se de que as dependências estão instaladas e o banco de dados configurado.
2. Inicie a aplicação executando o arquivo principal do projeto. Por exemplo:
bash
```
python nome_do_arquivo.py
```
3. A interface gráfica será aberta, onde você poderá realizar operações no banco de dados diretamente pela interface.

# Funcionalidades detalhadas
* Cadastro de Produtos: A partir da tela principal, insira os dados do produto e clique em "Cadastrar".
* Edição de Produtos: Selecione um produto na lista, clique em "Editar", modifique os dados e salve as alterações.
* Exclusão de Produtos: Selecione um produto e clique em "Excluir" para removê-lo.
* Geração de PDF: Clique em "Gerar PDF" para exportar a lista de produtos cadastrados.

# Arquivos UI
Os arquivos de interface (arquivos .ui) devem ser gerados ou carregados no projeto:
* formulario.ui: Interface para cadastro de produtos.
* listardados.ui: Interface para listagem de produtos.
* menu_editar.ui: Interface para edição de produtos.

# Melhorias futuras
* Implementar autenticação de usuários.
* Adicionar filtros de pesquisa para a tabela de produtos.
* Melhorar a interface gráfica para uma experiência de usuário mais fluida.

# Contribuição
Sinta-se à vontade para contribuir com melhorias ou relatórios de bugs!
