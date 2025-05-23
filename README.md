# mayor-legislativeaffairs
Documents for Legislative Affairs for the Mayor's Office

The .json file values will be used to populate the rows for the table, which look like this:

| Bill and resolution number | Title(s) | Introduced by                                                     | Date introduced |  Assigned committee  | Link to fiscal note |
|---------------|------------------------|---------------------------------------------------------------------------|:--------------------:|:--------------:|------------------------|
| <a href="{bill_link}">{bill_number}</a> <a href="{resolution_link}">{resolution_number}</a> | {bill_title} {resolution_title}           | {prime_sponsor} | {introduction_date} | {committee}       | {fiscal_note_download} |


The json file itself hosts a series of objects in the following format (with example values):

{

    "bill_number": "123456",
    
    "bill_title": "Amendments of Civil Service Regulation 6.31: Credential Based Pay",
    
    "prime_sponsor": "Mayor's Office",
    
    "introduction_date": "12/18/2024",

    "committee": "No",
    
    "fiscal_note_download": null,
    
    "bill_link": "_regulation-packet-chapter-2---205.2---signed.pdf"
    
}

Each value must be in quotes, and have a comma at the end of the line, except the last one. The same is true for the object itself in the curly brackets.

To add a new row to the table with data, you 1) add a new object (as above) to the legislativeaffairs.json file in the /legislativeaffairs_json directory, and 2) add any fiscal note PDF files to the /legislativeaffairs directory.

If a certain value is empty, then you write null, without quotes (see the fiscal_note_download field in the example).

*************

1.) When you are ready to move the files from Staging into Main, navigate to the repository. You will see a sentence at the top of the screen "This is X commits behind staging" click that blue link. It will take you to a screen titled "Comparing Changes" click the “Compare & Pull Request" button,

2.) Select the base: “Main” and compare: “Staging” options
    a.) It will let you know whether you are able to merge, or it will tell you if there are issues that need to be resolved.
    
3.) Select “Create Pull Request” button.

4.) Give the pull request a Title and a Description.
    a.) Provide a short description that will help someone else understand what changes were made.
    
5.) Click the “Create Pull Request” button.

6.) Confirm all the checks have been passed and that there are no conflicts with the base branch.

7.) Click the “Merge Pull Request” button.

8.) You will be prompted for a “Commit Message”
    a.) It will give you a starter message which you can use or add your own.
    
9.) Once added click on the “Confirm Merge” button.

10.) You are done! Changes should be visible within a few minutes; you may need to refresh your browser to see the changes. 


**Notes and best practices for working with the JSON file:**

1.) As long as the entry is formatted correctly, the order does not matter.

2.) The descriptions in the table are shortened to 200 characters on the webpage.

3.) If quotes are required in an item's description, single quotes should be used within the double quotes of the JSON entries.

4.) Use a JSON linter or validator to ensure your data is formatted correctly.

5.) The PDF file names need to be lower case to work correctly.


**For the Fiscal Note uploads:**

1.) Upload the file to the Legislative affairs PDF folder.

2.) Make sure there is a reference in your JSON file to the pdf file you added.

3.) Make sure the PDF the file names are lower case so they to work correctly.
