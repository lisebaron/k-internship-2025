
<div align="center" style="border: none;">
  <h1 style="border: none; text-weight : bold;">K-Internship 2025</h1>
</div>
<div align="center">
  <img src="Assets/keikenlogo.png" alt="keiken logo" width="100%"/>
</div>
<br>



## **TESTS DAYS**

Welcome to the **TESTS DAYS**! This collection is designed to challenge and enhance your skills in various technical domains, ranging from SQL and Regex to full-stack development and text processing. Each test is self-contained, focusing on a specific area to assess your proficiency and problem-solving abilities.


## **Directory Overview**

### 1. **TEST 1 - SQL**
   - **Objective**: Test your ability to write efficient SQL queries.
   - **Contents**: 
     - Tasks related to data retrieval, aggregation, and manipulation.
     - Real-world datasets to simulate practical scenarios.
   - **Skills Assessed**:
     - Data base architecture.
     - Use of SQL functions and joins.


### 2. **TEST 2 - A SMALL FULL STACK APP**
   - **Objective**: Work on a simple full-stack application.
   - **Contents**:
     - Frontend: Basic UI/UX implementation.
     - Backend: Server setup and API integration.
     - Database: CRUD operations with a database.
   - **Skills Assessed**:
     - Frontend and backend integration.
     - RESTful API design.
     - Debugging skills.


### 3. **TEST 3 - A QUICK QUIZ**
   - **Objective**: Solve a series of quick programming and problem-solving challenges.
   - **Contents**:
     - Short tasks across multiple domains, such as math, algorithms, and puzzles.
   - **Skills Assessed**:
     - Logical reasoning.
     - Time management.


### 4. **TEST 4 - XSLT**
   - **Objective**: Work with XML and XSLT for data transformation.
   - **Contents**:
     - Transform XML data into readable formats (HTML, text, etc.) using XSLT.
   - **Skills Assessed**:
     - Understanding of XML structure.
     - Mastery of XSLT templates and functions.
     - Formatting and data transformation techniques.


### 5. **TEST 5 - DO YOU REGEX?**
   - **Objective**: Solve complex text matching and extraction tasks using Regular Expressions.
   - **Contents**:
     - Exercises involving pattern matching, data validation, and string manipulation.
   - **Skills Assessed**:
     - Proficiency with Regex syntax.
     - Advanced text processing techniques.


### 6. **TEST 6 - GREP IT**
   - **Objective**: Use Linux command-line tools like `grep` to extract and process data.
   - **Contents**:
     - Real-world log file analysis tasks.
     - Data filtering and transformation using Linux commands.
   - **Skills Assessed**:
     - Mastery of `grep`, `awk`, `sed`, and other CLI tools.
     - Automation of text processing tasks.


<br><br>
# Setting Up Your EC2 Machine

Follow these steps to connect your GitHub account to your EC2 machine.

## I - Connecting to your machine : 

### **1. Connect to your EC2 Machine**
On your CLI, move to the directory where you put the `K-Internship-2025.pem`.

  - Set the right permissions to the key file so it can me used to your connection with the EC2 instance : 
    ```bash 
    chmod 400 /path/to/your-key.pem
    ```


  - Connect to your instance: 
    ```bash
    ssh -i K-Internship-2025.pem ec2-user@your-instance-public-ip
    ````

  - Launch `code-server`:
    ```bash
    code-server
    ```
Now you can access your Web IDE from your browser by going to: `your-instance-public-ip:8090`

## II - Setting up your Github account and getting your Tests Day repository: 

### **1. Configure Git**
Set your global Git configuration with your name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

Generate a new SSH key pair for authentication:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

- Save the key to the default location (e.g., `/home/ec2-user/.ssh/id_ed25519`).
- Optionally, set a passphrase or leave it blank.


### **2. Add the SSH Key to the SSH Agent**
Start the SSH agent and add your new key:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```


### **3. Add Your SSH Key to GitHub**
1. Display the public key:
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```
2. Copy the output of the above command.
3. Go to your GitHub account; on your local machine:
   - Navigate to **Settings > SSH and GPG Keys**.
   - Click **New SSH Key**.
   - Paste the key and give it a title (e.g., "EC2 Machine").
   - Click **Add SSH Key**.


### **4. Test the SSH Connection**
Verify that your EC2 instance is successfully connected to GitHub:

```bash
ssh -T git@github.com
```

You should see a message like this:

```plaintext
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```


### **5. Clone Repositories or Push Changes**
You are now ready to clone repositories:

```bash
git clone git@github.com:keiken-digital-solution/K-Internship-2025.git
``` 

  <br><br>
  
# Deliverables

1. Create a new branch with the name `KI2025/yourfullname`.
2. For each exercise, read the README.md file, follow the steps to complete the exercise, and save your work.
3. Commit your work and push it to on the branch you created. 

<br><br>
Good luck and happy coding!

—  
**The Keiken Team**
