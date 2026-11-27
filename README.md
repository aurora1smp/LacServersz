AURORAHOST LAC Arquivo LEIA-ME.txt

1.  SOBRE O PROJETO

AuroraHost LAC é um site desenvolvido para reunir, divulgar e organizar
anúncios de servidores do jogo Los Angeles Crimes (LAC). A interface foi
pensada para funcionar em celulares e computadores, com visual escuro e
elementos em destaque.

O site permite que jogadores encontrem servidores publicados e consultem
informações como nome, mapa, modo de jogo, região, tipo de conexão,
quantidade de jogadores, descrição e link relacionado ao mapa.

2.  RECURSOS PRINCIPAIS

-   Listagem pública de servidores publicados e ainda dentro do período
    de validade.
-   Pesquisa e filtros para ajudar a localizar servidores.
-   Exibição de informações e detalhes de cada servidor.
-   Opção para denunciar anúncios.
-   Área para publicar um servidor após entrar na conta.
-   Painel do proprietário para acompanhar e administrar o anúncio.
-   Renovação do período de publicação.
-   Atualização da quantidade de jogadores informada no painel.
-   Edição das informações e predefinições do anúncio após a publicação.
-   Opção para encerrar/remover o próprio anúncio.

3.  CONTAS E AUTENTICAÇÃO

A versão editada utiliza autenticação por e-mail e senha do Firebase
Authentication. O cadastro e o login dependem de o provedor E-mail/senha
estar habilitado no projeto Firebase usado pelo site.

O login com Google não está disponível nesta versão editada.

4.  ARMAZENAMENTO E SERVIÇOS

O site utiliza Firebase Firestore para armazenar e sincronizar dados,
incluindo anúncios de servidores e denúncias. A configuração do Firebase
está definida no código do site.

Para que o projeto funcione corretamente, o administrador precisa: -
Manter um projeto Firebase ativo. - Habilitar Authentication e o método
E-mail/senha. - Configurar regras de segurança adequadas no Firestore. -
Autorizar o domínio do site nas configurações do Firebase
Authentication.

5.  PUBLICAÇÃO E EDIÇÃO DE SERVIDORES

O formulário de publicação registra dados do servidor, como nome, mapa,
modo, conexão, endereço/IP, região, limite de jogadores, descrição e
link do mapa.

Depois da publicação, o proprietário pode abrir o painel de
gerenciamento e editar essas informações. As alterações são salvas no
Firestore.

IMPORTANTE SOBRE O MAPA E AS CONFIGURAÇÕES DO JOGO: O campo de mapa
recebe um link HTTP/HTTPS para baixar o mapa. Ele não realiza upload de
arquivos para o site nem hospeda o mapa. O editor de predefinições
altera os dados do anúncio no AuroraHost. Ele não altera automaticamente
configurações internas do Los Angeles Crimes, não inicia o servidor do
jogo e não controla o jogo remotamente. Configurações internas do LAC
precisam ser feitas no próprio jogo ou em uma ferramenta compatível.

6.  FUNCIONAMENTO DO STATUS

A listagem considera os anúncios cujo período de validade ainda não
terminou. O proprietário pode renovar a sessão pelo painel. A quantidade
de jogadores exibida é um valor informado/atualizado pelo painel, não
uma leitura automática da partida do LAC.

Portanto, a indicação de anúncio ativo no AuroraHost não é, por si só,
uma verificação técnica de que o servidor do jogo está acessível ou
funcionando.

7.  TECNOLOGIAS

-   HTML, CSS e JavaScript para a interface e a lógica do site.
-   Firebase Authentication para contas de usuário.
-   Firebase Firestore para armazenamento e sincronização dos dados.
-   Layout responsivo para telas móveis e desktop.

8.  SEGURANÇA E CONFIGURAÇÃO

Antes de publicar o site: - Revise as regras do Firestore para garantir
que cada usuário só possa editar ou encerrar seus próprios anúncios. -
Proteja as funções administrativas e não confie apenas em controles
visuais no navegador. - Não coloque senhas, chaves privadas ou
credenciais administrativas no código público. - Configure os domínios
autorizados no Firebase Authentication. - Teste cadastro, login,
publicação, edição, denúncia e encerramento com contas diferentes.

9.  LIMITAÇÕES CONHECIDAS

-   O site é um diretório e painel de anúncios; não é um serviço de
    hospedagem de partidas do LAC.
-   Não há integração/API do LAC implementada para controlar
    configurações internas do jogo.
-   O campo de link do mapa não equivale a upload ou armazenamento de
    arquivos.
-   O status e a contagem de jogadores não são confirmados
    automaticamente pelo jogo.
-   O funcionamento depende da configuração e disponibilidade do projeto
    Firebase.

10. IDENTIFICAÇÃO

Nome: AuroraHost LAC Finalidade: divulgação e gerenciamento de anúncios
de servidores de Los Angeles Crimes. Arquivo principal: index.html

Este documento descreve os recursos presentes na versão editada do
AuroraHost LAC. Recursos futuros ou integrações ainda não implementadas
não devem ser considerados disponíveis.
