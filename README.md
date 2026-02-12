# Documentação do Projeto: AluGames

Este arquivo descreve a estrutura do sistema de aluguel de jogos de tabuleiro (boardgames).

---

## 1. Estrutura de Metadados
O documento utiliza a codificação **UTF-8** e possui o título **AluGames**. 
* **CSS**: O arquivo de estilo principal está localizado em `css/main.css`.
* **Imagens**: O projeto utiliza arquivos vetoriais (`.svg`) para elementos visuais e logotipos, e arquivos `.png` para as capas dos jogos.

---

## 2. Dashboard de Jogos
A página apresenta uma lista de jogos disponíveis para aluguel dentro de uma lista não ordenada (`ul`) com a classe `dashboard__items`.

### Itens da Lista
Cada jogo é representado por um elemento `li` com um ID único (`game-1`, `game-2`, `game-3`). Os componentes de cada item são:

1.  **Imagem do Jogo**: Contida em uma `div` que pode receber a classe modificadora `--rented` para aplicar um filtro visual de alugado.
2.  **Nome do Jogo**: Exibido em um parágrafo.
3.  **Botão de Ação**: Um link (`<a>`) que dispara a função `alterarStatus(id)`. 
    * O texto muda entre **Alugar** e **Devolver**.
    * A classe `dashboard__item__button--return` é usada quando o item precisa ser devolvido.

---

## 3. Lista de Jogos Cadastrados

| ID | Nome do Jogo | Status Inicial |
| :--- | :--- | :--- |
| `game-1` | Monopoly | Disponível (Alugar) |
| `game-2` | Ticket to Ride | Disponível (Alugar) |
| `game-3` | Takenoko | Alugado (Devolver) |

---

## 4. Comportamento Esperado (JavaScript)
O arquivo `js/app.js` deve gerenciar a troca de estado dos jogos. Ao clicar no botão, a lógica deve:
1. Identificar o jogo pelo ID passado na função `alterarStatus`.
2. Alternar a classe da imagem (`dashboard__item__img--rented`).
3. Alternar a classe do botão (`dashboard__item__button--return`).
4. Alterar o texto do botão entre "Alugar" e "Devolver".

---

> **Dica**: A estrutura visual utiliza "hachuras" e barras de "fade" (SVG) para compor o design moderno da interface.
<img width="1794" height="903" alt="Image" src="https://github.com/user-attachments/assets/006d0784-90c5-4186-9971-fdf4d31ba4b4" />
