# Minha Rotina

Site da rotina da família.

- `index.html`: **Minha Rotina** (adultos). Entra com conta Google, sincroniza celular e computador. Hábitos, diário, semana e revisão são de cada pessoa; cardápio e lista de compras são da casa.
- `criancas.html`: **Meu Dia** (Zoé e Léo). Não precisa de login; salva no próprio celular de cada um.

## Configurar o Firebase (uma vez, uns 10 minutos)

1. Entre em https://console.firebase.google.com com sua conta Google e clique em **Criar um projeto** (ou **Começar com um projeto do Firebase**). Nome: `minha-rotina`. Pode desativar o Google Analytics e clicar em **Criar projeto**.
2. No menu da esquerda, abra **Criação** e depois **Authentication**. Clique em **Vamos começar**. Na aba **Método de login**, escolha **Google**, ative a chave, escolha seu e-mail de suporte e clique em **Salvar**.
   Ainda em Authentication, abra a aba **Configurações**, depois **Domínios autorizados**, clique em **Adicionar domínio** e digite `SEU-USUARIO.github.io`.
3. Volte para a **Visão geral do projeto** (ícone da casinha no topo do menu). Clique em **Adicionar app** e escolha o ícone **</>** (Web). Dê o apelido `site` e clique em **Registrar app**. Vai aparecer um código com `apiKey`, `authDomain`, `projectId` e `appId`: copie esses quatro valores e cole no arquivo `firebase-config.js` (ou me mande que eu colo).
4. No menu da esquerda, em **Criação**, abra **Firestore Database** e clique em **Criar banco de dados**. Escolha o local `southamerica-east1 (São Paulo)`, depois **Iniciar no modo de produção** e clique em **Criar**.
5. Ainda no Firestore, abra a aba **Regras**, apague tudo o que estiver lá, cole o conteúdo do arquivo `firestore.rules` e clique em **Publicar**.

## Ligar o site no GitHub Pages

Essa parte eu faço por você quando tiver acesso ao repositório. Se quiser fazer sozinha: o GitHub só existe em inglês, então no repositório abra **Settings**, depois **Pages**; em **Source** escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`, e clique em **Save**. Em 1 ou 2 minutos o site fica em `https://SEU-USUARIO.github.io/rotina/`.

## Usar

- Abra o link, toque em **Entrar com Google**.
- Para dividir cardápio e compras: na aba **Cardápio e compras**, em **Nossa casa**, copie o código e mande para sua noiva. Ela entra com o Google dela e digita o código no mesmo lugar.
- No celular: abra o link no navegador e use **Adicionar à Tela de Início**.
- A configuração do Firebase no `firebase-config.js` não é senha: quem protege os dados são as regras do passo 5.
