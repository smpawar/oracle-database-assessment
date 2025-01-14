# Masking a collection

While the collection script do not gather any data or source code, it does contain the name of schemas. If there is a requirement to obfuscate this data, there is an optional masking script included with the scripts.

This script will create a key file that maps the anonymized schema name to its original name.

**Note** This file should is not sent with the collection script and should not be lost, as it can't be recreated.

## Executing the script

The script can be executed at the shell or command prompt and requires 2 parameters:

- Path containing the collection archives you would like to mask. You should place the entire `zip` or `tar.gz` file in this folder, and you can include multiple collections with a single execution of the tool.
- Output directory is the path to write the masked collection archive.

```bash
$ ./masker/dma-collection-masker
usage: dma-collection-masker [-h] [--verbose] [--collection-path COLLECTION_PATH] [--output-path OUTPUT_PATH]

Google Database Migration Assessment - Collection Masking Script

options:
  -h, --help            show this help message and exit
  --verbose, -v         Logging level: 0: ERROR, 1: INFO, 2: DEBUG
  --collection-path COLLECTION_PATH
                        Path to search for collections.
  --output-path OUTPUT_PATH
                        Path to write masked collections.
```
