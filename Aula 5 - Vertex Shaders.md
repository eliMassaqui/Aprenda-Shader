# Unity Shader Graph Basics (Part 5 - Vertex Shaders)

Este projeto demonstra como criar um **efeito de onda animada** usando **Vertex Shader** no Unity com **Shader Graph** (URP).

## 🎯 Objetivo

Deformar a malha de um objeto aplicando um movimento senoidal (onda) nos seus vértices ao longo do tempo, criando um efeito visual animado. Também aplicamos uma cor base e uma textura para definir a aparência final.

---

## 🔧 Parâmetros Usados

- **Wave Speed (float)**: Velocidade da animação da onda.
- **Wave Strength (float)**: Altura da onda (quanto os vértices se movem).
- **Base Color (Color)**: Cor do material.
- **Base Texture (Texture2D)**: Textura aplicada sobre o objeto.

---

## 🧠 Lógica do Vertex Shader

1. **Obtemos a posição do vértice** em espaço do objeto.
2. **Extraímos o eixo X** da posição e somamos com o tempo multiplicado pela `Wave Speed`.
3. Aplicamos a função **Seno (Sine)** para gerar a oscilação.
4. O resultado é multiplicado pela `Wave Strength`.
5. **Somamos isso ao eixo Y** da posição original, criando o efeito de subida/descida.
6. A nova posição é passada para o nó **Vertex**, atualizando a malha.

---

## 🎨 Fragment Shader

- Multiplica a **cor base** pela **textura base**.
- O resultado é aplicado ao objeto (saída `Fragment`).

---

## 📦 Requisitos

- Unity 2022.3.62f1 ou superior
- URP (Universal Render Pipeline)
- Shader Graph habilitado

---

## 🖼️ Preview

![Preview](./Preview.png)

---

## 📁 Estrutura

