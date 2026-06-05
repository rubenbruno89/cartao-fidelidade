# 💳 Cartão Fidelidade Digital Seguro

Sistema simples, direto e à prova de fraudes para gerenciar cartões fidelidade de clientes. 

🚀 **Acesse agora a versão online:** [https://rubenbruno89.github.io/cartao-fidelidade/](https://rubenbruno89.github.io/cartao-fidelidade/)

---

## 🔒 Como funciona a segurança?

O sistema utiliza **Assinatura Digital (HMAC-SHA256)** para garantir que os pontos não sejam alterados pelo cliente. 

Quando você gera um cartão, o sistema cria um arquivo com os dados do cliente e uma "assinatura" matemática baseada em uma **Chave Secreta** que só você conhece. 

Se o cliente tentar abrir o arquivo no Bloco de Notas e alterar os pontos (ex: mudar de 5 para 50), a assinatura deixará de bater com os dados. Ao importar o arquivo, o sistema detectará a alteração instantaneamente e bloqueará a ação, alertando sobre a tentativa de fraude.

---

## 📖 Como usar no dia a dia

### ⚠️ Passo 0: A Chave Secreta (Muito Importante!)
A primeira vez que abrir o sistema, você verá um campo chamado **"Chave Secreta"**. 
* Crie uma senha forte (ex: `MinhaLoja_Segredo_2024!`).
* **ANOTE ESSA SENHA.** Se você perdê-la, não conseguirá ler os cartões antigos.
* **NUNCA** compartilhe essa senha com os clientes.
* *Dica: O sistema lembrará a senha apenas enquanto a aba estiver aberta. Se fechar a página, precisará digitar novamente.*

---

### 🆕 1. Cadastrar um Novo Cliente
Quando um cliente pedir um cartão fidelidade pela primeira vez:
1. Acesse o sistema: [https://rubenbruno89.github.io/cartao-fidelidade/](https://rubenbruno89.github.io/cartao-fidelidade/)
2. Digite sua **Chave Secreta**.
3. Preencha o **Nome do Cliente**.
4. Crie um **ID do Cartão** (pode ser o telefone do cliente, CPF ou um número sequencial como `001`).
5. Deixe os **Pontos Atuais** em `0`.
6. Clique em **💾 Gerar Arquivo do Cartão**.
7. Um arquivo `.json` será baixado. **Envie este arquivo para o cliente** (por WhatsApp, E-mail, etc).

---

### ➕ 2. O cliente comprou! (Adicionar Pontos)
Quando o cliente for à loja e precisar pontuar:
1. Peça para o cliente **enviar o arquivo `.json`** do cartão dele para você (pelo WhatsApp, por exemplo).
2. Salve o arquivo no seu computador ou celular.
3. No sistema, vá até a seção **🔍 Validar e Adicionar Ponto**.
4. Digite sua **Chave Secreta**.
5. Clique em "Escolher arquivo" e selecione o arquivo `.json` que o cliente enviou.
6. Clique em **✅ Validar e Adicionar 1 Ponto**.

**O que vai acontecer?**
* ✅ **Se o arquivo for original:** O sistema mostrará uma mensagem verde de sucesso, adicionará +1 ponto automaticamente e baixará um **novo arquivo atualizado**. Você deve enviar este novo arquivo de volta para o cliente substituir o antigo.
* 🚨 **Se o cliente tentou fraudar:** O sistema mostrará uma mensagem vermelha de **ALERTA DE FRAUDE**. O arquivo foi adulterado. Neste caso, não adicione pontos e chame a atenção do cliente.

---

## 💻 Rodando Localmente (Sem Internet)
Como o sistema é feito apenas em HTML e JavaScript, você não precisa de internet para usá-lo após o primeiro acesso.
1. Acesse o sistema online.
2. Clique com o botão direito na página e selecione "Salvar como..." (ou "View Page Source" e salve como `.html`).
3. Salve o arquivo no seu computador ou celular.
4. Basta dar dois cliques no arquivo para abrir o sistema no seu navegador, mesmo offline.

---

## 🛠️ Tecnologias Utilizadas
* HTML5 / CSS3
* JavaScript (Vanilla)
* Web Crypto API (Para geração do HMAC-SHA256)

---

## ⚠️ Avisos de Segurança
* **Backup:** Faça backups periódicos dos arquivos `.json` dos seus clientes.
* **Sigilo:** A segurança do sistema depende 100% da sua Chave Secreta. Mantenha-a em sigilo.
* **Alteração de Chave:** Se você decidir mudar a Chave Secreta no futuro, todos os cartões antigos gerados com a chave anterior se tornarão inválidos. Você terá que gerar novos cartões para todos os clientes.

---

Desenvolvido para facilitar a gestão de pequenos e médios negócios.
