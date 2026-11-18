# Instalação manual na Roku

`HEBIX-Roku.zip` é o pacote pronto para enviar pelo instalador do modo desenvolvedor da Roku. Ele foi gerado com `./tools/make.sh` e contém o manifesto, os componentes, as imagens e o código BrightScript necessários ao app.

## Enviar o pacote

1. Deixe o computador e a Roku na mesma rede local e ative o modo desenvolvedor da Roku. A Roku mostrará o IP e a senha do instalador; não publique esses dados.
2. No navegador do computador, abra `http://<IP-DA-ROKU>`.
3. Entre com o usuário `rokudev` e a senha definida no modo desenvolvedor. Digite a senha somente no instalador oficial da Roku.
4. Em **Development Application Installer**, selecione `HEBIX-Roku.zip`, envie e instale o pacote.
5. Inicie o canal de desenvolvimento. Se o app antigo continuar aberto, feche-o e inicie novamente.

## Configuração e atualização

- O arquivo é o pacote do cliente Roku. Configure o endereço do backend na primeira inicialização; informe o token apenas se o backend exigir autenticação.
- Ao reinstalar na mesma Roku, as configurações salvas no aparelho (servidor, token e perfil) permanecem no Registry.
- Em uma Roku sem configuração anterior, conclua a tela Setup na primeira inicialização.
- Para gerar um pacote atualizado a partir do código-fonte, execute `./tools/make.sh` e copie `out/erku.zip` para esta pasta como `HEBIX-Roku.zip`. Não inclua listas M3U/M3U8, URLs de provedores, tokens ou senhas no repositório.

O artefato foi compilado e validado pelo instalador de desenvolvimento da Roku. A instalação manual usa o mesmo ZIP aceito pelo instalador, sem precisar enviar os arquivos-fonte individualmente.
