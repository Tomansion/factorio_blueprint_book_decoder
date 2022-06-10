Factorio Blueprint Book Decoder
==========================

## Introduction

Decode [Factorio]'s encoded `blueprint-book` into a json.
This script will also provide each book blueprint as a Json and as an encoded string.

Players of [Factorio] can create "blueprints" which make it easier to store
plans of sections of their factory for later reuse. These blueprints can be
stored in a `blueprint-book` and ouputed by the game as an encoded string for sharing purpose.

[Factorio](https://factorio.com/)

## Usage

Basic Unix/Linux commandline knowledge is assumed :-)

The script requires [Python] 3.6 (or higher) installed.

```bash
# First of all
git clone https://github.com/Tomansion/factorio_blueprint_book_decoder.git
cd factorio_blueprint_book_decoder/
```

### Example

You can test the algorithm a provided blueprint book:

```bash
./decode
```

Expected output with the example:

```
file: ./example_blueprint_books/general
file decoded successfully
Saved book.json at blueprint_book_json/

The book has 9 blueprints:

 - empty
 - belt 2
 - belt
 - belt3
 - inputOutput
 - arms
 - arms2
 - beltFac1
 - beltFac2

Saved blueprints at blueprint_book_json/blueprints
```

A folder `blueprint_book_json` will be created in the current directory.
It will contain the decoded blueprint book as a JSON file.
A JSON file as well as the encoded text of each blueprint will also be available in the folder.

```
blueprint_book_json
├── blueprints
│   ├── arms
│   ├── arms2
│   ├── arms2.json
│   ├── arms.json
│   ├── belt
│   ├── belt 2
│   ├── belt 2.json
│   ├── belt3
│   ├── belt3.json
│   ├── beltFac1
│   ├── beltFac1.json
│   ├── beltFac2
│   ├── beltFac2.json
│   ├── belt.json
│   ├── empty
│   ├── empty.json
│   ├── inputOutput
│   └── inputOutput.json
└── book.json
```

### With your own blueprint book

```bash
./decode --input /my/path/to/encoded/blueprint_book
```

optional arguments:
```
  -h, --help                     show this help message and exit
  -s, --silent                   Stop verbose output on STDERR
  -i [INPUT], --input [INPUT]    Blueprint book file path
  -o [OUTPUT], --output [OUTPUT] Folder output for the json
  -f, --force                    Force overwrite of existing output folder
```
