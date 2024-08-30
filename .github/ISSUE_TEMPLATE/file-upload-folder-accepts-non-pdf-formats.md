---
name: File Upload Folder Accepts Non-PDF Formats
about: The website's file upload allows formats other than PDF (e.g., .docx, .jpg,
  .png), but it should only accept .pdf files.
title: File Type Restriction
labels: documentation
assignees: srujanaharinath

---

Role: QA Engineer
As a QA Engineer, your role is to ensure the website’s file upload functionality only accepts PDF files. You will test, identify, and report defects, and collaborate with the development team to implement and verify necessary changes.

Acceptance Criteria:
1. Client-Side Restriction: File selection must be limited to `.pdf` files only, with an error message for other formats: "Invalid file format. Only PDF files are allowed."
2. Server-Side Validation: The server must reject any non-PDF files and provide an error message: "Upload failed. Only PDF files are allowed."
3. User Feedback: Confirm successful uploads with: "File uploaded successfully."

Steps to Reproduce:

Navigate to the website's [Upload Page] (specify URL if applicable).
Click on the "Upload" button to open the file selection dialog.
Select a file with a format other than PDF (e.g., .docx, .jpg, .png).
Click "Open" to upload the file.
Expected Result:
The website should restrict the file upload to accept only .pdf files and display an error message for any non-PDF formats (e.g., "Invalid file format. Only PDF files are allowed.").

Actual Result:
The website allows files with formats other than .pdf to be uploaded without any error message or restriction.

Environment:

Browser: Chrome Version 95.0.4638.69, Firefox Version 94.0.1, Safari Version 15.1
OS: Windows 10, macOS Monterey
Additional Information:

The issue occurs across all tested browsers.
There is no client-side validation preventing non-PDF files from being selected and uploaded.
Server-side validation is also missing, allowing the upload of unauthorized file types.
Severity:
High – As this is a security risk, non-PDF file types could potentially allow malicious files to be uploaded.

Attachments:

Screenshots showing non-PDF files being uploaded successfully (attached).
Suggested Fix:

Implement client-side validation to restrict the file selection dialog to only show .pdf files.
Add server-side validation to reject any file uploads that are not in the PDF format and return an appropriate error message.
