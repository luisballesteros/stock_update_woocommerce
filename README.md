# Updating Stock in Woocommerce from Edisoft with Python

This Python script automates the process of updating the stock in a web store powered by Woocommerce. It retrieves stock data from a program called Edisoft and uses the Woocommerce REST API to update the stock in the web store. The script compares the stock data from Edisoft with the current stock in the web store and performs the necessary updates if there are any differences.

## Prerequisites

Before running the script, ensure that you have the following requirements:

- Python 3.x installed on your system
- Required Python libraries: pandas, numpy, re, woocommerce, smtplib, notebook
- Access to the Woocommerce REST API with appropriate consumer key and secret
- Access to the Edisoft program and the stock data files

## Setup

1. Clone the repository or download the script file.

2. Install the required Python libraries by running the following command:
   ```
   pip install pandas numpy re woocommerce smtplib notebook
   ```

3. Update the script with your specific configuration:
   - Set the `path` variable to the location where the stock files from Edisoft are located.
   - Configure the email parameters (`sender`, `recipient`, `mail_pass`, `smtp_server`, `bcc`) for sending email notifications.
   - Set the Woocommerce parameters (`url`, `consumer_key`, `consumer_secret`, `timeout`) with your specific values.

## Usage

To run the script and update the stock in the Woocommerce web store, follow these steps:

1. Open a command prompt or terminal.

2. Run the following command
   ```
   jupyter notebook
   ```

3. Navigate to the directory where the script file is located.

4. Run the following script:
   ```
   update_stock_woocommerce.ipynb
   ```

5. The script will execute the necessary steps:
   - Import and clean the Edisoft inventory dataset.
   - Import the inventory from the Woocommerce web store.
   - Compare the inventories and select items with different stock.
   - Update the stock in the web store using the Woocommerce REST API.
   - Verify the update by checking the stock of randomly selected items.

6. The script will send an email notification with the results of the stock update.

## Error Handling

The script includes error handling and logging mechanisms. If an exception occurs during execution, the script will log the error and send an email notification with the error message. Additionally, a log file named `log_update_stock.csv` will be created to track errors and updates.

## License

This script is released under the [MIT License](LICENSE).

---

Feel free to customize the README file according to your specific needs and add any additional sections or information that may be relevant for your users.
