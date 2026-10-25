# Minha Rotina

Site da rotina da família.

- `index.html`: **Minha Rotina** (adultos). Entra com conta Google, sincroniza celular e computador. Hábitos, diário, semana e revisão são de cada pessoa; cardápio e lista de compras são da casa.
- `criancas.html`: **Meu Dia** (Zoé e Léo). Não precisa de login; salva no próprio celular de cada um.

## Configurar o Firebase (uma vez, uns 10 minutos)

1. Entre em https://console.firebase.google.com com sua conta Google e clique em **Criar projeto**. Nome: `minha-rotina`. Pode desativar o Google Analytics.
2. No menu da esquerda: **Build > Authentication > Começar**. Em **Sign-in method**, ative **Google** e salve.
   Ainda em Authentication, abra **Settings > Authorized domains > Add domain** e adicione `SEU-USUARIO.github.io`.
3. Na página inicial do projeto, clique no ícone **</>** (Web), dê o nome `site` e registre. Copie os valores de `apiKey`, `authDomain`, `projectId` e `appId` e cole no arquivo `firebase-config.js`.
4. No menu: **Build > Firestore Database > Criar banco de dados**. Escolha a região `southamerica-east1 (São Paulo)` e o **modo de produção**.
5. Na aba **Regras** do Firestore, apague tudo, cole o conteúdo do arquivo `firestore.rules` e clique em **Publicar**.

## Ligar o site no GitHub Pages

No repositório: **Settings > Pages > Build and deployment**, em Source escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`, e salve. Em 1 ou 2 minutos o site fica em `https://SEU-USUARIO.github.io/rotina/`.

## Usar

- Abra o link, toque em **Entrar com Google**.
- Para dividir cardápio e compras: na aba **Cardápio e compras**, em **Nossa casa**, copie o código e mande para sua noiva. Ela entra com o Google dela e digita o código no mesmo lugar.
- No celular: abra o link no navegador e use **Adicionar à Tela de Início**.
- A configuração do Firebase no `firebase-config.js` não é senha: quem protege os dados são as regras do passo 5.
