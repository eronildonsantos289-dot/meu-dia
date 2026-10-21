# Meu Dia v2 — iPhone PWA

## Novidades
- Visual premium minimalista inspirado nas convenções visuais do iOS.
- Lembretes configuráveis para tarefas e compromissos (na hora, 5, 15, 30, 60 minutos ou 1 dia antes).
- Central de lembretes vencidos na tela Hoje.
- Notificações web apenas enquanto o aplicativo estiver aberto/ativo, caso o navegador permita.
- Exportação de itens individuais ou da agenda para arquivo `.ics`, com alarmes para importar no Calendário do iPhone.

## Limite importante
Esta versão **não** possui serviço de push remoto. Portanto **não promete notificações em segundo plano nem com o aplicativo fechado**. No iOS, alertas confiáveis com o app fechado dependem de um sistema de notificações push com servidor e permissão do usuário, ou da importação dos compromissos no Calendário do iPhone. Importar um `.ics` cria cópias dos eventos, não sincronização contínua.

## Como instalar
1. Publique os arquivos em hospedagem HTTPS (GitHub Pages, Netlify etc.), preservando a estrutura.
2. Abra o endereço no Safari do iPhone.
3. Compartilhar → Adicionar à Tela de Início.
4. Abra online uma vez para armazenar os arquivos do PWA em cache e depois teste offline.

## Dados
O armazenamento continua local no navegador (localStorage). Exporte backups em Ajustes; não há sincronização entre dispositivos.

## Atualização
A versão 2 reutiliza os dados do projeto anterior (`meu-dia-v1`), desde que publicada na **mesma origem e caminho de armazenamento**. Se mudar de domínio, exporte/importa a cópia JSON.

## Verificação desta entrega
- Projeto JavaScript validado sintaticamente com Node.js.
- Manifesto PWA e arquivos de cache incluídos.
- Alarmes no arquivo iCalendar (`VALARM`) com tempo relativo ao evento.
- Notificações internas não substituem push com app fechado.
- Para atualizações do service worker, publique todos os arquivos na mesma origem HTTPS.
