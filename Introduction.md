# Networking Agent:

🔹 Interactive Network Utility (Python)

This is a simple user-interactive Python tool that accepts natural-language prompts and performs different network-related tasks such as checking public IP, scanning TCP ports, testing connectivity, and (in development) fetching HTTP headers.

✨ Features

Check Public IP
Users can type any of the following prompts to retrieve their current public IP address:

what is my ip

check my ip

my public ip

my ip

TCP Port Scanning
Users can scan specific ports, multiple ports, or a range of ports for a given server. Examples:

scan port 80 of google.com server

scan port 80,443,20,21,8080,8000 of google.com server

scan port range 80-443 of google.com server

Continuous TCP Connectivity Test
Users can continuously attempt to connect to specific TCP ports on a server (like a persistent ping, but over TCP). Example:

connect port 80 to google.com server

connect port 80,443 to google.com server

Fetch HTTP Headers (in development)
Planned functionality: user simply enters a URL, and the tool will fetch and display its HTTP headers.
Example:

https://example.com

http://openai.com

🚀 How It Works

The program runs in a loop, waiting for user input.

It uses regular expressions and string matching to interpret commands.

Depending on the detected intent (IP check, port scan, connect test, headers), it calls the appropriate function.

💡 Example Session
You: what is my ip
Bot: Your public IP is: 203.0.113.25

You: scan port 80,443,20 of google.com server
Bot: Open ports on google.com -> 80, 443

You: connect port 80 to google.com server
Bot: Successfully connected to google.com:80 (continuous check running...)

You: https://example.com
Bot: [Fetching HTTP headers...]

🛠️ Future Improvements

Better natural language parsing.

Add HTTP methods detection (GET, POST, etc.).

Graceful exit handling (bye, exit, quit).

Enhanced error handling for invalid inputs.
