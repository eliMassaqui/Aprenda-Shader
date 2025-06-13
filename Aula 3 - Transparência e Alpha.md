# Unity Shader Graph - Transparência e Alpha (Aula 3)

Este projeto demonstra como criar um shader com **transparência controlada por Alpha** usando o **Shader Graph** na Unity (versão 2022.3.62f1, URP).

## 🎯 Objetivo

Aprender a:
- Usar o canal Alpha para controlar a transparência de materiais.
- Aplicar `Alpha Clip Threshold` para cortar áreas com baixa opacidade.
- Trabalhar com texturas RGBA e o nó `Split`.

## 🧱 Componentes do Shader

### Propriedades
- **Base Color**: Define a cor do objeto.
- **Base Texture**: Textura RGBA usada no material.
- **Trosh (Alpha Clip Threshold)**: Valor limite para descartar pixels com alpha baixo.

### Nós principais
- `Sample Texture 2D`: Lê a textura com canal Alpha.
- `Multiply`: Multiplica a cor base pela textura.
- `Split`: Separa os canais RGBA da textura.
- `Alpha`: Canal A da textura (usado para transparência).
- `Alpha Clip Threshold`: Controla o corte de pixels transparentes.

## 🖼️ Resultado

- Objetos vermelhos aparecem parcialmente transparentes, conforme o valor do canal Alpha da textura.
- Áreas com Alpha abaixo de `Trosh` ficam invisíveis.

## ⚙️ Configurações do Shader Graph

- **Surface Type**: Transparent
- **Blend Mode**: Alpha
- **Alpha Clipping**: Ativado (para corte com `Trosh`)

## 📂 Estrutura

