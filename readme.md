DOC - TECNOLOGIAS
========

I. ESCOPO

II. PORTAIS

III. SITE

IV. CHATBOT

V. BACKUP - IMÓVEIS

VI. BACKUP - IMAGENS

VII. SUPORTE

--------

I. ESCOPO DESTA DOCUMENTAÇÃO
--------

detalhando o funcionamento e configuração dos portais de imóveis, entradas de lead do site, funcionamento e integração do chatbot, backup do banco de dados dos imóveis e do funcionamento da cópia das imagens dos imóveis para o CDN da Leadz.

II. PORTAIS
--------

A integração com os portais e a roleta de atendimento do Vista funciona configurando o envio de lead do portal para o e-mail "cmsouza@cmslead.com.br".
Os portais integrados são:

- GrupoZap
- VivaReal
- ChavesNaMão

Uma vez que o servidor recebe o e-mail, ele o interpreta e extrai as informações necessárias para cadastrar o lead na roleta.
Exemplo de lead enviado:

    agencia: 1
    veiculo: GrupoZap
    mensagem:  Tenho interesse em visitar  
    nome: --nome do contato--
    fone: (43) 99170-####
    email: yohh.###@hotmail.com
    anuncio: 7230
    interesse: locação
    departamento: 12

A informação "departamento" segue a seguinte ordem:

    CMSOUZA VENDA: 11
    CMSOUZA LOCAÇÃO: 12
    CMSOUZA LANÇAMENTOS: 13

Caso seja necessária a integração de um novo portal, favor fazer a solicitação através do e-mail: paulo@leadz.agency

III. SITE
--------

As entradas de lead através do site são:

- Página do imóvel:
Os contatos de agendamento de horário para visitação entram para a roleta de atendimento do Vista com a mídia de origem definida como "Site" e com o horário preenchido pelo cliente no campo "Mensagem"

- Barra de contatos:
Os contatos provenientes da opção "Enviar e-mail para CMSouza" na barra de contatos entram para a roleta de atendimento do Vista com a mídia de origem definida como "Site" e com a mensagem preenchida pelo cliente no campo "Mensagem". Este lead será direcionado ao departamento de acordo com a seleção da finalidade do contato, sendo ela "Venda" ou "Locação".

IV. CHATBOT
--------


V. BACKUP - CÓPIA DO BANCO DE IMÓVEIS
--------


V. BACKUP - CÓPIA DAS IMAGENS DOS IMÓVEIS
--------


VII. SUPORTE
--------

paulo@leadz.agency
(43) 99969-6665
michael@leadz.agency



Última Atualização - 10/10/2022 - 17h30