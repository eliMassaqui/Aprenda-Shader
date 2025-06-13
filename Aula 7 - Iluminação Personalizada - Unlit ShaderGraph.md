# 🎨 Unity Shader Graph Basics - Parte 7: Iluminação Personalizada

Neste tutorial, vamos aprender como criar **iluminação personalizada** no Shader Graph da Unity, parte essencial para quem deseja controlar como a luz interage com os objetos além do sistema padrão da Unity.

## 📌 Requisitos

- Unity 2022.3 ou superior  
- Projeto com URP (Universal Render Pipeline) ativo  
- Shader Graph instalado  
- Conhecimentos básicos de Shader Graph (veja partes anteriores da série)

## 🎯 Objetivo

Criar um shader que use **lógica personalizada de iluminação**, simulando como a luz afeta a superfície de um objeto, como brilho direcional ou efeitos estilizados.

---

## 🚧 Passos Básicos

1. **Criar um novo Shader Graph:**
   - Tipo: *Lit Shader Graph* ou *Unlit Shader Graph* (conforme o efeito desejado).
   - Nome sugerido: `CustomLightingShader`.

2. **Adicionar Inputs:**
   - `Base Color` (Color)
   - `Normal Vector` (Vector3)
   - `Light Direction` (Vector3)
   - `Specular Power` (Float)

3. **Calcular Direção da Luz:**
   - Usar o nó `World Space Light Direction`.

4. **Normalização e Dot Product:**
   - Normalizar o vetor da luz e o normal da superfície.
   - Usar `Dot Product` para calcular a influência da luz.

5. **Efeito Specular (opcional):**
   - Calcular reflexo com `Reflect` e usar `Dot Product` com o `View Direction`.

6. **Misturar Resultado Final:**
   - Multiplicar a cor base pelo valor da luz.
   - Somar com componente especular, se houver.
   - Conectar ao `Base Color` (Unlit) ou `Emission` (Lit).

---

## 🔍 Preview do Resultado

O material vai responder à direção da luz com um brilho controlado, podendo simular cel shading, toon lighting ou brilho metálico estilizado.

---

## 🧪 Dica Extra

Se quiser mais realismo, adicione:
- Atenuação pela distância
- Cálculo de sombra manual (avançado)
- Cores por rampa (Ramp Texture)

---

## 📁 Recursos Extras

- [Documentação Oficial Shader Graph (Unity)](https://docs.unity3d.com/Packages/com.unity.shadergraph@latest/)
- [Vídeo Parte 7 no YouTube](#) *(adicione o link real do vídeo aqui)*

---

## ✅ Resultado Esperado

![Exemplo Final](./screenshot.png)

Shader com iluminação própria, totalmente controlada por nós no Shader Graph.

---

🛠️ Criado por [Seu Nome]  
📅 Data: Junho 2025
