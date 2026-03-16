#  CyberSentry – Web Application Vulnerability Scanner

CyberSentry is a simple web vulnerability scanning system built using Python and Streamlit.
The tool scans a target website, identifies some common vulnerabilities, calculates a risk score, and shows the results in an **interactive dashboard**.
If serious vulnerabilities are found, the system also sends an email alert automatically.


#  Project Overview

CyberSentry performs a scan on a selected website and checks for several common web security issues.
After the scan is complete, the system:

* Displays the vulnerabilities in a dashboard
* Assigns a **severity level** (Critical, High, Medium, Low, Informational)
* Calculates a **total risk score**
* Generates a **security grade (A–F)**
* Sends an **email notification** if high-risk vulnerabilities are found

 The main aim is to find the   vulnerabilities
 
# Main Features

• Detects **10 types of vulnerabilities**, including:

* Security header issues
* SSL/TLS certificate problems
* Cookie security problems
* Server information disclosure
* Dangerous HTTP methods
* Sensitive files or directories
* Missing CSRF protection in forms
* Clickjacking risk
* Mixed content on HTTPS pages
* Open redirect vulnerabilities

• **Automatic risk scoring system**

* Critical → 10 points
* High → 7 points
* Medium → 4 points
* Low → 2 points

• **Security Grade Calculation**

The total score is used to generate a grade from **A to F** to represent the overall security level of the website.


• **Interactive Dashboard**

The results are displayed using charts such as:

* Radar chart
* Funnel chart
* Treemap
* Bar chart

Users can also filter vulnerabilities by **severity or category**.

• **Email Alert System**

If the scan finds any **High or Critical vulnerabilities**, an email alert is automatically sent with the scan summary.

• **Export Results**

Users can download the scan results as a **CSV file**.



---

# ⚙️ How to Run the Project

## Option 1 – Using Jupyter Notebook (Recommended)

1. Download **notebook_cells.py**
2. Open **Jupyter Notebook**
3. Copy each CELL section into a notebook cell
4. Run **Cell 1** to install required libraries
5. Edit the **u.env** file and add your Gmail credentials
6. Run **Cell 2** to generate the project files
7. Run **Cell 3** to start the dashboard

Then open:

```
http://localhost:8501
```

# 📧 Email Alert Setup (Gmail)

To allow the program to send emails:

1. Go to **Google Account → Security**
2. Enable **2-Step Verification**
3. Generate an **App Password**
4. Add the credentials in the `u.env` file

Example:

GMAIL_SENDER=your_email@gmail.com
GMAIL_PASSWORD=xxxx xxxx xxxx xxxx
GMAIL_RECIPIENT=receiver@example.com


The system automatically sends an email **only if High or Critical vulnerabilities are detected**.

# 📦 Python Libraries Used

| Library        | Purpose                            |
| -------------- | ---------------------------------- |
| streamlit      | Creating the web dashboard         |
| requests       | Sending HTTP requests to websites  |
| pandas         | Storing and analysing scan results |
| plotly         | Creating interactive charts        |
| beautifulsoup4 | Parsing HTML content               |
| python-dotenv  | Loading environment variables      |

Some built-in Python modules were also used such as **ssl, socket, and smtplib**.

---

# 🎯 Test Websites

These websites are intentionally vulnerable and are safe to use for testing security tools.

```
http://testphp.vulnweb.com
http://testasp.vulnweb.com
http://testhtml5.vulnweb.com
http://zero.webappsecurity.com
```

<img width="1919" height="1077" alt="Screenshot 2026-03-17 030535" src="https://github.com/user-attachments/assets/a7bb5138-9365-4397-a729-4d04a63d8030" />

