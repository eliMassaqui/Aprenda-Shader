# 💡 Light Shaders em Unity

Este projeto demonstra como criar e aplicar **shaders de luz personalizados** usando **Shader Graph** e **HLSL** na Unity. O foco é entender e manipular diferentes tipos de iluminação em materiais 3D.

## ✨ Funcionalidades

- Shader com iluminação **Lambertiana** (difusa).
- Shader com efeito **Specular** (Phong/Blinn-Phong).
- Simulação de **normais personalizadas** para alterar a reflexão da luz.
- Implementação de luz direcional e ponto de luz com **Shader Graph** e **HLSL**.
- Suporte a URP (Universal Render Pipeline).

## 🛠️ Requisitos

- Unity 2022.3 ou superior  
- Projeto URP (Universal Render Pipeline)  
- Shader Graph instalado  
- Conhecimentos básicos em vetores e matemática 3D


## 🧠 Conceitos Importantes

- **Normal Vector**: define como a luz interage com a superfície.
- **Dot Product** (`dot`): usado para calcular luz difusa.
- **Reflection Vector**: usado para calcular brilho especular.
- **Shader Graph Nodes**:
  - `Normal Vector`, `Dot Product`, `Fresnel Effect`, `Light Direction`

## 📸 Screenshots

![Diffuse Shader](docs/diffuse_example.png)
*Exemplo de iluminação difusa simples com Shader Graph*

![Specular Shader](docs/specular_example.png)
*Shader com iluminação especular (Phong)*

## 📘 Referências

- Livro: *Building Quality Shaders for Unity Using Shader Graphs* - Daniel Ilett  
- Livro: *Unity Shaders and Effects Cookbook*  
- Documentação oficial da Unity Shader Graph

## 🧪 Testes

Os shaders foram testados em URP em dispositivos Windows e Android. Performance otimizada para cenas estáticas.

## ✅ Objetivo

O objetivo deste projeto é **aprender os fundamentos de iluminação em shaders**, explorando como a luz interage com superfícies usando matemática vetorial.

---

*Feito com ❤️ por [Sr.Massaqui]*


