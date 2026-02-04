---
{"dg-publish":true,"dg-path":"Tecnologia/O que acontece quando digitamos o endereço de um site no navegador.md","permalink":"/tecnologia/o-que-acontece-quando-digitamos-o-endereco-de-um-site-no-navegador/","created":"2023-12-06T18:38:40.000-03:00","updated":"2026-02-03T23:01:46.193-03:00"}
---

*Confiança:* Confiança média de que as informações estão corretas, confiança baixa de que incluí todos os detalhes importantes.
*Esforço*: Esforço baixo/médio. Usei o Chat-GPT para me guiar e pesquisei em outras fontes para conferir veracidade e completar detalhes.

---
> O que acontece quando digitamos o endereço de um site no navegador?
> Tenta descrever com o máximo de detalhes que você puder

Essa foi uma das perguntas que me fizeram em uma entrevista técnica para Desenvolvedor Back-end Sênior. Na primeira vez que fiz esse processo seletivo não soube responder muito bem a essa pergunta. Eu anotei essa pergunta como um dos pontos que me atrapalharam na entrevista e quando eu participei de novo do processo seletivo nessa mesma empresa, eu estava preparado.

Vamos considerar que existem 6 partes no processo de exibir para uma pessoa o site para o qual ela digitou o endereço no navegador:
1. [[3 - Resources/Tecnologia/O que acontece quando digitamos o endereço de um site no navegador#Resolução DNS\|Resolução DNS]]
2. [[3 - Resources/Tecnologia/O que acontece quando digitamos o endereço de um site no navegador#Estabelecimento de uma conexão TCP\|Estabelecimento de uma conexão TCP]]
3. [[3 - Resources/Tecnologia/O que acontece quando digitamos o endereço de um site no navegador#Envio e processamento da requisição HTTP\|Envio e processamento da requisição HTTP]]
4. [[3 - Resources/Tecnologia/O que acontece quando digitamos o endereço de um site no navegador#Geração e envio da resposta\|Geração e envio da resposta]]
5. [[3 - Resources/Tecnologia/O que acontece quando digitamos o endereço de um site no navegador#Renderização do site\|Renderização do site]]
6. [[3 - Resources/Tecnologia/O que acontece quando digitamos o endereço de um site no navegador#Exibição do site\|Exibição do site]]
## Resolução DNS
Os endereços que digitamos na barra de endereços do navegador para acessar sites, como [https://www.google.com](https://www.google.com), são apenas uma forma mais legível para humanos, são *aliases*. Eles não são os reais endereços dos servidores que hospedam os sites.

Para acessar um site, nosso navegador precisa do endereço IP do servidor que o hospeda. Então, quando digitamos um endereço de um site no navegador, ele tenta descobrir o endereço IP desse site. Primeiro, os arquivos locais do computador são consultados (eles podem conter cache de acessos anteriores ou alguma associação de domínio a endereço IP feita manualmente no arquivo hosts). Depois, se a informação não foi encontrada localmente, o navegador consulta um servidor DNS.
## Estabelecimento de uma conexão TCP
Com o endereço IP em mãos, o próximo passo é estabelecer uma conexão TCP com o servidor do site. Essa conexão é estabelecida por meio de uma troca de pacotes entre as duas máquinas para garantir que é uma conexão confiável.

Considerando que a conexão TCP foi estabelecida com sucesso, ela já pode ser usada para enviar a requisição HTTP para o servidor.

> [!faq] Versões do protocolo HTTP
> No protocolo HTTP 1.0, uma conexão TCP precisa ser estabelecida para cada requisição HTTP que vai ser feita, o que podia ser problemático para a performance.
> Nas [versões seguintes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP), no entanto, foram implementadas evoluções para permitir que a conexão fosse reutilizada para várias requisições.
## Envio e processamento da requisição HTTP
Nesse momento, o cliente *(seu navegador)* envia a requisição HTTP para o servidor por meio da requisição TCP que foi estabelecida. O servidor recebe a requisição e começa o processamento, o que pode envolver diversos processos como roteamento, balanceamento de carga, interações com bancos de dados, consulta de cache, requisições para outras aplicações, etc.
## Geração e envio da resposta
Depois de todo o processamento, o servidor devolve a resposta da requisição HTTP para o cliente, contendo status da requisição, headers e o próprio HTML site no corpo.
## Renderização do site
Quando o navegador recebe o HTML, ele começa o processo de renderizar a página, montar o DOM, baixar fontes, CSS, scripts JS, imagens, vídeos.
## Exibição do site
Depois que o navegador termina de baixar todos os scripts, folhas de estilização e mídia, e de montar o DOM, o site está pronto para ser exibido.
## Referências
- [Overview of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview#http_flow)
- [Evolution of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP)