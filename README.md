# tdm2

A project for table detection and structure recognition using deep learning, based on the Table Transformer (TATR) model.

## Project Structure

- `table-transformer/`: Contains the Table Transformer code and environment setup.
- `notebook.ipynb`, `visualize_training.ipynb`: Example notebooks for training and visualization.
- `coco_split/`, `output/`, etc.: Data and output directories.

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/MachineKe/tdm2.git
cd tdm2
```

### 2. Install Conda (if not already installed)

Download and install Miniconda or Anaconda from [conda.io](https://docs.conda.io/en/latest/miniconda.html).

### 3. Create and Activate the Environment

Create the environment using the provided `environment.yml`:

```bash
conda env create -f table-transformer/environment.yml
conda activate tables-detr
```

### 4. Install Additional Dependencies (if needed)

All main dependencies are included in the environment file. If you use the notebooks, ensure Jupyter is installed:

```bash
conda install jupyter
```

## Table Transformer (TATR) Setup

The Table Transformer code and detailed documentation are in the `table-transformer/` directory. For full details, see [table-transformer/README.md](table-transformer/README.md).

### Basic Usage

#### Training

To train a model, navigate to the `src` directory and run:

```bash
cd table-transformer/src
python main.py --data_type detection --config_file detection_config.json --data_root_dir /path/to/detection_data
```

#### Evaluation

To evaluate a model:

```bash
python main.py --mode eval --data_type detection --config_file detection_config.json --data_root_dir /path/to/detection_data --model_load_path /path/to/model.pth
```

For structure recognition, change `--data_type` and config file accordingly.

## Activating the Environment

Each time you start a new terminal session, activate the environment with:

```bash
conda activate tables-detr
```

## More Information

- For advanced usage, training on your own data, or using pre-trained models, see [table-transformer/README.md](table-transformer/README.md).
- For questions or contributions, refer to the contributing guidelines in the Table Transformer documentation.
