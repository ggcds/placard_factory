
# 🖼️ Speaker Placard Factory

Este projeto gera automaticamente **placards de palestrantes** para eventos usando Python.  
A aplicação remove o fundo das imagens dos palestrantes, insere-as em um background institucional e adiciona informações como **nome**, **cargo** e **país** de origem, obtidos de um arquivo CSV.

---

## 📂 Estrutura de pastas

```bash
.
├── background/            # Imagem de fundo principal (background.png)
├── speakers/               # Imagens dos palestrantes (.jpg, .png)
├── datasets/
│   └── government_positions.csv  # CSV com informações de palestrantes
├── output/                 # Onde os placards gerados serão salvos
├── placard_factory.py    # Script principal
└── README.md               # Este arquivo
```

---

## ⚙️ Tecnologias utilizadas

- **Python 3.8+**
- **Pandas** (manipulação do CSV)
- **Pillow (PIL)** (edição de imagens)
- **rembg** (remoção de fundo automático via IA)

---

## 🚀 Como rodar o projeto

1. Clone este repositório:

```bash
git clone https://github.com/seu-usuario/placard_factory.git
cd placard-factory
```

2. Instale as dependências:

```bash
pip install pandas pillow rembg
```

3. Certifique-se que as pastas `background/`, `speakers/` e `datasets/` estão preenchidas corretamente.

4. Execute o script:

```bash
python placard-factory.py
```

5. Os placards gerados estarão disponíveis na pasta `output/`.

---

## 📋 Formato esperado do CSV

O arquivo `datasets/government_positions.csv` deve ter o seguinte formato:

```csv
index,name,position,country
john-smith,John Smith,Senator,United States
olivia-brown,Olivia Brown,Governor,Canada
shrek,Shrek,Lord Protector of the Swamp,Far Far Away
```

- O `index` deve ser o **nome do arquivo de imagem**, sem a extensão (`.jpg`, `.png`).

---

## 🖌️ Layout do placard

- A imagem do palestrante é redimensionada para **85% da altura** do background.
- Uma faixa verde exibe:  
  **"Nome do Palestrante - Cargo, País"**  
- Na parte inferior, há uma faixa branca com o link de informações do evento.
