# GO Basic RPC API

This project demonstrates a simple **Remote Procedure Call (RPC)** implementation in Go. It consists of a server and a client application. The server exposes various RPC methods to manage a database of items, while the client interacts with the server to perform CRUD operations on these items.

## 🚀 Features

- **RPC Server**:
  - Manages a list of `Item` objects.
  - Provides methods for CRUD operations:
    - Add new items.
    - Retrieve the entire database or specific items by title.
    - Update existing items.
    - Delete items from the database.
- **RPC Client**:
  - Connects to the server.
  - Demonstrates interaction with the server's RPC methods.

## 📂 Project Structure

```
.
├── main.go            # Server code
├── client/
│   └── main.go        # Client code
├── go.mod             # GO Modules
└── README.md          # Project documentation
```

## 🛠️ Prerequisites

- Go (version 1.23.3 or later).

## 💻 Running the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Mates182/GO.Basic-RPC.git
```
```bash
cd GO.Basic-RPC
```

### 2. Run the Server

Navigate to the root directory and start the server:

```bash
go run main.go
```

The server will start listening on `localhost:4040`.

### 3. Run the Client

In a new terminal, navigate to the `client` directory and start the client:
```bash
cd client
```
```bash
go run main.go
```

The client will perform various operations and display the results.

---

## 🌐 RPC Server Methods

The server provides the following RPC methods:

### **1. AddItem**

Adds a new item to the database.



**Parameters:**
- `Item`: The item to add.

**Returns:**
- `Item`: The added item.

---

### **2. GetDB**

Retrieves the entire database.

**Parameters:**
- None.

**Returns:**
- `[]Item`: The list of all items in the database.

---

### **3. GetByName**

Retrieves a specific item by its title.

**Parameters:**
- `string`: The title of the item.

**Returns:**
- `Item`: The item with the specified title.

---

### **4. EditItem**

Updates the body of an existing item based on its title.

**Parameters:**
- `Item`: The item with the updated details.

**Returns:**
- `Item`: The updated item.

---

### **5. DeleteItem**

Deletes an item from the database.

**Parameters:**
- `Item`: The item to delete.

**Returns:**
- `Item`: The deleted item.

---

## 🧪 Example Interaction

Here’s a summary of what the client does:

1. Adds three items (`"first"`, `"second"`, `"third"`) to the server's database.
2. Retrieves and displays the full database.
3. Updates the `"second"` item with a new body.
4. Deletes the `"third"` item.
5. Retrieves the database again and displays the result.
6. Retrieves and displays details of the `"first"` item.

Here's what shows console:
```bash
$ go run main.go
Database:  [{first a test item} {second a second item} {third a third item}]
Database:  [{first a test item} {second A new second item}]
first item:  {first a test item}
```

