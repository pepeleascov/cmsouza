# DOCUMENTAÇÃO
# TECNOLOGIAS LEADZ - CMSOUZA


I. ESCOPO

II. PORTAIS

III. SITE

IV. CHATBOT

V. BACKUP - IMÓVEIS

VI. BACKUP - IMAGENS

VII. SUPORTE

IV. NOTAS

--------

# I. ESCOPO DESTA DOCUMENTAÇÃO

Detalha o funcionamento e configuração dos portais de imóveis, campos de entrada de lead do site, funcionamento e integração do chatbot, backup do banco de dados dos imóveis e do funcionamento da cópia das imagens dos imóveis para o CDN da Leadz[^1].

# II. PORTAIS

A integração com os portais com a roleta de atendimento do Vista funciona configurando o envio de lead do portal para o e-mail "cmsouza@cmslead.com.br".
Os portais integrados são informados com as seguintes mídias de origem:

- GrupoZap
- VivaReal
- ChavesNaMão

Uma vez que o servidor Leadz recebe o e-mail, ele o interpreta e extrai as informações necessárias para cadastrar o lead na roleta.
Exemplo de lead interpretado e enviado para o Vista:

    agencia: 1
    veiculo: GrupoZap
    mensagem:  Tenho interesse em visitar  
    nome: --nome do contato--
    fone: (43) 991##-####
    email: yohh.###@hotmail.com
    anuncio: 7230
    interesse: locação
    departamento: 12

A informação "departamento" segue a seguinte ordem:

    CMSOUZA VENDA: 11
    CMSOUZA LOCAÇÃO: 12
    CMSOUZA LANÇAMENTOS: 13

Caso seja necessária a integração de um novo portal, favor fazer a solicitação através do e-mail: paulo@leadz.agency

# III. SITE

As entradas de lead através do site são:

- Página do imóvel - Agendamento de Visitas:

Os contatos de agendamento de horário para visitação entram para a roleta de atendimento do Vista com a mídia de origem definida como "Site" e com o horário preenchido pelo cliente no campo "Mensagem".

- Barra de contatos:

Os contatos provenientes da opção "Enviar e-mail para CMSouza" na barra de contatos entram para a roleta de atendimento do Vista com a mídia de origem definida como "Site" e com a mensagem preenchida pelo cliente no campo "Mensagem". Este lead será direcionado ao departamento de acordo com a seleção da finalidade do contato, sendo ela "Venda" ou "Locação".

Os contatos provenientes da opção "Atendimento por WhatsApp" na barra de contatos redirecionam o cliente para o atendimento através do chatbot (detalhado na seção seguinte) e entram para a roleta de atendimento do Vista com a mídia de origem definida como "Site-Whatsapp", e com a mensagem preenchida pelo cliente no campo "Mensagem".

# IV. CHATBOT

Nosso sistema (Leadz) atua em conjunto com o serviço contratado "Sendpulse", utilizando o chatbot como forma de entrada de dados. O chatbot faz a interação com o usuário durante o atendimento dos leads no WhatsApp, onde posteriormente nosso sistema os envia para a roleta de atendimento do Vista.
Para os contatos provenientes dos portais, nosso sistema identifica os links dentro das mensagens e classifica a mídia de origem de acordo com o link do portal.
Dessa forma, os leads dos portais atendidos através do WhatsApp são enviados para a roleta de atendimento com uma das seguintes mídias de origem:

    GrupoZap-Whatsapp
    VivaReal-Whatsapp
    ChavesNaMão-Whatsapp

Os outros contatos provenientes da opção "Atendimento por WhatsApp" da barra de contatos do site da CMSouza são classificados com a mídia de origem "Site-Whatsapp".
O nosso sistema, em conjunto com o chatbot, armazena as mensagens recebidas durante a interação do chat e ao final as envia no campo "mensagem" do lead a ser cadastrado na roleta de atendimento.

O fluxo de atendimento funciona da seguinte forma:

    1. Início do atendimento
    2. Usuário seleciona a finalidade do atendimento, que indica a informação do departamento
    3. Usuário responde o nome
    4. O processamento dos dados é iniciado assim que o servidor recebe a resposta do "nome
    5. Após, o nosso sistema faz o envio do lead para a roleta do Vista

Exemplo de lead enviado através do chatbot:

    nome: --nome do contato--
    fone: 5543#####
    mensagem: Olá! Gostaria de falar com um corretor sobre o imóvel 8746
    veiculo: Site-Whatsapp
    interesse: Locação
    departamento: 12
    agencia:1

```json
{"nome":"Barbara","fone":"554391054499","mensagem":"Olá! Estou no site da CMSouza e gostaria de mais informações.","veiculo":"Site-Whatsapp","interesse":"Locação","agencia":"1"}
```

# V. BACKUP - CÓPIA DO BANCO DE IMÓVEIS

A cópia/backup do banco de imóveis salva apenas as informações que são pertinentes ao funcionamento do site. O backup não salva o banco de dados dos imóveis em sua totalidade e não tem acesso à outras informações do CRM Vista, como por exemplo, cadastro de clientes e negócios.
O intuito dessa cópia é para que o site não dependa do sistema do Novo Vista, que constantemente apresenta instabilidades. A cópia ocorre todos os dias, de hora em hora. Portanto, as atualizações de descrição e o cadastro de novos imóveis pode levar até uma hora para estarem disponíveis no site da CMSouza

As informações dos imóveis salvas são as seguintes:

    Status, Finalidade, Categoria, Codigo, BairroComercial, Bairro, Empreendimento, Cidade, 
    ValorVenda, ValorLocacao, Dormitorios, Caracteristicas, InfraEstrutura, CodigoEmpreendimento,
    BanheiroSocialQtd, Vagas, AreaPrivativa, AreaTotal, ValorCondominio, DescricaoWeb, 
    DescricaoEmpreendimento, Imediacoes, DestaqueWeb, SuperDestaqueWeb, Lancamento, Tour360, 
    Corretor, TotalBanheiros, Suites, Endereco, Numero, UF, FotoDestaque


# VI. BACKUP - CÓPIA DAS IMAGENS DOS IMÓVEIS

CDN (Content Delivery Network / Rede de entrega de conteúdo)[^1]

250ms a 300ms, 60ms, 75% a 80% mas rápido, ou seja, um ganho de velocidade de cerca de 4x em comparação ao CDN do Vista

# VII. SUPORTE

paulo@leadz.agency
(43) 99969-6665
michael@leadz.agency


#### Última Atualização
11/10/2022

#### NOTAS

[^1]: CDN - Content Delivery Network / Rede de entrega de conteúdo
[^2]: Every new line should be prefixed with 2 spaces.  
  This allows you to have a footnote with multiple lines.
[^note]:
    Named footnotes will still render with numbers instead of the text but allow easier identification and linking.  
    This footnote also has been made with a different syntax using 4 spaces for new lines.