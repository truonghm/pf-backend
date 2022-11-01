# Back-end Demo for Quantity Prediction Model (Pod Foods)



## Setting up

### Prerequisites

You will need:

1. python (required): The score services can be started without Docker, so Python is enough.
2. docker and docker-compose (optional, but preferable): Use docker for a better experience.

### Without Docker

Deploying without Docker will be limited, as Grafana and Prometheus are not completely usable. However, the API and simulation should still work.

A new Python environment should be created for isolation. If you use conda, you can use the following commands:

```
# note that I use Python 3.8 here
conda create --name pf python=3.8
conda activate pf
```

Next, install the neccessary packages:

```
pip install -r requirements.txt
```

Start the back-end services:

1. FastAPI

```bash
python model/serving.py
```

2. Locust (for simulation, optional)

```bash
locust -f simulation/locustfile.py --host http://127.0.0.1:8000
```

### With Docker & Docker Compose

Simply run:

```bash
docker-compose up
```

## Usage

### System architecture

### Model development

### Model serving

#### API

#### Monitoring

#### Testing