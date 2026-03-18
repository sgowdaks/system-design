## 1. Networking Fundamentals
Before data hits your code, it travels through the stack. You need to understand how "conversations" happen between computers.
* **OSI Model:** Specifically Layer 4 (Transport/TCP) and Layer 7 (Application/HTTP).
* **TCP vs. UDP:** When to prioritize reliability (Banking) vs. speed (Gaming/Video).
* **DNS (Domain Name System):** How a URL turns into an IP address.
* **Load Balancing:** Strategies like Round Robin, Least Connections, and IP Hash.
    * 
* **CDNs (Content Delivery Networks):** How to cache static data (images/JS) closer to the user.

---

## 2. API Design & Communication
This is how your LLD entities talk to the outside world.
* **RESTful APIs:** Constraints (Statelessness, Client-Server) and HTTP Methods (GET, POST, PUT, DELETE, PATCH).
* **Status Codes:** Knowing the difference between 401 (Unauthorized) vs. 403 (Forbidden), and 500-level errors.
* **GraphQL vs. gRPC:** Understanding modern alternatives to REST for flexibility or performance.
* **WebSockets:** For real-time, bi-directional communication (like a Chat App).

---

## 3. Storage & Databases
LLD focuses on class structures; Storage focuses on how that data lives forever.
* **Relational (SQL) vs. Non-Relational (NoSQL):**
    * **SQL:** ACID properties, Joins, and Structured schemas (PostgreSQL, MySQL).
    * **NoSQL:** Key-Value (Redis), Document (MongoDB), Columnar (Cassandra).
* **Indexing:** How to make database queries fast (B-Trees vs. Hash Indexes).
* **Replication & Sharding:** How to handle massive amounts of data by splitting it across multiple disks.
    * 

---

## 4. Operating System (OS) Basics
The environment where your code actually runs.
* **Processes vs. Threads:** Understanding memory isolation vs. shared memory.
* **Concurrency & Locking:** Mutexes, Semaphores, and Deadlocks (very important for LLD).
* **Memory Management:** Heap vs. Stack, and how Garbage Collection works.
* **I/O Models:** Blocking vs. Non-blocking (Event Loops like in Node.js).

---

## 5. Caching & Performance
Making the system feel "snappy."
* **Cache Eviction Policies:** LRU (Least Recently Used), LFU (Least Frequently Used), and FIFO.
* **Caching Strategies:** Cache-aside, Write-through, and Write-back.
* **Distributed Caching:** Using tools like Redis or Memcached to share a cache across servers.

---

## 6. Security & Observability
Ensuring the system is safe and trackable.
* **Authentication vs. Authorization:** JWT (JSON Web Tokens) vs. Sessions/Oauth2.
* **Encryption:** Symmetric (AES) vs. Asymmetric (RSA/HTTPS).
* **Logging & Monitoring:** Distributed tracing and metrics (Prometheus/Grafana) to see why a system crashed.
