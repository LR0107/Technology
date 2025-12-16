# Web Scraping Tutorial

This document introduces the main types of web crawlers (web scrapers), their characteristics, typical use cases, and standard workflows. 

---

## 1. Static Web Page Crawlers

### Characteristics

- Web content is written directly in the HTML source code  
- Does **not** rely on JavaScript for dynamic rendering  

### Typical Scenarios

- News websites  
- Blogs  
- Government or academic websites  

### Method

1. Send an HTTP request to retrieve the HTML page  
2. Parse the HTML and extract the target data  

### Common Technologies

- `requests`  
- `BeautifulSoup`  
- `lxml / XPath`  

---

## 2. Dynamic Web Page Crawlers (JavaScript-Based)

### Characteristics

- Data is fetched via JavaScript requests and rendered dynamically  
- The initial HTML source code does **not** contain the target data  

### Typical Scenarios

- E-commerce websites  
- Social media platforms  

---

### Method 1: Browser Automation (Simulated Rendering)

**Idea:**  
Launch a real browser, wait for JavaScript execution to complete, then parse the DOM.

**Tools**

- Selenium  
- Playwright  

---

### Method 2: Direct API Scraping (Recommended)

**Idea:**  
Skip browser rendering and directly request the backend data APIs used by the webpage.

**How to Find APIs**

1. Open browser developer tools (`F12`)  
2. Go to Network → XHR / Fetch  
3. Refresh the page  
4. Look for requests that return JSON data  

**Detailed Steps**

1. Copy the API URL  
2. Construct appropriate request headers  
3. Send a direct request to the API  

---

## Standard Crawling Workflow

### Step 1: Open the Web Page and Check for Data

**Actions**

1. Open the target page in a browser  
2. Right-click → View Page Source (`Ctrl + U`)  

**Judgment**

- If data is visible in the source code → **Static Web Crawler**  
- If the source contains only empty containers such as `div` or `#app` → **Dynamic Web Page**

---

### Step 2: Open Network Panel and Locate the Data Source (Critical Step)

**Actions**

1. Press `F12`  
2. Open Network → XHR / Fetch
3. Refresh the page  
4. Observe responses and check whether JSON data APIs exist  

---

### Step 3: Fallback to Browser Automation

If no usable data API is found, or if the API is heavily protected or hidden, use a **browser-based crawler** (e.g., Selenium or Playwright) to load the page, simulate user behavior, and then extract data from the rendered DOM.

---

**Key Principle:**  
Always identify the page type first, then choose the appropriate scraping strategy.
