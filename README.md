# GeraPrompt — Gerador de prompt para loteamentos

Ferramenta de **arquivo único (HTML)** que monta o prompt para transformar uma base chapada de AutoCAD + Google Earth em fotografia aérea realista de loteamentos e condomínios de alto padrão.

Sem instalação, sem servidor, sem login e sem internet. Abre no navegador com dois cliques.

![Interface do GeraPrompt](preview.png)

## O que ele gera

Sempre os três juntos:

1. **Prompt** — em português, em blocos (geometria, paisagismo, elementos, edificações, acabamentos, luz e realismo)
2. **Prompt negativo** — curto, em frases imperativas
3. **Checklist de preservação** — repetido no fim do prompt, onde o modelo ainda presta atenção

## Como usar

1. Abra o `index.html` no navegador
2. Escolha o enquadramento, o paisagismo, os equipamentos e os acabamentos
3. Clique em **Copiar prompt + negativo** e cole no campo de prompt da sua ferramenta

Para o Magnific, que não tem campo de negativo: o botão já entrega tudo num bloco só, com o negativo identificado no fim.

## O que o prompt protege

O princípio é simples: **textura pode, geometria não.**

| Elemento | Regra |
|---|---|
| Traçado, lotes e vias | idênticos à base |
| Paisagismo | mesma posição, espécie, porte e proporção; cor varia dentro do natural |
| Equipamentos | quadra permanece quadra; nada vira edificação |
| Edificações | mesmo número, planta e cobertura; nenhuma ocupa área verde |
| Água | só onde está desenhada |

## Por que funciona

Três decisões explicam o resultado:

**1. Uma instrução por bloco.** Modelos de imagem perdem regras no meio de textos longos. O prompt tem ~350 palavras, divididas em blocos curtos.

**2. Poucas negações.** Cada palavra citada no negativo vira candidata a aparecer na imagem. Por isso o negativo tem 4 frases, não 30.

**3. Regras de substituição explícitas.** O modelo não "cria" uma casa no lugar de uma quadra — ele substitui. Cada substituição possível precisa da sua própria frase: *"quadra permanece quadra"*, *"arbusto não vira árvore"*.

## Presets

- **Prancha atual** — configuração de uso diário
- **Base CAD + GEarth** — padrão limpo
- **Refinar humanização** — para melhorar um resultado anterior
- **Litorâneo** e **Chácaras e vinhedos** — variações de contexto

## Compatibilidade

Funciona com qualquer modelo que aceite prompt de imagem: Magnific (Seedream, Nano Banana), Gemini/Imagen, Flux, SDXL, DALL·E.

Para bases muito detalhadas, dá para usar o mesmo texto com ControlNet (lineart/canny) e travar o traçado de verdade.

## Rodando localmente

Não há build. Baixe o `index.html` e abra.

```bash
git clone https://github.com/luizabgk/geraprompt.git
cd geraprompt
# abra index.html no navegador
```

## Licença

MIT — veja [LICENSE](LICENSE).
