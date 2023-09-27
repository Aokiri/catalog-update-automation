# Catalog Update Automation

Welcome to the Catalog Update Automation project! This Python script is designed to streamline the process of updating your online fruit store's catalog with data provided by suppliers. It automates the conversion of product information from image and text files to a format suitable for your website and sends notifications as needed.

## Project Overview

At your online fruit store, suppliers send product data in the form of images (.TIF) and text descriptions (.txt). This script will perform the following tasks:

1. **Image Conversion:** Converts large TIF images to smaller JPEG format for web display.

2. **HTML Generation:** Creates HTML product descriptions that include the converted image and product details.

3. **Web Service Integration:** Uploads the generated HTML content to your Django-based web service for immediate catalog updates.

4. **Data Extraction:** Gathers product names and weights from the text files for further processing.

5. **Supplier Notification:** Sends an email to the supplier, including a PDF attachment containing the total weight of fruits (in lbs) that were uploaded.

6. **System Health Monitoring:** Checks the health status of the system while running and sends an email alert if any issues are detected.

## Getting Started

### Prerequisites

Before running the script, ensure you have the following:

- Python 3.x installed on your system.
- Required Python libraries, which can be installed using `pip`:
  - Pillow (for image processing)
  - requests (for web service communication)
  - smtplib (for sending emails)
  - reportlab (for PDF generation)

### Configuration

Modify the `config.py` file to set up your email credentials, supplier email addresses, and other configuration settings.

```python
# Email Configuration
EMAIL_SENDER = "your_email@mail.com"
EMAIL_PASSWORD = "your_password"

# Supplier Email Addresses
SUPPLIER_EMAILS = ["supplier1@example.com", "supplier2@example.com"]

# Django Web Service URL
WEB_SERVICE_URL = "http://your-django-website.com/catalog/update"

# Run the run.py main program and go!
```

## Usage

1. Place supplier data files (TIF and TXT) in the designated input folder.
2. Run the script using the command: `python catalog_update.py`.
3. The script will process the files, update the catalog, and notify suppliers.

## Automation

You can schedule the script to run at specific intervals (e.g., daily) using cron jobs or a task scheduler on your server. This ensures that your catalog remains up-to-date with minimal manual intervention.

## Monitoring

To monitor the health of the system and receive notifications in case of issues, you can run the following command:

```bash
python system_health_check.py
```

This script will check the status of your system and send an email alert if any problems are detected.

## Contributors
Aokiri

Feel free to contribute to this project by adding new features or improving existing ones. For any questions or issues, please open an [issue on GitHub.](https://github.com/Aokiri/catalog-update-automation/issues)

Happy automating your catalog updates! 🍎🍊🍇
