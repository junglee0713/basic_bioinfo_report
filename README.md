# sbx_shallowshotgun_pilot

## Installation

Clone the repo into your Sunbeam extensions directory, and install dependencies through Conda:

```bash
  source activate sunbeam
  cd $SUNBEAM_DIR/extensions
  git clone https://github.com/junglee0713/sbx_shallowshotgun_pilot.git
  conda install -c bioconda -c conda-forge -c r --file sbx_shallowshotgun_pilot/requirements.txt
```

## Usage

Shallow shotgun sample data are available through NCBI SRA, so you can pass the SRA project identifier to `sunbeam init`:

```bash
  sunbeam init shallow_shotgun --data_acc SRP178101
```
    
And then run Sunbeam, specifying `make_shallowshotgun_report` as the target rule:

```bash
  sunbeam run --configfile sunbeam_config.yml make_shallowshotgun_report
```