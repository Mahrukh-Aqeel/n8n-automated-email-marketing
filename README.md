# Automated Email Marketing System

An automated email marketing solution built with **n8n, Airtable, and Gmail** that simplifies bulk email distribution. Users can create marketing campaigns through a form, retrieve subscriber information from Airtable, and automatically deliver emails to multiple recipients with optional image attachments.

## Overview

This workflow allows users to send marketing emails to an entire subscriber list without manually emailing each recipient.

Users submit an email subject, message, and optionally an image through an n8n form. The workflow retrieves subscriber records from Airtable, processes recipients individually, and sends emails through Gmail.

It automatically handles two scenarios: sending emails with an image attachment and sending emails without an attachment.

## Key Features

- **Bulk Email Distribution:** Automatically sends marketing emails to multiple Airtable subscribers.
- **Custom Email Campaigns:** Users can define the email subject and message through a form.
- **Optional Image Attachments:** Supports PNG, JPG, and JPEG image uploads.
- **Conditional Workflow Routing:** Checks whether an image is attached and selects the appropriate email-sending path.
- **Airtable Integration:** Retrieves subscriber names and email addresses from a centralized database.
- **Automated Email Delivery:** Uses Gmail to distribute messages to individual recipients.
- **Batch Processing:** Processes subscribers using n8n's Loop Over Items node.

## Technology Stack

- **n8n:** Workflow automation and orchestration.
- **Airtable:** Subscriber database and contact management.
- **Gmail API:** Automated email delivery.
- **n8n Forms:** Marketing campaign input and image uploads.
- **JavaScript:** Dynamic email content processing and formatting.

## Workflow Architecture

1. **Marketing Email Form:** Collects the email subject, message, and optional image attachment.
2. **Search Records:** Retrieves subscriber information from Airtable.
3. **Loop Over Items:** Iterates through the subscriber records individually.
4. **Image Validation:** Checks whether an image was uploaded.
5. **Conditional Routing:** Directs the workflow based on image availability.
6. **Email Preparation:** Prepares recipient details, subject, message, and attachment data.
7. **Gmail Integration:** Sends the email with or without an image attachment.
8. **Loop Continuation:** Continues processing until all subscriber records have been handled.

## Supported Features

| Feature | Description |
|---|---|
| Bulk emails | Sends to multiple subscribers |
| Custom subject | User-defined email subject |
| Custom message | User-defined email content |
| Image upload | Optional PNG, JPG, JPEG |
| Subscriber database | Airtable |
| Email delivery | Gmail |

## Use Cases

- Email marketing campaigns
- Product announcements
- Promotional newsletters
- Customer engagement campaigns
- Business updates and announcements
- Subscriber communication

## Setup Requirements

- An active n8n instance
- Airtable account with subscriber records
- Gmail account with OAuth2 credentials
- Configured n8n form trigger

## Project Type

Email Marketing Automation | Bulk Email Distribution | Workflow Automation

---

**Security Note:** Configure your own Airtable and Gmail credentials before running the workflow. Never publish API keys, OAuth tokens, or private subscriber information in your repository.
