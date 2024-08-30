---
name: Bug report
about: 'non-PDF files being uploaded successfully '
title: 'High Priority '
labels: bug
assignees: ''

---

Steps to Reproduce:

Navigate to the website's [Upload Page] (specify URL if applicable).
Click on the "Upload" button to open the file selection dialog.
Select a file with a format other than PDF (e.g., .docx, .jpg, .png).
Click "Open" to upload the file.

Expected Result:
The website should restrict the file upload to accept only .pdf files and display an error message for any non-PDF formats (e.g., "Invalid file format. Only PDF files are allowed.").

Actual Result:
The website allows files with formats other than .pdf to be uploaded without any error message or restriction.

Additional Information:
The issue occurs across all tested browsers.
There is no client-side validation preventing non-PDF files from being selected and uploaded.
Server-side validation is also missing, allowing the upload of unauthorized file types.

Severity:
High – As this is a security risk, non-PDF file types could potentially allow malicious files to be uploaded.

Suggested Fix:
Implement client-side validation to restrict the file selection dialog to only show .pdf files.
Add server-side validation to reject any file uploads that are not in the PDF format and return an appropriate error message.
