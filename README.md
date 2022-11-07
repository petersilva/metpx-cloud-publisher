# metpxCloudPublisher

## Overview

MetPX-Sarracenia plugin for publishing data to cloud environments.

## Currently supported cloud object storage services

- S3
- Azure Blob Storage

## Installation

### Requirements
- Python 3
- [virtualenv](https://virtualenv.pypa.io/)

### Dependencies
Dependencies are listed in [requirements.txt](requirements.txt). Dependencies
are automatically installed during metpxCloudPublisher installation.

### Installing metpxCloudPublisher

```bash
# setup virtualenv
python3 -m venv --system-site-packages metpxCloudPublisher
cd metpxCloudPublisher
source bin/activate

# clone codebase and install
git clone https://github.com/wmo-cop/metpxCloudPublisher.git
cd metpxCloudPublisher
pip3 install -r requirements.txt

# configure environment
cp metpxCloudPublisher.env dev.env
vi dev.env  # update S3 or Azure credentials and path to MetPX filter
. dev.env

mkdir ~/.config ~/.config/sr3
cp metpxCloudPublisher.conf ~/.config/sr3/subscribe
vi ~/.config/sr3/subscribe/metpxCloudPublisher.conf  # adjust on_file path and desired subtopics

```

## Running

```bash
sr3 start subscribe/metpxCloudPublisher.conf

```

## Development

### Code Conventions

* [PEP8](https://www.python.org/dev/peps/pep-0008)

### Bugs and Issues

All bugs, enhancements and issues are managed on [GitHub](https://github.com/wmo-cop/metpxCloudPublisher/issues).

## Contact

* [Tom Kralidis](https://github.com/tomkralidis)
