# 0xOposec_HTTP

![C](https://img.shields.io/badge/language-C-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows-0078D6.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Version](https://img.shields.io/badge/version-v1.0.0-blueviolet.svg)

A lightweight, high-performance HTTP server written in C for Windows.

## 📖 About

**0xOposec_HTTP** is a minimalistic HTTP server implementation built with performance as a priority. Developed in C using the Windows Sockets (Winsock2) API, it delivers blazing-fast performance while maintaining an incredibly small footprint. It's the perfect solution for serving static content, acting as a backend for small-scale applications, or for educational purposes in understanding network programming.

## ✨ Features

-   **HTTP/1.1 Protocol:** Full support for HTTP/1.1 `GET` requests with proper response headers.
-   **Multiple Content Types:** Serves a wide range of file types, including HTML, CSS, JavaScript, JSON, and various image formats (PNG, JPG, GIF, etc.).
-   **Smart Routing:** Automatically serves `index.html` for root directory requests, providing clean URL handling.
-   **Robust Error Handling:** Delivers proper `404 Not Found` error pages for any requested resources that are missing.
-   **Lightweight & Fast:** Built with minimal dependencies for fast compilation and an exceptionally small memory and binary footprint.
-   **Production Ready:** Stable, tested, and ready for development and small-scale production use.

## 🚀 Getting Started

### Prerequisites

-   Windows operating system.
-   Visual C++ Redistributable

  > [!IMPORTANT]  
  > You must have Visual C++ runtime libraries installed to be able to run this executable!
  ```
    $url86 = "https://aka.ms/vs/17/release/vc_redist.x86.exe"
$output86 = "$env:TEMP\vc_redist_x86.exe"

Invoke-WebRequest -Uri $url86 -OutFile $output86
Start-Process -FilePath $output86 -ArgumentList "/install", "/quiet", "/norestart" -Wait
Remove-Item $output86
Write-Host "x86 version installed!" -ForegroundColor Green

```

### Running the Server

1. Download the latest release of the project.

2.  Place your static website files (e.g., `index.html`, `styles.css`, images) in **the same directory** as your executable.
  > [!IMPORTANT]  
  > You must at least have an `index.html` and a `flag.txt` file in the folder.

5.  Execute the compiled server:
    ```bash
    ./http_server.exe
    ```

6.  Open your web browser and navigate to:
    ```
    http://localhost:8080
    ```

By default, the server runs on port `8080`. You should see your `index.html` page served.

## 🔧 Configuration

The server can be configured by modifying the constants at the top of `http_server_c.c`:

-   `PORT`: Change the listening port for the server.
-   `BUFFER_SIZE`: Adjust the size of the request buffer.
-   `MAX_CLIENTS`: Change the number of clients you can serve concurrently.

## 🤝 Contributing

Contributions are welcome! If you have ideas for new features, improvements, or have found a bug, please feel free to open an issue or submit a pull request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

<p align="center">
  Built with ❤️ using C and Winsock2 | Open Source Software
  <br>
  &#169; 2026 0xOposec_HTTP Project
</p>
