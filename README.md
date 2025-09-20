markdown
# Java URL Shortener (HttpServer)

A simple **URL Shortener** built using Java’s built-in **HttpServer**.  
Enter a long URL to generate a short link, and opening the short link will redirect you to the original URL.  

Lightweight, dependency-free, and easy to run in IntelliJ IDEA or any **JDK 17+** environment. 🚀



## ✨ Features
- Shorten long URLs into easy-to-share short links.
- Redirect from short links to the original long URL.
- Minimal setup — runs with plain Java (no external libraries).
- Works in IntelliJ or any IDE / CLI with JDK 17+.



## 📂 Project Structure


src/
└── main/
└── java/
└── com/example/urlshortener/
├── Main.java        # Starts HttpServer
├── UrlHandler.java  # Handles shorten & redirect logic
└── UrlStore.java    # In-memory store for URLs

`



## ⚙ Requirements
- **Java 17+** installed  
- An IDE (e.g., IntelliJ) or terminal with `javac` / `java`



## ▶ Running the Application
### From IntelliJ IDEA
1. Open the project in IntelliJ.
2. Run `Main.java`.
3. The server starts at [http://localhost:8080](http://localhost:8080).

### From Command Line
bash
# Compile
javac -d out src/main/java/com/example/urlshortener/*.java

# Run
java -cp out com.example.urlshortener.Main
`


## 🌐 Usage

### 1. Shorten a URL

* Open [http://localhost:8080/shorten?url=https://example.com](http://localhost:8080/shorten?url=https://example.com)
* Response: `Shortened URL: http://localhost:8080/abc123`

### 2. Redirect

* Open the short link in your browser, e.g., [http://localhost:8080/abc123](http://localhost:8080/abc123)
* You’ll be redirected to the original URL.


## 📌 Notes

* Uses **in-memory storage**, so all shortened links reset when the server restarts.
* For persistence, you can extend it to use a database or file-based storage.


## 🛠 Next Steps (Optional Enhancements)

* Add custom aliases (e.g., `/shorten?url=...&alias=my-link`).
* Add expiration dates for short links.
* Add analytics (click counts, timestamps).
* Swap in a database for persistent storage.


## 📜 License

This project is open-source under the MIT License.
Feel free to fork, modify, and use it!

