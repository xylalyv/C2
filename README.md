# **Manhattan Project - Python Command and Control (C2) Framework**

## **Overview**

**Manhattan Project** is _a powerful and extensible Python-based **Command and Control (C2) framework** designed for managing and controlling remote systems securely_. This framework enables communication between a central server and multiple agent systems, providing a robust and flexible platform for remote administration and operation.
<br><br>

## **Features**

### **1. Command Set**

#### **1.1. `upload`**

- **Description:** _Upload a file from the central server to the remote system._
<br><br>

> - **Usage:** `upload <local_file_path><remote_file_path>`
<br><br>

> - **Example:** `upload /path/to/local/file.txt /path/on/remote/server/file.txt`
<br><br>

- **Functionality:**

  - _Initiates the transfer of a file from the central server to the specified location on the remote system._
<br><br>

#### **1.2. `download`**

- **Description:** _Download a file from the remote system to the central server._
<br><br>

> - **Usage:** `download <remote_file_path> <local_file_path>`
<br><br>

> - **Example:** `download /path/on/remote/server/file.txt /path/to/local/file.txt`
<br><br>

- **Functionality:**
  - _Initiates the transfer of a file from the remote system to the specified location on the central server._

#### **1.3. `cd`**

- **Description:** _Change the current working directory on the remote system._
<br><br>

> - **Usage:** `cd <remote_directory_path>`
<br><br>

> - **Example:** `cd /path/on/remote/server/`
<br><br>

- **Functionality:**
  - _Changes the current working directory on the remote system to the specified path._

#### 1.4. `dir`

- **Description:** _List the contents of the current working directory on the remote system._
<br><br>

> - **Usage:** `dir`
<br><br>

> - **Example:** `dir`
<br><br>

- **Functionality:**
  - _Retrieves and displays the contents of the current working directory on the remote system._

#### 1.5. `geo` (not ready yet)

- **Description:** _Planned command for retrieving geolocation information from the remote system._
<br><br>

> - **Usage:** `geo` 
<br><br>

> - **Example:** `geo`
<br><br>

- **Functionality:**
  - _Intended to retrieve geolocation information from the remote system (currently under development)._

### **2. Multiple Connection Handling**
- **Description:**
  - _Utilizes multithreading to handle multiple connections simultaneously, enabling efficient management of multiple remote systems._
<br><br>

## **Agent Code**

The agent code represents the functionality running on the target systems. It connects to the server, listens for commands, and executes them accordingly. The agent code provides a foundation for implementing various features.


### **Explanation:**

- **Connection Establishment:**
  - _The agent establishes a socket connection with the central server._

- **Command Processing:**
  - _Listens for incoming commands from the server._
  <br><br>
  - _Executes commands based on the received instructions._

- **Directory Navigation:**
  - _Implements the `cd` command for changing the current working directory on the remote system._

- **File Handling:**
  - _Handles file upload and download operations._
<br><br>

## **Server Code**

The server code manages multiple connections and facilitates communication between administrators and remote agents. It supports commands such as list, exit, cls, download, upload, and background.


### Explanation:

- **Connection Management:**
  - _Manages multiple connections using multithreading._

- **Command Line Interface:**
  - _Provides a command-line interface for the server administrator._

- **Session Management:**
  - _Lists active sessions and allows interaction with individual sessions._

- **File Handling:**
  - _Initiates file upload and download operations with remote agents._
<br><br>

## **Usage**

1. **Agent Setup:**

   - _Deploy the agent code on the target system._

2. **Server Setup:**
   - _Run the server code on a central machine._
   <br><br>
   - _Connect to the agent using the specified_ port.

3. **Commands:**
   - _Execute commands on the server to interact with the remote agents._
<br><br>

## **Future Enhancements**

- **Implement the `geo` command for geolocation information retrieval.**
<br><br>

- **Enhance security features, such as encryption and authentication.**
<br><br>

## **Contribution Guidelines**

- **Fork the repository, make your changes, and submit a pull request.**

- **Report issues or suggest enhancements through the GitHub issue tracker.**
<br><br>

## **Disclaimer**

> ***This project is intended for educational and ethical purposes only. Unauthorized access to computer systems is illegal and unethical.***
<br><br>

## **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
