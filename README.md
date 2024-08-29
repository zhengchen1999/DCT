# Enhancing Image Super-Resolution with Dual Compression Transformer



## Dependencies

- Python 3.8
- PyTorch 1.8.0
- NVIDIA GPU + [CUDA](https://developer.nvidia.com/cuda-downloads)

```bash
pip install -r requirements.txt
python setup.py develop
```

## Test

- We provide DCT with scale factors: x2, x3, x4. 

- Download testing (Set5, Set14, BSD100, Urban100, Manga109) datasets, place them in `datasets/`. 

- Run the following scripts. 

  **You can change the testing configuration in YML file, like 'test_DCT_light_x2.yml'.**

  ```shell
  # DCT, reproduces results in Table 3 of the main paper
  python basicsr/test.py -opt options/Test/test_DCT_light_x2.yml
  python basicsr/test.py -opt options/Test/test_DCT_light_x3.yml
  python basicsr/test.py -opt options/Test/test_DCT_light_x4.yml
  ```
  
- The output is in `results`.

## Acknowledgements

This code is built on  [BasicSR](https://github.com/XPixelGroup/BasicSR).