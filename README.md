# resumy

[![PyPI version](https://badge.fury.io/py/resumy.svg)](https://badge.fury.io/py/resumy)
![build status](https://github.com/alexlren/estel_secp256k1/actions/workflows/ci.yaml/badge.svg)

### Features

- Now supports the [jsonresume](https://jsonresume.org/schema/) format
- A default theme already supported
- Easy to create a theme or a config file
- Configs and schemas are both in yaml format
- Exports a pdf

## Latest theme

See my resume as example : [myresume.pdf](myresume.pdf)

## Install

Requires python3.11

```
python3.11 -m venv venv
source venv/bin/activate 
pip3 install .
```

## Commands

### Usage

```
resumy --help
```

### 

```
# Init a config file (might be broken)
resumy init -o myconfig.yaml

# Build resume using config (might be broken)
resumy build -o myresume.pdf myconfig.yaml

# Create and use your own theme
resumy theme -o /tmp/mytheme

# Generate resume with latest theme (replace with proper path to theme)
resumy build -o myresume.pdf --theme /home/linus/Documents/Projets/resumy/mytheme/ myconfig.yaml --disable-validation
```

## Tests

### Linting with flake8

```
tox -e flake8
```

### Type checking with mypy

```
tox -e mypy
```
