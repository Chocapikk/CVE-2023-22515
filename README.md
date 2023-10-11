# CVE-2023-22515 Exploit Script 🔐

This script is designed to exploit the CVE-2023-22515 vulnerability in Confluence, which allows for unauthorized access to Confluence Server and Confluence Data Center instances. The vulnerability is categorized as a Broken Access Control issue and has a CVSS base score of 10.0. ⚠️

## Prerequisites 💻

Before using this script, make sure you have the following prerequisites in place:

- Python 3.x installed 🐍
- Required Python packages (`requests`, `fire`, `rich`, and `alive-progress`) installed. You can install them using `pip`:

```shell
pip install -r requirements.txt
```

## Usage 🚀

The script provides two main commands for exploiting the vulnerability:

### 1. Normal Mode 🔍

In normal mode, you can exploit the Confluence vulnerability using a single target URL. Run the following command:

```shell
python3 exploit.py normal [TARGET_URL] --output-file=[OUTPUT_FILE]
```

Replace `[TARGET_URL]` with the URL of the Confluence instance you want to target, and `[OUTPUT_FILE]` with the file you'd like to save vulnerable server details to.

Example:

```shell
python3 exploit.py normal https://example.com/confluence --output-file=vulnerable_servers.txt
```

### 2. Mass Mode 🔍

In mass mode, you can exploit the vulnerability using a list of target URLs from a file. Create a text file with one target URL per line and run the following command:

```shell
python3 exploit.py mass [FILE_NAME] --output-file=[OUTPUT_FILE]
```

Replace `[FILE_NAME]` with the name of the file containing the list of target URLs, and `[OUTPUT_FILE]` with the file you'd like to save vulnerable server details to.

Example:

```shell
python3 exploit.py mass targets.txt --output-file=vulnerable_servers.txt
```

## Example Output ℹ️

The script will provide information about the exploitation process, such as whether the vulnerability was successfully triggered, whether a new administrator was created, and whether authentication was successful.

```shell
[INFO] Successfully exploited https://example.com/confluence and logged in as admin!
```

## Disclaimer ⚠️

This script is provided for educational and informational purposes only. Use it responsibly and only on systems that you have permission to test. Unauthorized access to computer systems is illegal and unethical. 🚫