# Apresentação do Código da Ouvidoria Universitária

## 1️⃣ Conexão com Banco de Dados
```python
conx = criarConexao("localhost","root","12345","ouvidoriaxyz")

while opcao != 7:
    print("\nMenu de opções: \n1) Listagem...")  # Menu completo
    opcao = int(input("Digite a opção: "))

consultaListagem = "select * from manifestacoes"
descricao = listarBancoDados(conx, consultaListagem)

consultaListagemTipo = "select * from manifestacoes where tipo like %s"

consultaInsert = "insert into manifestacoes values (%s,%s,%s,%s)"
insertNoBancoDados(conx,consultaInsert,dados)

consultaListagem = "select count(*) from manifestacoes"

consultaPesquisa = "select * from manifestacoes where codigo = %s"

consultaRemover = "delete from manifestacoes where codigo = %s"

⚙️ Estrutura do Banco de Dados

A tabela manifestacoes deve conter:

Código (chave primária)

Manifestacao (texto da manifestação)

Autor (nome do solicitante)

Ouvidor (responsável pelo registro)

Tipo (Reclamação/Elogio/Sugestão)

🚀 Como Executar

Configure o banco de dados MySQL

Instale as dependências necessárias

Execute o arquivo Python principal

Interaja com o sistema através do menu


---

Se você quiser, posso também criar **uma versão final com um resumo inicial curto**, pra ficar **mais chamativo na visualização do GitHub**, sem alterar o conteúdo principal.  

Quer que eu faça isso também?
