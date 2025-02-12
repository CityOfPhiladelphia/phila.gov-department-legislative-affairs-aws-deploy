# records-legislativeaffairs
Documents for Legislative Affairs for the Mayor's Office

The .json file values will be used to populate the rows for the table, which look like this:

| Bill and resolution number | Title(s) | Introduced by                                                     | Date introduced |  Assigned committee  | Link to fiscal note |
|---------------|------------------------|---------------------------------------------------------------------------|:--------------------:|:--------------:|------------------------|
| <a href="{bill_link}">{bill_number}</a> <a href="{resolution_link}">{resolution_number}</a> | {bill_title} {resolution_title}           | {prime_sponsor} | {introduction_date} | {committee}       | {fiscal_note_download} |


The json file itself hosts a series of objects in the following format (with example values):

{

    "bill_number": "123456",
    
    "title": "Amendments of Civil Service Regulation 6.31: Credential Based Pay",
    
    "prime_sponsor": "Mayor's Office",
    
    "introduction_date": "12/18/2024",

    "committee": "No",
    
    "fiscal_note_download": null,
    
    "bill_link": "_regulation-packet-chapter-2---205.2---signed.pdf"
    
}

Each value must be in quotes, and have a comma at the end of the line, except the last one. The same is true for the object itself in the curly brackets.

To add a new row to the table with data, you 1) add a new object (as above) to the legislativeaffairs.json file in the /legislativeaffairs_json directory, and 2) add any fiscal note PDF files to the /legislativeaffairs directory.

If a certain value is empty, then you write null, without quotes (see the fiscal_note_download field in the example).
