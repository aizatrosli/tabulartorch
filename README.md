# tabulartorch


Evaluating SOTA library/implementation on tabular data such as:
* widedeep
* tabzilla

Evaluation is based on:
* confusion matrix
* pytorch with GPU support
* memory usage (must fit in 24GB vmem GPU)
 
### Installation
* Install latest package from [RAPIS.ai](https://docs.rapids.ai/install) with pytorch support.


### How to Run

#### Widedeep

* Install widedeep libarary
  ```bash
  pip install pytorch-widedeep
  ```

#### Tabzilla
* Clone the [repo](https://github.com/naszilla/tabzilla)
* Install dependencies
    ```bash
    pip instal openml
    ```
* Download sample dataset from openml.
    ```bash
    cd tabzilla
    python tabzilla_data_preprocessing.py --dataset_name openml__california__361089
    ```
* Run test experiment with GPU config.
    ```bash
    python ./tabzilla_experiment.py --experiment_config ./tabzilla_experiment_config_gpu.yml --model_name SAINT --dataset_dir ./datasets/openml__california__361089/ 
    ```

### Enviroment
* Ubuntu 20.04 WSL
* Intel i7 12700k
* 32 GB RAM 
* Nvidia RTX3090 24GB