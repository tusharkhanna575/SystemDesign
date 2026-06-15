<p><a target="_blank" href="https://app.eraser.io/workspace/fZujYE9XsojCkYEbUn4C" id="edit-in-eraser-github-link"><img alt="Edit in Eraser" src="https://firebasestorage.googleapis.com/v0/b/second-petal-295822.appspot.com/o/images%2Fgithub%2FOpen%20in%20Eraser.svg?alt=media&amp;token=968381c8-a7e7-472a-8ed6-4a6626da5501"></a></p>

## System Design MCQs
### Section 1: Fundamentals
**Q1.** When scaling from 1 user to 10 users, which issue typically appears first?

- [ ] A. Multi-region replication
- [x] B. Concurrency conflicts
- [ ] C. Distributed consensus failure
- [ ] D. GPU bottleneck


**Technical Explanation:**
With a single user, no competition exists for resources. As multiple users interact simultaneously, problems like race conditions, database locks, and shared state conflicts begin appearing.

---

**Q2.** Which layer is responsible for storing persistent data?

- [ ] A. Transport layer
- [ ] B. Application layer
- [ ] C. Presentation layer
- [x] D. Data layer


**Technical Explanation:**
The data layer handles long-term storage such as databases, object storage, and files. The application layer processes logic, but persistence happens in the data layer.

---

**Q3.** What is the primary role of DNS in the request lifecycle?

- [ ] A. Authenticate users
- [ ] B. Cache application responses
- [ ] C. Encrypt traffic
- [x] D. Convert domain name to IP address


**Technical Explanation:** Browsers cannot directly communicate using domain names like `google.com`. DNS resolves
this human-readable name into a machine-readable IP address (like `142.250.x.x`) so the request can be routed to the correct server.

---

### Section 2: Scaling Strategies
**Q1.** A monolith architecture becomes difficult mainly due to

- [ ] A. Too many databases
- [x] B. Tight coupling between modules
- [ ] C. Network latency
- [ ] D. Multiple services deployment


**Technical Explanation:** In monoliths, all modules depend heavily on each other. A small change in one module can affect unrelated components, making scaling and deployment harder.

---

**Q2.** Which technique improves database read performance?

- [ ] A. Encryption
- [ ] B. Normalization
- [x] C. Replication
- [ ] D. Serialization


**Technical Explanation:** Replication creates read replicas of a database so read traffic can be distributed across multiple machines, reducing load on the primary database.
_Example:_

- `Primary DB → Writes` 
- `Replica DB → Reads` 
---

**Q3.** CAP theorem states you cannot guarantee all three simultaneously

- [ ] A. Consistency, Access, Priority
- [x] B. Consistency, Availability, Partition tolerance
- [ ] C. Compute, Availability, Persistence
- [ ] D. Cache, Access, Performance


**Technical Explanation:** In distributed systems;

- Consistency -> same data everywhere
- Availability -> system always responds
- Partition tolerance -> system works despite network failure
You must choose **only two at a time** during partitions.

_Example:_

- `C + A` (no partiton tolerance)
- `A + P` (eventual consistency)
- `C + P` (reduced availability) 
---

**Q4.** Horizontal Scaling means

- [ ] A. Increasing RAM size
- [x] B. Adding more machines
- [ ] C. Increasing disk speed
- [ ] D. Increasing CPU power


**Technical Explanation:** Instead of upgrading one server (vertical scaling), horizontal scaling adds more servers to distribute workload and improve fault tolerance.

_Example:_

`1 server -> 10 servers handling traffic together` 

---

### Caching & Async Systems
**Q1.** Pub/Sub architecture is most useful when:

- [ ] A. Database scaling is required
- [x] B. One sender communicates with multiple receivers
- [ ] C. One sender communicates with one receiver
- [ ] D. Authentication is required


**Technical Explanation:** Publisher sends one event -> multiple subscribers receive it independently.

_Example:_ 

`Order placed event -> Notification service -> Billing service -> Analytics service` 

---

**Q2.** Which system is best suited for background processing tasks?

- [ ] CDN
- [x] Message Queue
- [ ] Load Balancer
- [ ] Reverse Proxy


**Technical Explanation:** Message queues allows tasks like emails, video processing, or analytics jobs to run asynchronously without blocking user requests.

_Example:_

`User uploads video -> queue -> background transcoding worker` 

---

**Q3.** CQRS seprates

- [ ] UI and Backend
- [x] Reads and Writes
- [ ] Sync and Async Logic
- [ ] Cache and DB Layers


**Technical Explanation:** CQRS improves performance and scalability by using different models/databases for reading and writing operations.

_Example:_ 

- `Write DB -> optimized for transactions` 
-  




<!--- Eraser file: https://app.eraser.io/workspace/fZujYE9XsojCkYEbUn4C --->