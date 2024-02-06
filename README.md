# llm-chainlit-demo

**WORK IN PROGRESS**

TODO:

- [ ] TF for environment AWS or Azure
- [ ] Installation script for demo
- [ ] Document ingestion
- [ ] Start of web app
- [ ] example documents about open-source software
- [ ] example questions and explanation
- [ ] recording

The demo was developed on Ubuntu 22.04 LTS

## Installation - Work In Progress

Install GPU

```shell
sudo apt update
sudo apt install ubuntu-drivers-common -y
sudo ubuntu-drivers install nvidia:535
sudo reboot
nvidia-smi
```

Create a new venv and install requirements.txt

```shell
git clone https://github.com/Barteus/llm-chainlit-demo.git
python3 -m venv .venv
source ./.venv/bin/activate
pip install -r requirements.txt
```

## Create vector DB

Add documents to the documents folder and run:

```shell
python3 ingest.py
```

## Run UI

Start the UI:

```shell
chainlit run --debug app.py
```

Shuttle to the VM or port-forward to localhost

```shell
sshuttle -r ubuntu@<VM_IP> <LOCAL_IP>/32
```
