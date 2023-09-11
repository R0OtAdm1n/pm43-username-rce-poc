# Honeywell PM43 Username Command Injection POC

This is a proof-of-concept (POC) code that demonstrates the presence of a command injection vulnerability via the `username` parameter in PM43 printer devices. It confirms the vulnerability in PM43 devices with a version equal to or earlier than P10.11.013310.

## Prerequisites

To use this POC, ensure that you have the following:

- Go programming language version 1.17 or higher installed on your system.
- Access to a PM43 printer device running the vulnerable version.

## Usage

Follow the steps below to utilize this POC:

1. Clone or download the POC code to your local machine.
2. Open a terminal and navigate to the project directory.

### Single URL Testing

To test a single URL, execute the following command:

```bash
go run main.go -url <target URL>
```

Replace `<target URL>` with the URL of the PM43 printer device you wish to test. For example:

```bash
go run main.go -url http://printer.example.com
```

### Multiple URLs Testing

If you have a file containing multiple URLs that need to be tested, use the following command:

```bash
go run main.go -file <input file>
```

Replace `<input file>` with the path to the file containing the URLs. Each URL should be on a separate line in the file.

## Output

The POC will send a command injection payload to the provided URL(s) using the `username` parameter and analyze the response. If the vulnerability is present, it will display a success message along with the payload used. If no vulnerability is detected, it will display a failure message.

Note: The POC assumes a specific format for the command injection payload. Depending on the specific vulnerability you are testing, you may need to modify the payload in the code.

## Disclaimer

This POC is meant for educational and testing purposes only. Use it responsibly and ensure that you have proper authorization to test the target device. The author holds no responsibility for any misuse or damage caused by the utilization of this POC.

## License

This POC is released under the [MIT License](LICENSE).

## Credits

This POC is based on the original code from the OpenAI GPT-3.5 model.

**Please exercise responsible use of this POC and respect the security and privacy of others.**