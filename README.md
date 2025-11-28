# Diverse and High-Quality Text Generation Assisted by Large Language Models

by Thai Huy Nguyen, Ngoc Hoang Luong

Published at Knowledge-Based Systems

## Install and setup
Clone this repo

Install dependencies:
```
pip install -r requirements.txt
```

## Run experiments
To run the a task with MAP-Elites:
```
python run_elm.py output_dir=<output_dir> env=<task> model.model_path=<model_path or model_name> qd.map_grid_size=[<num_bins>] 'env.behavior=<desc_pair>'"
```

Other hyperparameters of our method can be found in openelm/configs.py

### Examples
Run textsum task with MAP-Elites and Llama-3.1-8B-Instruct as emitter and evaluator on length/formality descriptor pair:
```
python run_elm.py output_dir=logs env=textsum model.model_path=meta-llama/Llama-3.1-8B-Instruct qd.map_grid_size=[3] 'env.behavior=[0,1]' model.system_prompt=True"
```

### Citation

```bibtex
@article{NguyenLuongKBS2025,
    title = {Diverse and High-Quality Text Generation Assisted by Large Language Models},
    journal = {Knowledge-Based Systems},
    pages = {114954},
    year = {2025},
    issn = {0950-7051},
    doi = {https://doi.org/10.1016/j.knosys.2025.114954},
    url = {https://www.sciencedirect.com/science/article/pii/S0950705125019926},
    author = {Thai Huy Nguyen and Ngoc Hoang Luong}
}
```

## Acknowledgements

Our source code is built upon:
- [OpenELM](https://github.com/CarperAI/OpenELM.git)