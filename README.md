# 🖼️ AI Image Captioner — Give Meaningful Names to Your Photos with AI

An image captioning tool built with **Salesforce BLIP** (Hugging Face Transformers) and **Gradio**.
It turns images into natural-language descriptions — through a simple web interface, for every image on a web page, or for a whole folder of local photos.

> Built as part of the IBM Skills Network guided project *"Give Meaningful Names to Your Photos with AI"*.

---

## ✨ Why image captioning?

Images carry a lot of information that search engines and data systems can't read. Converting them into text helps to:

- **Improve accessibility** for visually impaired users
- **Boost SEO** by describing image content to search engines
- **Organize large image collections** and make them searchable
- **Automate descriptions** for social media, e-commerce and advertising
- **Save time** compared to writing captions by hand

---

## 🚀 Features

| Script | What it does |
|---|---|
| `image_captioning_app.py` | Gradio web app: upload an image and get a caption instantly |
| `automate_url_captioner.py` | Scrapes all images from a web page (e.g. Wikipedia) and writes their captions to `captions.txt` |
| `image_cap.py` | Generates a caption for a single local image |
| `hello.py` | Minimal Gradio "hello world" used to test the setup |

**Bonus:** captioning every `.jpg / .jpeg / .png` in a local folder and saving the results to a text file, with optional support for the larger **BLIP-2** model.

---

## 🧠 Model

- **[Salesforce/blip-image-captioning-base](https://huggingface.co/Salesforce/blip-image-captioning-base)** — the default, lightweight model
- **[Salesforce/blip2-opt-2.7b](https://huggingface.co/Salesforce/blip2-opt-2.7b)** — optional, more powerful (~10 GB, recommended to run locally)

---

## 🛠️ Tech Stack

- Python 3
- [Hugging Face Transformers](https://huggingface.co/docs/transformers) (BLIP)
- [PyTorch](https://pytorch.org/)
- [Gradio](https://www.gradio.app/)
- Pillow, NumPy
- Requests + BeautifulSoup4 (web scraping)

---

## ⚙️ Installation

```bash
git clone https://github.com/iremkursun/ai-image-captioner.git
cd ai-image-captioner

python3 -m venv my_env
source my_env/bin/activate      # Windows: my_env\Scripts\activate

pip install -r requirements.txt
```

---

## ▶️ Usage

**Web app**

```bash
python3 image_captioning_app.py
```

Open the local URL shown in the terminal (default `http://127.0.0.1:7860`), upload an image and read the generated caption.

**Caption all images on a web page**

```bash
python3 automate_url_captioner.py
```

Captions are saved to `captions.txt` in the format `image_url: caption`.

**Caption a single local image**

```bash
python3 image_cap.py
```

---

## 📸 Example

![Sample image](Beneklikedi.jpeg)

```
Caption: a cat sitting on ...
```

*(Replace with the actual caption the model produced for this image.)*

---

## 📚 What I learned

- Implementing an image captioning tool with the BLIP model from Hugging Face Transformers
- Building a user-friendly interface with Gradio
- Adapting the tool to real-world scenarios such as automated web image captioning

---

## 📄 License

Project content is based on the IBM Skills Network lab, licensed under [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).
