# Unity Shader Graph Basics – Parte 8: Scene Intersections 1

Este documento resume os principais conceitos e nós utilizados na Parte 8 da série *Unity Shader Graph Basics* de Daniel Ilett. O foco desta aula é criar efeitos de **interseção entre objetos e cenas** usando Shader Graph no Unity URP.

---

## 🎯 Objetivo da Aula

Criar um efeito visual que destaca **onde um objeto intersecta o mundo** — muito usado para mostrar áreas de contato com o chão, paredes, ou superfícies líquidas (ex: "onde um objeto toca a água").

---

## 🧪 Conceitos-Chave

- **Interseção**: detectar a "base" do objeto (sua parte mais baixa) e aplicar efeitos visuais nesse ponto de contato.
- **Espaços de coordenadas**: é necessário converter posições entre o mundo (`World Space`) e o objeto (`Object Space`) para medir distâncias corretamente.
- **Gradiente de Efeito**: é feito usando operações matemáticas com a posição do objeto e um controle de "largura".

---

## 🧩 Nós Essenciais Usados

| Nó                     | Função                                                                 |
|------------------------|------------------------------------------------------------------------|
| **Position**           | Captura a posição dos pixels do objeto no mundo ou no espaço do objeto. |
| **Object Position**    | Posição central do objeto em coordenadas de objeto.                     |
| **Split**              | Divide vetores para trabalhar com componentes individuais (X, Y, Z).    |
| **Subtract**           | Subtrai posições para medir altura relativa.                            |
| **Absolute**           | Garante que a diferença seja sempre positiva.                           |
| **Step**               | Cria uma borda nítida para o efeito de interseção.                      |
| **One Minus**          | Inverte valores, útil para criar máscaras.                              |
| **Multiply**           | Controla a intensidade do efeito ou mistura de cores.                   |
| **Color**              | Define a cor do efeito de interseção.                                   |
| **Lerp**               | Mistura entre a cor normal e a cor do efeito.                           |

---

## 🛠️ Lógica do Shader

1. **Captura a posição atual do fragmento** (Position node em *World* ou *Object* Space).
2. **Compara com a posição mais baixa do objeto** (Y da posição do centro do objeto).
3. **Calcula a distância vertical** até o chão.
4. **Aplica um Step** para definir uma faixa de transição.
5. **Multiplica por uma cor ou outro valor visual** para mostrar o efeito.
6. **Mistura com a cor base usando Lerp**, criando uma borda ou efeito colorido onde o objeto toca o mundo.

---

## 🔍 Exemplo de Uso

- **Highlight de pés de personagem tocando o chão**.
- **Contorno de objetos sendo inseridos no solo**.
- **Contato com superfícies líquidas ou efeitos mágicos**.

---

## 📌 Dicas

- Ajuste o valor de referência no **Step** para controlar a espessura do efeito.
- Combine com **Normal Vectors** ou **Fresnel** para adicionar mais realismo.
- Funciona bem em materiais **Unlit**, mas pode ser adaptado para **Lit** também.

---

> 🔗 Continuação: Este efeito é aprimorado na Parte 9 com controle de altura e máscaras 3D mais complexas.

