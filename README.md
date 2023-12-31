# Family Tree

A web application built with ReactJS and Vite, which displays a family tree of your direct ancestors based on data stored in a Google Spreadsheet document.

## How to use this web app

You'll need the following:
- A Google Sheets document, which will contain the data for your family tree
- A copy of this repository, cloned to your local hard drive and accessible in your terminal
- Your own `.env` configuration file, placed in the root of the repository directory, which will point the web app to your Google Sheets document

## Part 1: Google Sheets document

This web app will require a Google Sheets spreadsheet document and knowledge of the Google Sheets API.  If you are not already familiar with this API,
it is recommended that [you read here first](https://developers.google.com/sheets/api/guides/concepts).  

Here are the basic high-level steps, although you will find more detailed documentation on the links:

#### Create the document

- The first row should have the following labels:
  - A1: `name`
  - B1: `born`
  - C1: `notes`
  - D1: `color` (value should be hex color, i.e. `#FFFFFF`)
    
#### Share the document

- Click the "Share" button in the top right corner
- In the popup that appears, change the "General Access" setting to make it viewable to "Anyone with the link"

#### Create a Google API Key for Google Sheets

- Go to the [API Console](https://console.developers.google.com/).
- In the list underneath "Filters," click on the "Google Sheets" link.  It should take you to a "Google Sheets API" page.
- On that page, in the left column, click on the "Credentials" link.
- It will take you to a new "Credentials" page.  On the "Create Credentials" link dropdown, select "API Key."

## Part 2: Download local web app repository

- In the terminal, type: `git clone git@github.com:drumwolf/familytree.git`

## Part 3: Set up environmental variables in web app repository

- In the root directory, create a new file called `.env`

```
VITE_GSX_ID=[id]
VITE_GSX_KEY=[key]
VITE_GSX_SHEET=[name of sheet in the Google Sheets document, defaults to 'Sheet1']
```

## Part 4: Run web app on local workstation

- Install all packages:  `yarn install`
- In the project directory, you can run: `yarn dev`
- Open [http://localhost:5173](http://localhost:5173) to view it in the browser.
- The page will reload if you make edits.  You will also see any lint errors in the console.
