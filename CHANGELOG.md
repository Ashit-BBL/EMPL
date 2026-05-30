# Emco Meditek Order Management App — Changelog

---

## Ver 1.9
- **+ New Quotation** button at top of Quotations tab (no need to switch to New Order tab)
- **📎 Email / Share PDF** button in all quotation and order detail modals
  - Mobile: opens native share sheet — pick email, WhatsApp, Files, etc. — PDF arrives as attachment
  - Desktop/fallback: auto-downloads the PDF file for manual attachment

---

## Ver 1.8
- **Company letterhead** (emco-header.jpg) as PDF header — replaces plain text header
- **Warranty field** in both quotation and order forms (default: 2 Years)
  - Shown in PDF, WhatsApp/Share text, and detail view
- **Customer Email field** added to Customer Information section
  - Saved with quotation/order data in Firebase
- **WhatsApp + Share + Save as PDF** buttons now visible for sales execs in quotation detail view (were missing)
- **📧 Email Customer** button — opens device email app with full quotation details pre-filled (uses `mailto:`)
- Email notification subject changed to "New Quotation" vs "New Order" (previously both said Order)
- Multi-product email: each product shown as a separate paragraph
- All "Order" labels changed to "Quotation" throughout (PDF title, modal section, edit button, WhatsApp/Share text)

---

## Ver 1.7
- **Standard Accessories per product** — admin configures up to 12 accessories per product (stored in Firebase)
- Accessories auto-fill when exec selects a product in the form
- Exec can edit the auto-filled list before saving
- Accessories field changed from single-line input to multi-line textarea

---

## Ver 1.61
- Contact Number field accepts **any format** — removed 10-digit restriction
- Field is copy-paste friendly (inputmode="tel")

---

## Ver 1.6
- Admin can **delete quotations**
- **Reset data** button in Admin → Settings (clears all orders/quotations/notifications; keeps products and user accounts)
- **Email notifications** to admin on every new order or quotation (via EmailJS — free, no backend)
- **Multi-admin email** support — comma-separated list of admin email addresses in settings

---

## Ver 1.5
- **Quotation system** — separate flow from orders, with own counter (EMCQ-YYYYMMDD-XXX)
- Quotations tab for sales execs (list, status tracking: Pending / Order Received / Lost)
- Convert Quotation to Order with one tap
- **Multi-product support** — up to 3 products per quotation/order
- PDF filename set to order/quotation number

---

## Ver 1.4
- **Profile edit** — exec can update their display name
- **Sequential order numbers** using Firebase transactions (EMCO-YYYYMMDD-XXX format)
- Removed pending badge clutter from order cards

---

## Ver 1.3
- Fixed A4 page size and blank pages in PDF
- PDF now opens in a clean standalone window for reliable printing across devices

---

## Ver 1.2
- **WhatsApp, Share, Print** buttons for exec and admin in order detail view
- **Delivery Address** field with "Same as billing address" checkbox
- PDF layout improved — saved as A4 via print dialog

---

## Ver 1.1
- Bold company name on printed order
- Android Share button for orders

---

## Ver 1.0
- Initial app launched
- Firebase Auth (email/password login, register, forgot password)
- **New Order** form: customer info, product selection, GST tax calculation, payment terms
- **My Orders** tab for sales execs
- **Admin Panel**: product management, all orders view, user management (promote/demote roles)
- GST auto-calculation (CGST + SGST for intra-state, IGST for inter-state)
- Print/PDF layout for orders
