# 💳 Cartão Fidelidade Digital (PDF & QR Code)

Sistema profissional e à prova de fraudes para gerenciar cartões fidelidade. Emite cartões em formato **PDF** contendo **QR Codes** assinados criptograficamente.

🚀 **Acesse a versão online:** [https://rubenbruno89.github.io/cartao-fidelidade/](https://rubenbruno89.github.io/cartao-fidelidade/)

---

## 🔒 Segurança Anti-Fraude
Muitos clientes têm receio de baixar arquivos `.json` ou `.txt` por medo de vírus. Este sistema resolve isso emitindo um **PDF tradicional**, que passa confiança. 

A segurança está no **QR Code embutido**: ele contém os dados do cliente e uma assinatura digital (HMAC-SHA256) gerada por uma Chave Secreta que só o lojista possui. Se o cliente tentar editar o PDF ou falsificar um QR Code, o sistema detecta a fraude instantaneamente na hora do escaneamento.

---

## 📖 Como usar no dia a dia

### ⚠️ Passo 0: A Chave Secreta
* Defina uma **Chave Secreta** forte no sistema e **NUNCA** a compartilhe.
* Anote-a em local seguro. Se perdê-la, não conseguirá validar cartões antigos.

### 🆕 1. Cadastrar Novo Cliente
1. Preencha o Nome e ID do cliente na tela inicial.
2. Clique em **💾 Gerar PDF do Cartão**.
3. Um arquivo PDF estilizado com um QR Code será baixado.
4. Envie este PDF para o cliente (WhatsApp, E-mail, etc). O cliente deve salvá-lo no celular.

### ➕ 2. Adicionar Pontos (Na hora da compra)

O sistema oferece **3 formas** de validar o cartão do cliente:

#### 📸 Opção A: Câmera ao vivo (Presencial)
1. Peça para o cliente abrir o PDF e mostrar o QR Code na tela do celular.
2. Clique em **📸 Ligar Câmera para Escanear**.
3. Aponte para o celular do cliente.
4. O sistema lê, valida, soma 1 ponto e baixa automaticamente um novo PDF.
5. Envie o novo PDF para o cliente guardar.

#### 🖼️ Opção B: Enviar Imagem (Cliente mandou print)
1. Se o cliente enviou um print/screenshot do cartão por WhatsApp.
2. Clique na área **"Opção 2: Enviar Foto/Imagem do Cartão"**.
3. Faça o upload da imagem.
4. O sistema valida e gera o novo PDF atualizado.

#### 📄 Opção C: Enviar Arquivo PDF (Recomendado à distância)
1. Se o cliente enviou o **arquivo PDF original** pelo WhatsApp/E-mail.
2. Clique na área **"Opção 3: Enviar arquivo PDF do Cartão"**.
3. Selecione o PDF baixado.
4. O sistema abre o PDF automaticamente, encontra o QR Code, valida a assinatura e gera o novo PDF com +1 ponto.
5. Envie o novo PDF de volta para o cliente.

---

## 🛠️ Tecnologias
* **jsPDF**: Geração dos cartões em PDF.
* **qrcode-generator**: Criação dos QR Codes de segurança.
* **html5-qrcode**: Leitura dos códigos via câmera ou upload de imagens.
* **PDF.js (Mozilla)**: Renderização de PDFs para leitura do QR Code embutido.
* **Web Crypto API**: Assinatura HMAC-SHA256 (Nativo do navegador).

---

Desenvolvido para modernizar a fidelidade de pequenos e médios negócios com segurança de nível bancário, sem a complexidade de servidores.
