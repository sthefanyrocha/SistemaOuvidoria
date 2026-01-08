Apresentação do Código da Ouvidoria Universitária:

1. Conexão com Banco de Dados
conx = criarConexao("localhost","root","12345","ouvidoriaxyz")
Estabelece conexão com o banco de dados MySQL.
Parâmetros: servidor, usuário, senha e nome do banco.

2. Menu Principal
while opcao != 7:
    print("\nMenu de opções: \n1) Listagem...")  # Menu completo
    opcao = int(input("Digite a opção: "))
Loop principal que mantém o sistema em execução.
Oferece 7 opções de interação.

3. Operações Disponíveis

🔍 Listagem de Manifestações
consultaListagem = "select * from manifestacoes"
descricao = listarBancoDados(conx, consultaListagem)
Exibe todas as manifestações cadastradas
Mostra código, descrição, tipo, autor e ouvidor
🏷️ Listagem por Tipo
consultaListagemTipo = "select * from manifestacoes where tipo like %s"
Filtra manifestações por tipo (Reclamação/Elogio/Sugestão)
Interface amigável para seleção do tipo
➕ Cadastro de Nova Manifestação
consultaInsert = "insert into manifestacoes values (%s,%s,%s,%s)"
insertNoBancoDados(conx,consultaInsert,dados)
Coleta: descrição, autor, ouvidor e tipo
Valida campos obrigatórios
Retorna código da nova manifestação
🔢 Contagem de Manifestações
consultaListagem = "select count(*) from manifestacoes"
Exibe quantidade total de registros
📄 Pesquisa por Código
consultaPesquisa = "select * from manifestacoes where codigo = %s"
Localiza manifestação específica
Exibe todos os detalhes do registro
❌ Remoção de Manifestação
consultaRemover = "delete from manifestacoes where codigo = %s"
Remove registro permanentemente
Verifica existência do código antes de deletar

⚙️ Estrutura do Banco de Dados
A tabela manifestacoes deve conter:
Código (chave primária)
Manifestacao (texto da manifestação)
Autor (nome do solicitante)
Ouvidor (responsável pelo registro)
Tipo (Reclamação/Elogio/Sugestão)

🚀 Como Executar:
Configure o banco de dados MySQL
Instale as dependências necessárias
Execute o arquivo Python principal
Interaja com o sistema através do menu
