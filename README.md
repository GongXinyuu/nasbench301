# NAS-Bench-301

This repository containts code for the paper: ["NAS-Bench-301 and the Case for Surrogate Benchmarks for Neural Architecture Search"](https://arxiv.org/abs/2008.09777).

The surrogate models can be downloaded on figshare. This includes the models for [v0.9](https://figshare.com/articles/software/nasbench301_models_v0_9_zip/12962432) and [v1.0](https://figshare.com/articles/software/nasbench301_models_v1_0_zip/13061510) as well as the [dataset](https://figshare.com/articles/dataset/NAS-Bench-301_Dataset_v1_0/13246952) that was used to train the surrogate models. We also provide the [full training logs](https://figshare.com/articles/dataset/nasbench301_full_data/13286105) for all architectures, which include learning curves on the train, validation and test sets.

To install all requirements (this may take a few minutes), run

```sh
$ cat requirements.txt | xargs -n 1 -L 1 pip install
$ pip install nasbench301
```

To run a quick example, adapt the model paths in 'nasbench301/example.py' and from the base directory run

```sh
$ export PYTHONPATH=$PWD
$ python3 nasbench301/example.py
```

To fit a surrogate model run

```sh
$ python3 fit_model.py --model gnn_gin --nasbench_data PATH_TO_NB_301_DATA_ROOT --data_config_path configs/data_configs/nb_301.json  --log_dir LOG_DIR
```

## NOTE: This codebase is still subject to changes. Upcoming updates include improved versions of the surrogate models and code for all experiments from the paper. The API may still be subject to changes.
