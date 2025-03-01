---
title: Negotiable Quotes
description: Learn about quote workflows and how you can provide this service to your company accounts.
exl-id: c278818b-fa5a-4e7a-8ca2-c4b757da4f05
feature: B2B, Quotes
---
# Negotiable Quotes

Buyers and sellers use Quotes to manage the negotiation process for an order–adding items, updating quantities, requesting and applying discounts, and so on—until they reach agreement. The quote negotiation process can be initiated by an authorized company buyer, or by a company sales representative.

![Quotes list view in Admin](./assets/quotes-admin-list-view-intro.png){width="700" zoomable="yes"}

After the quote is created, the negotiation process begins when the buyer or seller submits the quote for review. The _Quotes_ grid which lists each quote received and maintains a history of the communication between buyer and seller. Use the standard [workplace controls](../getting-started/admin-workspace.md) to filter the list, change the column layout, save views, and export data.

- In the storefront, buyers submit the quote as a [request to negotiate](quote-price-negotiation.md) the price from the shopping cart. When creating the quote request, a buyer can save the quote as a draft, or submit it directly to the seller.

- In the Admin, Sales representatives can create quotes on behalf of company buyer. When creating the quote, a seller can save the quote as a draft, or submit it directly to the buyer to initiate the negotiation process.

During the negotiation process, the quote can only be updated by the person reviewing and proposing terms for further negotiation.

## Prerequisites

Negotiable quotes are available only if Adobe Commerce has the following configuration settings:

- [The Adobe Commerce B2B extension is installed](install.md)
- [Configured B2B features](enable-basic-features.md)
  - Enable company accounts
  - Enable B2B quote

## Quote workflow

Quotes can be initiated by the buyer or the seller.

This diagram shows the quote statuses for a buyer and seller (Admin) in the different steps when you initiate a quote.

![Quotes Status Workflow](./assets/quote-status-workflow.svg){width="700" zoomable="yes"}

**Step 1: Quote creation (New)**

- **Buyer requests quote** - The buyer [requests a quote](quote-request.md) from the shopping cart. The request appears in the _My Quotes_ list in the account dashboard of the buyer and email notification is sent to the sales representative who is assigned to the company account. In the Admin, the request appears in the _Quotes_ grid, with a status of `New`. A request for a quote can be modified by the buyer until it is opened by the seller.

  ![Quotes](./assets/quote-request-from-shopping-cart.png){width="700" zoomable="yes"}

- **Sales representative** — A Sales Representative can [create a quote](sales-rep-initiates-quote.md) from the Admin on behalf of a specific company buyer. The Sales Representative must update the quote to add products and other information like discounts and notes to the buyer. The Sales Representation can save the quote as a `draft` or send it to the buyer to start the negotiation. In draft state, the quote is visible only to the seller. Once the quote is sent, the status is `Submitted`. It cannot be modified by the seller until the buyer sends it back.

  ![Seller initiating a buyer quote from the Quotes grid in the Admin](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

**Step 2: Quote review and negotiation (Review)**

Reviewing or negotiating a quote can include changing quantities, removing items, adding line item comments, applying line item or quote discounts (seller), and adding a shipping address (buyer).

- **Seller views request and sends response** - In the Admin, the seller views the request for a quote. On the storefront, the status of the quote changes to `Pending`, and the buyer cannot make any changes. The [seller responds](quote-price-negotiation.md) by offering price discounts and adjusting quantities and items as needed, enters a comment, and sends the quote back to the buyer. The buyer and sales representative are notified by email that the seller has responded.

- **Buyer views quote from seller and sends response** - The buyer clicks the link in the email notification to open the quote, or opens the quote from the _My Quotes_ page of the account dashboard. The buyer can leave notes to the seller at the line item or quote level, change quantities, and remove items.

The buyer and seller can continue the negotiation process until an agreement is reached, or the seller declines the quote. If the buyer makes changes to the quote—adding or removing products or changing product quantities—the quote must be returned to the seller for review.

- **Buyer adds a shipping address** - The buyer can add a shipping address to the quote. After the buyer adds the address, the seller can provide shipping and delivery options. The shipping methods shown depend on the Storefront configuration.

If the buyer adds a shipping address, the negotiation agreement has to be reviewed, and the seller can continue the negotiation process until an agreement is reached, or the seller declines the quote.

**Step 3: Buyer accepts quote (Checkout)**

The buyer accepts the proposed price and proceeds to checkout. Additional discounts cannot be added to the negotiated quote.

Shipping options are locked on checkout.

## Quote Status

Quote status provides information about the current state of the quote in the quote workflow. The status of a quote changes only when a buyer or seller takes an action on the quote. For example, the status changes to order if a buyer selects [!UICONTROL Proceed to Checkout] on an active quote.

- *[!UICONTROL New]** - The buyer submitted a request for a quote, but it has not been viewed by the seller. The request can be updated by the buyer until it is opened by the seller.

- **[!UICONTROL Draft]** - The seller creates a draft quote for a buyer. The quote is not visible to the buyer until the seller adds the offer details (items, quantity, discount, and so on) and submits the quote to the buyer.

- **[!UICONTROL Open]** - The seller opened the request and is in the process of reviewing it and preparing a response

- **[!UICONTROL Submitted]** - The seller sent a response to the buyer. The quote record cannot be edited during the negotiation process.

- **[!UICONTROL Client Reviewed]** - The buyer viewed the response from the seller and is in the process of preparing a reply.

- **[!UICONTROL Updated]** - The buyer submitted a response, but it has not been viewed by the seller.

- **[!UICONTROL Ordered]** - The buyer submitted the order based on the negotiated quote.

- **[!UICONTROL Closed]** - The buyer canceled the quote request.

- **[!UICONTROL Declined]** - The seller declined the request for a quote. Any custom pricing is removed from the quote and the record is locked from further edits.

- **[!UICONTROL Expired]** - The buyer did not respond to the seller's reply within the designated time period and the quote is no longer valid.

## B2B role resources for store quotes

Configuration options for quotes are controlled using the [role resources](../systems/permissions-user-roles.md#role-resources). These role resources must be set for the Admin user role that is assigned to the store administrator.

To grant access to quote functions in the Admin, go to **[!UICONTROL System]** > _[!UICONTROL Permissions]_ > **[!UICONTROL User Roles]**, select the role, and navigate to [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] in the _Role Resources_ tree.

![Quotes Roles & Permissions](./assets/roles-permissions-quotes.png){width="700" zoomable="yes"}

## Apply an action

In the Admin, B2B Administrators and Sellers can manage quotes from the Quote Grid by using the [!UICONTROL Actions] menu.

![Quotes](./assets/quotes-grid.png){width="700" zoomable="yes"}

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > **[!UICONTROL Quotes]**.

1. In the first column of the grid, select the checkbox for each record that you want to apply the action to.

1. In the **[!UICONTROL Actions]** select the action to apply.

### View a quote

1. In the **[!UICONTROL Actions]** column for a record, click **[!UICONTROL View]**.

1. To respond to the customer request, follow the instructions and begin the [price negotiation](quote-price-negotiation.md) process.

### View quote activity

View the negotiation timeline, communication, and other quote activity from the [!UICONTROL Comments] and [!UICONTROL History Log]--information includes status changes, updates to customer and shipping info, item and price updates, and other important information.

1. Open a quote.

1. View quote negotiation comments and history by scrolling to **[!UICONTROL Negotiation]**, and selecting **[!UICONTROL Comments]** and **[!UICONTROL History Log]**.

   ![View History](./assets/quote-view-history.png){width="400"}

1. History is also tracked at the line item level.

   ![View Line Item History](./assets/quote-view-line-item-history.png){width="400"}


### Decline a request for a quote

Only quote requests with an `Open` status can be declined.

1. Select each open quote request that you want to decline.

1. Set the _[!UICONTROL Actions]_ control to `Declined`.

1. When prompted, enter the reason the quote was declined and click **[!UICONTROL Confirm]**.

   ![Decline Quote?](./assets/quote-decline-confirm.png){width="400"}
