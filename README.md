<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

</head>
<body>
    <h1>Form Upload
        
Upload forms from a website to Google Docs</h1>
    <p>This script listens for the form submission event and sends the form data to the Google Sheet using the web app. It then shows an alert with the submission result.</p>
    <p>We are going to be using Google Apps to do this, and I will give a full walkthrough.</p>

 <h2>STEPS</h2>

<h3>1. Create a Google Sheet:</h3>
    <pre><code>
        Go to Google Sheets (<a href="https://sheets.google.com">https://sheets.google.com</a>) and create a new sheet.
        Set up the headers in the first row of the sheet to match the input fields in your HTML form. For example, if you have a form with a name and email field, the headers should be "Name" and "Email". 
        These are added by order, so if Name is first, then Name will be sent to Column A.
    </code></pre>
 <h3>2. Create a Google Apps Script:</h3>
    <pre><code>
        Open the Google Sheet and click on "Extensions" -> "Apps Script".
        Replace the default code with the code in googlescript 
        be sure to make an required changes if your sheet is not default
        Save the project (Ctrl + S or click the floppy disk icon).
        Run the script to grant necessary permissions.
    </code></pre>

<h3>3. Set up the form submission trigger:</h3>
    <pre><code>
        Click on the trigger on the sidebar and click the button to add a trigger.
        the button is on the bottom right of the screen for some reason
        Configure the trigger as follows:
        Select event type: "On form submit"
        Save the trigger
    </code></pre>

<h3>4. Deploy the script as a web app:</h3>
    <pre><code>
        Click on the blue Deploy button on the top-right corner and select "New Deployment".
        Configure the web app settings as follows:
        Description: Any description you want
        Execute as: "Me"
        Who has access: "Anyone"
        Deploy the web app and copy the web URL
    </code></pre>

<h3>5. Copy the script from addtohtml:</h3>
    <pre><code>
        Copy the script to your own HTML
        be sure to replace the web URL with the google web URL!!!!
        Made sure to give your <code>&lt;form&gt;</code> an ID and make sure it matches the id in the script!!!
        It probably wont work without an id
    </code></pre>

 <h3>6. Test!</h3>
    <pre><code>
        test it!
        as always make sure the form is filling properly before deploying to the public!
    </code></pre>

   <p>I Probably wont be doing any more work on this as it seems to be working for what i need it to do.
