# 🎨 Shader Graph – Aulas 1 e 2 (Resumo)

## 📘 Aula 1 – Primeiro Shader (Cor Base)
- Criei um shader básico no Unity usando o **Shader Graph**.
- Usei um **nó "Color"** para definir a cor do objeto.
- A cor foi conectada ao **Master Node (Base Color)**.
- Apliquei esse shader num objeto 3D (por exemplo, uma esfera).
- Resultado: o objeto mostra a cor definida no shader.

## 🖼️ Aula 2 – Texturas e Scroll com UVs
- Aprendi a usar **texturas** com coordenadas UV.
- As **coordenadas UV** são como um plano 2D (horizontal = U, vertical = V) usado para mapear a textura no objeto.
- Para fazer a **textura se mover**, apliquei uma **translação nas UVs**.
- Usei os nós:
  - **Time** (tempo)
  - **Vector2** (Scroll Velocity)
  - **Multiply** (Scroll Velocity × Time)
  - **Add** (UV + deslocamento)
- Resultado: a textura desliza no objeto com o tempo.

## 📐 Explicação Geométrica
- O plano UV funciona como um **plano cartesiano 2D**, onde cada ponto tem coordenadas (u, v).
- O **scroll da textura** é uma **translação geométrica**: todos os pontos UV são deslocados numa direção.
- Isso muda quais partes da imagem são mostradas, criando a **ilusão de movimento**.
- O objeto não muda — apenas o mapeamento da imagem sobre ele se desloca.

## 🔢 Ligação com Matemática (Análise)
- O movimento das UVs pode ser descrito como uma **função linear do tempo**:

- - Isso gera um movimento suave e contínuo da textura.
- A derivada da função é constante, indicando **velocidade constante** na direção escolhida.

---

✍️ Autor: [Elísio Luamba]  
📅 Data do Commit: 2025-06-09

