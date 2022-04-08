# LTW-Project

## Database (SQL)

### Contexto

#### Utilizadores - Proprietários e Clientes
É necessário criar uma base de dados para armazenar dados referentes a um site de entrega de comida, que serve como plataforma para vários restaurantes e estabelecimentos venderem os seus produtos alimentares. Os utilizadores registados no site podem ser **Clientes** ou **Proprietários de Restaurantes**. De **qualquer utilizador**, interessa saber o seu nome, a sua idade, o seu NIF, o seu username e password no site. Cada utilizador tem um ID associado. Dos **Proprietários de Restaurantes** interessa registar um email e um número de telefone. Dos **Clientes**, importa registar uma morada.

#### Restaurantes
Cada **Proprietário de Restaurante** pode ter 1 ou mais restaurantes. A cada **Restaurante** está associado um nome, uma morada, uma classificação média (de 0 a 5 estrelas) obtida das reviews dos utilizadores, um tipo (associado ao tipo de comida servida), um ou mais intervalos de tempo durante o dia entre os quais o estabelecimento está aberto para take away, uma listagem dos pratos disponíveis e uma listagem dos pedidos da última semana. A cada restaurante corresponde um ID.

#### Pratos
Cada Restaurante pode ter 1 ou mais **Pratos**, com um ID próprio, um nome, uma categoria (bebida, acompanhamento, prato principal, sobremesa...), um preço associado, uma promoção (que é 0 quando não houver nenhuma em vigor), uma descrição do produto (listagem de ingredientes, avisos sobre alergias, etc) e um estado (disponível/indisponível para compra).

#### Pedidos
Um Cliente pode efetuar um ou mais pedidos e esses pedidos podem conter 1 ou mais Pratos de um mesmo Restaurante. Os Pedidos têm um número associado, um estado (Recebido, Em Preparação, Pronto a Entregar, Entregue),  um comentário adicional feito pelo cliente se este desejar, uma morada de entrega (que pode ser a mesma que o Cliente tem registada na sua conta ou outra) e uma data e hora de submissão.

#### Reviews (Classe de Associação)
Um Cliente pode efetuar uma ou mais Reviews direcionadas a um restaurante específico. Estas reviews têm um título, um comentário (definidos pelo cliente), um horário e data de submissão, uma avaliação (de 0 a 5) e uma resposta (dada pelo Proprietário).

#### Favoritos (Classe de Associação)
Um Cliente pode definir zero ou mais Restaurantes como favoritos.
