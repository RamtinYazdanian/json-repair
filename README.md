# json-repair

Repairs broken JSON strings and turns them into valid JSONs. Able to fix missing quotations, commas, etc.

Python port of https://github.com/josdejong/jsonrepair

## Installation

Clone this repository and then run (preferably in a new virtual environment):

```
pip install -e .
```

## Usage

```
>>> from json_repair.repairer import repair_json
>>> a = repair_json('{"h:25}')
>>> a
'{"h":25}'
>>> b = repair_json('{h:25}')
>>> b
'{"h":25}'
>>> c = repair_json('{"h:25 c:"2}')
>>> c
'{"h":25, "c":"2"}'
```
