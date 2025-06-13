# 🌊 Unity Shader Graph - Parte 9 - Scene Intersections 2

Este projeto apresenta dois efeitos visuais avançados usando **Shader Graph** no Unity: **espuma dinâmica em água** e **brilho em objetos na interseção com o solo**. Ambos usam a técnica de *scene depth intersection*.

> 🔧 Requer: Unity URP + Shader Graph + Câmera com Depth Texture ativada

---

## 📌 Conteúdos

### 1. Subgraph: `DepthIntersection`

Utilizado para detectar a distância entre um objeto e o que está embaixo dele na cena (baseado na textura de profundidade da câmera).

- **Output:** valor entre 0 (próximo) e 1 (distante)
- Pode ser reutilizado para efeitos como espuma, brilho, dissolução etc.

---

## 🌊 Efeito 1: Espuma nas Ondas

### 📁 Shader: `FoamShader`

Adaptação do shader de água criado na Parte 5. Agora com espuma visível onde a água encontra outros objetos.

### 🔧 Parâmetros:

- `Foam Distance`: distância de ativação da espuma (ex: 1.5)
- `Foam Color`: cor da espuma
- `Foam Scale`: escala do ruído
- `Foam Velocity`: movimento do ruído
- `Depth Sample Offset`: evita blocos sólidos de espuma

### 🔄 Lógica:

1. Usa o subgraph `DepthIntersection`
2. Aplica `Step` para detectar se está dentro da `Foam Distance`
3. Multiplica com `Simple Noise` para aleatoriedade
4. Usa `Time` para animar o ruído e dar movimento
5. Aplica suavização com `Saturate` e `OneMinus`

---

## ✨ Efeito 2: Brilho nas Bordas

### 📁 Shader: `IntersectionGlow`

Cria um efeito de brilho nas áreas do objeto que tocam o solo ou água, com base na profundidade da cena.

### 🔧 Parâmetros:

- `Glow Color` (HDR): cor do brilho emissivo
- `Intersection Power`: força da transição de brilho
- `Glow Intensity`: intensidade total
- `UV Edge Width`: largura do brilho nas bordas

### 🔄 Lógica:

1. Gera máscara de borda usando UV (valores próximos de 0 e 1)
2. Combina máscaras com `OneMinus`, `Multiply` e `Smoothstep`
3. Aplica cor HDR com `Emission`
4. Multiplica pelo valor do `DepthIntersection` para ativar apenas em interseção com o solo

---

## 🎮 Como Usar

1. **Ative a Depth Texture** na sua câmera:
   - Selecione a Main Camera
   - Marque "Depth Texture" na aba URP

2. **Adicione os shaders aos objetos desejados**
3. **Ajuste os parâmetros no material** para personalizar

---

## 🧠 Aprendizado

✔ Uso prático do **Scene Depth**  
✔ Combinação de **ruído + tempo** para efeitos naturais  
✔ Controle de efeitos via **UVs e máscaras**  
✔ Reutilização com **Subgraph**

---

## 📚 Referência

Tutorial completo por Daniel Ilett:  
[danielilett.com - Shader Graph Part 9](https://danielilett.com/2024-05-28-tut7-13-intro-to-shader-graph-part-9/)

---
