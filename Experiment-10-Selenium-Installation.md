# Experiment 10: Install and Explore Selenium for Automated Testing

## Aim
To install Selenium and explore its features for automating web application testing.

## Objectives
1. To understand Selenium and its components.
2. To install and configure Selenium.
3. To launch a web browser using Selenium WebDriver.
4. To automate basic browser operations.
5. To understand the role of Selenium in software testing.

## Software Requirements
- Python 3
- Selenium WebDriver library
- Google Chrome or another supported browser
- Compatible browser driver, where required
- Code editor

## Introduction
Selenium is an open-source framework used to automate web browsers for testing web applications. Selenium WebDriver allows programs to interact with web pages by locating elements, clicking buttons, entering text, and verifying results. It supports multiple programming languages, including Python, Java, and JavaScript.

## Installation Procedure
1. Install Python on the system.
2. Verify the installation using `python --version`.
3. Install Selenium using `pip install selenium`.
4. Open a code editor and create a Python file named `test_selenium.py`.
5. Write a simple Selenium WebDriver program.
6. Run the program and observe the browser automation.
7. Verify that the requested web page opens successfully.

## Sample Program

```python
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()

try:
    driver.get("https://www.google.com")

    print("Page title:", driver.title)

    search_box = driver.find_element(By.NAME, "q")
    search_box.send_keys("Selenium WebDriver")
    search_box.submit()

    print("Search performed successfully.")

finally:
    driver.quit()
```

## Important Selenium Commands

- `pip install selenium` – Installs the Selenium Python library.
- `webdriver.Chrome()` – Creates a Chrome browser session.
- `driver.get(URL)` – Opens the specified web page.
- `driver.title` – Retrieves the page title.
- `driver.find_element(By.NAME, "q")` – Locates an element by its name attribute.
- `element.send_keys("text")` – Enters text into an input field.
- `element.click()` – Clicks a web element.
- `driver.current_url` – Returns the current page URL.
- `driver.quit()` – Closes the browser session and its associated windows.

## Expected Output
- The Chrome browser opens.
- Google loads successfully.
- The search field receives the text `Selenium WebDriver`.
- The search is submitted.
- The program displays the page title and a success message.

## Result
Successfully studied Selenium installation and explored browser automation using Selenium WebDriver.

## Applications
- Automated web application testing
- Regression testing
- Functional testing
- Cross-browser testing
- Repetitive browser task automation
