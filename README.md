# rifa-solidaria-taquari

## Uma Rifa Beneficente para Apoiar o Projeto Saúde Bucal no Taquari

Este projeto consiste em uma página web simples e informativa para divulgar e gerenciar uma rifa solidária com o objetivo de arrecadar fundos para o "Projeto Saúde Bucal", que atua na comunidade do Taquari. Ao participar desta rifa, você concorre a um lindo centro de mesa da Sgabello e contribui para levar sorrisos mais saudáveis a crianças e adultos da região.

## Como o Código Funciona (Para Curiosos em Programação)

Se você tem interesse em saber como esta página funciona por dentro, aqui vai uma breve explicação:

* **HTML (estrutura):** O arquivo `index.html` define a estrutura de todos os elementos da página, como textos, imagens, formulários e a tabela de participantes.
* **CSS (estilos):** As tags `<style>` dentro do `<head>` contêm o código CSS, responsável por toda a aparência visual da página, como cores, fontes, espaçamentos e o layout responsivo (que se adapta a diferentes tamanhos de tela, como celulares e computadores).
* **JavaScript (interatividade):** O código dentro da tag `<script>` no final do `<body>` adiciona interatividade à página:
    * **Formatação do Telefone:** A função `formatarTelefone` formata o número de telefone digitado no formulário para o padrão brasileiro (com parênteses e hífen).
    * **Carregamento dos Números:** A função `carregarNumeros` é executada quando a página é carregada (`DOMContentLoaded`). Ela faz uma requisição (usando a função `Workspace`) para a API do Google Apps Script (`apiUrl`). Essa API retorna os dados dos participantes que compraram cotas, e a função atualiza a tabela na página com essas informações.
    * **Registro de Escolha:** Quando o formulário é enviado, o evento `submit` é capturado. A função associada impede o envio padrão do formulário e envia os dados (quantidade de cotas, nome e telefone) para a mesma API do Google Apps Script através de uma requisição `POST`. O modo `no-cors` indica que a comunicação com a API pode ter algumas restrições de segurança no navegador, mas o envio dos dados ainda deve ocorrer. Após o envio (assumindo sucesso), um alerta é exibido e a lista de participantes é recarregada.
    * **Carrossel de Imagens:** O código JavaScript também é responsável por controlar o carrossel de imagens. Ele seleciona as imagens, define um índice para a imagem atual, e utiliza as funções `showImage`, `nextImage` e `prevImage` para exibir as imagens em sequência automática (a cada 5 segundos) ou quando os botões de navegação são clicados. O carrossel pausa quando o mouse passa por cima e volta a funcionar quando o mouse sai.

## Próximos Passos (Opcional)

Se você pretende continuar desenvolvendo este projeto, algumas ideias para os próximos passos poderiam ser:

* **Integração de Pagamento:** Integrar um sistema de pagamento online diretamente na página para que os participantes possam comprar as cotas sem precisar enviar comprovante manualmente.
* **Geração de Números Aleatórios:** Em vez de deixar os participantes escolherem a quantidade, você poderia gerar números aleatórios para cada cota comprada.
* **Melhorias na Interface:** Adicionar mais estilos CSS para deixar a página ainda mais atraente e profissional.
* **Validação de Formulário:** Adicionar validações no formulário para garantir que os campos obrigatórios sejam preenchidos corretamente.
* **Compartilhamento em Redes Sociais:** Adicionar botões de compartilhamento para facilitar a divulgação da rifa.

## Contribuição (Se aplicável)

Se você é um desenvolvedor e gostaria de contribuir com este projeto, sinta-se à vontade para entrar em contato! Podemos discutir melhorias e novas funcionalidades.

## Licença

Este projeto não possui uma licença específica definida. Caso queira adicionar uma licença de código aberto, como a MIT License ou a Apache License 2.0, você pode incluir as informações aqui.
---

Agradecemos imensamente a sua participação e colaboração com o Projeto Saúde Bucal no Taquari! Juntos, podemos fazer a diferença!
