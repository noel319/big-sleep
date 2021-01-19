<img src="./samples/artificial_intelligence.png" width="250px"></img>

*artificial intelligence*

<img src="./samples/cosmic_love_and_attention.png" width="250px"></img>

*cosmic love and attention*

<img src="./samples/fire_in_the_sky.png" width="250px"></img>

*fire in the sky*

<img src="./samples/a_pyramid_made_of_ice.png" width="250px"></img>

*a pyramid made of ice*

<img src="./samples/a_lonely_house_in_the_woods.png" width="250px"></img>

*a lonely house in the woods*

<img src="./samples/marriage_in_the_mountains.png" width="250px"></img>

*marriage in the mountains*

<img src="./samples/a_lantern_dangling_from_the_tree_in_a_foggy_graveyard.png" width="250px"></img>

*lantern dangling from a tree in a foggy graveyard*

<img src="./samples/a_vivid_dream.png" width="250px"></img>

*a vivid dream*

## Big Sleep

<a href="https://twitter.com/advadnoun">Ryan Murdock</a> has done it again, combining OpenAI's <a href="https://github.com/openai/CLIP">CLIP</a> and the generator from a <a href="https://arxiv.org/abs/1809.11096">BigGAN</a>! This repository wraps up his work so it is easily accessible to anyone who owns a GPU.

You will be able to have the GAN dream up images using natural language with a one-line command in the terminal.

Original notebook [![Open In Colab][colab-badge]][colab-notebook]

Simplified notebook [![Open In Colab][colab-badge]][colab-notebook-2]

[colab-notebook]: <https://colab.research.google.com/drive/1NCceX2mbiKOSlAd_o7IU7nA9UskKN5WR?usp=sharing>
[colab-notebook-2]: <https://colab.research.google.com/drive/1MEWKbm-driRNF8PrU7ogS5o3se-ePyPb?usp=sharing>
[colab-badge]: <https://colab.research.google.com/assets/colab-badge.svg>

## Install

```bash
$ pip install big-sleep
```

## Usage

```bash
$ dream "a pyramid made of ice"
```

Images will be saved to whereever the command is invoked

## Advanced

You can invoke this in code with

```python
from big_sleep import Imagine

train = Imagine(
    text = "fire in the sky",
    lr = 5e-2,
    save_every = 25,
    save_progress = True
)

train()
```

To save the progression of images during training, you simply have to supply the `--save-progress` flag

```bash
$ dream "a bowl of apples next to the fireplace" --save-progress --save-every 100
```

## Alternatives

<a href="https://github.com/lucidrains/deep-daze">Deep Daze</a> - CLIP and a deep SIREN network

## Citations

```bibtex
@misc{unpublished2021clip,
    title  = {CLIP: Connecting Text and Images},
    author = {Alec Radford, Ilya Sutskever, Jong Wook Kim, Gretchen Krueger, Sandhini Agarwal},
    year   = {2021}
}
```

```bibtex
@misc{brock2019large,
    title   = {Large Scale GAN Training for High Fidelity Natural Image Synthesis}, 
    author  = {Andrew Brock and Jeff Donahue and Karen Simonyan},
    year    = {2019},
    eprint  = {1809.11096},
    archivePrefix = {arXiv},
    primaryClass = {cs.LG}
}
```
