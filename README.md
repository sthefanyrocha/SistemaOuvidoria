# Apresentação do Código da Ouvidoria Universitária

A Ouvidoria da Universidade XYZ é o espaço certo para você dar sua opinião sobre o que acontece na universidade.  
Aqui, você pode enviar sugestões, fazer reclamações, deixar críticas construtivas ou até elogiar quando algo der certo (adoramos elogios!).  
A ideia é ouvir você de verdade e usar esse feedback para melhorar cada vez mais o nosso ambiente acadêmico.  
Fique à vontade para se expressar — a casa é sua também!  

---

## 1️⃣ Conexão com Banco de Dados
- Estabelece conexão com o banco de dados MySQL.  
- Parâmetros: servidor, usuário, senha e nome do banco.  

---

## 2️⃣ Menu Principal
- Loop principal que mantém o sistema em execução.  
- Oferece 7 opções de interação.  

---

## 3️⃣ Operações Disponíveis

### 🔍 Listagem de Manifestações
- Exibe todas as manifestações cadastradas.  
- Mostra código, descrição, tipo, autor e ouvidor.  

### 🏷️ Listagem por Tipo
- Filtra manifestações por tipo (Reclamação/Elogio/Sugestão).  
- Interface amigável para seleção do tipo.  

### ➕ Cadastro de Nova Manifestação
- Coleta: descrição, autor, ouvidor e tipo.  
- Valida campos obrigatórios.  
- Retorna código da nova manifestação.  

### 🔢 Contagem de Manifestações
- Exibe quantidade total de registros.  

### 📄 Pesquisa por Código
- Localiza manifestação específica.  
- Exibe todos os detalhes do registro.  

### ❌ Remoção de Manifestação
- Remove registro permanentemente.  
- Verifica existência do código antes de deletar.  

---

## ⚙️ Estrutura do Banco de Dados
A tabela `manifestacoes` deve conter:  

- Código (chave primária)  
- Manifestacao (texto da manifestação)  
- Autor (nome do solicitante)  
- Ouvidor (responsável pelo registro)  
- Tipo (Reclamação/Elogio/Sugestão)  

---

## 🚀 Como Executar
1. Configure o banco de dados MySQL  
2. Instale as dependências necessárias  
3. Execute o arquivo Python principal  
4. Interaja com o sistema através do menu

Trabalho acadêmico em Python, desenvolvido na faculdade, marcando a primeira experiência em projetos de programação! :)
