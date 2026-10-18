# Auditoria da loja Walk Cards

Auditoria do projeto local, concluída em 17/10/2026. Este relatório descreve o código e os arquivos encontrados nesta pasta. Não certifica a operação da empresa nem aprovação por Google Ads ou Merchant Center.

## 1. Corrigido

- Criadas as páginas /sobre-nos/, /contato/, /politica-de-privacidade/, /politica-de-envio/, /trocas-devolucoes/ e /termos-de-uso/, com navegação e rodapé responsivos.
- Adicionados ao rodapé e às páginas os dados fornecidos: razão social, CNPJ, endereço em Osasco, e-mail, telefone e WhatsApp. O horário continua marcado como [INFORMAÇÃO NECESSÁRIA].
- O formulário de contato abre um rascunho no aplicativo de e-mail do visitante. Ele não envia dados ao site e depende de um aplicativo de e-mail configurado.
- Desativado o login Google não configurado; o site informa que não exige cadastro para consultar os produtos.
- Removidas notas e estrelas calculadas artificialmente, quantidades de estoque aleatórias, rótulos de “mais vendidos”/“lançamento” sem comprovação, o vendedor incorreto “Poké Central”, prazo fixo de 10 dias úteis, preço de frete fixo de R$ 11,31 e promessa de frete grátis.
- O estoque agora aparece como consulta até ser conferido e registrado no painel. A confirmação de estoque no painel fica salva somente neste navegador.
- O carrinho agora prepara uma consulta pelo WhatsApp. A mensagem não reserva produto nem confirma pedido. Checkout e pagamento online não são processados.
- Valores existentes no catálogo são marcados como referência e precisam ser confirmados pela loja.
- Incluídos metadados básicos, Open Graph, dados estruturados Schema.org Organization, robots.txt e noindex para admin.html. Não foi criado canonical nem sitemap com domínio inventado.

## 2. Precisa de informação do proprietário

- [INFORMAÇÃO NECESSÁRIA] Horário e prazo de resposta do atendimento.
- [INFORMAÇÃO NECESSÁRIA] Confirmar no comprovante oficial da Receita Federal a razão social, titularidade do CNPJ, situação cadastral, endereço e atividades econômicas vigentes.
- O texto enviado informa como atividade principal “96.09-2-06 — serviços de tatuagem e colocação de piercing”. Essa atividade não corresponde à venda de cartas e colecionáveis. Confirmar se há atividade secundária de comércio eletrônico e quais dados devem aparecer no Merchant Center. A divergência não foi ocultada nem alterada no site.
- [INFORMAÇÃO NECESSÁRIA] Confirmar que o endereço fornecido é endereço comercial de atendimento/correspondência e esclarecer se há atendimento presencial.
- [INFORMAÇÃO NECESSÁRIA] Revisar os 258 preços e confirmar que os produtos estão à venda, serão entregues e têm disponibilidade real.
- [INFORMAÇÃO NECESSÁRIA] Informar estoque físico real por SKU e definir quem o atualizará.
- [INFORMAÇÃO NECESSÁRIA] Confirmar imagens próprias/licenciadas, marca/fabricante, edição, condição, conteúdo e variações. As imagens e parte dos dados estão na pasta local “Cartas Pokémon_ Coleção Premium, Edição Especial e Mais - Ri Happy_files”; não foi comprovada autorização de uso.
- [INFORMAÇÃO NECESSÁRIA] Definir áreas atendidas, frete, prazo de processamento, prazo de transporte, transportadoras, rastreamento e procedimentos para endereço incorreto/retorno.
- [INFORMAÇÃO NECESSÁRIA] Confirmar operação de trocas, logística reversa, devoluções, defeitos, cancelamentos e processamento de reembolsos. A página preserva direitos legais, mas não inventa procedimentos internos.
- [INFORMAÇÃO NECESSÁRIA] Confirmar quem decide as finalidades do tratamento de dados, bases e prazos de retenção, responsáveis por solicitações LGPD e provedores usados.

## 3. Precisa de configuração externa

- O projeto é HTML/CSS/JavaScript estático. Não há servidor de pedidos, banco de dados, controle de estoque compartilhado ou integração de pagamento. O painel e os dados locais não constituem proteção ou registro central da loja.
- Escolher/publicar em uma hospedagem e configurar domínio, DNS e certificado HTTPS. Como o domínio oficial não foi informado, não foi possível testar TLS, configurar canonical ou gerar um sitemap válido com URLs absolutas.
- Para aceitar pedidos, integrar backend seguro, gestão de catálogo/estoque, cálculo de frete, envio de confirmação, atendimento e um provedor de pagamento real. A versão atual apenas abre o WhatsApp para consulta.
- O formulário usa mailto; para envio dentro do site, será necessário configurar serviço/API de e-mail com proteção contra abuso.
- A proteção de admin.html é demonstrativa e executada no navegador. Ela não deve ser publicada como controle de acesso seguro; mover painel e autenticação para ambiente protegido no servidor.
- Configurar políticas de privacidade, retenção e operadores da hospedagem, e rever a página de privacidade quando esses serviços forem contratados.
- Configurar Google Merchant Center e Ads, propriedade/verificação do domínio, dados comerciais e fonte de produtos só depois de validar a operação real.

## 4. Possíveis problemas para Google Ads

- Atividade principal de tatuagem/piercing informada para uma empresa cujo site oferece cartas colecionáveis pode gerar divergência de identidade/atividade; confirmar o cadastro e eventuais atividades secundárias.
- A loja informa que não conclui pedidos nem processa pagamento. Não anunciar como compra online disponível até a integração real existir.
- Preços são referências e precisam ser atualizados; frete, regiões, prazos, trocas e horário ainda têm campos incompletos.
- O catálogo é carregado por JavaScript e detalhes aparecem em modal. Não há uma landing page independente por produto.
- Domínio, HTTPS, políticas definitivas, operação de entrega e consistência entre anúncio e página dependem de configuração e revisão externa.

## 5. Possíveis problemas para Merchant Center

- Foram encontrados 258 itens no arquivo de catálogo. Todos têm nome, preço e caminho de imagem preenchidos; os 258 arquivos principais existem localmente. Isso não confirma que preço, estoque, imagem, marca ou oferta estejam atuais/autorizados.
- 32 de 258 imagens principais têm menos de 500 × 500 px (menor dimensão encontrada: 400 px). Revisar resolução e qualidade antes de enviar o feed.
- O catálogo não traz SKU do comerciante, GTIN/EAN ou MPN verificados. IDs imported-1 etc. são identificadores técnicos derivados da ordem dos dados, não SKUs comerciais; não enviar como se fossem GTIN/MPN.
- Não há páginas estáticas/permalinks individuais por produto, feed XML/TSV nem dados estruturados Product/Offer. A marca nem sempre foi fornecida; GTIN e disponibilidade não devem ser inventados.
- A descrição de muitos produtos é montada por modelo em JavaScript; conteúdo/edição/itens da embalagem precisam ser verificados por produto.
- Estoque, preço final, condição, disponibilidade, custo/prazo de frete e imagem precisam coincidir entre página, checkout e feed. O checkout online está desativado e os valores atuais são de referência, então o catálogo ainda não deve ser enviado como fonte de ofertas ativas.
- As páginas de políticas estão no projeto, mas campos operacionais continuam com [INFORMAÇÃO NECESSÁRIA].

## Verificações realizadas

- As sete rotas públicas, robots.txt e admin.html responderam com HTTP 200 no servidor local.
- Nenhuma referência local href/src quebrada foi encontrada nas páginas principais e institucionais.
- Não foram encontradas URLs de recursos http:// nos arquivos auditados; isso não comprova HTTPS na hospedagem, que ainda não foi informada.
- A verificação de renderização e erros do navegador não pôde ser concluída: o Edge headless foi bloqueado pelo ambiente com erro de acesso ao canal Mojo/Crashpad. A validação de caminhos, arquivos e status HTTP foi feita separadamente.

## Referências oficiais para revisão antes da publicação

- Código de Defesa do Consumidor, art. 49: <https://www.planalto.gov.br/ccivil_03/leis/l8078compilado.htm>
- Direitos dos titulares (ANPD): <https://www.gov.br/anpd/pt-br/assuntos/titular-de-dados>
- Consultar CNPJ na Receita Federal: <https://www.gov.br/receitafederal/pt-br/assuntos/cadastros-e-registros-especiais/cnpj>
- Política de representação enganosa do Merchant Center: <https://support.google.com/merchants/answer/6150127>
- Especificação de dados de produtos do Merchant Center: <https://support.google.com/merchants/answer/7052112>
- Dados estruturados no Merchant Center: <https://support.google.com/merchants/answer/7331077>
