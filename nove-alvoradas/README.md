# Nove Alvoradas

Protótipo de ação em mundo aberto (Three.js). Em nove dias, Afran desce da Torre Rubra:
explore a Ilha de Aura, aprenda técnicas com os seis mestres, vença duelistas e campeões e fique forte
antes do último amanhecer.

- `index.html` — o jogo inteiro (render, mundo, personagens, combate, IA, HUD, save).
- `models/models.js` — esqueletos animados (Quaternius) embutidos em base64; também animam o Kai.
- `assets/models/` — modelos 3D em `.glb` (Kai, árvores, rochas, cactos, palmeiras, flores).
- `assets/textures/` — texturas PBR do terreno (cor, normal, rugosidade) e a textura das nuvens.

Publicado como Artifact: https://claude.ai/artifact/R15RuBrfQn5nvtBMEFTz2n

Para rodar localmente: `python3 -m http.server` nesta pasta e abrir `http://localhost:8000`
(os assets são carregados por `fetch`, então abrir o arquivo direto com `file://` não funciona).

## Créditos dos assets

| Arquivo | Origem | Licença |
| --- | --- | --- |
| `assets/models/kai.glb` | "HairSample_Male", modelo de exemplo do VRoid Studio (pixiv), via [madjin/vrm-samples](https://github.com/madjin/vrm-samples) | CC0 |
| `assets/models/nature.glb`, `nature_lo.glb` (árvores, pinheiros, árvores mortas, rochas, arbustos, samambaia, flores) | [Stylized Nature MegaKit](https://quaternius.com/packs/stylizednaturemegakit.html), Quaternius | CC0 |
| `assets/models/nature.glb`, `nature_lo.glb` (cactos e palmeiras) | [Nature Kit](https://kenney.nl/assets/nature-kit), Kenney | CC0 |
| `assets/textures/grass_*`, `sand_*`, `gravel_*` (rockyGround), `rock_*` | [Babylon.js Assets](https://github.com/BabylonJS/Assets/tree/master/textures) | CC BY 4.0 — © Babylon.js |
| `assets/textures/cloud.webp` | [@pmndrs/assets](https://github.com/pmndrs/assets) | CC0 |
| `models/models.js` | [Animated Men Pack](https://quaternius.com/), Quaternius | CC0 |

Conversões feitas para a web: texturas redimensionadas e convertidas para WebP; os modelos da natureza
foram juntados num único `.glb` com texturas compartilhadas, e `nature_lo.glb` é a versão simplificada
usada de longe (folhas reduzidas a ~1/3 dos cartões, aumentados; troncos simplificados com meshoptimizer).
