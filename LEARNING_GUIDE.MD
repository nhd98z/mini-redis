### **Phase 0: Prerequisites**
- [ ] **Basic Rust knowledge** - ownership, borrowing, Result<T,E>, Option<T>
- [ ] **Read the Tokio tutorial** - https://tokio.rs/tokio/tutorial first
- [ ] **Understand async/await basics** - what `async fn` and `.await` do

### **Phase 1: Start Small**
- [ ] **`README.md`** - Context and goals
- [ ] **`examples/hello_world.rs`** - See it work first!
- [ ] **Run the server and client** - Get hands-on experience
- [ ] **`Cargo.toml`** - What dependencies we're using

### **Phase 2: Simple Commands**
- [ ] **`src/cmd/ping.rs`** - Simplest command, good patterns
- [ ] **`src/cmd/get.rs`** - Basic key-value operation
- [ ] **`src/cmd/set.rs`** - Setting values

### **Phase 3: Core Infrastructure**
- [ ] **`src/lib.rs`** - Public API
- [ ] **`src/frame.rs`** - Protocol representation
- [ ] **`src/connection.rs`** - TCP handling

### **Phase 4: Advanced Patterns**
- [ ] **`src/db.rs`** - Shared state management
- [ ] **`src/server.rs`** - Full server implementation
- [ ] **`src/shutdown.rs`** - Graceful shutdown patterns

### **Phase 5: Client Side**
- [ ] **`src/clients/client.rs`** - Async client implementation
- [ ] **`src/clients/blocking_client.rs`** - Sync wrapper patterns
- [ ] **`src/clients/buffered_client.rs`** - Performance optimizations

### **Phase 6: Complete Picture**
- [ ] **`src/cmd/mod.rs`** - Command system overview
- [ ] **`src/cmd/publish.rs`** and **`src/cmd/subscribe.rs`** - Pub/sub pattern
- [ ] **`src/parse.rs`** - Command parsing
- [ ] **`src/bin/server.rs`** and **`src/bin/cli.rs`** - Actual executables
- [ ] **Other examples** - `pub.rs`, `sub.rs` for more complex usage

## 🧠 **Key Learning Focus Areas**

- [ ] **Async/Await with Tokio** - The entire project is built around this
- [ ] **Error Handling** - Look for `Result<T, E>` patterns throughout
- [ ] **Ownership & Borrowing** - Pay attention to `&mut`, `Arc`, `Mutex` usage
- [ ] **Pattern Matching** - Extensive use in command parsing
- [ ] **Traits** - Custom traits for commands and protocol handling
- [ ] **Modules** - Well-organized module structure
- [ ] **Concurrency** - Shared state, channels, spawning tasks

## 💡 **Pro Tips for Learning**

- [ ] **Run the code first**: Start the server and play with examples
- [ ] **Follow the data flow**: Trace how a command goes from client → network → parsing → execution → response
- [ ] **Focus on error handling**: Notice how errors are propagated and handled
- [ ] **Study the `Arc<Mutex<>>` pattern** in `db.rs` - this is crucial for shared state
- [ ] **Pay attention to lifetimes** - especially in connection handling

## 🚀 **Hands-on Learning**

After reading, try:

- [ ] Adding a new simple command (like `ECHO`)
- [ ] Modifying existing commands
- [ ] Adding logging to understand flow
- [ ] Running with `RUST_LOG=debug` to see what happens
