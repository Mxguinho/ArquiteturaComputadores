# 🔐 DMA Sec — Segurança em Barramentos e DMA Attacks

Página interativa criada para um seminário sobre **Direct Memory Access (DMA)**, seus riscos de segurança e as defesas modernas. Em vez de slides estáticos, cada conceito é apresentado como um pequeno experimento que você pode manipular direto no navegador.

> Projeto de uma única página (`index.html`), sem build, sem dependências para instalar.

## 🧪 Experimentos

| # | Experimento | O que demonstra |
|---|-------------|-----------------|
| 0 | **Introdução** | O que é DMA e por que dar acesso direto à RAM a periféricos é um problema de segurança |
| 1 | **CPU vs. DMA** | Animação comparando uma transferência de dados mediada pela CPU (uso alto) com uma feita via DMA (CPU livre) |
| 2 | **Caça-Tesouro** | Simulação de um ataque DMA: você é um dispositivo Thunderbolt malicioso varrendo a RAM em busca de senhas e chaves |
| 3 | **Porteiro IOMMU** | A defesa: arraste políticas de acesso (Total ou Restrita) para cada dispositivo e veja o IOMMU bloquear (ou não) o ataque |
| 4 | **Evil Maid** | Linha do tempo interativa de um ataque com acesso físico ao equipamento |

## 🚀 Como usar

Não precisa instalar nada. Basta abrir o arquivo no navegador:

```bash
git clone https://github.com/<seu-usuario>/<nome-do-repositorio>.git
cd <nome-do-repositorio>
# abra o index.html no navegador (duplo clique ou:)
xdg-open index.html   # Linux
open index.html       # macOS
start index.html      # Windows
```

Ou, se preferir servir localmente:

```bash
python3 -m http.server 8000
# acesse http://localhost:8000
```

> ⚠️ É necessário conexão com a internet, pois Tailwind CSS, Font Awesome e as fontes são carregados via CDN.

## 🛠️ Tecnologias

- **HTML5 / CSS3 / JavaScript** puro (vanilla)
- [Tailwind CSS](https://tailwindcss.com/) via CDN
- [Font Awesome 6](https://fontawesome.com/) para ícones
- Fontes [Inter](https://fonts.google.com/specimen/Inter) e [Fira Code](https://fonts.google.com/specimen/Fira+Code)
- SVG animado e API nativa de Drag and Drop

## 📁 Estrutura

```
.
├── index.html   # todo o projeto (HTML, estilos e scripts)
└── README.md
```

## 🎓 Contexto

Material desenvolvido para apresentação de seminário sobre segurança em barramentos, com foco em ataques DMA via Thunderbolt/USB4/PCIe e mitigação com IOMMU. As simulações têm **fins estritamente educacionais** e não executam nenhum ataque real.

## 👤 Autor

**João Pedro Nogueira Hartung** — (https://github.com/Mxguinho)
