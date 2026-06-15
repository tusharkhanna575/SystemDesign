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

----


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
*Example:*
- `Primary DB → Writes`
- `Replica DB → Reads`

---

