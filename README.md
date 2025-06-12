# Unity Shader Graph Basics

Este projeto contém exemplos básicos de **Shader Graph** na Unity, mostrando como criar shaders visuais simples sem precisar programar em código.

## O que tem aqui?

- Shaders simples feitos com Shader Graph  
- Materiais aplicados usando esses shaders  
- Cenas de exemplo para testar os shaders  
- Explicações básicas para entender o funcionamento  

## Requisitos

- Unity 2022.3 LTS ou superior  
- Universal Render Pipeline (URP) configurado no projeto  

## Como usar

1. Clone ou baixe este repositório.  
2. Abra o projeto na Unity.  
3. Navegue até a pasta `Shaders` para ver os gráficos de shader.  
4. Abra as cenas na pasta `Scenes` para testar os shaders em ação.  
5. Experimente editar os Shader Graphs para aprender e criar seus próprios efeitos.  

## Links úteis

- [Documentação oficial do Shader Graph](https://docs.unity3d.com/Packages/com.unity.shadergraph@latest)  
- [Tutorial Shader Graph na Unity Learn](https://learn.unity.com/tutorial/introduction-to-shader-graph)

- # 🎨 Shaders com Shader Graph na Unity (URP)

Este repositório reúne estudos práticos e efeitos visuais criados com **Shader Graph** na **Unity URP**. A proposta é explorar o poder da criação visual de shaders — sem código — para alcançar resultados profissionais e otimizados em jogos e aplicações interativas.

---

## ✨ Destaques

- ✅ Shaders 100% criados com **Shader Graph**
- 🚀 Otimizados para **Universal Render Pipeline (URP)**
- 🧠 Controláveis por tempo, interação, distância e luz
- 🕹️ Com suporte a **valores expostos** para fácil ajuste via Inspector
- ⚡️ Prontos para uso em projetos estilizados ou realistas

---

## 🧠 O que você vai encontrar aqui

### 1. Fundamentos do Shader Graph
- Interface do Shader Graph e fluxo de trabalho.
- Tipos de shader (URP Unlit, URP Lit, Sprite Unlit).
- Nós essenciais: `Time`, `UV`, `Color`, `Multiply`, `Add`, `Sine`, `Step`, etc.
- Aplicação de shaders em materiais e prefabs.

### 2. Efeitos Visuais Reais

#### 🔥 Dissolve Shader
- Efeito de desintegração com textura de ruído.
- Controle por slider (`Edge Threshold`) e cor de borda (`Edge Color`).
- Pode ser usado para simular desaparecimento, destruição ou stealth.

#### 🌈 Fresnel Border
- Brilho nas bordas do objeto com base no ângulo da câmera.
- Ideal para efeitos mágicos, energéticos ou indicadores de seleção.

#### 💡 Emissão Dinâmica
- Controle de brilho emissivo via tempo, distância ou trigger.
- Perfeito para LEDs, objetos energizados ou destaque visual.

#### 📡 Reatividade com Jogador
- Shaders que reagem à **distância da câmera ou do jogador**.
- Útil para criar ambientes dinâmicos, feedback visual ou mecânicas de jogo.

#### 🎭 Máscaras de Interação
- Uso de texturas ou formas para aplicar efeitos apenas em regiões específicas.
- Exemplo: efeito de dano localizado, ou materiais interativos por toque.

#### 🎯 Pulsar Effect
- Variações cíclicas na cor, brilho ou forma (com `Sine` + `Time`).
- Recomendado para feedback visual ou elementos vivos.

#### 🕳️ Holograma & Scanline
- Shaders com linhas animadas e transparência variável.
- Estilo futurista ou sci-fi com luz pulsante e flicker.

---

## ⚙️ Técnicas Utilizadas

- **Exposição de propriedades** para controle no Inspector
- **Uso de canais RGBA** de texturas como máscaras ou mapas
- **Espaços de coordenadas**: UV, Object, World e View
- **Math Nodes**: `Sine`, `Cosine`, `One Minus`, `Lerp`, `Clamp`, etc.
- **Texturas Procedurais** e ruído para dissolução ou movimento
- **Integração com Iluminação URP** (Specular, Emission, Normals)
- **Shader Graph Sub-graphs** para organização e reuso
- **Nodes customizados** com blocos matemáticos combinados

---


