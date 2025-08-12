# Grid Styles - Curated AI Art Style Collection

A curated collection of high-quality AI art styles for Stable Diffusion, SDXL, Flux, and Cascade models. This repository contains only mainstream, popular models that produce excellent results without the weird/goofy styles.

## 📁 Repository Structure

### Core Files

- **`styles.json`** - The main styles configuration file containing all style definitions
- **`categories.json`** - Organizes styles into logical categories for easy browsing
- **`attribution.md`** - Credits and attributions for all models and creators
- **`enhancements.json`** - Quality enhancement prompts for better results

### Utility Files

- **`format.sh`** - Script to format and validate JSON files
- **`requirements.txt`** - Python dependencies for testing
- **`tests/`** - Test suite to validate style configurations

## 🎨 Style Categories

### Flux Models
- **flux** - Standard Flux model (1024x1024)
- **flux-small** - Compact Flux (512x512)
- **flux-vertical** - Portrait orientation (704x1472)
- **flux-extreme-vertical** - Tall portrait (640x1536)
- **flux-portrait** - Portrait (896x1152)
- **flux-portrait-big** - Large portrait (1024x1408)
- **flux-photo** - Photo aspect (1024x1024)
- **flux-photo-horizontal** - Horizontal photo (1472x1024)
- **flux-landscape** - Landscape (1472x1024)
- **flux-landscape-big** - Large landscape (1536x1024)
- **flux-widescreen** - Widescreen (1792x1024)
- **flux-cinematic** - Cinematic (2048x1024)

### FluxKrea Models (SDXL-based)
- **fluxkrea** - Standard FluxKrea (1024x1024)
- **fluxkrea-small** - Compact FluxKrea (512x512)
- **fluxkrea-vertical** - Portrait orientation (704x1472)
- **fluxkrea-extreme-vertical** - Tall portrait (640x1536)
- **fluxkrea-portrait** - Portrait (896x1152)
- **fluxkrea-portrait-big** - Large portrait (1024x1408)
- **fluxkrea-photo** - Photo aspect (1024x1024)
- **fluxkrea-photo-horizontal** - Horizontal photo (1472x1024)
- **fluxkrea-landscape** - Landscape (1472x1024)
- **fluxkrea-landscape-big** - Large landscape (1536x1024)
- **fluxkrea-widescreen** - Widescreen (1792x1024)
- **fluxkrea-cinematic** - Cinematic (2048x1024)

### SDXL Models
- **sdxl** - Standard SDXL (1024x1024)
- **sdxl-vertical** - Portrait orientation (704x1472)
- **sdxl-portrait** - Portrait (896x1152)
- **sdxl-landscape** - Landscape (1472x1024)
- **sdxl-widescreen** - Widescreen (1792x1024)

### Cascade Models
- **cascade** - Standard Cascade (1024x1024, 25 steps)
- **cascade+** - Enhanced Cascade with hires fix (1024x1024, 20 steps)

### Basic Models
- **raw** - Base Stable Diffusion 1.5
- **raw2** - Base Stable Diffusion 2.1

### Realistic Models
- **deliberate** - Generalist realistic model
- **realistic** - Photorealistic model
- **photographic** - High-quality photography style
- **cinematic** - Movie-like aesthetic
- **realistic-xl** - SDXL realistic model
- **photographic-xl** - SDXL photographic model

### Artistic Models
- **dreamshaper** - Artistic and creative style
- **epic** - Epic and dramatic style
- **artistic** - General artistic style

### Anime Models
- **anime** - Anime style (SD1.5)
- **anime-xl** - Anime style (SDXL)

## 🔧 Usage

### Basic Usage
Each style can be used with the following parameters:
- `{p}` - Your positive prompt
- `{np}` - Your negative prompt

### Example
```json
{
    "flux": {
        "prompt": "{p}{np}",
        "model": "Flux.1-Schnell fp8 (Compact)",
        "steps": 4,
        "width": 1024,
        "height": 1024,
        "cfg_scale": 1,
        "karras": false,
        "sampler_name": "k_euler"
    }
}
```

### Quality Enhancements
Many styles include quality enhancements in `enhancements.json` that automatically add:
- "masterpiece, best quality, highly detailed" to positive prompts
- Standard negative prompts to avoid common issues

## 🧪 Testing

Run the test suite to validate all styles:

```bash
# Set up virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run tests
python -m pytest tests/ -v
```

## 🔄 Formatting

Use the included formatting script to maintain consistent JSON formatting:

```bash
chmod +x format.sh
./format.sh styles.json
```

## 📚 Model Reference

This repository uses models from the [AI Horde Model Reference](https://github.com/Haidra-Org/AI-Horde-image-model-reference). The model reference contains:

- Complete model information and metadata
- Download links and file hashes
- Model showcases and examples
- Usage guidelines and requirements

### Key Models Used

- **Flux.1-Schnell fp8 (Compact)** - Fast, high-quality Flux model
- **SDXL 1.0** - Base SDXL model by Stability AI
- **Stable Cascade 1.0** - Latest Cascade model by Stability AI
- **Deliberate** - Popular generalist model by efreak
- **DreamShaper XL** - Artistic model by efreak
- **Realistic Vision** - Photorealistic model by efreak
- **ICBINP** - "I Can't Believe It's Not Photography" model
- **Animagine XL** - High-quality anime model
- **Juggernaut XL** - Realistic SDXL model

## 🤝 Contributing

This repository is curated to maintain high quality. When contributing:

1. Only add mainstream, popular models
2. Ensure all models exist in the AI Horde Model Reference
3. Test all styles before submitting
4. Update attribution.md with proper credits
5. Follow the existing format and structure

## 📄 License

This repository is licensed under the same terms as the AI Horde Model Reference. Please respect the individual licenses of the models used.

## 🔗 Links

- [AI Horde Model Reference](https://github.com/Haidra-Org/AI-Horde-image-model-reference)
- [AI Horde Discord](https://discord.gg/ai-horde)
- [Stability AI](https://stability.ai/)
- [Black Forest Labs](https://blackforestlabs.ai/)

## 📝 Changelog

### 2025-01-11
- Curated repository to include only mainstream, popular models
- Removed all weird/goofy styles
- Added comprehensive Flux and FluxKrea model variants
- Updated documentation and testing
- Cleaned up categories, attributions, and enhancements
