# 🎨 Unity Shader Graph Basics – Parte 10: Custom Functions

Este documento resume a Parte 10 da série **Shader Graph Basics** do [Daniel Ilett](https://danielilett.com), focando no uso de **Custom Functions** no Shader Graph da Unity.

---

## 📌 Objetivo

Aprender a **criar funções personalizadas** no Shader Graph utilizando blocos `Custom Function`. Isso permite ir além dos nós padrões e usar lógica personalizada via:

- Código HLSL direto
- Arquivos externos `.hlsl`

---

## 🧱 Principais Componentes

### 🔧 Nó: `Custom Function`

Permite inserir código HLSL personalizado no Shader Graph.

| Parâmetro | Descrição |
|-----------|-----------|
| **Function Name** | Nome da função (obrigatório se for inline) |
| **Source** | Inline ou arquivo externo (.hlsl) |
| **Inputs** | Variáveis de entrada da função |
| **Outputs** | Valores retornados |

---

## 🧪 Exemplo de Uso

### 🎯 Objetivo:
Criar uma função personalizada para **manipular UVs** com seno e cosseno.

### 🧩 Passos:

1. Adicione o nó `Custom Function`.
2. Defina o Source como `String`.
3. Escreva a função:

```hlsl
void SineUV(float2 UV, out float2 Out)
{
    Out = float2(sin(UV.x), cos(UV.y));
}
Adicione os Inputs:

UV (Vector2)

Adicione o Output:

Out (Vector2)

Conecte o Output a um nó UV ou Base Color.

📂 Alternativa: Usando Arquivo Externo
Crie um arquivo MyFunctions.hlsl na pasta Assets/Shaders/.

Escreva a função HLSL lá:

hlsl
Copiar
Editar
void MultiplyByTwo(float In, out float Out)
{
    Out = In * 2;
}
No Shader Graph:

Adicione um nó Custom Function

Mude o Source para File

Selecione o arquivo .hlsl

Digite MultiplyByTwo como o nome da função

💡 Dicas
Nome de função HLSL não pode colidir com funções internas da Unity.

Use out nos parâmetros para cada saída.

Sempre use float, float2, etc., para tipos — evite vec2, int, etc.

🔍 Aplicações
Operações matemáticas personalizadas

Efeitos visuais únicos

Integração com lógica de jogos

Otimização de performance com código HLSL específico

📘 Recurso Complementar
Shader Graph Custom Functions - Unity Docs

🧠 Conclusão
O uso de Custom Functions dá liberdade total para criar comportamentos visuais avançados que não são possíveis apenas com os nós padrões. Uma ferramenta poderosa para quem deseja expandir os limites do Shader Graph.

