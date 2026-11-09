> As imagens desta pasta são ativos locais do escritório e **não são versionadas** no repositório público. O GitHub guarda apenas este README e o `manifest.json`.

# Biblioteca de referências dos presets

Regra: referência é ativo do escritório, não lixo de teste.

## Critérios

- render 3D ou foto real do escritório, ou referência explicitamente aprovada;
- nítida, sem motion blur;
- lado menor de pelo menos 1024 px;
- sem texto, watermark, logo ou interface;
- enquadramento parecido com a cena que o preset quer gerar;
- imagem de IA só entra como conceito provisório.

## Masterplan

O fluxo top-down usa duas imagens:

1. `masterplan_obliquo.jpg` — referência visual aprovada pela Luiza, 4096×2286.
2. `loteamento_linhas.jpg` — planta com divisas, usada como estrutura para as linhas de lote continuarem aparecendo.

A referência visual dá o acabamento. A planta de divisas dá o traçado. Uma não substitui a outra.

## Situação atual

- Clube: benchmark aprovado.
- Lago e deck: referência preferida da Luiza.
- Masterplan top-down: referência visual aprovada + planta de divisas como estrutura.
- Masterplan oblíquo: render 3D oblíquo do escritório.
- Pavilhão: revisar enquadramento.
- Entrada: portaria real padrão Alphaville, Wikimedia Commons, CC BY-SA 4.0.
- Haras: foto real CC0, Wikimedia Commons.
- Playground: moodboard de 3 fotos reais com visão geral, balanços e gangorra, Wikimedia Commons, com autores e links no manifesto.

O arquivo `manifest.json` guarda origem, tipo, resolução e status de cada imagem.
