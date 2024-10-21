# Nginx Log Analyzer

[Project Ideas Roadmap](https://roadmap.sh/projects/nginx-log-analyser)

This repository contains a shell script (`nginx_log_analyzer.sh`) that analyzes Nginx access logs from the command line. The goal of this script is to provide a quick overview of various aspects of the logs, such as frequently requested paths, common IP addresses, response status codes, and user agents.

## Features

- **Top 5 IP addresses** with the most requests.
- **Top 5 most requested paths**.
- **Top 5 response status codes**.
- **Top 5 user agents**.

## Requirements

- Nginx log file (`access.log`) should be present on the server. By default, the script reads from `/var/log/nginx/access.log`.
- Bash shell.
- Basic Unix utilities like `awk`, `sort`, and `uniq`.

## Usage

1. **Download the Script**
   Clone this repository and navigate to the directory containing the script.

   ```bash
   git clone https://github.com/yourusername/nginx-log-analyser.git
   cd nginx-log-analyser
   ```

2. **Make the Script Executable**
   
   ```bash
   chmod +x nginx_log_analyzer.sh
   ```

3. **Run the Script**

   ```bash
   ./nginx_log_analyzer.sh
   ```

   If the log file is located in a different path, update the `LOG_FILE` variable in the script accordingly.

## Example Output

```
Top 5 IP addresses with the most requests:
45.76.135.253 - 1000 requests
142.93.143.8 - 600 requests
178.128.94.113 - 50 requests
43.224.43.187 - 30 requests
178.128.94.113 - 20 requests

Top 5 most requested paths:
/api/v1/users - 1000 requests
/api/v1/products - 600 requests
/api/v1/orders - 50 requests
/api/v1/payments - 30 requests
/api/v1/reviews - 20 requests

Top 5 response status codes:
200 - 1000 requests
404 - 600 requests
500 - 50 requests
401 - 30 requests
304 - 20 requests

Top 5 user agents:
Mozilla/5.0 - 1000 requests
curl/7.68.0 - 600 requests
PostmanRuntime/7.26.8 - 50 requests
```

## Notes

- Ensure that the script has read permissions to the Nginx log file.
- You may need to use `sudo` if the log file is in a protected directory.

## License

This project is licensed under the MIT License.


