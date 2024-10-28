Here's a beautifully formatted write-up for your GitHub that organizes your analysis into clear sections and enhances readability:

---

# Part 01 — Website Analysis

## Question 01: Open Ports
### Task:
Let’s run `nmap` and check what ports are open.

### Answer:
*No Answer Needed*

---

## Question 02: Web Server Port
### Task:
What port is for the web server?

### Answer:
Run an `nmap` scan with the following command:

```bash
nmap <target-ip>
```

---

## Question 03: Remote Desktop Service Port
### Task:
What port is for remote desktop service?

### Answer:
Use the same `nmap` scan:

```bash
nmap <target-ip>
```

---

## Question 04: Possible Password from Web Crawlers
### Task:
What is a possible password in one of the pages web crawlers check for?

### Answer:
A file that tells search engine crawlers which URLs the crawler can access on your site.

---

## Question 05: Content Management System
### Task:
What CMS is the website using?

### Answer:
Utilize the Wappalyzer extension.

---

## Question 06: Website Domain
### Task:
What is the domain of the website?

### Answer:
Analyze the HTTP header.

---

## Question 07: Administrator's Name
### Task:
What’s the name of the Administrator?

### Answer:
Search details provided about the person in the 2nd blog.

---

## Question 08: Administrator's Email
### Task:
Can we find the email address of the administrator?

### Answer:
The 1st blog contains an email address; just change the first two letters.

---

# Spot The Flags

### Flag 1
Inspect the following URL using `CTRL + U`:

```
http://target-ip/umbraco_client
```
*Use `CTRL + F` to search for the flag.*

---

### Flag 2
Inspect this URL using `CTRL + U`:

```
http://target-ip
```
*Use `CTRL + F` to search for the flag.*

---

### Flag 3
Click on the person shown in the 2nd blog.

---

### Flag 4
Inspect this URL using `CTRL + U`:

```
http://target-ip
```
*Use `CTRL + F` to search for the flag.*

---

# Final Stage

## Question 01: Login Credentials
### Task:
Let’s figure out the username and password to log in to the box (the box is not on a domain).

### Answer:
*No Answer Needed*

---

## Question 02: Accessing User File
### Task:
Gain initial access to the machine; what are the contents of `user.txt`?

### Answer:
Time to use the second open port. Access the remote desktop and get the text file named `user`.

```bash
rdesktop -u <username> -p <password> <target-ip>
```

---

## Question 03: Spotting the Admin Password
### Task:
Can we spot the admin password?

### Answer:
Check the "show hidden files" option, then `cd` into the backups directory. Reset all types of permission from the file to read it.

Use the following command to reset all types of permissions:

```bash
icacls "filename" /reset
```

---

## Question 04: Escalating Privileges
### Task:
Escalate your privileges to root; what are the contents of `root.txt`?

### Answer:
Access the remote desktop this time using the root user and the password.

---

Feel free to adjust any section as needed or let me know if you'd like further modifications!
