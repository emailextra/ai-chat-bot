# Conversation Flow – AI-Powered Chatbot for Customer Support

This document defines the main dialogue paths for the chatbot. All flows have been reviewed and approved before being added to the repository.

---

## 1. Greeting Flow

**Trigger:** Customer opens the chat widget or sends a first message.

```
Bot:  Hello! Welcome to our customer support chat.
      How can I help you today?
      You can ask me about:
        - Order status and delivery
        - Refunds and returns
        - Account help
        - Product information
      Or type "agent" at any time to speak with a human.

Customer: [types their question]
Bot:  [matches to FAQ or routes to correct flow below]
```

---

## 2. Order Status Flow

**Trigger:** Customer asks about an order, delivery, or tracking.

```
Bot:  I can help you with your order.
      Please provide your order number so I can look it up.

Customer: [provides order number]
Bot:  Thank you. Your order #[number] is currently [status].
      Estimated delivery: [date].
      Would you like help with anything else?

If order not found:
Bot:  I could not find that order number. Please check and try again,
      or I can connect you to a support agent for further help.
      Type "agent" to be transferred.
```

---

## 3. Refund and Return Flow

**Trigger:** Customer asks about a refund, return, or damaged item.

```
Bot:  I can help you with a return or refund.
      Was your item damaged, incorrect, or are you simply returning it?

Customer: [selects or describes reason]
Bot:  Our return policy allows returns within 30 days of delivery.
      To start your return, log into your account, go to My Orders,
      and click Return Item next to your order.
      Would you like me to walk you through it step by step?

Customer: Yes
Bot:  Step 1 - Log into your account.
      Step 2 - Go to My Orders.
      Step 3 - Select the order and click Return Item.
      Step 4 - Choose your reason and print the return label.
      Step 5 - Drop the parcel at your nearest post office.
      Refunds are processed within 5 to 7 business days after we receive the item.
```

---

## 4. Account Help Flow

**Trigger:** Customer asks about password, login, or account settings.

```
Bot:  I can help with your account.
      What do you need help with?
        1. Reset password
        2. Update personal details
        3. Unlock account
        4. Delete account

Customer: [selects option]

If reset password:
Bot:  Click Forgot Password on the login page and enter your email address.
      You will receive a reset link within a few minutes.
      Check your spam folder if you do not see it.

If unlock account:
Bot:  Accounts are locked after 5 failed login attempts.
      Please use Forgot Password to reset and unlock your account.
      If this does not work, I will connect you to a support agent.
```

---

## 5. Human Handover Flow

**Trigger:** Customer types "agent", "human", "speak to someone", or the chatbot cannot match the question after two attempts.

```
Bot:  I will connect you to a support agent now.
      Please hold on for a moment.

      [If agent available]
      Bot:  You are now connected to [Agent Name]. They will assist you shortly.

      [If no agent available]
      Bot:  All agents are currently busy. Your request has been logged
            and a team member will contact you within 24 hours.
            Your reference number is [REF-XXXX].
            Is there anything else I can help you with in the meantime?
```

---

## 6. Unrecognised Input Flow

**Trigger:** Chatbot cannot match the customer's message to any known intent.

```
Bot:  I am sorry, I did not quite understand that.
      Could you try rephrasing your question?
      You can also choose from these topics:
        - Orders and delivery
        - Refunds and returns
        - Account help
        - Product information
      Or type "agent" to speak with a human.

[If unrecognised a second time]
Bot:  I am having trouble understanding your request.
      Let me connect you to a support agent who can help you directly.
```
