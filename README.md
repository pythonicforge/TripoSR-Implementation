# TripoSR Reimplementation

This is a clean and reproducible **Colab-based reimplementation** of [Stability AI's TripoSR](https://huggingface.co/stabilityai/TripoSR) — a powerful zero-shot model that generates 3D object meshes from a single 2D image.

Built on top of the [PyImageSearch blog tutorial]([https://pyimagesearch.com/](https://pyimagesearch.com/2024/11/25/create-a-3d-object-from-your-images-with-triposr-in-python/)), this notebook integrates:

- 2D input image upload
- Background removal via `rembg`
- Inference using TripoSR via `Hugging Face`
- 360° turntable render output
- Mesh export in `.obj` format

<br/>

## Project Highlights

- **Zero-shot inference**: No need for fine-tuning — just drop an image and get a 3D model
- **Background cleanup**: Uses `rembg` for cleaner foreground object extraction
- **Smooth renders**: Generates 30-angle renders + MP4 video
- **Mesh export**: Outputs ready-to-use 3D `.obj` files

<br/>

## How to Use (in Colab)

1. **Open the Colab notebook**  
   > [▶️ Click here to run in Colab](https://colab.research.google.com/drive/127g5BFZoHsj4dt6nspENpLUN6RRX9Ldr?usp=sharing)

2. **Upload an image** (preferably product-style or with clear foreground)

3. **Run all cells**  
   Sit back and let the notebook:
   - Process the image
   - Run the TripoSR model
   - Render 360° views
   - Export a `.obj` 3D mesh

4. **Preview your result!**  
   A video preview will auto-play inside the notebook 🎬

<br/>

## Output Structure

After running the notebook, your `output/` folder will look like this:

output/
<br/>
└── 0/
<br/>
├── input.png # Processed input image
<br/>
├── render_000.png # 30 rendered views
<br/>
├── render_001.png
<br/>
├── ...
<br/>
├── render.mp4 # Turntable video
<br/>
└── mesh.obj # Exported mesh

<br/>

## References

- [TripoSR on Hugging Face](https://huggingface.co/stabilityai/TripoSR)
- [Original PyImageSearch tutorial](https://pyimagesearch.com/2024/11/25/create-a-3d-object-from-your-images-with-triposr-in-python/)
- [Paper: TripoSR: Ultra-Fast 3D Reconstruction from a Single Image](https://arxiv.org/pdf/2403.02151)

<br/>

## Future Plans

- [ ] Wrap this into an end-to-end web app
- [ ] Dockerize for easier deployment
- [ ] Add sample gallery + download links
