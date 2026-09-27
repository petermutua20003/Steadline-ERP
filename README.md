Steadline
Accounting, inventory, HR, payroll, and M-Pesa — one system, always balanced.
Steadline is a full-stack business management system built for small and medium businesses in Kenya. It replaces spreadsheets and notebooks with a real double-entry ledger, automatic M-Pesa reconciliation, multi-branch stock tracking, and HR and payroll — so a business's finances and workforce are managed in one place, always accurate and audit-ready.
🔗 Live site: steadline.site
Overview
Most small businesses in Kenya track sales, stock, payments, and staff payroll across notebooks, spreadsheets, and M-Pesa statements that never quite agree. Steadline solves this by running every transaction through a single, real double-entry ledger — every sale, purchase, payment, and payroll run posts as a proper accounting entry, atomically, so the books can never silently drift out of balance.
Key Features
Double-entry ledger core — append-only, atomic postings, with an automatic self-check that freezes the system if anything fails to reconcile
Sales & Purchases — full order lifecycle (draft → committed → posted), quotations, supplier purchase orders, weighted-average costing
M-Pesa integration — native Daraja API integration, tested end-to-end against Safaricom's sandbox environment
Multi-branch & multi-warehouse support — stock tracked per branch, with role-based access control per user
Banking — each payment method (cash, M-Pesa, bank) modeled as its own account, with fund transfers between them
Stock take — physical count reconciliation with reversible variance posting
HR & Payroll — employee records, salary processing, and payroll runs that post directly into the same ledger core, keeping payroll expenses fully reconciled with the rest of the business's finances
Full financial reporting — Trial Balance, Profit & Loss, Balance Sheet, Cash Flow, AR/AP Aging, VAT Summary, General Ledger
Role-based access control — Admin, Accountant, and Cashier roles, enforced at the API and database level
Multi-tenant architecture — row-level security ensures complete data isolation between businesses sharing the platform
Tech Stack
Backend: Django, PostgreSQL, REST API, JWT authentication
Frontend: Next.js
Payments: M-Pesa Daraja API
Security: Row-level security (RLS), company-scoped multi-tenancy
Architecture Highlights
Ledger integrity enforced through atomic transactions and an automated self-check that halts the system on any imbalance, rather than allowing silent data corruption
Company-level row-level security (RLS) with FORCE ROW LEVEL SECURITY, ensuring one business's data can never be accessed by another
Idempotent API design to safely handle retries from unreliable network conditions, common in the target market
Status
Live in production, onboarding real paying customers. Verified through simulated real-world usage (13,000+ transactions across a full simulated month), independently audited for ledger integrity, stock accuracy, and cross-report consistency.
Try It
Live demo: No signup required — steadline.site
Free trial: 30 days, full feature access, no card required
Built solo by Peter Ndiku  (https://github.com/petermutua20003).
