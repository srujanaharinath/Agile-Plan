---
name: File Upload Folder Accepts Non-PDF Formats
about: The website's file upload allows formats other than PDF (e.g., .docx, .jpg,
  .png), but it should only accept .pdf files.
title: ''
labels: ''
assignees: ''

---

Role: QA Engineer
As a QA Engineer, your role is to ensure the website’s file upload functionality only accepts PDF files. You will test, identify, and report defects, and collaborate with the development team to implement and verify necessary changes.

Acceptance Criteria:
1. Client-Side Restriction: File selection must be limited to `.pdf` files only, with an error message for other formats: "Invalid file format. Only PDF files are allowed."
2. Server-Side Validation: The server must reject any non-PDF files and provide an error message: "Upload failed. Only PDF files are allowed."
3. User Feedback: Confirm successful uploads with: "File uploaded successfully."
