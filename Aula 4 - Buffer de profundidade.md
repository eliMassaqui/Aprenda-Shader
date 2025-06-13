# Unity Shader Graph Basics (Parte 4 - Depth Buffer)

## 🧠 O que é o Depth Buffer?

O **Depth Buffer** (ou Z-Buffer) é uma estrutura usada pela GPU para **armazenar a distância de cada pixel em relação à câmera**. Isso permite que a Unity saiba **qual objeto está na frente** de outro, garantindo que a cena seja renderizada corretamente.

---

## 🎯 Para que serve?

- Determinar **quais objetos estão visíveis**.
- Criar efeitos visuais baseados na profundidade da cena.
- Controlar **transparência, névoa, sombras falsas**, entre outros.

---

## 🧱 Nó importante: `Scene Depth`

No **Shader Graph**, usamos o nó `Scene Depth` para **acessar a profundidade dos pixels** da cena.

### 🔁 Conversão necessária
O valor de `Scene Depth` geralmente vem em **Clip Space**, então é comum usar o nó:




Para converter esse valor para um formato mais útil (View Space).

---

## 💡 Exemplo de uso

### 🔻 Escurecer objetos distantes

1. Usar o nó `Scene Depth`.
2. Passar pelo `Linear Eye Depth`.
3. Usar o valor convertido para controlar a cor do objeto:
   - Objetos mais longe = mais escuros.
   - Objetos mais perto = mais claros.

---

## 🎨 Efeitos possíveis com Depth Buffer

- Neblina/Névoa (Fog)
- Falso sombreamento (Fake Shadows)
- Transparência baseada na distância
- Contornos de objetos ao fundo
- Estilização de camadas

---

## 📌 Dica

Nem todos os pipelines têm suporte total ao `Scene Depth`. Certifica-te que estás a usar o **URP** ou **HDRP**, e que o objeto está marcado para ser renderizado com profundidade.

---

## 📚 Requisitos

- Unity 2022.3+  
- Shader Graph ativado  
- URP (Universal Render Pipeline) configurado  
- Câmera com Depth Texture ativada (`URP Asset > General > Depth Texture`)

---

## 🔗 Recursos úteis

- [Unity Docs: Scene Depth Node](https://docs.unity3d.com/Packages/com.unity.shadergraph@latest)
- [URP Depth Texture](https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@latest)

---

