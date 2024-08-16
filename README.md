# Python-Chat-Room

## Overview

This project demonstrates a basic multi-client chat room application using Python. It includes two main components: a server-side script to manage client connections and a client-side script for user interaction. The chat room allows multiple clients to connect and exchange messages in real-time using socket programming and multi-threading.

## Features

- Real-time messaging between multiple clients
- Server manages multiple client connections simultaneously
- Client can send and receive messages
- Error handling and connection management

## Requirements

- Python 3.x
- Basic knowledge of Python socket programming and threading

## Installation

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/Jaysharma2/Python-Chat-Room.git
   ```

2. Navigate to the project directory:

   ```bash
   cd Python-Chat-Room
   ```

## Usage

### Running the Server

1. Open a terminal and navigate to the project directory.
2. Run the server script with the desired IP address and port number:

   ```bash
   python chat_server.py <IP_address> <Port>
   ```

   Example:

   ```bash
   python chat_server.py 192.168.1.10 8081
   ```

### Running the Client

1. Open a new terminal and navigate to the project directory.
2. Run the client script with the server's IP address and port number:

   ```bash
   python client.py <IP_address> <Port>
   ```

   Example:

   ```bash
   python client.py 192.168.1.10 8081
   ```

3. Enter messages in the client terminal to send them to the chat room. Messages from other clients will be displayed as they arrive.

## Code Explanation

### Server Script

- **`chat_server.py`**: This script sets up a server socket, listens for incoming client connections, and handles each client connection in a separate thread. It broadcasts messages from one client to all other connected clients and manages active connections.

### Client Script

- **`client.py`**: This script connects to the server socket using the provided IP address and port. It reads messages from the server and user input, and displays incoming messages while sending user input to the server.

## Error Handling

The server script includes basic error handling to manage broken connections and client disconnections gracefully.

## Example

**Server Side:**

```
192.168.1.10 connected
<192.168.1.11> Hello everyone!
```

**Client Side:**

```
<You> Hello, server!
<192.168.1.10> Welcome to this chatroom!
```

## Contributing

Feel free to fork this repository and submit pull requests for improvements or bug fixes. For major changes, please open an issue to discuss your modifications before implementing them.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
