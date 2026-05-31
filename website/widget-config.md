# Website Chat Widget – Configuration Notes

This document describes how the chatbot widget is placed on the company website and how it is configured for the first release.

---

## Widget Placement

The chat widget is placed in the **bottom-right corner** of every page on the sample company website. It appears as a small circular button with a chat icon. When clicked, the chat window opens as an overlay without leaving the current page.

Pages where the widget is active:
- Home page
- Product pages
- Order tracking page
- Account page
- Contact us page

---

## Widget Configuration

| Setting | Value |
|---|---|
| Widget position | Bottom-right |
| Widget colour | Brand primary colour |
| Chat window title | Customer Support |
| Welcome message | Hello! How can I help you today? |
| Fallback message | I am sorry, I could not understand that. Type 'agent' for human support. |
| Human handover trigger | Keywords: agent, human, speak to someone, live support |
| Session timeout | 10 minutes of inactivity |
| Mobile responsive | Yes |

---

## Security and Privacy Notes

- The widget does not collect or store personal information such as names or email addresses unless the customer provides them voluntarily.
- No payment information is accepted or stored through the chat widget.
- All chat sessions are encrypted in transit.
- Chat logs are stored securely and are only accessible to the support team.
- The widget complies with basic privacy requirements as stated in the project scope.

---

## Integration Steps

1. Add the chatbot widget script to the website's `<head>` section on all pages.
2. Configure the widget with the settings in the table above.
3. Connect the widget to the chatbot intent engine using the API endpoint provided.
4. Test the widget on desktop and mobile before go-live.
5. Confirm the human handover function is working and routes correctly to the support queue.

---

## First Release Notes

This is a controlled first release. The widget is limited to the approved FAQ topics defined in `/knowledge-base/faq.md`. Any new topics or features must go through the formal change request process described in `/docs/change-request-log.md` before being added.
