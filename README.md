# proxy brasil: como escolher e configurar IP brasileiro para scraping do Mercado Livre e SERP, com preços por GB

Quem procura "proxy brasil" normalmente não está atrás de uma explicação sobre o que é um servidor intermediário. Está atrás de uma coisa só: um endereço IP que sites brasileiros tratem como brasileiro. Porque é isso que destrava o Mercado Livre, o Magazine Luiza, a página `.com.br` da Amazon, o Google com resultados localizados e as campanhas que você precisa conferir como elas realmente aparecem para quem está em São Paulo.

O problema aparece rápido. Site grande no Brasil roda Cloudflare, Akamai ou DataDome na frente, e essas camadas não olham só o user-agent. Elas olham ASN. Um IP de datacenter alemão pedindo a página de um produto no Mercado Livre é sinalizado antes de você terminar o handshake do TLS. Já um IP residencial de Vivo, Claro ou TIM no mesmo pedido passa como um usuário comum.

É aí que a escolha do provedor deixa de ser detalhe e passa a ser a diferença entre o job rodar e o job travar no terceiro mil requests. A DataImpulse é uma das opções mais baratas desse mercado — a partir de **$1 por GB** em proxies residenciais, sem assinatura e com tráfego que não expira. Vale entender onde ela encaixa bem em projetos brasileiros e onde ela não é a ferramenta certa.

## Antes de comprar: qual tipo de proxy brasileiro resolve o seu caso

Os provedores vendem quatro tipos de proxy, e a diferença entre eles não é preço por acaso. É o nível de confiança que o IP carrega diante do servidor de destino.

| Tipo | Preço padrão por GB | No que funciona | Onde costuma travar |
| --- | --- | --- | --- |
| Residencial | $1 | e-commerce, SERP, redes sociais, scraping em geral | alvos com anti-bot muito agressivo |
| Datacenter | $0,50 | volume alto em páginas públicas, velocidade, testes | sites com Cloudflare/DataDome ativos |
| Mobile (3G/4G/5G) | $2 | apps, Instagram, TikTok, verificações antifraude | custo por GB mais alto |
| Residencial premium | $5 | projetos críticos, latência baixa, sessões estáveis | orçamento |

Para trabalho sério com mercado brasileiro, a resposta costuma ser residencial. É o tipo que a maioria dos sites locais espera ver chegando, e é onde o DataImpulse concentra o preço mais competitivo. Datacenter serve bem para varrer catálogos públicos ou medir disponibilidade, mas não espere passar por proteção séria de varejo com ele.

Mobile entra quando a residencial começa a apanhar: APIs de app, redes sociais e fluxos que dependem de impressão digital de celular. O pool brasileiro é menor, e o preço reflete isso.

## Preços e todos os planos do DataImpulse

Aqui está a parte que interessa. A DataImpulse trabalha com pagamento por uso — você compra GB, não assinatura. O tráfego comprado não expira, e **não existe mensalidade**.

| Produto | Plano | Tráfego incluído | Preço | Preço por GB | Cobrança | Comprar |
| --- | --- | --- | --- | --- | --- | --- |
| Residencial | Intro | 5 GB | $5 | $1,00 | pagamento único | [ Ver o plano residencial de entrada](https://dataimpulse.com/residential-proxies/?aff=86938) |
| Residencial | Basic | 50 GB | $50 | $1,00 | pagamento único | [ Ver o plano residencial Basic](https://dataimpulse.com/residential-proxies/?aff=86938) |
| Residencial | Advanced | 1 TB | $800 | $0,80 | pagamento único | [ Ver o plano residencial Advanced](https://dataimpulse.com/residential-proxies/?aff=86938) |
| Residencial | Custom | 5 TB+ | sob consulta | a partir de ~$0,70 | sob consulta | [ Falar sobre volume residencial](https://dataimpulse.com/residential-proxies/?aff=86938) |
| Datacenter | Intro | 10 GB | $5 | $0,50 | pagamento único | [ Ver planos de datacenter](https://bit.ly/dataimPulse) |
| Datacenter | Basic | 100 GB | $50 | $0,50 | pagamento único | [ Ver planos de datacenter](https://bit.ly/dataimPulse) |
| Datacenter | Advanced | 1 TB | $450 | $0,45 | pagamento único | [ Ver planos de datacenter](https://bit.ly/dataimPulse) |
| Datacenter | Custom | 5 TB+ | a partir de $2.250 | $0,45 | sob consulta | [ Ver planos de datacenter](https://bit.ly/dataimPulse) |
| Mobile | Intro | 2,5 GB | $5 | $2,00 | pagamento único | [ Ver planos de proxy mobile](https://bit.ly/dataimPulse) |
| Mobile | Basic | 25 GB | $50 | $2,00 | pagamento único | [ Ver planos de proxy mobile](https://bit.ly/dataimPulse) |
| Mobile | Advanced | 1 TB | $1.600 | $1,60 | pagamento único | [ Ver planos de proxy mobile](https://bit.ly/dataimPulse) |
| Mobile | Custom | 5 TB+ | a partir de $8.000 | $1,60 | sob consulta | [ Ver planos de proxy mobile](https://bit.ly/dataimPulse) |
| Residencial premium | Intro | 1 GB | $5 | $5,00 | pagamento único | [ Ver o pool residencial premium](https://dataimpulse.com/premium-residential-proxies/?aff=86938) |
| Residencial premium | Basic | 10 GB | $50 | $5,00 | pagamento único | [ Ver o pool residencial premium](https://dataimpulse.com/premium-residential-proxies/?aff=86938) |
| Residencial premium | Custom | 1.000 GB+ | a partir de $4.000 | $4,00 | sob consulta | [ Ver o pool residencial premium](https://dataimpulse.com/premium-residential-proxies/?aff=86938) |

Vale olhar a curva de preço com atenção, porque ela é mais plana do que a de quase todo concorrente. No residencial, de 5 GB até perto de 850 GB a taxa continua em $1/GB. O único degrau real aparece em 1 TB, quando cai para $0,80/GB. Na prática: 50 GB custam $50 e 200 GB custam $200, sem nenhum bônus intermediário por se comprometer com mais. Se o seu projeto em mercado brasileiro gira em torno de 20–60 GB por mês, isso é irrelevante — você paga o mesmo por GB em qualquer tamanho.

Duas condições que costumam pegar gente de surpresa:

- **Mínimo de $5 na primeira compra.** Depois disso, há relatos consistentes de que o mínimo sobe para $50 por recarga. Como o tráfego não expira, isso é uma questão de fluxo de caixa, não de prazo — mas muda a conta para quem faz jobs pequenos e esporádicos.
- **Garantia de 7 dias.** Não existe camada gratuita permanente; o teste real é a primeira recarga pequena, que a empresa reembolsa dentro desse prazo.

Se você quer começar pequeno antes de assumir qualquer volume, [👉 testar o pool residencial com 5 GB por $5](https://dataimpulse.com/residential-proxies/?aff=86938) é a entrada de menor risco da tabela.

## Quantos IPs brasileiros existem, de fato, no pool

Provedor nenhum é obrigado a publicar isso, e a maioria não publica. A DataImpulse mostra contadores ao vivo nas páginas por país, o que ajuda a separar marketing de capacidade real.

Na página de proxies residenciais premium do Brasil, os números giram em torno de **41 a 43 mil IPs ativos em tempo real**, cerca de **580 a 588 mil IPs únicos nos últimos 30 dias** e algo entre **81 e 88 mil IPs únicos nas últimas 24 horas**. A variação é normal — é um painel de disponibilidade instantânea, não um censo.

No datacenter brasileiro a escala é outra: aproximadamente **2.720 IPs ativos**, **25,7 mil únicos em 30 dias** e **10,8 mil únicos em 24 horas**. Suficiente para varreduras de catálogo e checagem de disponibilidade, apertado para operações que exigem rotação constante com boa variedade de sub-redes.

O pool residencial padrão do Brasil não aparece com contador próprio na mesma página, mas faz parte da rede de 90 milhões de IPs em 195 países que a empresa declara — com a diferença importante de que ela afirma não revender rede de terceiros. Se isso se sustenta, é o que explica o preço de $1/GB sem gargalo de sobrecarga: IPs de pool próprio tendem a ser filtrados com menos frequência justamente porque não estão sendo consumidos por dez revendedores ao mesmo tempo.

## Como configurar na prática: gateway, portas e country-br

A configuração é mais simples do que a maioria das ferramentas de scraping sugere. Tudo passa pelo mesmo gateway.

- **Gateway:** `gw.dataimpulse.com`
- **HTTP/HTTPS rotativo:** porta `823`
- **SOCKS5 rotativo:** porta `824`
- **Sessões sticky:** portas entre `10000` e `20000`, com duração de 1 a 120 minutos (padrão de 30 minutos)

A localização vai grudada no usuário, com underscore. Para forçar IP brasileiro:

bash
curl -x http://SEU_LOGIN:SUA_SENHA_country-br@gw.dataimpulse.com:823 https://api.ipify.org


Um detalhe que confunde no começo: em modo rotativo, o IP troca a cada requisição nova. Se você precisa manter a mesma sessão para login, carrinho ou sequência de requisições paginadas, use uma porta sticky e um session ID fixo no usuário. O tempo padrão é de 30 minutos, o que cobre a maioria dos fluxos com autenticação.

Existem também endpoints de API para gerar listas de proxy e acompanhar consumo de banda de forma programática, além de subcontas — útil quando o time tem mais de uma pessoa rodando coleta no mesmo pool.

## A conta que ninguém faz: quanto o targeting encarece

No DataImpulse, mira por **país é gratuita**. É o que permite montar um job para o Brasil sem custo extra. Já os filtros de **estado, cidade, CEP e ASN** entram com uma regra que muda o orçamento: **no residencial padrão, esse tráfego é cobrado pelo dobro da tarifa por GB.**

Traduzindo para números concretos. Uma página HTML de catálogo com cerca de 200 KB significa aproximadamente 5.000 páginas por GB a $1/GB. Se o seu projeto exige IPs de São Paulo especificamente — para ver preço regionalizado, conferir frete ou medir SERP local —, a tarifa efetiva vira $2/GB e a produtividade cai para cerca de 2.500 páginas por GB. O mesmo orçamento entrega metade.

A decisão prática é essa: use `country-br` como padrão e reserve `city` para a amostra em que a geografia local realmente importa. Em monitoramento de SERP nacional, o resultado quase nunca muda entre um IP do Rio e um de Curitiba. Em verificação de anúncio ou checagem de frete por região, muda, e aí os $2/GB passam a ser custo justificado.

Um ponto que merece confirmação antes de comprar em volume: material de terceiros indica que os mesmos filtros aparecem incluídos nos proxies de datacenter, enquanto no residencial são cobrados em dobro. Como isso mexe direto na conta, vale confirmar no suporte antes de fechar um pacote grande.

## Limites honestos

Nem tudo nessa faixa de preço vem sem troca.

**Não é a escolha para multi-contas.** Quem precisa manter dezenas de contas separadas com IP fixo e estável costuma ir para proxies ISP/estáticos. O residencial rotativo da DataImpulse é feito para coleta e automação, não para sustentar 40 perfis de navegador a longo prazo.

**Não há API de scraping pronta.** O produto entrega conexão de proxy crua. Requisições, parsing, retentativas e tratamento de CAPTCHA ficam com o seu código. Para quem já tem pipeline próprio isso é até preferível — menos camada, menos markup —, mas quem procura solução "plug and play" de coleta vai precisar montar essa parte.

**O pool brasileiro de datacenter é pequeno.** Cerca de 2,7 mil IPs ativos não sustentam uma operação de escala no país se a rotação for agressiva.

**O mínimo de recarga sobe depois da primeira compra**, o que penaliza projetos intermitentes.

Do lado positivo, há três coisas que contam a favor: a TechRadar publicou uma análise do serviço descrevendo taxas de sucesso altas em scraping com os residenciais; a empresa divulga certificação ISO para o sistema de gestão de segurança da informação; e a política de tráfego que não expira tira o relógio do seu lado — você não perde GB pago porque o mês acabou.

## Perguntas que aparecem antes da compra

**Proxy brasileiro ou VPN?** A VPN tunela todo o tráfego do dispositivo. O proxy roteia só a aplicação que você mandar, o que permite rodar dez sessões em paralelo com IPs diferentes na mesma máquina. Para scraping e automação, proxy é a ferramenta certa; VPN resolve outra coisa.

**Funciona em site brasileiro com Cloudflare ou DataDome?** IP residencial e mobile tendem a passar onde o datacenter travar, porque a camada anti-bot enxerga uma conexão de bairro. Não existe garantia de 100% em alvo nenhum — o teste, de novo, é a primeira recarga de $5 no seu próprio alvo.

**Consigo escolher cidade?** Sim, com os filtros avançados. Só conte com a tarifa dobrada no residencial padrão.

**O tráfego expira?** Não. Os GB comprados continuam na conta até serem consumidos, e não há mensalidade.

**É legal usar?** Coleta de dados publicamente acessíveis para pesquisa de mercado, monitoramento de anúncios, verificação de preço e inteligência competitiva é uso legítimo. Circundar controle de acesso, raspar dado atrás de autenticação ou coletar dado pessoal tem regras próprias sob a LGPD — e a responsabilidade pelo uso fica com quem opera, não com o provedor.

## Onde essa escolha faz sentido

Se o seu projeto brasileiro roda entre 5 e 200 GB por mês, com foco em e-commerce, SERP ou redes sociais, o modelo de $1/GB sem assinatura é difícil de bater: você não paga por pacote que não vai terminar, e o resto do saldo continua lá quando o job voltar. É o caso clássico de time pequeno, agência ou dev solo que quer medir custo por requisição bem-sucedida antes de escalar.

Se a operação é enterprise, exigindo SLA fechado, IPs estáticos e integrações gerenciadas, o caminho natural é outro — e provavelmente o pool premium ou um plano sob consulta.

Para a maioria que começa agora, o teste real cabe em cinco dólares: [👉 começar com 5 GB de proxy residencial e medir o resultado no seu próprio alvo](https://dataimpulse.com/residential-proxies/?aff=86938). Se a taxa de sucesso no Mercado Livre ou no SERP brasileiro compensar, escalar é só comprar mais GB — sem trocar de plano, sem renegociar contrato, sem reiniciar a integração.
