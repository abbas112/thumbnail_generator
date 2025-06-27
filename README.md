# thumbnail_generator
AI thumbnail generator
graph TD
A[User logs in with Google] -->|OAuth: confirms channel ownership| B(UI – Next.js)
B --> C["Prompt + style opt-in"]
C --> D[Inference API – FastAPI @ DataVault GPU]
D -->|SD-XL + LoRA style| E[3 draft PNGs]
E --> F[Web editor (Canvas / Fabric.js)]
F --> G["Publish ➜ push to YouTube via Data API"]
G --> H["Write ‘altered content’ flag"]
