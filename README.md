<h1 align="center">FastV</h1>

*FastV is a plug-and-play inference acceleration method for large vision language models relying on visual tokens. It could reach 45\% theoretical FLOPs reduction without harming the performance through pruning redundant visual tokens in deep layers.*

<div align=center>
<img width="600" src="./figs/fastv_tradeoff.png"/>
</div>

---
*Latest News 🔥*

- [x] LVLM Inefficent Visual Attention Visualization Code
- [ ] FastV demo inference code
- [ ] Intergrate FastV to LLM inference framework

Stay tuned!

## Setup
```bash
conda create -n fastv python=3.10
cd src
bash setup.sh
```

## Visualization: Inefficient Attention over Visual Tokens 

we provide a script (./src/FastV/inference/visualization.sh) to reproduce the visualization result of each LLaVA model layer for a given image and prompt.

```bash
bash ./src/FastV/inference/visualization.sh
```
or
```bash
python ./src/FastV/inference/plot_inefficient_attention.py \
    --model-path "PATH-to-HF-LLaVA1.5-Checkpoints" \
    --image-path "./src/LLaVA/images/llava_logo.png" \
    --prompt "Describe the image in details."\
    --output-path "./output_example"\
```

Model output and attention maps for different layers would be stored at "./output_example"

