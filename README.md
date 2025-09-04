# Lab 1 - Web Server

## Overview
This project implements a simple web server using Python socket programming.  
The server handles one HTTP request at a time. It accepts a request from a browser, retrieves the requested file from the server’s directory, and sends it back to the client with appropriate HTTP headers. If the file does not exist, the server responds with a **404 Not Found** message.

## Features
- Listens for TCP connections on a specified port.
- Parses incoming HTTP `GET` requests.
- Serves static HTML files stored in the server directory.
- Sends proper HTTP response headers (`200 OK` or `404 Not Found`).
- Gracefully closes connections after serving the request.

## Requirements
- Python 3.x
- A test HTML file in the same directory (e.g., `HelloWorld.html`).
- A web browser or HTTP client (e.g., `curl`) for testing.

## How to Run
1. Clone or download this repository.
2. Place your test HTML file (e.g., `HelloWorld.html`) in the same directory as `WebServer.py`.
3. Run the server:
   ```bash
   python WebServer.py
   ```
4. Open a browser and go to:
   ```
   http://127.0.0.1:6789/HelloWorld.html
   ```
   Replace `127.0.0.1` with your **local IP address** if testing from another device.

## Example
### Successful Request
Request:
```
http://127.0.0.1:6789/HelloWorld.html
```
Response:
- Browser displays the content of `HelloWorld.html`.

### File Not Found
Request:
```
http://127.0.0.1:6789/NotExist.html
```
Response:
- Browser shows a **404 Not Found** error page.

## Notes
- The default port is `6789`. You can change this in the code if needed.
- To stop the server, press `Ctrl + C` in the terminal.
- If you see a port conflict error, change the port number in the script.