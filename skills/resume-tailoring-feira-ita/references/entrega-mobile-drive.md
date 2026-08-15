# Entrega pelo celular e Google Drive

## Ordem de entrega

1. Anexar os arquivos criados à conversa do Claude para visualização e download no celular.
2. Quando o Google Drive estiver conectado e autorizado, salvar uma cópia no Drive.
3. Quando a sessão estiver usando arquivos locais via Dispatch, salvar também na pasta local
   configurada.

Não retornar apenas um caminho do computador. O usuário precisa conseguir abrir o PDF no celular.

## Sessão remota do Claude

Preferir sessão remota de Chat/Cowork para o evento. Os arquivos vivem na conta do Claude e ficam
disponíveis na mesma conversa no celular, sem depender do computador ligado.

## Dispatch com o computador

Quando usar Dispatch ou acesso local:

- o computador deve permanecer ligado, conectado e com Claude Desktop aberto;
- salvar localmente em `CV/gerados/{AAAA-MM-DD}/{Empresa}/`;
- ainda anexar o resultado à conversa;
- informar o caminho local somente como cópia adicional.

## Google Drive

Se o conector Google Drive estiver disponível:

1. Usar ou criar a pasta privada `Feira de Carreiras ITA`.
2. Dentro dela, usar `Curriculos/{Empresa}/{AAAA-MM-DD}`.
3. Enviar PDF, DOCX, Markdown e briefing.
4. Não converter o PDF; preservar como arquivo.
5. Verificar o upload e retornar o link observado no conector.
6. Nunca inventar link do Drive.

Cada gravação pode exigir aprovação do usuário. Se a aprovação não ocorrer, manter os anexos na
conversa e continuar; Drive é redundância, não condição para a entrega.

## Configuração única recomendada

No Projeto do Claude, definir:

```text
delivery.mobile_attachment = true
delivery.google_drive = true
delivery.drive_folder = Feira de Carreiras ITA/Curriculos
delivery.local_copy = false
```

Usar `delivery.local_copy = true` apenas quando Dispatch estiver configurado e o computador puder
ficar ligado durante o evento.

