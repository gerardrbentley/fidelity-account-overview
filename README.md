# Fidelity Account Overview App

tl;dr:

Assuming you have at least one Fidelity account.

- Go to the "Accounts & Trade" -> "Account Position" page
- Click the "Download" button on the right side of the page
- Either drag the csv into the app from your browser downloads or find it in your files / documents to upload it
- Optionally filter certain accounts or trading symbols

*DISCLAIMER*:

I'm not interested in your data, it is not uploaded anywhere besides to the streamlit process that serves your charts.
This application does require you uploading information to the streamlit cloud server unless you self-host it (See Local Setup below).

Act within reason; this app follows the Fidelity terms that the data is for your own informational purposes only.

From Fidelity Download:

"The data and information in this spreadsheet is provided to you solely for your use and is not for distribution. The spreadsheet is provided for informational purposes only, and is not intended to provide advice, nor should it be construed as an offer to sell, a solicitation of an offer to buy or a recommendation for any security by Fidelity or any third party. Data and information shown is based on information known to Fidelity as of the date it was exported and is subject to change. It should not be used in place of your account statements or trade confirmations and is not intended for tax reporting purposes. For more information on the data included in this spreadsheet, including any limitations thereof, go to Fidelity.com."

"Brokerage services are provided by Fidelity Brokerage Services LLC, 900 Salem Street, Smithfield, RI 02917. Custody and other services provided by National Financial Services LLC. Both are Fidelity Investment companies and members SIPC, NYSE."

## What is this?

A web app I built to visualize my current account standings in my brokerage accounts.
Fidelity doesn't provide API access to my knowledge, but downloading an account summary CSV is somewhat convenient.

The idea is not specific to Fidelity, it just happens to be where I have accounts.
It would work with any csv with the needed columns.

Built with :heart: from [Gar's Bar](https://tech.gerardbentley.com/).
Powered by [Streamlit](https://streamlit.io), [pandas](https://pandas.pydata.org/docs/), [plotly](https://plotly.com/python/), and [streamlit-aggrid](https://github.com/PablocFonseca/streamlit-aggrid).

## Sample Data

If you just want to see it in action, no worries.
I've included a set of example data that mimics the data shape I get from my real account.
The numbers won't add up and the stocks don't exist; for demonstration only.

## Local Setup

Assumes you have a [working python 3.9 installation](https://tech.gerardbentley.com/python/beginner/2022/01/29/install-python.html).

```sh
git clone git@github.com:gerardrbentley/fidelity-account-overview.git
cd fidelity-account-overview

python -m venv venv
. ./venv/bin/activate
# .\venv\Scripts\Activate for windows
pip install -r requirements.txt

streamlit run app.py
```

## Further Ideas

This was the basic idea for me to get a better look at my accounts and picks breakdown.

A better version of this would be able to track changes over time or provide some forecasting prediction.
