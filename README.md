# <p align="center"><img src="https://raw.githubusercontent.com/your-repo/auto-mep-ai/main/assets/banner.png" alt="Auto MEP AI Banner" width="800"></p>

# Auto MEP AI

<div align="center">
  <a href="https://github.com/your-repo/auto-mep-ai/stargazers"><img src="https://img.shields.io/github/stars/your-repo/auto-mep-ai?style=for-the-badge&color=ffcb2b" alt="Stars"></a>
  <a href="https://github.com/your-repo/auto-mep-ai/network/members"><img src="https://img.shields.io/github/forks/your-repo/auto-mep-ai?style=for-the-badge&color=ffcb2b" alt="Forks"></a>
  <a href="https://github.com/your-repo/auto-mep-ai/blob/main/LICENSE"><img src="https://img.shields.io/github/license/your-repo/auto-mep-ai?style=for-the-badge&color=ffcb2b" alt="License"></a>
</div>

---

## ✨ Overview

<p align="center"><img src="https://raw.githubusercontent.com/your-repo/auto-mep-ai/main/assets/overview_demo.gif" alt="Overview Animation" width="700"></p>

**Auto MEP AI** is a cutting‑edge, AI‑powered tool that extracts, analyses, and visualises Mechanical, Electrical, and Plumbing (MEP) data from Revit models. Leveraging advanced parsing and a sleek, glass‑morphism UI, it empowers engineers to:

- **Rapidly extract** all MEP element properties.
- **Filter & search** through massive datasets with an intuitive sidebar.
- **Detect clashes** automatically and view them on a dynamic dashboard.
- **Export** results to JSON, CSV, or directly to IFC.

Designed for both **researchers** and **industry professionals**, the application combines a powerful Python backend with a modern web front‑end that feels like a premium SaaS product.

---

## 🎯 Key Features

<table style="width:100%; border-collapse:collapse;">
<tr style="background:linear-gradient(90deg, #0f2027, #203a43, #2c5364); color:#fff;">
<th>Feature</th><th>Description</th>
</tr>
<tr>
<td>📂 <strong>Broad‑Spectrum Extraction</strong></td><td>Supports every MEP family type via parent‑class inheritance, removing previous file‑size limits.</td>
</tr>
<tr style="background:#f0f8ff;">
<td>🧩 <strong>Dynamic Dashboard</strong></td><td>Glass‑morphism cards, gradient backgrounds, and real‑time filtering for a stunning visual experience.</td>
</tr>
<tr>
<td>⚡ <strong>Clash Detection Engine</strong></td><td>Automated detection with colour‑coded alerts and exportable reports.</td>
</tr>
<tr style="background:#f0f8ff;">
<td>🔄 <strong>Bidirectional Conversion</strong></td><td>Convert Revit (`.rvt`) ↔︎ IFC (`.ifc`) seamlessly.</td>
</tr>
<tr>
<td>📊 <strong>Export Options</strong></td><td>JSON, CSV, Excel, and IFC outputs ready for downstream workflows.</td>
</tr>
<tr style="background:#f0f8ff;">
<td>🛠️ <strong>Extensible Plugin System</strong></td><td>Add custom extraction rules or analytics modules with minimal code changes.</td>
</tr>
</table>

---

## 🚀 Quick Start

### Prerequisites

- **Python 3.10+** (recommended 3.10.9 – see `requirements.txt`)
- **Node.js 18+** (for the optional web UI)
- **Git**

### Installation

```bash
# Clone the repository
git clone https://github.com/your-repo/auto-mep-ai.git
cd auto-mep-ai

# Create a virtual environment
python -m venv .venv
source .venv/Scripts/activate  # Windows
# .venv/bin/activate      # macOS/Linux

# Install Python dependencies
pip install -r requirements.txt

# (Optional) Install the UI dependencies
cd prototype
npm install
```

### Running the Backend

```bash
# From the project root
python process.py
```

The server will start on `http://127.0.0.1:5000`. You can now POST a Revit file to `/convert` or use the CLI utilities in `stage4.py`.

### Running the Front‑End (Optional)

```bash
cd prototype
npm run dev
```

Open `http://localhost:3000` in your browser to explore the beautiful dashboard.

---

## 📦 Usage Examples

### CLI Extraction

```bash
python stage4.py --input model.rvt --output extracted.json
```

### API Call (cURL)

```bash
curl -X POST http://127.0.0.1:5000/convert \
     -F "file=@/path/to/model.rvt" \
     -o model.ifc
```

### Python Integration

```python
from xml_to_json_api import convert_rvt_to_json

json_data = convert_rvt_to_json('model.rvt')
print(json_data['elements'][:5])  # preview first 5 extracted items
```

---

## 🤝 Contributing

We love contributions! Follow these steps to get started:

1. **Fork** the repository.
2. Create a **feature branch** (`git checkout -b feature/awesome-feature`).
3. Write **tests** for your changes (see `tests/` directory).
4. Ensure **code style** with `black` and `flake8`.
5. Submit a **Pull Request** with a clear description and screenshots if UI changes are involved.

> **Tip:** Use the built‑in `run_command` scripts in `scripts/` to lint and run tests automatically.

---

## 📜 License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

## 📞 Support & Community

- **Issues:** Open a GitHub issue for bugs or feature requests.
- **Discussions:** Join the `#auto-mep-ai` channel on our Discord for real‑time help.
- **Documentation:** Detailed API docs are available at `https://your-repo.github.io/auto-mep-ai`.

---

<div align="center">
  <sub>Made with ❤️ by the Auto MEP AI team.</sub>
</div>
