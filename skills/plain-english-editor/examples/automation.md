# Example: automation explanation

## Before

> So basically this automation is our way of making sure no invoice falls through the cracks.
> Whenever someone marks an invoice as "Sent" in the Invoices table, the system kicks in and
> waits 14 days, and then if it still hasn't been paid it fires off a reminder email to the
> client contact and also pings the #billing channel in Slack so the team knows. If it HAS been
> paid by then, nothing happens. It also logs everything to the Reminder Log table. Pretty neat!

## After

**Trigger:** Someone sets an invoice's `Status` field to "Sent" in the `Invoices` table.

**Inputs:**

- The invoice record from the `Invoices` table.
- The invoice's `Paid` field.
- The client contact's email address on the invoice record.

**What happens:**

1. The automation waits 14 days.
2. The automation checks the `Paid` field.
3. If the invoice is paid, the automation skips steps 4 and 5.
4. If the invoice is not paid, the automation emails a reminder to the client contact.
5. If the invoice is not paid, the automation posts a message in the `#billing` Slack channel.
6. The automation adds a row to the `Reminder Log` table.

**Outputs:**

- A reminder email to the client contact, for unpaid invoices only.
- A Slack message in `#billing`, for unpaid invoices only.
- A new row in the `Reminder Log` table.

## Unknown

- The source does not say which email address sends the reminder. Confirm the sender before
  sharing this document.

## What changed

- Removed the opening metaphor ("falls through the cracks") and the closing opinion.
- Put each condition before its result.
- Kept exact table, field, and channel names in code format.
- Labeled the missing fact as unknown instead of guessing.
